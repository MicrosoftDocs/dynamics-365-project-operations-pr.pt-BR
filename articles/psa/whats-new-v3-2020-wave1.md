---
title: Novidades ou alterações no Project Service Automation versão 3.x, onda 1 2020
description: Este artigo inclui informações sobre o que há de novo e o que foi alterado no ciclo 1 de 2020 do Project Service Automation versão 3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c762f2e7931046d32464cfa8486ef8405aa7d836
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928602"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novidades ou alterações no Project Service Automation versão 3.x onda 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

O artigo destaca as principais considerações de atualização ao migrar para a versão mais recente do ciclo 1 de 2020 do Project Service Automation (PSA) versão 3.x.

## <a name="time-entry"></a>Entrada de tempo
A experiência de entrada de hora foi estendida para fornecer recursos para estender a entrada de hora em mais cenários de clientes. Isso inclui a capacidade de adicionar tipos de entrada, que agora acionam um comportamento específico com base no nome do esquema de campo **Configurações de Entrada de Hora**, exibido como **Fonte de Tempo**. Uma nova solução, chamada Tempo, Despesa, Status e Aprovações (TESA) foi adicionada para oferecer suporte a essa funcionalidade.

### <a name="upgrade-consideration"></a>Consideração sobre atualização
Para oferecer suporte a esta funcionalidade, as funções no PSA foram atualizadas para incluir novos privilégios. Esses privilégios concedem acesso de leitura à nova entidade **Configurações de Entrada de Hora**.

Os usuários que precisam da capacidade de registrar o tempo devem receber a função de usuário **Usuário de Entrada de Hora** além das funções existentes. Esta função inclui a nova funcionalidade e garante que a entrada de hora continuará funcionando.

Além disso, se você tiver algum módulo de aplicativo personalizado que inclua todos os formulários para a entidade de entrada de horas, será necessário remover o **Formulário de criação rápida de entrada de tempo TESA** do módulo.

### <a name="currently-extended-time-entry-changes"></a>Alterações da entrada de hora atualmente estendida
Para minimizar o impacto aos usuários atuais da entrada de hora, esta função altera somente o principal requisito necessário para continuar utilizando a entrada de hora. Se você tiver criado exibições personalizadas ou experiências de entrada de hora separadas, será necessário configurar os campos da **Configuração de Entrada de Hora** com os valores corretos do PSA.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
