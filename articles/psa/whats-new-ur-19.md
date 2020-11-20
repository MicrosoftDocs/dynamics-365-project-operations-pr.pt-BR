---
title: Novidades ou alterações na Versão de Atualização 19 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 19 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071381"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="9fafd-103">Versão de Atualização 19, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="9fafd-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="9fafd-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9fafd-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9fafd-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="9fafd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9fafd-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9fafd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9fafd-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="9fafd-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9fafd-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9fafd-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9fafd-109">Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 19.</span><span class="sxs-lookup"><span data-stu-id="9fafd-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="9fafd-110">Esta versão apresenta o número de compilação V3.10.30.41 e está disponível para o público em geral por meio de uma atualização automática de maio de 2020.</span><span class="sxs-lookup"><span data-stu-id="9fafd-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="9fafd-111">Versão de Atualização 19</span><span class="sxs-lookup"><span data-stu-id="9fafd-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9fafd-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="9fafd-112">Bug fixes</span></span>

<span data-ttu-id="9fafd-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="9fafd-113">**Time and Expense**</span></span>

<span data-ttu-id="9fafd-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="9fafd-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="9fafd-115">Erros derivados de importações de entrada de horas não são apresentados corretamente.</span><span class="sxs-lookup"><span data-stu-id="9fafd-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="9fafd-116">A Grade de entrada de horas não oferece suporte ao comportamento de campo **Somente Data**.</span><span class="sxs-lookup"><span data-stu-id="9fafd-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="9fafd-117">Os Recursos do Projeto não conseguem criar uma despesa com um projeto.</span><span class="sxs-lookup"><span data-stu-id="9fafd-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="9fafd-118">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="9fafd-118">**Project Management**</span></span>

<span data-ttu-id="9fafd-119">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="9fafd-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="9fafd-120">A tarefa neto causa uma estimativa de esforço incorreta durante o cálculo de conclusão (EAT).</span><span class="sxs-lookup"><span data-stu-id="9fafd-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="9fafd-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9fafd-121">**Sales**</span></span>

<span data-ttu-id="9fafd-122">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="9fafd-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="9fafd-123">A ação **Recalcular** não funciona com os detalhes da linha do contrato de despesa ou com os detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="9fafd-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="9fafd-124">**Atualizar Preços** está ausente para estimativas de despesas.</span><span class="sxs-lookup"><span data-stu-id="9fafd-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="9fafd-125">Os clientes não podem selecionar razões do status do contrato personalizadas na página **Contrato do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="9fafd-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="9fafd-126">Os clientes sofrem uma degradação no desempenho ao criar uma lista de preços personalizada a partir de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="9fafd-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="9fafd-127">Os clientes sofrem inconsistências com **unidades** padrão nas páginas **Detalhes da linha de cotação** e **Detalhes da linha do contrato**.</span><span class="sxs-lookup"><span data-stu-id="9fafd-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="9fafd-128">Adicionar itens de categoria de transação não passível de cobrança a uma linha de contrato passível de cobrança não respeitará o tipo de cobrança **Não Passível de Cobrança** da categoria de transação.</span><span class="sxs-lookup"><span data-stu-id="9fafd-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="9fafd-129">Os clientes não podem usar as funções e a categoria recém-adicionadas em contratos criados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9fafd-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="9fafd-130">Os clientes sofrem uma degradação no desempenho Recuperação desnecessária em PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="9fafd-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="9fafd-131">Funções configuradas como não passíveis de cobrança na lista **Categorias de Recursos** devem ser adicionadas à guia **Funções Passíveis de Cobrança** como **Não Passível de Cobrança** na linha do contrato de um projeto.</span><span class="sxs-lookup"><span data-stu-id="9fafd-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="9fafd-132">Os clientes podem sofrer uma degradação no desempenho ao criar um projeto porque **GetBookableResourceIdFromUser** recupera todas as colunas de recursos reserváveis em vez de apenas o ID principal.</span><span class="sxs-lookup"><span data-stu-id="9fafd-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="9fafd-133">Entidade **TransactionType** ausente do plug-in de atualização de pré-validação para impedir que os usuários insiram **Unidades** e **UnitGroups** que não são válidos para os tipos de transação.</span><span class="sxs-lookup"><span data-stu-id="9fafd-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="9fafd-134">A etapa **Retirar** não funciona para a importação de entrada de horas.</span><span class="sxs-lookup"><span data-stu-id="9fafd-134">The **Remove** step does not work for time entry import.</span></span>