---
title: Novidades ou alterações na Versão de Atualização 29 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 29 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499657"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novidades ou alterações na Versão de Atualização 29 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 29. Esta versão tem um número de compilação de V3.10.45.98 e está geralmente disponível por meio de uma atualização automática em fevereiro de 2021.

## <a name="update-release-29"></a>Versão de Atualização 29

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

Os seguintes problemas foram corrigidos:

- Os usuários não podem ver as horas de trabalho registradas em dias não úteis na grade de entrada de hora.
- As entradas de despesas aprovadas podem ser editadas na grade.

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- Lógica de validação ausente para garantir que as horas de esforço de atribuição de recursos não possam ser negativas.
- A ação personalizada **AssignResourcesForTask** atualiza todos os campos em vez de somente os campos alterados.
- Ao copiar um projeto em um ambiente com plug-ins ou fluxos de trabalho que estão registrados no evento **CreateProject**, o atributo **msdyn_bulkgenerationstatus** não é atualizado se houver falha em **CopyWBSToProject**.
- Ao expandir o calendário do projeto, os dias úteis não são classificados em ordem ascendente, gerando falha em algumas atualizações de tarefa do projeto.
- Alterar o Gerente de Projeto em um projeto existente aciona a lógica de uso padrão da unidade organizacional.

**Vendas**

Os seguintes problemas foram corrigidos:

- A guia **Desempenho do Contrato** na página **Contrato** falha silenciosamente durante a inicialização quando não houver linhas de contrato presentes.
