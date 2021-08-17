---
title: Reservas x atribuições
description: Este tópico fornece informações sobre as diferenças entre reservas de recursos e atribuições de recursos.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1906ebd76f5fc66215aa5963242de13206a81668cb4973cccaf5b153514672d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008436"
---
# <a name="bookings-vs-assignments"></a>Reservas x atribuições

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As reservas são a alocação fixa ou flexível de recursos para um projeto. As reservas fixas consomem a capacidade de um recurso. As reservas representam conceitos organizacionais para equipes, para que possam entender como os recursos serão envolvidos em vários projetos. O Dynamics 365 Project Operations considera as reservas como um conceito de nível de projeto. 

Diferente das reservas, as atribuições representam o compromisso de recursos a tarefas do projeto na agenda do projeto. Os recursos podem ser nomeados ou genéricos.  Quando um requisito de recurso é derivado das atribuições de tarefas do projeto, o Project Operations usam os contornos de esforço da atribuição de recursos para criar os contornos dos detalhes dos requisitos de recursos. No entanto, uma referência às atribuições de recursos não é mantida. As atualizações nas reservas derivadas do requisito de recurso não atualizam nenhuma atribuição de recurso.

Normalmente, a soma das reservas para um recurso será igual à soma das atribuições do recurso em uma ou mais tarefas. No entanto, o Project Operations não impõe essa correspondência. A exibição **Reconciliação** mostra ao gerente de projetos os locais em que as reservas e atribuições de um recurso não são correspondentes.




[!INCLUDE[footer-include](../includes/footer-banner.md)]