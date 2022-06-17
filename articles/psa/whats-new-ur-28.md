---
title: Novidades ou alterações na Versão de Atualização 28 do Project Service Automation V3
description: Este artigo lista os recursos e as correções disponíveis na atualização do Project Service Automation versão 28, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930580"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novidades ou alterações na Versão de Atualização 28 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista os recursos e as correções que são novos ou alterados para a atualização do Project Service Automation versão 28, V3. Esta versão tem um número de build V3.10.46.32 e foi disponibilizada para o público em geral por meio de uma autoatualização em janeiro de 2021.

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
