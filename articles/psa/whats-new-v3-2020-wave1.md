---
title: Novidades ou alterações no Project Service Automation versão 3.x, onda 1 2020
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado no Project Service Automation versão 3 onda 1 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2308f83e09c25059b6a36599b04b5b00f66c704f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126469"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novidades ou alterações no Project Service Automation versão 3.x onda 1 2020
O tópico destaca as principais considerações de atualização ao passar para a versão mais recente do Project Service Automation (PSA) versão 3.x onda 1 2020.

## <a name="time-entry"></a>Entrada de tempo
A experiência de entrada de hora foi estendida para fornecer recursos para estender a entrada de hora em mais cenários de clientes. Isso inclui a capacidade de adicionar tipos de entrada, que agora acionam um comportamento específico com base no nome do esquema de campo **Configurações de Entrada de Hora**, exibido como **Fonte de Tempo**. Uma nova solução, chamada Tempo, Despesa, Status e Aprovações (TESA) foi adicionada para oferecer suporte a essa funcionalidade.

### <a name="upgrade-consideration"></a>Consideração sobre atualização
Para oferecer suporte a esta funcionalidade, as funções no PSA foram atualizadas para incluir novos privilégios. Esses privilégios concedem acesso de leitura à nova entidade **Configurações de Entrada de Hora**.

Os usuários que precisam da capacidade de registrar o tempo devem receber a função de usuário **Usuário de Entrada de Hora** além das funções existentes. Esta função inclui a nova funcionalidade e garante que a entrada de hora continuará funcionando.

Além disso, se você tiver algum módulo de aplicativo personalizado que inclua todos os formulários para a entidade de entrada de horas, será necessário remover o **Formulário de criação rápida de entrada de tempo TESA** do módulo.

### <a name="currently-extended-time-entry-changes"></a>Alterações da entrada de hora atualmente estendida
Para minimizar o impacto aos usuários atuais da entrada de hora, esta função altera somente o principal requisito necessário para continuar utilizando a entrada de hora. Se você tiver criado exibições personalizadas ou experiências de entrada de hora separadas, será necessário configurar os campos da **Configuração de Entrada de Hora** com os valores corretos do PSA.
