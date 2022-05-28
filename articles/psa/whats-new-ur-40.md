---
title: Novidades ou alterações na Versão de Atualização 40 do Project Service Automation V3
description: Este tópico lista os recursos e as correções disponíveis na Versão de Atualização 40 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588630"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Novidades ou alterações na Versão de Atualização 40 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas do Project Service Automation Versão de Atualização 40, V3. Esta versão tem um número de compilação de V3.10.61.61 e está geralmente disponível por meio de uma atualização automática em fevereiro de 2022.

## <a name="update-release-40"></a>Versão de Atualização 40

### <a name="features"></a>Recursos
A fase 1 da atualização do Project Service Automation para o Project Operations - Lite será lançada em fevereiro de 2022 para todos os clientes. Para verificar a elegibilidade, consulte [Atualizar do Project Service Automation para o Project Operations](upgrade-project-operations-non-stocked.md). Se o aplicativo não aparecer na sua instância no Centro de Administração do Power Platform, entre em contato com o suporte e solicite que a versão piloto seja habilitada para seus ambientes. Sua solicitação deve incluir uma lista de IDs de ambiente em que a versão piloto precisa ser habilitada.

### <a name="bug-fixes"></a>Correções de bug

Os seguintes problemas foram corrigidos.

**Tempo e Despesa**
- Uma entrada de observação está ausente quando uma entrada de hora é rejeitada ou cancelada. 

**Vendas**

- Ao atualizar estimativas de custos ou vendas usando plug-ins prontos para uso, você incorretamente recebe permissão para enviar cargas JSON que não são válidas fora da interface do usuário.
- Ao atualizar linhas de cotação usando a exibição rápida, você recebe permissão para ativar cotações.
