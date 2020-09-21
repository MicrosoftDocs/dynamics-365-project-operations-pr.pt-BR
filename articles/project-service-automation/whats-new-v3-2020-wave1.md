---
title: Novidades ou alterações no Project Service Automation versão 3.x, onda 1 2020
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado no Project Service Automation versão 3 onda 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749070"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novidades ou alterações no Project Service Automation versão 3.x onda 1 2020
O tópico destaca as principais considerações de atualização ao passar para a versão mais recente do Project Service Automation (PSA) versão 3.x onda 1 2020.

## <a name="time-entry"></a>Entrada de tempo
A experiência de entrada de hora foi estendida para fornecer recursos para estender a entrada de hora em mais cenários de clientes. Isso inclui a capacidade de adicionar tipos de entrada, que agora acionam um comportamento específico com base no nome do esquema de campo **Configurações de Entrada de Hora**, exibido como **Fonte de Tempo**.

### <a name="upgrade-consideration"></a>Consideração sobre atualização
Para oferecer suporte a esta funcionalidade, as funções no PSA foram atualizadas para incluir novos privilégios. Esses privilégios concedem acesso de leitura à nova entidade **Configurações de Entrada de Hora**.

Os usuários que precisam da capacidade de registrar o tempo devem receber a função de usuário **Usuário de Entrada de Hora** além das funções existentes. Esta função inclui a nova funcionalidade e garante que a entrada de hora continuará funcionando.

### <a name="currently-extended-time-entry-changes"></a>Alterações da entrada de hora atualmente estendida
Para minimizar o impacto aos usuários atuais da entrada de hora, esta função altera somente o principal requisito necessário para continuar utilizando a entrada de hora. Se você tiver criado exibições personalizadas ou experiências de entrada de hora separadas, será necessário configurar os campos da **Configuração de Entrada de Hora** com os valores corretos do PSA.
