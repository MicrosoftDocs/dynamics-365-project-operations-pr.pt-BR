---
title: Novidades ou alterações na Versão de Atualização 47 do Project Service Automation V3
description: Este artigo lista os recursos e as correções disponíveis na atualização do Microsoft Dynamics 365 Project Service Automation versão 47, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477224"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Novidades ou alterações na Versão de Atualização 47 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista os recursos e as correções novos ou alterados na atualização do Project Service Automation versão 45, V3. Esta versão tem um número de compilação de V3.10.78.8 e geralmente fica disponível por meio de uma atualização automática em julho de 2022.

## <a name="update-release-47"></a>Versão de Atualização 47

### <a name="bug-fixes"></a>Correções de bug

Os seguintes problemas foram corrigidos.

**Gerenciamento de Recursos**
- Uma validação foi atualizada para garantir que os usuários não possam desencadear uma exceção de referência nula ao tentar criar um membro da equipe do projeto sem um **Recurso Reservável**.
