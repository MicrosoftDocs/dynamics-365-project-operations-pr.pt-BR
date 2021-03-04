---
title: Novidades ou alterações na Versão de Atualização 28 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 28 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150609"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novidades ou alterações na Versão de Atualização 28 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e correções novos ou alterados para o Project Service Automation V3, versão de atualização 28 Esta versão tem um número de compilação de V 3.10.46.32 e está geralmente disponível por meio de uma atualização automática em janeiro de 2021.

## <a name="update-release-28"></a>Versão de Atualização 28

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

Os seguintes problemas foram corrigidos:

- Os usuários podem usar **Edição em massa** para atualizar as entradas de tempo que foram aprovadas e enviadas.

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- Nos casos em que o GUID da tarefa é interpretado como um número, as tarefas não podem ser abertas para edição usando **Editar Tarefa** na faixa de opções na página **Estrutura de detalhamento de trabalho**.

**Sales**

Os seguintes problemas foram corrigidos:

- Uma exceção de referência nula é gerada quando o plug-in **GetEstimatesForProject** é chamado.
- **Marcar como pronto para faturar** na grade de marcos atualiza apenas parcialmente os atributos, exceto para o atributo **InvoiceStatus**, que é atualizado.

