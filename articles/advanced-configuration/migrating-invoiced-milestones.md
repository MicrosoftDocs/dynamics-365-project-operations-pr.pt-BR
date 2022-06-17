---
title: Migrar etapas de cobrança totalmente faturadas na substituição
description: Este artigo explica como migrar etapas de cobrança de preço fixo faturadas ao cliente para contratos de projeto abertos antes da data de ativação.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d7bb3dbb5acd9be447c405ec17f18d00c500f655
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912226"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrar etapas de cobrança totalmente faturadas na substituição

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

## <a name="scenario"></a>Cenário

A Contoso vai ser ativada com o Microsoft Dynamics 365 Project Operations para cenários de recursos/itens sem estoque. Como parte das atividades de substituição, a equipe de implementação deve migrar os contratos de projeto abertos do sistema antigo. Alguns dos contratos de projeto incluem linhas de contrato que usam o método de cobrança de preço fixo e já foram parcialmente faturadas ao cliente final. A equipe de implementação deve migrar essas etapas de cobrança como **Fatura do cliente lançada** porque elas devem ser incluídas no valor total do contrato para fins de reconhecimento de receita. No entanto, os saldos de cliente em Contas a receber e Contabilidade não devem ser afetados.

## <a name="solution"></a>Solução

### <a name="prerequisites"></a>Pré-requisitos

- O Dynamics 365 Finance 10.0.24 ou posterior deve estar instalado.
- O ambiente em que as etapas de migração serão concluídas deve estar no modo de manutenção. Nenhuma outra atividade deverá ser executada enquanto as etapas estiverem sendo migradas.
- As etapas de migração devem ser seguidas exatamente como descritas aqui e só podem ser usadas para a atividade de substituição. A Microsoft não aceita nenhum outro uso desse recurso.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Criar uma versão de substituição do mapa de gravação dupla de etapas da linha de contrato de integração do Project Operations 

1. Certifique-se de que o mapeamento de destino para a entidade **Etapas da linha de contrato de integração do Project Operations** está atualizado. 

    1. Em Finanças, acesse **Gerenciamento de Dados** \> **Entidades de dados** e selecione a entidade **Etapas da linha de contrato de integração do Project Operations**. 
    2. Selecione **Modificar mapeamentos de destino**. 
    3. Na página **Mapear preparo para destino**, selecione **Gerar mapeamento** e confirme que deseja gerar o mapeamento.

2. Interrompa e atualize o mapa de gravação dupla **Etapas da linha de contrato de integração do Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Acesse **Gerenciamento de dados** \> **Gravação dupla**, selecione o mapa e abra os detalhes. 
    2. Selecione **Parar** e aguarde até o sistema parar o mapa. 
    3. Selecione **Atualizar tabelas**.

3. Adicione um mapeamento para o status da transação.

    1. Selecione **Adicionar mapeamento**.
    2. Na nova linha, na coluna **Aplicativos de finanças e operações**, selecione o campo **TRANSSTATUS \[ TRANSSTATUS\]**.
    3. Na coluna **Microsoft Dataverse**, selecione **msdyn\_invoicestatus \[Status da fatura\]**.
    4. Na coluna **Tipo de mapa**, selecione a seta para a direita (**\>**).
    5. Na caixa de diálogo que aparece, no campo **Direção de sincronização**, selecione **Dataverse para aplicativos de finanças e operações**.
    6. Selecione **Adicionar transformação**.
    7. No campo **Tipo de transformação**, selecione **ValueMap**.
    8. Selecione **Adicionar mapeamento de valores**.
    9. No campo esquerdo, insira **4**. No campo direito, insira **192350001**. 
    10. Selecione **Salvar** e feche a caixa de diálogo.

4. Selecione **Salvar como** para salvar a versão do mapa de gravação dupla. 
5. No painel **Adicionar tabela**, no campo **Publicador**, selecione **Publicador padrão**.
6. No campo **Versão**, insira a versão.
7. No campo **Descrição**, insira uma nota sobre esta versão de substituição do mapa. 
8. Selecione **Salvar**.
9. Inicie o mapa.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrar etapas faturadas para o ambiente do Dataverse

1. No ambiente do Dataverse do Project Operations, crie etapas que tenham o status de fatura **Pronta para faturamento**. Nesse ponto, não migre nenhuma etapa que não tenha sido faturada.

    > [!NOTE]
    > Antes de migrar as etapas de cobrança, verifique se as dimensões financeiras relacionadas à linha de contrato do projeto estão definidas conforme o esperado. As dimensões financeiras não podem ser editadas depois que a migração é concluída.

2. Depois que todas as etapas forem migradas, pare os seguintes mapas de gravação dupla:

    - Etapas da linha de contrato da integração do Project Operations (msdyn\_contractlinescheduleofvalues)
    - Valores reais da integração do Project Operations (msdyn\_actuals)
    - Proposta de fatura do projeto V2 (faturas)

    Para parar os mapas, siga estas etapas:

    1. No Finance, acesse **Gerenciamento de dados** \> **Gravação dupla**, selecione um mapa e abra os detalhes.
    2. Selecione **Parar** e aguarde até o sistema parar o mapa.

3. No ambiente do Dataverse do Project Operations, crie e confirme faturas pro forma para as etapas de cobrança. 

    1. No mapa do site, acesse os contratos de projeto, selecione os contratos e, depois, selecione **Criar faturas**.
    2. Depois que as faturas forem criadas, abra-as no menu **Faturas** no mapa do site e selecione **Confirmar**.

    Esta etapa cria os registros necessários no ambiente do Dataverse. No entanto, ela não afeta finanças e contas a receber porque os mapas de gravação dupla listados anteriormente foram interrompidos.

4. Depois que todas as faturas pro forma forem confirmadas, retorne todos os mapas de gravação dupla ao estado inicial.

    1. Atualize a versão do mapa de gravação dupla **Etapas da linha de contrato de integração do Project Operations** (**msdyn\_contractlinescheduleofvalues**) de volta para a original. 
    2. Selecione o mapa de gravação dupla na lista de mapas, selecione **Versão do mapa de tabela** e selecione a versão original do mapa de tabela.
    3. Selecione **Salvar**.
    4. Reinicie os seguintes mapas de gravação dupla:

        - Etapas da linha de contrato da integração do Project Operations (msdyn\_contractlinescheduleofvalues)
        - Valores reais da integração do Project Operations (msdyn\_actuals)
        - Proposta de fatura do projeto V2 (faturas)

Agora, as etapas são migradas e o sistema está pronto para as próximas etapas da atividade de substituição.
