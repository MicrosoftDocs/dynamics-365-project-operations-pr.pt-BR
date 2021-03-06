---
title: Estágios do projeto
description: Este tópico fornece informações sobre as etapas do projeto que estão disponíveis em Operações do projeto do Microsoft Dynamics.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b11c67ebd21fdf423eeae2db8154f26787c2e64f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897932"
---
# <a name="project-stages"></a>Estágios do projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

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

Quando você vence uma cotação associada a um projeto e este é movido para a fase **Contrato**, o estágio do projeto é atualizado para **Planejar**. Enquanto o projeto está no estágio **Planejar**, a página **Entidade de Projeto** exibe detalhes do contrato.

## <a name="deliver"></a>Entregar

Quando o plano do projeto estiver concluído e você estiver pronto para iniciar o projeto, o gerente deverá atualizar o estágio do projeto para **Entregar** a fim de mostrar que o projeto foi iniciado.

## <a name="complete"></a>Concluído 

Quando o trabalho no projeto estiver concluído, o gerente do projeto poderá atualizar o estágio para **Concluído**. Ao atualizar o estágio do projeto para **Concluído**, o gerente indica que o trabalho está 100% concluído, mas que o projeto está sendo mantido aberto para que quaisquer entradas pendentes de hora ou despesa possam ser registradas.

## <a name="close"></a>Fechar

Quando todas as transações do projeto estiverem registradas, o gerente do projeto poderá atualizar o estágio para **Fechar**. Nesse momento, nenhuma transação pode ser registrada e o projeto é definido como somente leitura.

