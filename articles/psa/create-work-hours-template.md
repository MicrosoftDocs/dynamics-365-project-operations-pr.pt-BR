---
title: Criar um modelo de horas de trabalho
description: Este tópico descreve como criar um modelo de horas de trabalho no Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5788378c7e015c4b11182aaf427aca7d1da48b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598934"
---
# <a name="create-a-work-hours-template-project-service"></a>Criar um modelo de horário de trabalho (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Para criar e gerenciar um projeto, você deve aplicar um modelo de calendário ao projeto. O modelo de calendário define os seguintes atributos de projeto:

- Horas de trabalho, incluindo horário de início e término
- Dias úteis
- Exceções de calendário, como dias não úteis

O modelo de calendário aplicado a um projeto é uma cópia do modelo de calendário definido nas configurações da sua organização.

> [!NOTE]
> Se você alterar o modelo de calendário, essas alterações não se propagarão para as horas de trabalho do projeto. Para alterar as horas de trabalho do projeto, um novo modelo deve ser aplicado.

Para criar um modelo de calendário para sua organização, existem dois requisitos principais:

- Defina as horas de trabalho desejadas do modelo usando um recurso reservável novo ou existente.
- Crie um novo modelo de calendário e associe o modelo ao recurso reservável.

**Defina as horas de trabalho do modelo**

1. Vá para **Recursos** \> **Recursos**.
2. Crie um novo recurso para fazer referência no modelo de calendário ou selecione um recurso existente.
3. Selecione a guia **Horas de Trabalho** do recurso e complete as instruções em [Definir horas de trabalho para um recurso](/dynamics365/field-service/set-work-hours-resource) para configurar as regras de calendário.

**Criar um novo modelo de calendário**

1. Acesse **Configurações** \> **Modelo de Calendário**.
2. Selecione **Novo** e insira um nome, uma descrição e um recurso de modelo.


> [!NOTE]
> Quando um recurso é referenciado em um modelo de calendário, uma cópia do calendário do recurso é associada ao modelo de calendário. Se as horas de trabalho do modelo copiado mudarem, essas alterações não serão propagadas no modelo de calendário.


### <a name="see-also"></a>Consulte também  
 [Configurar recursos](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
