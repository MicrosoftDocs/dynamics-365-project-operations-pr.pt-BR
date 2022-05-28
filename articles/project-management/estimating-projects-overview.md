---
title: Conceitos de estimativa financeira
description: Este tópico fornece informações sobre estimativas financeiras de projetos no Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 338d2924f0e2a4a7fb943686eaad421a892dce70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597738"
---
# <a name="financial-estimation-concepts"></a>Conceitos de estimativa financeira

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

No Dynamics 365 Project Operations, você pode estimar financeiramente seus projetos em duas fases: 
1. Durante a fase de pré-venda, antes de fechar o negócio. 
2. Durante a fase de execução após a criação do contrato do projeto. 

Você pode criar uma estimativa financeira para o trabalho baseado em projeto usando qualquer uma das seguintes 3 páginas:
- A página **Linha de cotação**, usando os detalhes da linha de cotação.  
- A página **Linha de contrato do projeto**, usando os detalhes da linha do contrato. 
- A página **Projeto**, usando as página da guia **Tarefas**  ou **Estimativas de Despesas**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Use uma cotação de projeto para criar uma estimativa
Em uma cotação baseada em projeto, você pode usar a entidade **Detalhes da linha de cotação** para estimar o trabalho que é necessário para entregar um projeto. Essa estimativa pode ser compartilhada com o cliente.

As linhas de cotação baseadas em projeto podem ter de zero a muitos detalhes da linha de cotação. Os detalhes da linha de cotação são usados para estimar horas, despesas ou tarifas. O Microsoft Dynamics 365 Project Operations não permite estimativas de material em detalhes da linha de cotação. Essas são chamadas de classes de transação. Os valores estimados de impostos também podem ser inseridos em uma classe de transação.

Além das classes de transação, os detalhes da linha de cotação têm um tipo de transação. Há suporte a dois tipos de transação para detalhes da linha de cotação: **Custo** e **Contrato de Projeto**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Use um contrato de projeto para criar uma estimativa

Se você usou uma cotação quando criou um contrato baseado em projeto, a estimativa que foi feita para cada linha de cotação será copiada para o contrato de projeto. A estrutura de um contrato de projeto é como a estrutura da cotação do projeto, que tem linhas, detalhes da linha e agendamento de fatura.

As estimativas podem ser feitas diretamente em um contrato de projeto, como em uma cotação de projeto. Para uma cotação de projeto, a estimativa é feita usando linhas de contrato e detalhes da linha de contrato. Os detalhes da linha de contrato também podem ser gerados de um plano de projeto que foi criado usando a abordagem de estimativa crescente.

Os detalhes da linha de contrato podem ser usados para estimar horas, despesas ou tarifas. Os valores estimados de imposto também podem ser inseridos em um detalhe da linha de contrato.

As estimativas de material não são permitidas em detalhes da linha de contrato.

## <a name="use-a-project-to-create-an-estimate"></a>Use um projeto para criar uma estimativa 

Você pode estimar horas e despesas nos projetos. O Project Operations não suporta estimativas de materiais ou taxas nos projetos.

As estimativas de horas são geradas quando você cria uma tarefa e identifica os atributos de um recurso genérico que é exigido para executar a tarefa. As estimativas de tempo são geradas nas tarefas de agendamento. As estimativas de horas não serão criadas se você criar membros da equipe genéricos fora do contexto da agenda.

As estimativas de despesa são inseridas na grade da página **Estimativas de Despesas**.

A criação de uma estimativa para um projeto é considerada uma prática recomendada porque você pode construir estimativas crescentes detalhadas para mão de obra ou tempo e despesas em cada tarefa no plano do projeto. Você pode então usar esta estimativa detalhada para criar estimativas para cada linha de cotação e construir uma cotação mais confiável para o cliente. Quando você importa ou cria uma estimativa detalhada na linha de cotação usando o plano do projeto, o Project Operations importa os valores de vendas e os valores de custo dessas estimativas. Após a importação, você pode visualizar a lucratividade, as margens e as métricas de viabilidade na cotação do projeto.

## <a name="understanding-estimates"></a>Reconhecendo estimativas

Use a tabela a seguir como um guia para reconhecer a lógica de negócios na fase de estimativa.

| Cenário                                                                                                                                                                                                                                                                                                                                          | Registro da entidade                                                                                                                                                                                                       | Tipo de Transação | Classe da Transação | Informações adicionais                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Quando você precisar estimar o valor do tempo de vendas em uma cotação                                                                                                                                                                                                                                                                                    | O registro QLD (detalhes da linha de cotação) é criado                                                                                                                                                                               | Contrato do projeto | Time        | O campo de origem da transação na linha QLD do lado das vendas faz referência ao QLD do lado do custo |
|                                                                                                                                                                                                                                                                                     | Um segundo registro QLD é criado pelo sistema para armazenar os valores de custo correspondentes. Todos os campos não monetários são copiados pelo sistema do QLD de vendas para o QLD de custo.                                                                                                                                                                               | Custo | Time        | O campo de origem da transação na linha QLD (detalhes da linha de cotação) do lado das vendas faz referência ao QLD do lado do custo |
| Quando você precisar estimar o valor do tempo de vendas em um contrato                                                                                                                                                                                                                                                                                 | O registro CLD (detalhes da linha de contrato) do projeto é criado                                                                                                                                                                    | Contrato do Projeto | Time        | O campo de origem da transação na linha CLD do lado das vendas faz referência ao CLD do custo      |
|                                                                                                                                                                                                                                                                                  | Um segundo registro CLD é criado pelo sistema para armazenar os valores de custo correspondentes. Todos os campos não monetários são copiados pelo sistema do CLD de vendas para o CLD de custo.                                                                                                                                                                    | Custo | Time        | O campo de origem da transação na linha CLD do lado das vendas faz referência ao CLD do custo      |
| Quando o usuário descreve um recurso em uma tarefa do projeto                                                                                                                                                                                                                                                                                            | O registro de linha de estimativa para mostrar o valor de vendas da tarefa é criado quando uma tarefa é criada com todas as dimensões de preço. A função e as unidades organizacionais são as dimensões de preço | Contrato do Projeto | Hora        |                                                                                   |
|     | O registro de linha de estimativa para mostrar o valor de custo da tarefa é criado quando uma tarefa é criada com todas as dimensões de preço. Todos os campos não monetários são copiados pelo sistema da linha de estimativa de vendas para a linha de estimativa de custo. A função e a unidade organizacional são as dimensões de preço para taxas de custo e cobrança.                                                                                                                                                                                                                | Custo             | Hora           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalizar as entidades Detalhes da linha de cotação e Detalhes da linha de contrato

Se você adicionou um campo personalizado nos detalhes da linha de cotação e deseja que o sistema insira o valor do campo como um valor padrão na linha de custo relacionada que ele cria, use as ferramentas de registro de plug-in **PreOperationContractLineDetailUpdate** e **PreOperationQuoteLineDetailUpdate**. Esses plug-ins devem ser registrados novamente depois que os detalhes da linha de cotação ou os detalhes da linha de contrato são alterados. Siga estas etapas para concluir o processo.

1. Abra PluginRegistrationTool e conecte-se à sua instância online
2. Selecione **Pesquisar** e procure o plug-in a ser atualizado.
3. Selecione o plug-in e, em seguida, na página principal, clique em **Selecionar**.
4. Selecione a etapa do plug-in a ser atualizado, clique com o botão direito do mouse e selecione **Atualizar**.
5. Na caixa de diálogo **Atualizar Etapa Existente**, no campo **Filtrando Atributos**, selecione o botão de reticências (**...**):
6. Na caixa de diálogo **Selecionar Atributos**, marque as caixas de seleção de atributos personalizados.
7. Selecione **OK** para fechar a caixa de diálogo e, em seguida, **Atualizar Etapa**.
8. Repita as etapas de 1 a 7 para o segundo plug-in.
9. Feche a **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
