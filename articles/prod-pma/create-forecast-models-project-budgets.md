---
title: Criar modelos de previsão para orçamentos de projeto
description: Este artigo descreve como criar um modelo de previsão para orçamentos restantes.
author: Yowelle
ms.date: 04/24/2020
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
ms.openlocfilehash: e6b1419c41124d2062595f7346efb7538e50ee33
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916688"
---
# <a name="create-forecast-models-for-project-budgets"></a>Criar modelos de previsão para orçamentos de projeto 

[!include [banner](../includes/banner.md)]

Este artigo descreve como criar um modelo de previsão para orçamentos restantes. Um projeto sujeito a controle de orçamento usa dois tipos de orçamento: original e restante. Ao criar um orçamento de projeto, você deverá especificar os modelos de previsão de orçamento original e restante que foram criados na página **Modelos de previsão**. Os orçamentos do projeto com base nos modelos especificados são criados quando você compromete o orçamento do projeto.

> [!NOTE]
> Um modelo de previsão usado para controle de orçamento não pode ter um submodelo ou ser usado como um submodelo.

1. Selecione **Gerenciamento e contabilidade de projeto** > **Configuração** > **Previsões**  > **Modelos de previsão**.
2. Selecione **Novo** para criar um novo modelo de previsão e, em seguida, insira um número de ID de modelo e nome para o novo modelo. 
3. Defina a opção **Parado** como **Sim** para evitar quaisquer alterações nas linhas de previsão do modelo de previsão. 
4. Se as linhas de previsão às quais o modelo está associado tiverem de gerar previsões de fluxo de caixa no razão geral, defina **Incluir nas previsões de Fluxo de caixa** como **Sim.** 
5. Para usar a data do projeto como data da fatura, defina **Previsão da data da fatura** como **Sim**. 
6. No campo **Tipo de orçamento**, selecione um dos seguintes tipos de modelo:

   - **Orçamento original**: use os valores do orçamento original comprometidos quando o orçamento inicial for criado e aprovado.
   - **Orçamento restante**: use os valores de orçamento restante durante a vida do projeto. Os saldos neste modelo de previsão são reduzidos por transações reais e aumentados ou diminuídos por revisões de orçamento.
   - **Transferência**: use os valores do orçamento de transferência para o projeto. Transporte é um processo opcional que pode ser executado para transferir valores de orçamento não utilizados de um ano fiscal para outro.

7. Defina as seguintes opções como necessário:

   - Habilite **Previsão da data da fatura** para usar a data do projeto como a data da fatura.
   - Habilite **Previsão com WIP** para prever com base no trabalho em andamento (WIP) e, em seguida, selecione o tipo de WIP. 
   - Você pode manter o **Tipo de orçamento** padrão como **Nenhum** ou insira um novo tipo. O tipo de orçamento não poderá ser alterado após a alteração de um registro.     
    > [!NOTE]
    > Se você alterar o tipo de orçamento padrão, todas as outras opções ficarão indisponíveis para atualizações e você não poderá reutilizar esse modelo de previsão. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]