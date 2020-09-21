---
title: Estágios do projeto
description: Este tópico fornece informações sobre os estágios do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749049"
---
# <a name="project-stages"></a>Estágios do projeto 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os estágios do projeto são atualizados para refletir o estado do projeto conforme ele avança. O fluxo do processo empresarial padrão atualiza automaticamente alguns estágios do projeto enquanto outros são atualizados pelo gerente de projetos. 

Os estágios a seguir são definidos no BPF padrão:

- Novo
- Cotação
- Planejar
- Entregar
- Concluído
- Fechar 

## <a name="new"></a>Novo

Ao criar um projeto, o estágio dele é definido como **Novo**. Se o projeto foi criado com base em um modelo, ele pode ter dados de agenda, estimativas e equipe. Caso contrário, é apenas um resumo do projeto e os componentes restantes devem ser inseridos.

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
