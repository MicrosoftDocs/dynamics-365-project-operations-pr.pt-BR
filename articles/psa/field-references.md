---
title: Adicionar campos personalizados a entidades transacionais e de configuração de preço
description: Este tópico fornece informações sobre como adicionar campos personalizados às entidades transacionais e de configuração de preço.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 32d0dbc3a69d713dcae8d27e52f2a0c6fc296127
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071534"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a><span data-ttu-id="6f6e4-103">Adicionar campos personalizados a entidades transacionais e de configuração de preço</span><span class="sxs-lookup"><span data-stu-id="6f6e4-103">Add custom fields to price setup and transactional entities</span></span> 
<span data-ttu-id="6f6e4-104">Este tópico pressupõe que você concluiu os procedimentos do tópico [Criar campos e entidades personalizados](create-custom-fields-entities.md).</span><span class="sxs-lookup"><span data-stu-id="6f6e4-104">This topic assumes that you have completed the procedures in the topic, [Create custom fields and entities](create-custom-fields-entities.md).</span></span> <span data-ttu-id="6f6e4-105">Se você não concluiu esses procedimentos, volte e conclua-os e retorne a este tópico.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="6f6e4-106">Neste tópico, os procedimentos mostrarão como adicionar as referências de campo personalizadas necessárias às entidades e aos elementos da interface do usuário, como formulários e exibições.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-106">In this topic, the procedures will show you how to add the required custom field references to entities and to the user interface (UI) elements such as forms and views.</span></span>

## <a name="add-custom-pricing-dimension-fields"></a><span data-ttu-id="6f6e4-107">Adicionar campos personalizados de dimensão de preço</span><span class="sxs-lookup"><span data-stu-id="6f6e4-107">Add custom pricing dimension fields</span></span> 
<span data-ttu-id="6f6e4-108">Depois que campos e entidades personalizados tiverem sido criados, a próxima etapa será conscientizar entidades transacionais e de configuração de preço sobre todos os conjuntos de opções e entidades personalizadas criando campos de referência.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-108">After custom fields and entities have been created, the next step is to make price setup and transactional entities aware of any custom entities or option sets by creating reference fields.</span></span> <span data-ttu-id="6f6e4-109">De acordo com o que a lista de dimensões de preço incluir, dimensões de conjunto de opções ou dimensões de entidade, ou ambas, siga somente as etapas em **Dimensões de preço personalizadas baseadas em conjunto de opções** ou **Dimensões de preço personalizadas baseadas em entidade** , ou em ambas, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-109">Depending on whether your pricing dimensions list includes option set dimensions or entity dimensions or both, follow only the steps in **Option set-based custom pricing dimensions** or **Entity-based custom pricing dimensions** , or both, respectively.</span></span>

### <a name="option-set-based-custom-pricing-dimensions"></a><span data-ttu-id="6f6e4-110">Dimensões de preço personalizadas baseadas em conjunto de opções</span><span class="sxs-lookup"><span data-stu-id="6f6e4-110">Option set-based custom pricing dimensions</span></span>
<span data-ttu-id="6f6e4-111">Quando uma dimensão personalizada de preço for baseada no conjunto de opções, adicione-a como um campo às principais entidades do Project Service.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-111">When a custom pricing dimension is option set-based, add it as a field to key Project Service entities.</span></span> <span data-ttu-id="6f6e4-112">No procedimento a seguir, **Local de Trabalho do Recurso** e **Horas de Trabalho do Recurso** são usadas como as dimensões de preço baseadas em conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-112">In the following procedure, **Resource Work Location** and **Resource Work Hours** are used as the option set-based pricing dimensions.</span></span> <span data-ttu-id="6f6e4-113">Primeiro elas devem ser adicionadas como campos às entidade de preço, **Preço da Função** e **Markup de Preço da Função**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-113">These must first be added as fields to the pricing entities, **Role Price** and **Role Price Markup**.</span></span>

1. <span data-ttu-id="6f6e4-114">No PSA (Project Service Automation), clique em **Configurações** > **Soluções** e clique duas vezes em **Dimensões de preço do(a) \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-114">In Project Service Automation (PSA), click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="6f6e4-115">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Preço da Função**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-115">In Solution Explorer, on the left navigation pane, select **Entities > Role Price**.</span></span>
3. <span data-ttu-id="6f6e4-116">Expanda a entidade **Preço da Função** e selecione **Campos**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-116">Expand the entity **Role Price** and select **Fields**.</span></span>
4. <span data-ttu-id="6f6e4-117">Clique em **Novo** para criar um novo campo chamado **Local de Trabalho do Recurso** e selecione **Conjunto de opções** como o tipo de campo.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-117">Click **New** to create a new field called **Resource Work Location** and select **Option set** as the field type.</span></span> 
5. <span data-ttu-id="6f6e4-118">Selecione **Usar um Conjunto de opções existente** , escolha o conjunto de opções **Local de Trabalho do Recurso** e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-118">Select **Use an existing Option set** , select the **Resource Work Location** option set, and then click **Save**.</span></span>
6. <span data-ttu-id="6f6e4-119">Repita as etapas de 1 a 5 para adicionar esse campo à entidade **Markup de Preço da Função**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-119">Repeat steps 1 - 5 to add this field to the **Role Price Markup** entity.</span></span> 
7. <span data-ttu-id="6f6e4-120">Repita as etapas de 1 a 5 para o conjunto de opções **Horas de Trabalho do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-120">Repeat steps 1 - 5 for the **Resource Work Hours** option set.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f6e4-121">Quando você adiciona um campo a mais de uma entidade, use o mesmo nome de campo em todas as entidades.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-121">When you add a field to more than one entity, use the same field name across all of the entities.</span></span> 

> ![Adicionando Local de Trabalho do Recurso ao Preço da Função](media/RWL-Field.png)

<span data-ttu-id="6f6e4-123">Nas fases de vendas e estimativa de um projeto, as estimativas do esforço de trabalho que é exigido para concluir o trabalho **Local** e **No local** , em **Horas regulares** e **Horas extras** são usadas para estimar o valor da Cotação/do Projeto.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-123">In the sales and estimation phases for a project, estimates of the work effort that is required to complete **Local** and **Onsite** work, in **Regular hours** and **Overtime hours**  are used to estimate the value of the Quote/Project.</span></span> <span data-ttu-id="6f6e4-124">Os campos **Local de Trabalho do Recurso** e **Horas de Trabalho do Recurso** serão adicionados às entidades de estimativa **Detalhe da Linha de Cotação** , **Detalhe da Linha de Contrato** , **Tarefa de Projeto** , **Membro da Equipe de Projeto** e **Linha de Estimativa**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-124">The fields **Resource Work Location** and **Resource Work Hours** will be added to the estimation entities, **Quote Line Detail** , **Contract Line detail** , **Project Task** , **Project Team Member** , and **Estimate Line**.</span></span>

1. <span data-ttu-id="6f6e4-125">No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **Dimensões de preços do(a) \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-125">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="6f6e4-126">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Detalhes da Linha de Cotação**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-126">In Solution Explorer, on the left navigation pane, select **Entities > Quote Line Detail**.</span></span>
3. <span data-ttu-id="6f6e4-127">Expanda a entidade **Detalhes da Linha de Cotação** e selecione **Campos**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-127">Expand the **Quote Line Detail** entity, and select **Fields**.</span></span>
4. <span data-ttu-id="6f6e4-128">Clique em **Novo** para criar um novo campo chamado **Local de Trabalho do Recurso** e selecione o tipo de campo **Conjunto de opções**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-128">Click **New** to create a new field called **Resource Work Location** and select the field type, **Option set**.</span></span> 
5. <span data-ttu-id="6f6e4-129">Selecione **Usar um Conjunto de opções existente** e **Local de Trabalho do Recurso** e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-129">Select **Use an existing Option set** and **Resource Work Location** , and then click **Save**.</span></span>
6. <span data-ttu-id="6f6e4-130">Repita as etapas de 1 a 5 para adicionar esse campo às entidades **Detalhe da Linha de Contrato de Projeto** , **Tarefa de Projeto** , **Membro da Equipe de Projeto** e **Linha de Estimativa**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-130">Repeat steps 1 - 5 to add this field to the **Project Contract line detail** , **Project Task** , **Project Team Member** , and **Estimate Line** entities.</span></span>
7. <span data-ttu-id="6f6e4-131">Repita as etapas de 1 a 6 para o conjunto de opções **Horas de Trabalho do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-131">Repeat steps 1 - 6 for the **Resource Work Hours** option set.</span></span> 

> ![Adicionando Local de Trabalho do Recurso à Linha de Estimativa](media/RWL-Default-Value.png)


<span data-ttu-id="6f6e4-133">Para entrega e faturamento, o trabalho concluído precisa ser precificado precisamente para seleção de **Local** ou **No Local** e se foi concluído durante **Horas regulares** ou **Horas extras** nos Dados Reais do Projeto.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-133">For delivery and invoicing, completed work needs to be accurately priced to select whether it was performed **Local** or **Onsite** , and whether it was completed during **Regular hours** or **Overtime** on the Project Actuals.</span></span> <span data-ttu-id="6f6e4-134">Os campos **Local de Trabalho do Recurso** e **Horas de Trabalho do Recurso** devem ser adicionados às entidades **Entrada de Tempo** , **Dados Reais** , **Detalhes da Linha de Fatura** e **Linha do Diário**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-134">The **Resource Work Location** and **Resource Work hours** fields should be added to the **Time Entry** , **Actual** , **Invoice Line Detail** , and **Journal Line** entities.</span></span>

1. <span data-ttu-id="6f6e4-135">No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **Dimensões de preços do(a) \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-135">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="6f6e4-136">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Entrada de Temo**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-136">In Solution Explorer, on the left navigation pane, select  **Entities > Time Entry**.</span></span>
3. <span data-ttu-id="6f6e4-137">Expanda a entidade **Detalhes da Linha de Cotação** e selecione **Campos**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-137">Expand the **Quote Line Detail** entity, and then select **Fields**.</span></span>
4. <span data-ttu-id="6f6e4-138">Clique em **Novo** para criar um novo campo chamado **Local de Trabalho do Recurso** e selecione **Conjunto de opções** como o tipo de campo.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-138">Click **New** to create a new field called **Resource Work Location** and select **Option set** as the field type.</span></span> 
5. <span data-ttu-id="6f6e4-139">Selecione **Usar um Conjunto de opções existente** , escolha o conjunto de opções **Local de Trabalho do Recurso** e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-139">Select **Use an existing Option set** , select the **Resource Work Location** option set, and then click **Save**.</span></span>
6. <span data-ttu-id="6f6e4-140">Repita as etapas de 1 a 5 para adicionar esse campo às entidades **Dados Reais** , **Detalhes da Linha de Fatura** e **Linha do Diário**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-140">Repeat steps 1 - 5 to add this field to the **Actual** , **Invoice Line Detail** , and **Journal Line** entities.</span></span>
7. <span data-ttu-id="6f6e4-141">Repita as etapas de 1 a 6 para o conjunto de opções **Horas de Trabalho do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-141">Repeat steps 1 - 6 for the **Resource Work Hours** option set.</span></span> 

> ![Adicionando Local de Trabalho do Recurso à Entrada de Tempo](media/RWL-time-entry.png)

<span data-ttu-id="6f6e4-143">Isso conclui as alterações no esquema exigidas para dimensões personalizadas baseadas em conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-143">This completes the schema changes required for option set-based custom dimensions.</span></span>

## <a name="entity-based-custom-pricing-dimensions"></a><span data-ttu-id="6f6e4-144">Dimensões de preço personalizadas baseadas em entidade</span><span class="sxs-lookup"><span data-stu-id="6f6e4-144">Entity-based custom pricing dimensions</span></span>

<span data-ttu-id="6f6e4-145">Quando a dimensão de preço personalizada for uma entidade, você adicionará relacionamentos 1:N entre a entidade da dimensão e as principais entidades do Project Service.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-145">When the custom pricing dimension is an entity, you will add 1:N relationships between the dimension entity and key Project Service entities.</span></span> <span data-ttu-id="6f6e4-146">Usando o exemplo do Cargo Padrão acima, é razoável esperar que cada funcionário receba um cargo padrão.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-146">Using the Standard Title example from above, it is reasonable to expect that each employee is assigned a standard title.</span></span> <span data-ttu-id="6f6e4-147">Consequentemente, você precisará de um relacionamento 1:N do Cargo Padrão para Recurso Reservável, ou do relacionamento N:1 se tiver sido criado do Recurso Reservável para o Cargo Padrão.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-147">SAs a result, you will need a 1:N relationship from Standard Title to Bookable Resource, or a N:1 relationship if it were created from Bookable Resource to Standard Title.</span></span>

1. <span data-ttu-id="6f6e4-148">No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **Dimensões de preços do(a) \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-148">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="6f6e4-149">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-149">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
3. <span data-ttu-id="6f6e4-150">Expanda a entidade **Cargo Padrão** e selecione **Relacionamentos 1: N**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-150">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
4. <span data-ttu-id="6f6e4-151">Clique em **Novo** para criar um novo relacionamento 1:N chamado **Cargo Padrão para Recurso Reservável**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-151">Click **New** to create a new 1:N relationship called **Standard Title to Bookable Resource**.</span></span> <span data-ttu-id="6f6e4-152">Insira as informações necessárias e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-152">Enter the required information, and then click **Save**.</span></span>

> ![Adicionando Cargo Padrão como um campo de referência para Recurso Reservável](media/ST-BR.png)

<span data-ttu-id="6f6e4-154">O Cargo Padrão também precisará ser adicionado às entidades Preço do Project Service, **Preço da Função** e **Markup de Preço da Função**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-154">The Standard Title will also need to be added to Project Service Pricing entities, **Role Price** and **Role Price Markup**.</span></span> <span data-ttu-id="6f6e4-155">Isso também pode ser feito usando relacionamentos 1:N entre as entidades **Cargo Padrão** e **Preço da Função** e as entidades **Cargo Padrão** e **Markup de Preço da Função**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-155">This is also completed using 1:N relationships between the **Standard Title** and **Role Price** entities and **Standard Title** and **Role Price Markup** entities.</span></span>

1. <span data-ttu-id="6f6e4-156">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-156">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
2. <span data-ttu-id="6f6e4-157">Expanda a entidade **Cargo Padrão** e selecione **Relacionamentos 1: N**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-157">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
3. <span data-ttu-id="6f6e4-158">Clique em **Novo** para criar um novo relacionamento 1:N chamado **Cargo Padrão para Preço da Função**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-158">Click **New** to create a new 1:N relationship called **Standard Title to Role Price**.</span></span> <span data-ttu-id="6f6e4-159">Insira as informações necessárias e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-159">Enter the required information, and then click **Save**.</span></span>
4. <span data-ttu-id="6f6e4-160">Repita as etapas de 1 a 4 para criar relacionamentos 1:N entre as entidades **Cargo Padrão** e **Markup de Preço da Função**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-160">Repeat steps 1 - 4 to create 1:N relationships between the **Standard Title** and **Role Price Markup** entities,</span></span>

<span data-ttu-id="6f6e4-161">Nas fases de vendas e estimativa do projeto, para chegar ao preço da Cotação/do Projeto, as estimativas do esforço de trabalho são necessárias para cada cargo padrão.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-161">In the sales and estimation phases for the project, to price the Quote/Project, estimates of the work effort are required for each standard title.</span></span> <span data-ttu-id="6f6e4-162">Isso significa que são necessários relacionamentos 1:N do Cargo Padrão para cada uma dessas entidades de estimativa no Project Service:</span><span class="sxs-lookup"><span data-stu-id="6f6e4-162">This means that 1:N relationships from Standard Title to each of these estimation entities in Project Service are needed:</span></span> 

- <span data-ttu-id="6f6e4-163">**Detalhe da Linha de Cotação**</span><span class="sxs-lookup"><span data-stu-id="6f6e4-163">**Quote line Detail**</span></span>
- <span data-ttu-id="6f6e4-164">**Detalhe da Linha de Contrato do Projeto**</span><span class="sxs-lookup"><span data-stu-id="6f6e4-164">**Project Contract Line Detail**</span></span>
- <span data-ttu-id="6f6e4-165">**Tarefa do Projeto**</span><span class="sxs-lookup"><span data-stu-id="6f6e4-165">**Project Task**</span></span>
- <span data-ttu-id="6f6e4-166">**Membro da Equipe do Projeto**</span><span class="sxs-lookup"><span data-stu-id="6f6e4-166">**Project Team Member**</span></span>
- <span data-ttu-id="6f6e4-167">**Linha de Estimativa**</span><span class="sxs-lookup"><span data-stu-id="6f6e4-167">**Estimate Line**</span></span>

5. <span data-ttu-id="6f6e4-168">Repita as etapas de 1 a 5 para criar relacionamentos 1:N de **Cargo Padrão** para **Detalhe da Linha de Cotação** , **Detalhe da Linha de Contrato de Projeto** , **Tarefa de Projeto** , **Membro da Equipe de Projeto** e **Linha de Estimativa**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-168">Repeat steps 1 - 5 to create 1:N relationships from **Standard Title** to **Quote line Detail** , **Project Contract Line Detail** , **Project Task** , **Project Team Member** , and **Estimate Line**.</span></span>

> ![Adicionando Cargo Padrão como um campo de referência para Linha de Estimativa](media/ST-Estimate-Line.png)

<span data-ttu-id="6f6e4-170">Nas fases Entrega e Faturamento, o trabalho concluído por cada cargo padrão deve ser precisamente precificado nos Dados Reais do Projeto.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-170">In the Delivery and Invoicing phases, the work completed by each standard title must be accurately priced on the Project Actuals.</span></span> <span data-ttu-id="6f6e4-171">Isso significa que há necessidades de relacionamentos 1:N de **Cargo Padrão** para as entidades **Entrada de Tempo** , **Dados Reais** , **Detalhes da Linha de Fatura** e **Linha do Diário**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-171">This means that there needs to be 1:N relationships from **Standard Title** to **Time Entry** , **Actual** , **Invoice Line Detail** , and **Journal Line entities**.</span></span>

6. <span data-ttu-id="6f6e4-172">Repita as etapas de 1 a 6 para criar relacionamentos 1:N de **Cargo Padrão** para as entidades **Entrada de Tempo** , **Dados Reais** , **Detalhes da Linha de Fatura** e **Linha do Diário**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-172">Repeat steps 1 - 6 to create 1:N relationships from **Standard Title** to **Time Entry** , **Actual** , **Invoice Line Detail** , and **Journal Line entities**.</span></span>

> ![Adicionando Cargo Padrão como um campo de referência para Entrada de Tempo](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a><span data-ttu-id="6f6e4-174">Configurar padronização do valor de Dimensão usando os recursos de mapeamento da plataforma</span><span class="sxs-lookup"><span data-stu-id="6f6e4-174">Set up Dimension value defaulting using the mappings features of the platform</span></span>
<span data-ttu-id="6f6e4-175">Para Entrada de Tempo, seria útil que o sistema padronizasse o cargo padrão na Entrada de Tempo do Recurso Reservável que está registrando a entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-175">For Time Entry, it would be helpful to have the system default the standard title on the Time Entry from the Bookable Resource that is recording the time entry.</span></span> <span data-ttu-id="6f6e4-176">Use as etapas a seguir para adicionar mapeamentos de campo no relacionamento 1:N de **Recurso Reservável** para **Entrada de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-176">Use the following steps to add field mappings on the 1:N relationship from **Bookable Resource** to **Time Entry**.</span></span>

1. <span data-ttu-id="6f6e4-177">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-177">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
2. <span data-ttu-id="6f6e4-178">Expanda a entidade **Cargo Padrão** e selecione **Relacionamentos 1: N**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-178">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
3. <span data-ttu-id="6f6e4-179">Clique duas vezes em **Recurso Reservável para Entrada de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-179">Double-click **Bookable Resource to Time Entry**.</span></span> <span data-ttu-id="6f6e4-180">Na página **Relacionamento** , clique em **Usar Mapeamentos de Campo**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-180">On the **Relationship** page, click **Use Field mappings**.</span></span> 
4. <span data-ttu-id="6f6e4-181">Clique em **Novo** de modo a criar um novo mapeamento de campo entre o campo **Cargo Padrão** na entidade **Recurso Reservável** para o campo de referência **Cargo Padrão** na entidade **Entrada de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-181">Click **New** to create a new field mapping between the **Standard Title** field on the **Bookable Resource** entity to the **Standard Title** reference field on **Time Entry** entity.</span></span> 

> ![Configurar mapeamentos de campo para permitir a padronização de Cargo Padrão, de Recurso Reservável para Entrada de Tempo](media/ST-Mapping2.png)


<span data-ttu-id="6f6e4-183">Isso conclui as alterações no esquema exigidas para dimensões personalizadas baseadas em entidade.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-183">This completes the schema changes required for entity-based custom dimensions.</span></span>

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a><span data-ttu-id="6f6e4-184">Adicionar campos personalizados a formulários, exibições e regras de negócios</span><span class="sxs-lookup"><span data-stu-id="6f6e4-184">Add custom fields to forms, views, and business rules</span></span>

<span data-ttu-id="6f6e4-185">Depois de ter feito todas as alterações de esquema necessárias, a próxima etapa é tornar os campos visíveis na interface do usuário adicionando os campos aos formulários e exibições.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-185">After you have made all of the required schema changes, the next step is to make the fields visible in the UI by adding the fields to the forms and views.</span></span>

1. <span data-ttu-id="6f6e4-186">Abra o formulário ou a exibição.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-186">Open the form or the view.</span></span> <span data-ttu-id="6f6e4-187">No painel de navegação à direita, selecione o campo e arraste-o para a tela de formulário.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-187">On the right navigation pane, select the field and drag it on to the form canvas.</span></span> 
2. <span data-ttu-id="6f6e4-188">Se estiver editando uma exibição, use o painel de navegação à direita, clique em **Adicionar campos** e, na caixa de diálogo **Listagem de campo** , selecione os campos necessários e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-188">If you are editing a view, use the right navigation pane, click **Add fields** , and in the **Field listing** dialog box, select the fields that you need and click **Ok**.</span></span>

<span data-ttu-id="6f6e4-189">A tabela a seguir fornece uma lista abrangente de formulários e exibições prontos para uso, por entidade, que precisarão ser atualizados com os novos campos.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-189">The following table provides a comprehensive list of out-of-the-box forms and views, by entity, that will need to be updated with the new fields.</span></span> <span data-ttu-id="6f6e4-190">Se você tiver exibições ou formulários adicionais em suas personalizações nessas entidades, adicione os novos campos a eles também.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-190">If you have any additional views or forms in your customizations on these entities, add the new fields to those as well.</span></span>

| <span data-ttu-id="6f6e4-191">Entidade do Project Service</span><span class="sxs-lookup"><span data-stu-id="6f6e4-191">Project Service Entity</span></span>        | <span data-ttu-id="6f6e4-192">Formulários que precisam do novo campo</span><span class="sxs-lookup"><span data-stu-id="6f6e4-192">Forms that need the new field</span></span>   |<span data-ttu-id="6f6e4-193">Exibições que precisam do novo campo</span><span class="sxs-lookup"><span data-stu-id="6f6e4-193">Views that need the new field</span></span>      |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="6f6e4-194">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="6f6e4-194">Role Price</span></span>|<span data-ttu-id="6f6e4-195">• Informações</span><span class="sxs-lookup"><span data-stu-id="6f6e4-195">• Information</span></span> |<span data-ttu-id="6f6e4-196">• Preços Ativos de Categorias de Recursos</span><span class="sxs-lookup"><span data-stu-id="6f6e4-196">• Active Resource Category Prices</span></span><br> <span data-ttu-id="6f6e4-197">• Exibição Associada de Preços de Categorias de Recursos</span><span class="sxs-lookup"><span data-stu-id="6f6e4-197">• Resource Category Price Associated View</span></span>|
|  <span data-ttu-id="6f6e4-198">Markup de Preço da Função</span><span class="sxs-lookup"><span data-stu-id="6f6e4-198">Role Price Markup</span></span>|<span data-ttu-id="6f6e4-199">• Informações</span><span class="sxs-lookup"><span data-stu-id="6f6e4-199">• Information</span></span>|<span data-ttu-id="6f6e4-200">• Markup de Preço da Função Ativo</span><span class="sxs-lookup"><span data-stu-id="6f6e4-200">• Active Role Price Markup</span></span><br><span data-ttu-id="6f6e4-201">• Exibição Associada do Markup de Preço da Função</span><span class="sxs-lookup"><span data-stu-id="6f6e4-201">• Role Price Markup Associated View</span></span>|
|  <span data-ttu-id="6f6e4-202">Detalhes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="6f6e4-202">Quote line detail</span></span>|<span data-ttu-id="6f6e4-203">• Informações do Projeto</span><span class="sxs-lookup"><span data-stu-id="6f6e4-203">• Project Information</span></span><br><span data-ttu-id="6f6e4-204">• Criação Rápida do ProJeto</span><span class="sxs-lookup"><span data-stu-id="6f6e4-204">• Project Quick Create</span></span>|<span data-ttu-id="6f6e4-205">• Detalhes da Linha de Cotação Ativos</span><span class="sxs-lookup"><span data-stu-id="6f6e4-205">• Active Quote Line Detail</span></span><br><span data-ttu-id="6f6e4-206">• Detalhes Combinados da Linha de Cotação</span><span class="sxs-lookup"><span data-stu-id="6f6e4-206">• Combined Quote Line Details</span></span><br><span data-ttu-id="6f6e4-207">• Exibição Associada de Detalhes da Linha de Cotação</span><span class="sxs-lookup"><span data-stu-id="6f6e4-207">• Quote Line Detail associated view</span></span>|
|  <span data-ttu-id="6f6e4-208">Detalhe da Linha de Contrato do Projeto</span><span class="sxs-lookup"><span data-stu-id="6f6e4-208">Project Contract line detail</span></span>|<span data-ttu-id="6f6e4-209">• Informações do Projeto</span><span class="sxs-lookup"><span data-stu-id="6f6e4-209">• Project Information</span></span><br><span data-ttu-id="6f6e4-210">• Criação Rápida do ProJeto</span><span class="sxs-lookup"><span data-stu-id="6f6e4-210">• Project Quick Create</span></span>|<span data-ttu-id="6f6e4-211">• Detalhes Combinados da Linha de Contrato</span><span class="sxs-lookup"><span data-stu-id="6f6e4-211">• Combined Contract Line Details</span></span><br><span data-ttu-id="6f6e4-212">• Detalhes da Linha de Contrato Ativa</span><span class="sxs-lookup"><span data-stu-id="6f6e4-212">• Active Contract Line Details</span></span><br><span data-ttu-id="6f6e4-213">• Exibição Associada de Detalhes da Linha de Contrato</span><span class="sxs-lookup"><span data-stu-id="6f6e4-213">• Contract Line Details Associated View</span></span>|
|  <span data-ttu-id="6f6e4-214">Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="6f6e4-214">Project Task</span></span>|<span data-ttu-id="6f6e4-215">• Informações</span><span class="sxs-lookup"><span data-stu-id="6f6e4-215">• Information</span></span><br><span data-ttu-id="6f6e4-216">• Novo Formulário</span><span class="sxs-lookup"><span data-stu-id="6f6e4-216">• New Form</span></span>||
|  <span data-ttu-id="6f6e4-217">Membro da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="6f6e4-217">Project Team Member</span></span>|<span data-ttu-id="6f6e4-218">• Informações</span><span class="sxs-lookup"><span data-stu-id="6f6e4-218">• Information</span></span><br><span data-ttu-id="6f6e4-219">• Novo Formulário</span><span class="sxs-lookup"><span data-stu-id="6f6e4-219">• New Form</span></span>|<span data-ttu-id="6f6e4-220">• Membros Ativos da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="6f6e4-220">• Active Project Team Members</span></span><br><span data-ttu-id="6f6e4-221">• Membros da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="6f6e4-221">• Project Team Members</span></span><br><span data-ttu-id="6f6e4-222">• Exibição Associada de Membros da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="6f6e4-222">• Project Team members associated View</span></span>|
|  <span data-ttu-id="6f6e4-223">Entrada de Horas</span><span class="sxs-lookup"><span data-stu-id="6f6e4-223">Time Entry</span></span>|<span data-ttu-id="6f6e4-224">• Informações</span><span class="sxs-lookup"><span data-stu-id="6f6e4-224">• Information</span></span><br><span data-ttu-id="6f6e4-225">• Criar Entrada de Hora</span><span class="sxs-lookup"><span data-stu-id="6f6e4-225">• Create Time Entry</span></span>|<span data-ttu-id="6f6e4-226">• Minhas Entradas de Hora por Data</span><span class="sxs-lookup"><span data-stu-id="6f6e4-226">• My Time Entries By Date</span></span><br><span data-ttu-id="6f6e4-227">• Minhas Entradas de Horas para Esta Semana</span><span class="sxs-lookup"><span data-stu-id="6f6e4-227">• My time Entries for this week</span></span><br><span data-ttu-id="6f6e4-228">• Entradas de hora para aprovação</span><span class="sxs-lookup"><span data-stu-id="6f6e4-228">• Time entries for approval</span></span>|
|  <span data-ttu-id="6f6e4-229">Linha do Diário</span><span class="sxs-lookup"><span data-stu-id="6f6e4-229">Journal Line</span></span>|<span data-ttu-id="6f6e4-230">• Informações</span><span class="sxs-lookup"><span data-stu-id="6f6e4-230">• Information</span></span><br><span data-ttu-id="6f6e4-231">• Criação rápida:</span><span class="sxs-lookup"><span data-stu-id="6f6e4-231">• Quick create</span></span>|<span data-ttu-id="6f6e4-232">• Linhas de diário ativas</span><span class="sxs-lookup"><span data-stu-id="6f6e4-232">• Active journal lines</span></span><br><span data-ttu-id="6f6e4-233">• Exibição Associada de Linhas de Diário</span><span class="sxs-lookup"><span data-stu-id="6f6e4-233">• Journal Line associated view</span></span>|
|  <span data-ttu-id="6f6e4-234">Detalhes da Linha da Fatura</span><span class="sxs-lookup"><span data-stu-id="6f6e4-234">Invoice Line Detail</span></span>|<span data-ttu-id="6f6e4-235">• Informações</span><span class="sxs-lookup"><span data-stu-id="6f6e4-235">• Information</span></span><br><span data-ttu-id="6f6e4-236">• Criação rápida:</span><span class="sxs-lookup"><span data-stu-id="6f6e4-236">• Quick create</span></span>|<span data-ttu-id="6f6e4-237">• Detalhes de Linha de Fatura Ativos</span><span class="sxs-lookup"><span data-stu-id="6f6e4-237">• Active Invoice Line Details</span></span><br><span data-ttu-id="6f6e4-238">• Transações de Fatura Passíveis de Cobrança</span><span class="sxs-lookup"><span data-stu-id="6f6e4-238">• Chargeable Invoice Transactions</span></span><br><span data-ttu-id="6f6e4-239">• Transações de Fatura Complementares</span><span class="sxs-lookup"><span data-stu-id="6f6e4-239">• Complimentary Invoice Transactions</span></span><br><span data-ttu-id="6f6e4-240">• Exibição Associada de Detalhes de Linha de Fatura</span><span class="sxs-lookup"><span data-stu-id="6f6e4-240">• Invoice Line Detail associated view</span></span><br><span data-ttu-id="6f6e4-241">• Transações de Fatura Não Passíveis de Cobrança</span><span class="sxs-lookup"><span data-stu-id="6f6e4-241">• Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="6f6e4-242">Real</span><span class="sxs-lookup"><span data-stu-id="6f6e4-242">Actual</span></span>|<span data-ttu-id="6f6e4-243">• Informações</span><span class="sxs-lookup"><span data-stu-id="6f6e4-243">• Information</span></span><br><span data-ttu-id="6f6e4-244">• Dados Reais Ativos</span><span class="sxs-lookup"><span data-stu-id="6f6e4-244">• Active Actuals</span></span>|<span data-ttu-id="6f6e4-245">• Exibição Associada de Dados Reais</span><span class="sxs-lookup"><span data-stu-id="6f6e4-245">• Actual Associated view</span></span>|

<span data-ttu-id="6f6e4-246">Talvez os campos personalizados também tenham que ser adicionados às regras de negócios, dependendo do que você definiu.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-246">Custom fields may also need to be added on business rules depending on what you have defined.</span></span> <span data-ttu-id="6f6e4-247">Um exemplo pronto para uso é para a regra de negócios **Capacidade de Edição da Entrada de Tempo baseada no status**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-247">One out-of-the-box example is for the business rule **Editability of Time Entry based on status**.</span></span> <span data-ttu-id="6f6e4-248">Essa regra define quais campos precisam ser bloqueados quando a Entrada de Tempo estiver em um status não editável, como **Aprovado**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-248">This rule defines which fields need to be locked when the Time Entry is in a non-editable status such as **Approved**.</span></span> <span data-ttu-id="6f6e4-249">Adicione campos a essa regra de negócios para que os campos sejam bloqueados para edição quando a Entrada de Tempo estiver em um status diferente de **Rascunho** ou **Devolvido**.</span><span class="sxs-lookup"><span data-stu-id="6f6e4-249">Add fields to this business rule so that the fields are locked for editing when the Time Entry is in a status other than **Draft** or **Returned**.</span></span>