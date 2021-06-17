---
title: Novidades ou alterações na Versão de Atualização 12 do Project Service Automation V3
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado na Versão da Atualização 12 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f29eaf7c471104ad3e319d8f4e1cbc70e44fc1ca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000332"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="f52f5-103">Versão de Atualização 12, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="f52f5-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f52f5-104">Temos o orgulho de anunciar a versão mais recente do aplicativo Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="f52f5-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="f52f5-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="f52f5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f52f5-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f52f5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f52f5-107">Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e vá para a página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="f52f5-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="f52f5-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f52f5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f52f5-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 12.</span><span class="sxs-lookup"><span data-stu-id="f52f5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="f52f5-110">Esta versão tem um número de compilação da V3.10.2.34 e está geralmente disponível por meio de uma atualização automática em outubro de 2019.</span><span class="sxs-lookup"><span data-stu-id="f52f5-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="f52f5-111">Versão de Atualização 12</span><span class="sxs-lookup"><span data-stu-id="f52f5-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f52f5-112">Correções de bugs</span><span class="sxs-lookup"><span data-stu-id="f52f5-112">Bug fixes</span></span>

- <span data-ttu-id="f52f5-113">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="f52f5-113">Time and Expense</span></span>

    - <span data-ttu-id="f52f5-114">Corrigido: As mensagens de erro de entrada de hora foram atualizadas com um contexto mais relevante.</span><span class="sxs-lookup"><span data-stu-id="f52f5-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="f52f5-115">Corrigido: A grade de entrada de hora e a agenda exibem corretamente a barra de rolagem quando necessário.</span><span class="sxs-lookup"><span data-stu-id="f52f5-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="f52f5-116">Corrigido: As despesas e as entradas de tempo enviadas podem ser aprovadas.</span><span class="sxs-lookup"><span data-stu-id="f52f5-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="f52f5-117">Corrigido: A mensagem da caixa de diálogo de confirmação do cancelamento da aprovação foi corrigida para refletir o status da aprovação quando alterado de **Aprovada** para **Enviada**.</span><span class="sxs-lookup"><span data-stu-id="f52f5-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="f52f5-118">Corrigido: Os campos **Preço**, **Unidade** e **Quantidade** são bloqueados no registro de Despesas após a aprovação.</span><span class="sxs-lookup"><span data-stu-id="f52f5-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="f52f5-119">Gerenciamento de projetos</span><span class="sxs-lookup"><span data-stu-id="f52f5-119">Project Management</span></span>

    - <span data-ttu-id="f52f5-120">Corrigido: A ação **Novo** no formulário principal de **Membro da equipe** foi removida.</span><span class="sxs-lookup"><span data-stu-id="f52f5-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="f52f5-121">Corrigido: As atribuições de recursos foram atualizadas para considerar erros de arredondamento imprecisos, que resultam em uma alteração na data de término da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f52f5-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="f52f5-122">Corrigido: Na grade da tarefa, erros relevantes do lado do servidor serão exibidos para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f52f5-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="f52f5-123">Corrigido: O nome do membro da equipe agora é processado no seletor de pessoas da tarefa, e não no nome da posição.</span><span class="sxs-lookup"><span data-stu-id="f52f5-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="f52f5-124">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="f52f5-124">Resource Management</span></span>

    - <span data-ttu-id="f52f5-125">Corrigido: Os detalhes dos requisitos de recursos para projetos criados a partir de um modelo agora usam o calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="f52f5-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="f52f5-126">Corrigido: As habilidades e competências agora são padronizadas a partir dos dados mestre da função para o requisito do recurso criado para essa função.</span><span class="sxs-lookup"><span data-stu-id="f52f5-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="f52f5-127">Sales</span><span class="sxs-lookup"><span data-stu-id="f52f5-127">Sales</span></span>

    - <span data-ttu-id="f52f5-128">Corrigido: IDs de objeto duplicados encontrados no formulário do **Contrato principal**.</span><span class="sxs-lookup"><span data-stu-id="f52f5-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="f52f5-129">Corrigido: A lógica foi atualizada para tornar a guia **Análise de cotação** visível para exibir a configuração de metadados da guia.</span><span class="sxs-lookup"><span data-stu-id="f52f5-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="f52f5-130">Corrigido: Data contábil no registro real agora é gerada com base na data da entrada de hora/despesa e não da data da aprovação.</span><span class="sxs-lookup"><span data-stu-id="f52f5-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]