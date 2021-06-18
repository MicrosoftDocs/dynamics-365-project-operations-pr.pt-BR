---
title: Tipos de estágio do projeto
description: Este tópico fornece informações sobre os estágios do projeto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ed725d8ea2f671c45a7a19bb017bbb08c41f42db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008972"
---
# <a name="project-stage-types"></a>Tipos de estágio do projeto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os estágios do projeto são elaborados para refletir o estado do projeto conforme o progresso. As personalizações podem ser usadas para atualizar os estágios automaticamente com fluxos do processo empresarial, Power Automate, ou extensões de plug-in.

Os estágios a seguir são definidos no BPF padrão:

- Nova
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]