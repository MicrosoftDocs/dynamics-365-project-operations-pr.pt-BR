---
title: Novidades ou alterações na Versão de Atualização 43 do Project Service Automation V3
description: Este artigo lista os recursos e as correções disponíveis na atualização do Microsoft Dynamics 365 Project Service Automation versão 43, V3.
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915292"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Novidades ou alterações na Versão de Atualização 43 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista os recursos e as correções novos ou alterados na atualização do Project Service Automation versão 43, V3. Esta versão apresenta o número de compilação V3.10.74.200 e está disponível para o público em geral por meio de uma atualização automática de maio de 2022.

## <a name="update-release-43"></a>Versão de Atualização 43

### <a name="bug-fixes"></a>Correções de bug

Os seguintes problemas foram corrigidos.


**Tempo e Despesa**

- Ao importar entradas de hora de reservas ou atribuições de recursos, a referência ao recurso reservável relacionado não é mantida.
- Quando a grade de entrada de horas é expandida para tela inteira, a navegação na grade com a tecla Tab não funciona.
- Ao enviar uma entrada de hora criada por outro usuário, o campo **Enviado por** é preenchido incorretamente com o usuário que criou a folha de ponto.
