---
title: Novidades ou alterações na Versão de Atualização 45 do Project Service Automation V3
description: Este artigo lista os recursos e as correções disponíveis na atualização do Microsoft Dynamics 365 Project Service Automation versão 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169147"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Novidades ou alterações na Versão de Atualização 45 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista os recursos e as correções novos ou alterados na atualização do Project Service Automation versão 45, V3. Esta versão tem um número de compilação de V3.10.76.168 e geralmente fica disponível por meio de uma atualização automática em julho de 2022.

## <a name="update-release-45"></a>Versão de Atualização 45

### <a name="bug-fixes"></a>Correções de bug

Os seguintes problemas foram corrigidos.

**Vendas**

- Os usuários não conseguirão criar faturas com êxito depois de tentarem criar uma fatura sem nenhuma venda não faturada se também estiverem visualizando a mesma instância da página e não a atualizarem.

**Tempo e Despesa**

- Quando as Aprovações Modernas estão habilitadas e uma aprovação de projeto recuperada é aprovada, o estágio de registro é atualizado incorretamente para **Solicitação de Recuperação Aprovada**.
- Quando as Aprovações Modernas estão habilitadas e Fluxos de Nuvem está inativo, não há êxito no processo de aprovação e os usuários que enviam ou aprovam não são notificados.
