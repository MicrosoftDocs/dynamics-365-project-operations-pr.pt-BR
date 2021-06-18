---
title: Estimativas
description: Este tópico fornece informações sobre estimativas no Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fcb3c85af092667cc5a473ab4674c3be47e33327
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007577"
---
# <a name="estimates"></a>Estimativas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Em uma cotação baseada em projeto, você pode usar a entidade Detalhes da linha de cotação para estimar o trabalho que é necessário para entregar um projeto. Essa estimativa pode ser compartilhada com o cliente.

As linhas de cotação baseadas em projeto não precisam ter qualquer detalhe da linha de cotação. Ou, elas podem ter muitos detalhes da linha de cotação. Os detalhes da linha de cotação são usados para estimar tempo, despesas ou tarifas. O PSA não permite estimativas de material em detalhes da linha de cotação. Essas são chamadas de classes de transação. Os valores estimados de impostos também podem ser inseridos em uma classe de transação.

Além das classes de transação, os detalhes da linha de cotação têm um tipo de transação. O PSA aceita dois tipos de transação para detalhes da linha de cotação: **Custo** e **Contrato de Projeto**.

## <a name="estimate-by-using-a-contract"></a>Estimativa usando um contrato

Se você usou uma cotação do PSA quando criou um contrato baseado em projeto, a estimativa que foi feita para cada linha na cotação será copiada para o contrato de projeto. A estrutura de um contrato de projeto é como a estrutura da cotação do projeto, que tem linhas, detalhes da linha e agendamento de fatura.

As estimativas podem ser feitas diretamente em um contrato de projeto, como em uma cotação de projeto. Para uma cotação de projeto, a estimativa é feita usando linhas de contrato e detalhes da linha de contrato. Os detalhes da linha de contrato também podem ser gerados de um plano de projeto que foi criado usando a abordagem de estimativa crescente.

Os detalhes da linha de contrato podem ser usados para estimar horas, despesas ou tarifas. Os valores estimados de imposto também podem ser inseridos em um detalhe da linha de contrato.

O PSA não permite estimativas de material em detalhes da linha de contrato.

Os processos que são aceitos em um contrato de projeto são a criação e a confirmação da fatura. A criação da fatura cria um rascunho de uma fatura baseada em projeto que inclui todos os dados reais de vendas não cobradas até a data atual.

A confirmação torna o contrato somente leitura e muda seu status de **Rascunho** para **Confirmado**. Depois de tomada essa ação, não é possível desfazê-la. Como essa ação é permanente, é uma prática recomendada manter o contrato no status de **Rascunho**.

As únicas diferenças entre rascunhos de contratos e contratos confirmados são os respectivos status e o fato de que os rascunhos de contratos podem ser editados enquanto os confirmados, não. A criação da fatura e o acompanhamento de dados reais podem ser feitos em rascunhos de contratos e contratos confirmados.

O PSA não permite mudança de ordens em contratos nem projetos.

## <a name="estimating-projects"></a>Estimando projetos

Você pode estimar tempo e despesas nos projetos. O PSA não permite estimativas de materiais nem tarifas em projetos.

As estimativas de tempo são geradas quando você cria uma tarefa e identifica os atributos de um recurso genérico que é exigido para executar a tarefa. As estimativas de tempo são geradas nas tarefas de agendamento. As estimativas de horas não serão criadas se você criar membros da equipe genéricos fora do contexto da agenda.

As estimativas de despesa são inseridas na grade da página **Estimativas**.

## <a name="understanding-estimation"></a>Reconhecendo a estimativa

Use a tabela a seguir como um guia para reconhecer a lógica de negócios na fase de estimativa.

| Cenário                                                                                                                                                                                                                                                                                                                                          | Registro da entidade                                                                                                                                                                                                       | Tipo de Transação | Classe da Transação | Informações adicionais                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Quando você precisar estimar o valor do tempo de vendas em uma cotação                                                                                                                                                                                                                                                                                    | O registro QLD (detalhes da linha de cotação) é criado                                                                                                                                                                               | Contrato do projeto | Time        | O campo de origem da transação na linha QLD do lado das vendas faz referência ao QLD do lado do custo |
|                                                                                                                                                                                                                                                                                     | Um segundo registro QLD é criado pelo sistema para armazenar os valores de custo correspondentes. Todos os campos não monetários são copiados pelo sistema do QLD de vendas para o QLD de custo.                                                                                                                                                                               | Custo | Time        | O campo de origem da transação na linha QLD (detalhes da linha de cotação) do lado das vendas faz referência ao QLD do lado do custo |
| Quando você precisar estimar o valor do tempo de vendas em um contrato                                                                                                                                                                                                                                                                                 | O registro CLD (detalhes da linha de contrato) do projeto é criado                                                                                                                                                                    | Contrato do Projeto | Time        | O campo de origem da transação na linha CLD do lado das vendas faz referência ao CLD do custo      |
|                                                                                                                                                                                                                                                                                  | Um segundo registro CLD é criado pelo sistema para armazenar os valores de custo correspondentes. Todos os campos não monetários são copiados pelo sistema do CLD de vendas para o CLD de custo.                                                                                                                                                                    | Custo | Time        | O campo de origem da transação na linha CLD do lado das vendas faz referência ao CLD do custo      |
| Quando o usuário descreve um recurso em uma tarefa do projeto                                                                                                                                                                                                                                                                                            | O registro de linha de estimativa para mostrar o valor de vendas da tarefa é criado quando uma tarefa é criada com todas as dimensões de preço. A função e as unidades organizacionais são as dimensões de preço OOB do Project Service | Contrato do Projeto | Time        |                                                                                   |
|     | O registro de linha de estimativa para mostrar o valor de custo da tarefa é criado quando uma tarefa é criada com todas as dimensões de preço. Todos os campos não monetários são copiados pelo sistema da linha de estimativa de vendas para a linha de estimativa de custo. A função e a unidade organizacional são as dimensões de preço OOB do PSA para taxas de custo e cobrança.                                                                                                                                                                                                                | Custo             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalizando as entidades Detalhes da linha de cotação e Detalhes da linha de contrato

Se você adicionou um campo personalizado nos detalhes da linha de cotação e quer que o sistema insira o valor do campo como um valor padrão na linha de custo relacionada que ele cria, use as ferramentas de registro de plug-in PreOperationContractLineDetailUpdate e PreOperationQuoteLineDetailUpdate. Esses plug-ins devem ser registrados novamente depois que os detalhes da linha de cotação ou os detalhes da linha de contrato são alterados. Siga estas etapas para concluir o processo.

1. Abra PluginRegistrationTool e conecte-se à sua instância online
2. Selecione **Pesquisar** e procure o plug-in a ser atualizado.

    ![Caixa de diálogo Árvore de Pesquisa](media/basic-guide-19.png)

3. Selecione o plug-in e, em seguida, na página principal, escolha **Selecionar**.
4. Selecione a etapa do plug-in a ser atualizado, clique com o botão direito do mouse e selecione **Atualizar**.

    ![Selecionando uma etapa no plug-in](media/basic-guide-20.png)

5. Na caixa de diálogo **Atualizar Etapa Existente**, no campo **Filtrando Atributos**, selecione o botão de reticências (**...**):
 
    ![Caixa de diálogo Atualizar Etapa Existente](media/basic-guide-21.png)

6. Na caixa de diálogo **Selecionar Atributos**, marque as caixas de seleção de atributos personalizados.

    ![Caixa de diálogo Selecionar Atributos](media/basic-guide-22.png)

7. Selecione **OK** para fechar a caixa de diálogo e, em seguida, **Atualizar Etapa**.
 
    ![Botão Atualizar Etapa](media/basic-guide-23.png)

8. Repita as etapas de 1 a 7 para o segundo plug-in.
9. Feche a ferramenta PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]