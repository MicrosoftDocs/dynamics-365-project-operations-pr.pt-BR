---
title: Reservas x atribuições
description: Este tópico fornece informações sobre as diferenças entre reservas de recursos e atribuições de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130204"
---
# <a name="bookings-vs-assignments"></a>Reservas x atribuições

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As reservas são a alocação fixa ou flexível de recursos para um projeto. As reservas fixas consomem a capacidade de um recurso. As reservas representam conceitos organizacionais para equipes, para que possam entender como os recursos serão envolvidos em vários projetos. O Dynamics 365 Project Operations considera as reservas um conceito de nível de projeto. 

Diferente das reservas, as atribuições representam o compromisso de recursos a tarefas do projeto na agenda do projeto. Os recursos podem ser nomeados ou genéricos. 

Normalmente, a soma das reservas para um recurso será igual à soma das atribuições do recurso em uma ou mais tarefas. No entanto, o Project Operations não impõe essa correspondência. A exibição **Reconciliação** mostra ao gerente de projetos os locais em que as reservas e atribuições de um recurso não são correspondentes.
