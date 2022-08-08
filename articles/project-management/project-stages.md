---
title: Estágios do projeto
description: Este artigo fornece informações sobre os estágios do projeto que estão disponíveis no Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a8c8e63a2d8c238f582b67348f88b7285a0b1e12
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177321"
---
# <a name="project-stages"></a>Estágios do projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os estágios do projeto são elaborados para refletir o estado do projeto conforme o progresso. As personalizações podem ser usadas para atualizar os estágios automaticamente com fluxos do processo empresarial, Power Automate, ou extensões de plug-in.

Os seguintes estágios são definidos no fluxo do processo empresarial padrão:

- Criar
- Cotação
- Plano
- Entregar
- Complete
- Fechar 

## <a name="new"></a>Criar

Ao criar um projeto, o estágio dele é definido como **Novo**. Se o projeto foi criado com base em um modelo, ele pode ter dados de agenda, estimativas e equipe. Caso contrário, é um resumo do projeto e os componentes restantes devem ser inseridos.

## <a name="quote"></a>Cotação

Ao associar um projeto a uma cotação ou criar um projeto com base em uma cotação, o estágio do projeto é definido como **Cotação** e as datas estimadas de início e de término são atualizadas. Enquanto o projeto está no estágio **Cotação**, a guia **Vendas** na página **Entidade de Projeto** exibe detalhes da cotação.

## <a name="plan"></a>Planejar

Quando você vence uma cotação associada a um projeto e este é movido para a fase **Contrato**, o estágio do projeto é atualizado para **Planejar**. Enquanto o projeto está no estágio **Plano**, a guia **Vendas** na página **Entidade do Projeto** exibe detalhes do contrato.

## <a name="deliver"></a>Entregar

Quando o plano do projeto estiver concluído e você estiver pronto para iniciar o projeto, o gerente deverá atualizar o estágio do projeto para **Entregar** a fim de mostrar que o projeto foi iniciado.

## <a name="complete"></a>Concluído 

Quando o trabalho no projeto estiver concluído, o gerente do projeto poderá atualizar o estágio para **Concluído**. Ao atualizar o estágio do projeto para **Concluído**, o gerente indica que o trabalho está 100% concluído, mas que o projeto está sendo mantido aberto para que quaisquer entradas pendentes de hora ou despesa possam ser registradas.

## <a name="close"></a>Fechar

Quando todas as transações do projeto estiverem registradas, o gerente do projeto poderá atualizar o estágio para **Fechar**. Nesse momento, nenhuma transação pode ser registrada e o projeto é definido como somente leitura.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
