---
title: Estimativa de receita de projeto de preço fixo
description: Este tópico fornece informações sobre receita de preço fixo em projetos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013787"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="1096a-103">Estimativa de receita de projeto de preço fixo</span><span class="sxs-lookup"><span data-stu-id="1096a-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="1096a-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="1096a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1096a-105">Quando você cria uma linha de contrato de projeto com os atributos a seguir no Dynamics 365 Project Operations no Microsoft Dataverse, o sistema cria automaticamente uma estimativa de projeto de receita de preço fixo.</span><span class="sxs-lookup"><span data-stu-id="1096a-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="1096a-106">As informações neste projeto são baseadas em:</span><span class="sxs-lookup"><span data-stu-id="1096a-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="1096a-107">Um método de cobrança de preço fixo.</span><span class="sxs-lookup"><span data-stu-id="1096a-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="1096a-108">Um projeto associado.</span><span class="sxs-lookup"><span data-stu-id="1096a-108">An associated project.</span></span>
  - <span data-ttu-id="1096a-109">Pelo menos um marco definido na guia **Agenda de faturas** na página **Linha de contrato do projeto**.</span><span class="sxs-lookup"><span data-stu-id="1096a-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="1096a-110">Revisar estimativas de projetos de receita de preço fixo</span><span class="sxs-lookup"><span data-stu-id="1096a-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="1096a-111">Para revisar estimativas de projetos de receita de preço fixo, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="1096a-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="1096a-112">No ambiente do Dynamics 365 Finance, acesse **Gerenciamento e contabilidade de projetos** > **Projetos** > **Estimativa de projetos de receita de preço fixo**.</span><span class="sxs-lookup"><span data-stu-id="1096a-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="1096a-113">Selecione o projeto que você deseja exibir e clique duas vezes em **Estimar ID do projeto** para abrir o registro e revisar os detalhes do projeto.</span><span class="sxs-lookup"><span data-stu-id="1096a-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="1096a-114">Expanda a guia **Projeto**. Você verá um projeto na grade **Projetos selecionados**.</span><span class="sxs-lookup"><span data-stu-id="1096a-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="1096a-115">O sistema usa este como o projeto padrão porque ele é o projeto associado à linha de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="1096a-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="1096a-116">Para alterar a associação, selecione projetos adicionais e adicione-os à grade **Projetos selecionados**.</span><span class="sxs-lookup"><span data-stu-id="1096a-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="1096a-117">Se vários projetos forem selecionados nesta grade, a porcentagem de conclusão do projeto e as estimativas de receita serão calculadas em conjunto para todos os projetos selecionados.</span><span class="sxs-lookup"><span data-stu-id="1096a-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="1096a-118">O custo do projeto, o perfil de receita, o modelo de custo e o código do período podem ser definidos manualmente.</span><span class="sxs-lookup"><span data-stu-id="1096a-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="1096a-119">Se eles não forem definidos manualmente, os valores serão padronizados durante o primeiro cálculo da estimativa para o projeto usando as regras configuradas para perfis de custo e receita do projeto.</span><span class="sxs-lookup"><span data-stu-id="1096a-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]