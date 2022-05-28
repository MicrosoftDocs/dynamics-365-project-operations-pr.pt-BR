---
title: Novidades ou alterações na Versão de Atualização 43 do Project Service Automation V3
description: Este tópico lista os recursos e as correções disponíveis na Versão de Atualização 43 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8709959"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Novidades ou alterações na Versão de Atualização 43 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas do Project Service Automation Versão de Atualização 43, V3. Esta versão apresenta o número de compilação V3.10.74.200 e está disponível para o público em geral por meio de uma atualização automática de maio de 2022.

## <a name="update-release-43"></a>Versão de Atualização 43

### <a name="bug-fixes"></a>Correções de bug

Os seguintes problemas foram corrigidos.


**Tempo e Despesa**

- Ao importar entradas de hora de reservas ou atribuições de recursos, a referência ao recurso reservável relacionado não é mantida.
- Quando a grade de entrada de horas é expandida para tela inteira, a navegação na grade com a tecla Tab não funciona.
- Ao enviar uma entrada de hora criada por outro usuário, o campo **Enviado por** é preenchido incorretamente com o usuário que criou a folha de ponto.
