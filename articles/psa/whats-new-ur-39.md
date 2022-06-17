---
title: Novidades ou alterações na Versão de Atualização 39 do Project Service Automation V3
description: Este artigo lista os recursos e as correções disponíveis na atualização do Microsoft Dynamics 365 Project Service Automation versão 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922438"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Novidades ou alterações na Versão de Atualização 39 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista os recursos e as correções novos ou alterados na atualização do Project Service Automation versão 39, V3. Esta versão tem um número de compilação de V3.10.60.170 e está geralmente disponível por meio de uma atualização automática em janeiro de 2022.

## <a name="update-release-39"></a>Versão de Atualização 39

### <a name="bug-fixes"></a>Correções de bug

Os seguintes problemas foram corrigidos.

**Geral**

- Várias melhorias foram feitas no mapa do site para tradução em árabe.

**Gerenciamento de projetos**

- Ocorre um erro quando você altera o gerente de projeto para um usuário que já é membro da equipe do projeto.

**Vendas**

- O proprietário da **Lista de preços do contrato do projeto** fica incorreto quando a lista de preços é criada automaticamente. 
- A efetividade de data de uma lista de preços não é honrada quando a lista de preços é aplicada ao parâmetro do projeto.
- A unidade de contratação pode não ter o valor padrão correto ao editar duas cotações separadas.
