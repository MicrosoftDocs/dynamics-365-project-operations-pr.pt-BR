---
title: Como posso personalizar o fluxo do processo empresarial Estágios do projeto?
description: Uma visão geral de como personalizar o fluxo do processo empresarial Estágios do Projeto.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2dccc33088cd9e49e7ffe609f9d9754ef33a5dba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071614"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="885c3-103">Como posso personalizar o fluxo do processo empresarial Estágios do projeto?</span><span class="sxs-lookup"><span data-stu-id="885c3-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="885c3-104">Há uma limitação conhecida em versões anteriores do aplicativo Project Service, em que os nomes dos estágios do fluxo do processo empresarial Estágios do projeto devem corresponder exatamente aos nomes esperados em inglês ( **Quote** , **Plan** , **Close** ).</span><span class="sxs-lookup"><span data-stu-id="885c3-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names ( **Quote** , **Plan** , **Close** ).</span></span> <span data-ttu-id="885c3-105">Caso contrário, a lógica de negócios, que depende dos nomes dos estágios em inglês, não funciona conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="885c3-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="885c3-106">Por isso, você não vê ações conhecidas como **Alternar Processo** ou **Editar Processo** disponíveis no formulário do projeto. Além disso, não é recomendável personalizar o fluxo do processo empresarial.</span><span class="sxs-lookup"><span data-stu-id="885c3-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="885c3-107">Essa restrição foi solucionada na versão 2.4.5.48 e posterior.</span><span class="sxs-lookup"><span data-stu-id="885c3-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="885c3-108">Este artigo fornece soluções alternativas sugeridas para versões anteriores, caso seja necessário personalizar o fluxo do processo empresarial padrão.</span><span class="sxs-lookup"><span data-stu-id="885c3-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="885c3-109">A lógica de negócios exige uma correspondência exata com nomes dos estágios em inglês</span><span class="sxs-lookup"><span data-stu-id="885c3-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="885c3-110">O fluxo do processo empresarial Estágios do projeto inclui uma lógica de negócios que leva aos seguintes comportamentos no aplicativo:</span><span class="sxs-lookup"><span data-stu-id="885c3-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="885c3-111">Quando o projeto é associado a uma cotação, o código define o fluxo do processo empresarial para o estágio **Quote**.</span><span class="sxs-lookup"><span data-stu-id="885c3-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="885c3-112">Quando o projeto é associado a um contrato, o código define o fluxo do processo empresarial para o estágio **Plan**.</span><span class="sxs-lookup"><span data-stu-id="885c3-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="885c3-113">Quando o fluxo de processo empresarial avança para o estágio **Close** , o registro do projeto é desativado.</span><span class="sxs-lookup"><span data-stu-id="885c3-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="885c3-114">Quando o projeto é desativado, o formulário do projeto e a estrutura de detalhamento de trabalho (WBS) são definidos como somente leitura, as reservas de recursos nomeados são liberadas, e todas as listas de preços associadas são desativadas.</span><span class="sxs-lookup"><span data-stu-id="885c3-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="885c3-115">Essa lógica de negócios depende dos nomes em inglês para os estágios do projeto.</span><span class="sxs-lookup"><span data-stu-id="885c3-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="885c3-116">Essa dependência dos nomes dos estágios em inglês é o motivo principal pelo qual a personalização do fluxo do processo empresarial Estágios do projeto não é recomendável. Essa também é a razão pela qual você não vê ações do fluxo do processo empresarial como **Alternar Processo** ou **Editar Processo** na entidade de projeto.</span><span class="sxs-lookup"><span data-stu-id="885c3-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="885c3-117">O que acontece se os nomes de estágios não correspondem aos nomes em inglês?</span><span class="sxs-lookup"><span data-stu-id="885c3-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="885c3-118">Na versão 1.x do aplicativo Project Service na plataforma 8.2, quando os nomes dos estágios no fluxo do processo empresarial não correspondem exatamente aos nomes dos estágios em inglês, a lógica de negócios que define o estágio adequado para cotações ou contratos, ou que encerra o projeto, é ignorada.</span><span class="sxs-lookup"><span data-stu-id="885c3-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="885c3-119">Nenhuma mensagem de erro é exibida.</span><span class="sxs-lookup"><span data-stu-id="885c3-119">No error messages are displayed.</span></span> <span data-ttu-id="885c3-120">Por isso, parece que você pode personalizar o fluxo do processo empresarial Estágios do projeto.</span><span class="sxs-lookup"><span data-stu-id="885c3-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="885c3-121">Entretanto, não verá nenhum processo automático funcionando para cotações, contratos e fechamentos de projetos.</span><span class="sxs-lookup"><span data-stu-id="885c3-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="885c3-122">Na versão 2.4.4.30 ou anterior do aplicativo Project Service na plataforma 9.0, houve uma alteração significativa na arquitetura para fluxos do processo empresarial, que exigiu a regravação da lógica de negócios do fluxo do processo empresarial.</span><span class="sxs-lookup"><span data-stu-id="885c3-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="885c3-123">Consequentemente, se os nomes dos estágios do processo não corresponderem aos nomes esperados em inglês, você receberá uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="885c3-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="885c3-124">Portanto, se você quiser personalizar o fluxo do processo empresarial Estágios do projeto para a entidade de projeto, você só pode adicionar novos estágios ao fluxo do processo empresarial padrão para a entidade de projeto, mantendo os estágios **Quote** , **Plan** e **Close** da maneira em que se encontram.</span><span class="sxs-lookup"><span data-stu-id="885c3-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote** , **Plan** , and **Close** stages as-is.</span></span> <span data-ttu-id="885c3-125">Essa restrição garante que você não receba erros da lógica de negócios que espera os nomes dos estágios em inglês no fluxo do processo empresarial.</span><span class="sxs-lookup"><span data-stu-id="885c3-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="885c3-126">Em uma versão 2.4.5.48 ou futura, a lógica de negócios descrita neste artigo é removida do fluxo do processo empresarial padrão para a entidade de projeto.</span><span class="sxs-lookup"><span data-stu-id="885c3-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="885c3-127">A atualização para a versão ou posterior permitirá que você personalize ou substitua o fluxo do processo empresarial padrão por um que seja seu.</span><span class="sxs-lookup"><span data-stu-id="885c3-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="885c3-128">Soluções alternativas para versões anteriores</span><span class="sxs-lookup"><span data-stu-id="885c3-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="885c3-129">Se a atualização não for uma opção, será possível personalizar o fluxo do processo empresarial Estágios do projeto para a entidade de projeto de uma destas duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="885c3-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="885c3-130">Adicione mais estágios à configuração padrão, mantendo os nomes dos estágios em inglês para **Quote** , **Plan** e **Close**.</span><span class="sxs-lookup"><span data-stu-id="885c3-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote** , **Plan** , and **Close**.</span></span>


![Captura de tela da adição de estágios à configuração padrão](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="885c3-132">Crie seu próprio fluxo do processo empresarial e o torne o fluxo do processo empresarial principal para a entidade de projeto, permitindo que você tenha qualquer nome de estágio que quiser.</span><span class="sxs-lookup"><span data-stu-id="885c3-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="885c3-133">Entretanto, se você quiser usar os mesmos estágios do projeto padrão, **Quote** , **Plan** e **Plan** , será necessário fazer algumas personalizações baseadas em seus nomes de estágios personalizados.</span><span class="sxs-lookup"><span data-stu-id="885c3-133">However, if you want to use the same standard project stages **Quote** , **Plan** , and **Close** , you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="885c3-134">A lógica mais complexa está no fechamento do projeto, que você ainda pode acionar por meio da desativação do registro do projeto.</span><span class="sxs-lookup"><span data-stu-id="885c3-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Personalização de BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="885c3-136">Considerações adicionais para a versão 2.4.4.30 ou anterior do aplicativo Project Service na plataforma 9.0</span><span class="sxs-lookup"><span data-stu-id="885c3-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="885c3-137">Na versão 2.4.4.30 ou anterior do Project Service na plataforma 9.0, com um fluxo do processo empresarial personalizado, o campo **Nome de estágio** na entidade de projeto usada no gráfico **Projeto por estágio** e exibições de listas do projeto não serão atualizados, pois estão acoplados ao fluxo do processo empresarial padrão Estágios do projeto.</span><span class="sxs-lookup"><span data-stu-id="885c3-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="885c3-138">Você pode resolver esse problema com uma as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="885c3-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="885c3-139">Adicione um campo personalizado para capturar o estágio atual do fluxo do processo empresarial que é atualizado conforme o usuário avança no fluxo de processo empresarial personalizado.</span><span class="sxs-lookup"><span data-stu-id="885c3-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="885c3-140">Modifique o gráfico **Projeto por estágio** para trabalhar com o seu campo personalizado em vez da configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="885c3-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="885c3-141">Etapas para criar seu próprio fluxo do processo empresarial para a entidade de projeto</span><span class="sxs-lookup"><span data-stu-id="885c3-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="885c3-142">Para criar seu próprio fluxo do processo empresarial para a entidade de projeto, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="885c3-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="885c3-143">Vá para **Configurações** > **Centro de processos**.</span><span class="sxs-lookup"><span data-stu-id="885c3-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="885c3-144">Não copie o fluxo do processo empresarial Estágios do projeto porque isso também copiará a lógica de negócios do Project Service.</span><span class="sxs-lookup"><span data-stu-id="885c3-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Criar processo](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="885c3-146">Use o designer de processo para criar os nomes de estágios que quiser.</span><span class="sxs-lookup"><span data-stu-id="885c3-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="885c3-147">Caso queira a mesma funcionalidade dos estágios padrão para **Quote** , **Plan** e **Close** , é necessário criá-la com base nos nomes dos estágios do fluxo do processo empresarial personalizado.</span><span class="sxs-lookup"><span data-stu-id="885c3-147">If you want the same functionality as the default stages for **Quote** , **Plan** , and **Close** , you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Captura de tela do designer de processo usado para personalizar o fluxo do processo empresarial](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="885c3-149">No designer de processo, clique em **Ordenar Fluxo do Processo** para tornar o fluxo do processo empresarial personalizado o fluxo do processo empresarial principal para a entidade de projeto ao movê-lo acima do fluxo do processo empresarial Estágios do projeto para o topo da lista.</span><span class="sxs-lookup"><span data-stu-id="885c3-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="885c3-150">Captura de tela do uso de Ordenar Fluxo do Processo</span><span class="sxs-lookup"><span data-stu-id="885c3-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="885c3-151">As etapas a seguir se aplicam à versão 2.4.4.30 ou anterior do aplicativo Project Service na plataforma 9.0</span><span class="sxs-lookup"><span data-stu-id="885c3-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="885c3-152">Adicione um novo campo personalizado à entidade de projeto para capturar as etapas personalizadas no fluxo do processo empresarial personalizado.</span><span class="sxs-lookup"><span data-stu-id="885c3-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="885c3-153">Será necessário adicionar a lógica de negócios (plug-in/fluxo de trabalho) para atualizar esse campo quando o estágio no fluxo do processo empresarial personalizado for atualizado.</span><span class="sxs-lookup"><span data-stu-id="885c3-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Captura de tela da personalização da entidade de projeto](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="885c3-155">Modifique o gráfico **Projeto por estágio** para usar o novo campo personalizado para os estágios.</span><span class="sxs-lookup"><span data-stu-id="885c3-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Captura de tela do uso do gráfico Projeto por estágio](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="885c3-157">Modifique todas as exibições para a entidade de projeto para incluir o novo campo personalizado para os estágios.</span><span class="sxs-lookup"><span data-stu-id="885c3-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Captura de tela das modificações de exibições na entidade de projeto](media/FAQ-Customize-BPF-8-720.png)

