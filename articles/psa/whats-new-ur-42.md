---
title: Novidades ou alterações na Versão de Atualização 42 do Project Service Automation V3
description: Este tópico lista os recursos e as correções disponíveis na Versão de Atualização 42 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589182"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novidades ou alterações na Versão de Atualização 42 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas do Project Service Automation Versão de Atualização 42, V3. Esta versão apresenta o número de build V3.10.73.61 e geralmente está disponível por meio de uma atualização automática de abril de 2022.

## <a name="update-release-42"></a>Versão de Atualização 42

### <a name="bug-fixes"></a>Correções de bug

Os seguintes problemas foram corrigidos.

**Tempo e Despesa**

- Quando uma folha de ponto é rejeitada, o usuário que a rejeitou é identificado incorretamente como **Sistema**.
- Quando as entradas de hora são importadas, o valor **Categoria de Recurso** fica ausente.
- Os aprovadores de projeto podem aprovar projetos enviados quando suas permissões não estão especificamente definidas como **Pode Aprovar**.

**Vendas**

- Quando os dados reais são registrados em tarefas de nível não raiz, os custos reais são agregados incorretamente.
