---
title: Eliminar um estimativa de projeto
description: Este artigo fornece informações sobre como eliminar uma estimativa de projeto após sua conclusão.
author: Yowelle
ms.date: 05/26/2020
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
ms.openlocfilehash: de54659f9e69daf1566f86bec16436c19eeacf49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932190"
---
# <a name="eliminate-a-project-estimate"></a>Eliminar um estimativa de projeto

[!include [banner](../includes/banner.md)]

As estimativas de projeto fornecem a visão financeira do trabalho estimado e agendado para um projeto. Para trabalhar com estimativas de projeto, você deve anexar o projeto a uma estimativa de projeto. Uma estimativa de projeto é sempre baseada em um projeto existente; no entanto, vários projetos podem se referir a uma única estimativa de projeto. Apenas os projetos de preço fixo e de investimento podem ser anexados às estimativas de projetos. Esses projetos devem pertencer ao mesmo grupo de projetos que a estimativa do projeto.

Para eliminar uma estimativa de projeto, ela deve ser concluída. As etapas a seguir explicam como eliminar uma estimativa.

1. Vá para **Gerenciamento e contabilidade de projetos** > **Todos os Projetos** e abra o projeto. 
2. Na guia **Gerenciar**, selecione **Estimativas**. Na página **Estimativa**, selecione **Eliminar**.
3. Na página **Eliminar estimativa** na guia **Geral**, defina as seguintes opções:

   - **Código de período**: selecione o código do período para escolher as estimativas de projeto apropriadas. 
   - **Data estimada**: selecione a data estimada apropriada para eliminação.
   - **Eliminar com avisos WIP**: habilite esta opção para fornecer notificação quando uma estimativa associada a um trabalho em andamento (WIP) for eliminada. Quando esta opção não estiver habilitada, a eliminação não poderá continuar se houver transações não estimadas. 
   > [!NOTE]
   > Esta opção está disponível apenas quando a eliminação é aplicada a uma estimativa de projeto. Ela não estará disponível se você estiver usando postagens periódicas. Esta configuração funciona com as configurações na guia **Estimativa** na página **Parâmetros do projeto**, no grupo de campos **Permitir eliminação quando houver transações não estimadas**.
   - **Definir estágio como Concluído**: habilite esta opção para definir o estágio de estimativa do projeto como **Concluído** depois de executar a eliminação.
   - **Imprimir lista de estimativa**: selecione as informações a serem incluídas quando a lista de orçamentos for impressa.
   - **Mostrar Log de Informações**: habilite esta opção para exibir o log de informações.
   - **Data de postagem**: escolha a data de lançamento contábil da estimativa.

4.  Selecione **OK**.
5. Após a conclusão do processo de eliminação, a estimativa do projeto eliminada é exibida com um valor negativo. 

Se você não pretendia eliminar uma estimativa, poderá selecionar a estimativa eliminada e selecionar **Reverter eliminação**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]