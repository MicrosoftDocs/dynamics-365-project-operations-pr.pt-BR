---
title: Novidades ou alterações na Versão de Atualização 32 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 32 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 3ad87eceb90a48997aadf00803b8d14c5108eb83
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580074"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Novidades ou alterações na Versão de Atualização 32 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 32. Esta versão tem um número de compilação de V3.10.53.108 e está geralmente disponível por meio de uma atualização automática em junho de 2021.

## <a name="update-release-32"></a>Versão de Atualização 32

### <a name="bug-fixes"></a>Correções de bug

#### <a name="general"></a>Geral

- Quando uma grande atualização falha, apenas os principais pontos de entrada do aplicativo devem ser bloqueados, para garantir que as entidades compartilhadas ainda estejam acessíveis.

#### <a name="time-and-expense"></a>Tempo e Despesa

Os seguintes problemas foram corrigidos:

- **TimeEntriesImportFromResourceAssignment** não mantém os horários de início e término da fatia de contorno de atribuição de recursos.
- Quando você seleciona a grade **Abrir Entrada** na grade **Entrada de Tempo**, você pode ser impedido de selecionar outros formulários.
- Enquanto você importa atribuições para entradas de tempo, a consulta do código do cliente pode gerar um URL longo que falha na consulta.
- Na grade **Entrada de Tempo**, depois que um valor é excluído de uma célula, o foco não permanece na grade.
- O botão **Rejeitar** foi removido da exibição **Processando aprovações** para aprovações modernas.
- A estabilidade e o desempenho da aprovação em massa de entrada de tempo são afetados por impasses e uma falha em lidar de forma adequada com personalizações relacionadas à entidade **Entrada de Tempo**.

#### <a name="project-planning"></a>Planejamento do Projeto

- Uma exceção de referência nula é gerada quando você atualiza um projeto que tem um valor nulo no campo **Unidade de Contratação**.
- **Atualizar Totais do Projeto** calcula incorretamente o custo restante e as vendas restantes em um projeto.
- Cálculos de preços redundantes afetam o desempenho relacionado a atualizações nos contornos de atribuição de recursos.

#### <a name="resource-management"></a>Gerenciamento de Recursos

O seguinte problema foi corrigido:

- Quando a capacidade do calendário de um recurso reservável for maior que 1, o Project Service Automation reconhece incorretamente a capacidade como 0 (zero). Portanto, um loop infinito ocorre na exibição da agenda.

#### <a name="sales"></a>Vendas

Os seguintes problemas foram corrigidos:

- Quando uma linha de diário é criada com um tipo de transação personalizado, ocorre a seguinte exceção de referência nula: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- As funções e categorias que são desativadas antes de uma cotação ser copiada não devem ser adicionadas às funções e categorias cobráveis da cotação recém-copiada.
- A data do documento e a data contábil não estão alinhadas com a data de início fornecida em um detalhe de linha de fatura criado diretamente em um rascunho de fatura.
- Exceções de referência nula são geradas em cenários relacionados à desativação de funções e categorias antes que uma cotação seja copiada.
- A ação **Atualizar Preços** na página **Projetos** não atualiza estimativas de despesas e estimativas de material.
