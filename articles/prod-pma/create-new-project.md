---
title: Criar um novo projeto
description: Este tópico fornece informações sobre como criar um novo projeto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006227"
---
# <a name="create-a-new-project"></a><span data-ttu-id="391a8-103">Criar um novo projeto</span><span class="sxs-lookup"><span data-stu-id="391a8-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="391a8-104">Conclua as etapas a seguir para criar um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="391a8-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="391a8-105">Na página **Gerenciamento de projetos**, selecione **Novo projeto** e insira estes valores:</span><span class="sxs-lookup"><span data-stu-id="391a8-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="391a8-106">**Tipo de projeto:** Tempo e material</span><span class="sxs-lookup"><span data-stu-id="391a8-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="391a8-107">**Nome do projeto:** Atualização do XYZ fase 2</span><span class="sxs-lookup"><span data-stu-id="391a8-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="391a8-108">**Grupo de projeto:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="391a8-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="391a8-109">**ID do contrato de projeto:** 00000002</span><span class="sxs-lookup"><span data-stu-id="391a8-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="391a8-110">Selecione **Criar projeto**.</span><span class="sxs-lookup"><span data-stu-id="391a8-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="391a8-111">Atribuir um recurso a um projeto</span><span class="sxs-lookup"><span data-stu-id="391a8-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="391a8-112">Na página **Funcionários**, na lista **Funcionários**, selecione o registro do funcionário para o qual você anteriormente configurou as competências e abra o registro dele.</span><span class="sxs-lookup"><span data-stu-id="391a8-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="391a8-113">No Painel de ações, na guia **Projeto**, no grupo **Configuração**, selecione **Atribuir projetos**.</span><span class="sxs-lookup"><span data-stu-id="391a8-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="391a8-114">Na página **Atribuições de projetos de validação de recursos**, na guia **Projetos**, no campo **Adicionar o projeto aos projetos selecionados**, filtre pelo projeto **Atualização do XYZ fase 2**.</span><span class="sxs-lookup"><span data-stu-id="391a8-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="391a8-115">No painel **Projetos pendentes**, selecione um projeto e, em seguida, selecione o botão de seta para adicioná-lo ao painel **Projetos selecionados**.</span><span class="sxs-lookup"><span data-stu-id="391a8-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="391a8-116">Você também pode atribuir categorias a um recurso conforme sua necessidade.</span><span class="sxs-lookup"><span data-stu-id="391a8-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="391a8-117">O tipo de categoria é **Custo** ou **Receita**.</span><span class="sxs-lookup"><span data-stu-id="391a8-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="391a8-118">O tipo de categoria é determinado por sua organização.</span><span class="sxs-lookup"><span data-stu-id="391a8-118">The category type is determined by your organization.</span></span> <span data-ttu-id="391a8-119">Se nenhuma categoria for atribuída a um recurso, o Finance procurará a categoria padrão nos preços por hora para custo e receita.</span><span class="sxs-lookup"><span data-stu-id="391a8-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="391a8-120">Configurar as características da função e recurso do projeto</span><span class="sxs-lookup"><span data-stu-id="391a8-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="391a8-121">Um gerente de projeto pode usar a funcionalidade de alocação de recursos do projeto para criar as funções necessárias para o projeto.</span><span class="sxs-lookup"><span data-stu-id="391a8-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="391a8-122">As funções podem ser usadas se os recursos confirmados ainda forem desconhecidos quando os estiverem sendo reservados.</span><span class="sxs-lookup"><span data-stu-id="391a8-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="391a8-123">As funções podem ser reservadas temporariamente como recursos planejados, para que você possa continuar as etapas de planejamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="391a8-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="391a8-124">[![Exemplo de uma função](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="391a8-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="391a8-125">**Cenário:** A Contoso foi contratada para concluir um projeto de tempo e material que tem um estatuto do projeto aprovado.</span><span class="sxs-lookup"><span data-stu-id="391a8-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="391a8-126">O gerente de projeto júnior ainda está preenchendo o escopo do projeto.</span><span class="sxs-lookup"><span data-stu-id="391a8-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="391a8-127">O gerente de recursos está no momento identificando recursos específicos que serão reservados para trabalhar no novo projeto.</span><span class="sxs-lookup"><span data-stu-id="391a8-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="391a8-128">Devido à natureza crítica do projeto, o patrocinador dele solicitou um gerente de projeto sênior como uma das funções.</span><span class="sxs-lookup"><span data-stu-id="391a8-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="391a8-129">O gerente de recursos deve encontrar o novo recurso e definir a função no sistema, caso o gerente de projeto júnior precise das informações do recurso durante o planejamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="391a8-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="391a8-130">As etapas a seguir mostram como o gerente de recursos pode configurar a função de gerente de projeto sênior e associar características de recursos a ela.</span><span class="sxs-lookup"><span data-stu-id="391a8-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="391a8-131">Posteriormente, a função poderá ser usada para pesquisar recursos disponíveis que correspondam às competências de recursos necessárias.</span><span class="sxs-lookup"><span data-stu-id="391a8-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="391a8-132">Na página **Configurar funções**, selecione **Novo** e insira estes valores:</span><span class="sxs-lookup"><span data-stu-id="391a8-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="391a8-133">**ID da função:** Gerente de projeto sênior</span><span class="sxs-lookup"><span data-stu-id="391a8-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="391a8-134">**Descrição:** Gerente de projeto sênior</span><span class="sxs-lookup"><span data-stu-id="391a8-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="391a8-135">Selecione **Criar**.</span><span class="sxs-lookup"><span data-stu-id="391a8-135">Select **Create**.</span></span>
3. <span data-ttu-id="391a8-136">Selecione a função **Gerente de projeto sênior** e, em seguida, **Configurar características**.</span><span class="sxs-lookup"><span data-stu-id="391a8-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="391a8-137">No campo **Tipo de característica**, selecione **Habilidade**.</span><span class="sxs-lookup"><span data-stu-id="391a8-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="391a8-138">No campo **Características disponíveis**, insira a habilidade para pesquisar.</span><span class="sxs-lookup"><span data-stu-id="391a8-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="391a8-139">No campo **Tipo de característica**, selecione **Certificado**.</span><span class="sxs-lookup"><span data-stu-id="391a8-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="391a8-140">No campo **Características disponíveis**, insira o tipo de certificado para pesquisar.</span><span class="sxs-lookup"><span data-stu-id="391a8-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="391a8-141">Atribuir um recurso a um projeto</span><span class="sxs-lookup"><span data-stu-id="391a8-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="391a8-142">Na página **Todos os projetos**, selecione o projeto **Atualização do XYZ fase 2**.</span><span class="sxs-lookup"><span data-stu-id="391a8-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="391a8-143">Na guia **Equipe do projeto e agendamento**, selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="391a8-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="391a8-144">No campo **Função**, selecione **Membro da equipe**.</span><span class="sxs-lookup"><span data-stu-id="391a8-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="391a8-145">Selecione **Reservar do calendário**.</span><span class="sxs-lookup"><span data-stu-id="391a8-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="391a8-146">Na página **Disponibilidade do recurso**, selecione **Configurações de exibição**.</span><span class="sxs-lookup"><span data-stu-id="391a8-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="391a8-147">Na página **Ajustar configurações de exibição**, insira os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="391a8-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="391a8-148">**Formato da exibição do intervalo de datas:** Dia</span><span class="sxs-lookup"><span data-stu-id="391a8-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="391a8-149">**Exibir descrições de disponibilidade:** Sim</span><span class="sxs-lookup"><span data-stu-id="391a8-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="391a8-150">**Exibir capacidade restante:** Sim</span><span class="sxs-lookup"><span data-stu-id="391a8-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="391a8-151">Na lista de recursos, selecione um recurso.</span><span class="sxs-lookup"><span data-stu-id="391a8-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="391a8-152">Selecione **Reserva fixa** e **Capacidade total**.</span><span class="sxs-lookup"><span data-stu-id="391a8-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="391a8-153">Atribuir um recurso a uma função padrão</span><span class="sxs-lookup"><span data-stu-id="391a8-153">Assign a resource to a default role</span></span>

<span data-ttu-id="391a8-154">Para ajudar os gerentes de projeto ou de recursos, é possível se aprofundar mais nos recursos que podem ser reservados para um projeto.</span><span class="sxs-lookup"><span data-stu-id="391a8-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="391a8-155">Você pode associar uma função padrão a um recurso existente ou a um recurso recém-adquirido.</span><span class="sxs-lookup"><span data-stu-id="391a8-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="391a8-156">Por exemplo, quando Daniel foi contratado, ele tinha a experiência e as habilidades para preencher a função de analista de negócios.</span><span class="sxs-lookup"><span data-stu-id="391a8-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="391a8-157">O gerente de recursos atribuiu essa função como a função padrão de Daniel.</span><span class="sxs-lookup"><span data-stu-id="391a8-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="391a8-158">Portanto, o gerente de recursos adicionou Daniel a um grupo de analistas de negócios que estão disponíveis para trabalhar em projetos.</span><span class="sxs-lookup"><span data-stu-id="391a8-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="391a8-159">Durante a reserva de recursos, os gerentes de projeto podem filtrar os recursos de função que estão disponíveis para trabalhar em projetos.</span><span class="sxs-lookup"><span data-stu-id="391a8-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="391a8-160">Eles podem usar essas informações como um critério ao realizar análises de decisão de vários critérios durante o preenchimento de recursos.</span><span class="sxs-lookup"><span data-stu-id="391a8-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="391a8-161">Eles também podem adicionar outras características de recurso ao filtro para pesquisar recursos que tenham habilidades, formação e experiência específicas para um determinado projeto.</span><span class="sxs-lookup"><span data-stu-id="391a8-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="391a8-162">**Cenário:** um projeto aprovado foi iniciado e a função de gerente de projeto sênior foi reservada como um recurso planejado durante o estágio de planejamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="391a8-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="391a8-163">O gerente de recursos agora encontrou um recurso para ocupar a função de gerente de projeto sênior.</span><span class="sxs-lookup"><span data-stu-id="391a8-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="391a8-164">Na página **Lista de recursos**, selecione **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="391a8-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="391a8-165">Na página **Função do recurso**, selecione **Novo** e insira estes valores:</span><span class="sxs-lookup"><span data-stu-id="391a8-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="391a8-166">**Efetivo:** insira a data atual.</span><span class="sxs-lookup"><span data-stu-id="391a8-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="391a8-167">**Expiração:** insira **Nunca**.</span><span class="sxs-lookup"><span data-stu-id="391a8-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="391a8-168">**Função:** insira **Gerente de projeto sênior**.</span><span class="sxs-lookup"><span data-stu-id="391a8-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="391a8-169">Selecione **Salvar** e feche a página.</span><span class="sxs-lookup"><span data-stu-id="391a8-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="391a8-170">Na guia **Competências**, adicione a habilidade **ProjectMgmt** e o certificado **PMP**.</span><span class="sxs-lookup"><span data-stu-id="391a8-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]