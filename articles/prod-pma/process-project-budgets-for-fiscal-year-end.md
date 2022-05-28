---
title: Transferir orçamentos de projetos no fim do ano fiscal
description: Este artigo fornece informações sobre como transferir os valores de orçamento restantes para os próximos anos e criar detalhes do registro de orçamento.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5b4e768cb78d6a6cb76b3c338fd76363d5290ebd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684030"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Transferir orçamentos de projetos no fim do ano fiscal

[!include [banner](../includes/banner.md)]

Ao trabalhar em um projeto de vários anos, você pode ter orçamento restante no final do ano fiscal. Você pode transferir os valores de orçamento restantes para um ano futuro e criar detalhes de registro de orçamento para os valores nas contas do razão geral associadas. Antes de transferir os valores restantes, revise e analise os valores restantes do orçamento.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Revisar e analisar os valores de orçamento restantes

Conclua as etapas a seguir para revisar os valores do orçamento de final de ano para projetos, mas não transfira os valores.

1. Vá para **Gerenciamento e contabilidade de projetos** > **Periódico** > **Orçamentos** > **Transferir orçamentos**. 
2. Na página **Processo de transferência de orçamento do projeto**, na guia **Opções de fim de ano**, verifique se **Transferir valores restantes do orçamento do projeto** não está habilitado.
3. Na guia **Parâmetros**, no campo **Ano do orçamento do projeto**, selecione o ano fiscal para o qual deseja exibir o valor do orçamento restante. 
4. No campo **Ano fiscal de abertura**, selecione o ano fiscal para o qual deseja exibir o valor do orçamento restante. 
5. No campo **Do modelo de previsão**, selecione **Orçamento restante**. 
6. Para incluir projetos que atendam aos critérios selecionados e não tenham orçamento restante, selecione **Mostrar zero restante**.  
7. Na guia **Selecione Orçamentos**, selecione **Recuperar todos os orçamentos** para carregar todos os orçamentos que correspondam aos critérios selecionados e, depois, selecione **Processo**. 
8. Para criar uma consulta de banco de dados que carregue um conjunto específico de orçamentos no painel, selecione **Recuperar orçamentos selecionados**.

Para obter mais informações sobre uma linha específica no painel, selecione a linha e selecione **Exibir detalhes do orçamento** ou **Exibir contas**.

## <a name="carry-forward-remaining-budget-amounts"></a>Transferir valores restantes do orçamento 

Ao processar os valores restantes do orçamento, você pode criar transações no razão geral para os valores que está transferindo. Para criar transações do razão geral, conclua as etapas na seção [Transferir valores do orçamento e criar transações do razão geral](#carry-forward). 

> [!NOTE]
> Os valores do orçamento são transferidos para o modelo de previsão selecionado na página **Modelos de previsão** como o modelo de previsão de transferência.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Transferir valores do orçamento e criar transações do razão geral

1.  Selecione **Gerenciamento e contabilidade de projetos** > **Periódico** > **Orçamentos** > **Transferir orçamentos**. 
2. Na página **Processo de transferência do orçamento do projeto**, selecione **Fim de ano** e habilite **Transferir valores restantes do orçamento do projeto** e **Criar entradas de registro de orçamento no razão geral**. 
3. Na guia **Parâmetros**, no grupo de campo **Parâmetros do projeto**, selecione o seguinte:

   - **Ano de orçamento do projeto**: selecione o início do ano fiscal para o qual deseja exibir os valores do orçamento restantes. 
   - **Lucros e perdas**: crie transações de lucros e perdas no razão geral. 
   -  **WIP**: crie transações de Trabalho em Andamento (WIP) no razão.
   -  **Folha de pagamento**: crie transações de alocação de folha de pagamento no razão geral. 

5. No grupo de campos **Razão geral**, forneça as seguintes informações: 

   - No campo **Ano fiscal de abertura**, selecione o ano fiscal para o qual você deseja transferir os valores do orçamento restantes para os projetos. O valor padrão é um ano após o valor no campo **Ano do orçamento do projeto**.
   -  No campo **Período de transferência**, selecione o período para o qual deseja criar detalhes do registro de orçamento no razão geral. Este é costuma ser o primeiro período no ano fiscal de abertura.

6. No grupo de campos **Copiar de/para**, forneça as seguintes informações:

   - No campo **Do modelo de previsão**, selecione o modelo de previsão de orçamento do projeto associado aos valores de orçamento restantes que você deseja transferir para os projetos. 
   - No campo **Para modelo de orçamento do razão**, selecione o modelo de orçamento do razão associado aos valores de orçamento que você deseja transferir para o razão geral. 
   -  Selecione **Transferir moeda de vendas** para usar a moeda de vendas do projeto para as transações do razão geral que são criadas quando você transfere os valores do orçamento para os projetos. Quando a opção não é selecionada, as transações usam a moeda contábil. 
   -  Selecione **Mostrar zero restante** para incluir projetos sem valores de orçamento restantes, mas que atendam aos outros critérios selecionados nos projetos exibidos no painel inferior.

7. Na guia **Selecione Orçamentos**, selecione **Recuperar todos os orçamentos** para carregar todos os orçamentos que correspondam aos critérios selecionados. Se preferir criar uma consulta de banco de dados que carregue um conjunto específico de orçamentos do projeto no painel, selecione **Recuperar orçamentos selecionados**.
8. Para cada projeto que você deseja processar, selecione a opção no início da linha para o projeto.

    > [!TIP]
    > Para selecionar todos ou a maioria dos projetos, selecione a marca de seleção no canto superior esquerdo. Para excluir o processamento de qualquer projeto, limpe a marca de seleção desse projeto.

9. Para transferir os valores de orçamento restantes para os projetos selecionados para o ano fiscal selecionado e criar detalhes de registro de orçamento no razão geral, selecione **Processo**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Transferir valores do orçamento sem criar transações do razão geral

1. Vá para **Gerenciamento e contabilidade de projetos** > **Periódico** > **Orçamentos** > **Transferir orçamentos**.
2. Na página **Processo de transferência de orçamento do projeto**, no campo **Opções de fim de ano**, selecione **Transferir valores restantes do orçamento do projeto**.
3. No grupo **Parâmetros**, no campo **Ano do orçamento do projeto**, selecione o ano fiscal para o qual deseja exibir os valores de orçamento restantes.
4. No grupo **Copiar de/para**, forneça as seguintes informações:

   - No campo **Do modelo de previsão**, selecione o modelo de previsão de orçamento do projeto que está associado aos valores de orçamento restantes que você deseja transferir para os projetos. 
   - Selecione **Mostrar zero restante** para incluir projetos sem valores de orçamento restantes, mas que atendam a outros critérios selecionados.
   - No grupo **Selecione Orçamentos**, selecione **Recuperar todos os orçamentos** para carregar todos os orçamentos que correspondam aos critérios selecionados. Para criar uma consulta de banco de dados que carregue um conjunto específico de orçamentos de projeto no painel, selecione **Recuperar orçamentos selecionados**.

5. Para cada projeto que você deseja processar, selecione a opção no início da linha para o projeto. 
6. Selecione **Processo** para transferir os valores de orçamento restantes dos projetos selecionados para o ano fiscal selecionado.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
