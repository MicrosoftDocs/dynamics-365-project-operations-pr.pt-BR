---
title: Adicionar novos formulários de entidade personalizada (Project Service Automation 2.x)
description: Este tópico fornece informações sobre como adicionar formulários da entidade personalizada para oportunidades, cotações, ordens ou faturas no Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 400d817ee7cbae6f6da95db4286ad6c4d6ff349a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007982"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="03efd-103">Adicionar novos formulários de entidade personalizada (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="03efd-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="03efd-104">Campo Tipo</span><span class="sxs-lookup"><span data-stu-id="03efd-104">Type field</span></span> 

<span data-ttu-id="03efd-105">O Dynamics 365 Project Service Automation depende do campo **Tipo** (**msdyn\_ordertype**) das entidades Oportunidade, Cotação, Ordem e Fatura para diferenciar versões **baseadas em trabalho** dessas entidades nas versões **baseadas em item** e **baseadas em serviço**.</span><span class="sxs-lookup"><span data-stu-id="03efd-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="03efd-106">As versões baseadas no local dessas entidades são tratadas pelo PSA.</span><span class="sxs-lookup"><span data-stu-id="03efd-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="03efd-107">Muito da lógica de negócios no cliente e servidor da solução depende do campo **Tipo**.</span><span class="sxs-lookup"><span data-stu-id="03efd-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="03efd-108">Portanto, é importante que o campo seja inicializado com um valor correto quando as entidades são criadas.</span><span class="sxs-lookup"><span data-stu-id="03efd-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="03efd-109">Um valor incorreto pode causar comportamentos incorretos, e alguma lógica de negócios pode não ser executada corretamente.</span><span class="sxs-lookup"><span data-stu-id="03efd-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="03efd-110">Alternação automática de formulário</span><span class="sxs-lookup"><span data-stu-id="03efd-110">Automatic form switching</span></span>

<span data-ttu-id="03efd-111">Para evitar a possível corrupção de dados e comportamentos inesperados que são causados pela inicialização e edição incorretas dos registros de entidade de vendas, o PSA agora inclui lógica para alternação automática de formulário em formulários prontos para uso.</span><span class="sxs-lookup"><span data-stu-id="03efd-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="03efd-112">Essa lógica conduz os usuários ao formulário correto para trabalhar com a versão baseada em trabalho ou qualquer outro tipo de entidade Oportunidade, Cotação, Ordem ou Fatura.</span><span class="sxs-lookup"><span data-stu-id="03efd-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="03efd-113">Quando um usuário abre a versão baseada em trabalho de uma entidade Oportunidade, Cotação, Ordem ou Fatura, o formulário é alternado para **Informações do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="03efd-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="03efd-114">A lógica de alternância automática de formulário depende do mapeamento entre o valor **formId** e o campo **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="03efd-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="03efd-115">Todos os formulários prontos para uso foram adicionados a esse mapeamento.</span><span class="sxs-lookup"><span data-stu-id="03efd-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="03efd-116">No entanto, os formulários personalizados devem ser adicionados manualmente para indicar com qual versão da entidade eles pretendem lidar.</span><span class="sxs-lookup"><span data-stu-id="03efd-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="03efd-117">Isso se baseia no campo **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="03efd-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="03efd-118">Se a alternância de formulário não estiver no mapeamento, a lógica será alternada para o formulário pronto para uso, com base no valor que é salvo no campo **msdyn\_ordertype** da entidade.</span><span class="sxs-lookup"><span data-stu-id="03efd-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="03efd-119">Adicionar formulários personalizados e ativar a lógica de alternância de formulário</span><span class="sxs-lookup"><span data-stu-id="03efd-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="03efd-120">O exemplo a seguir mostra como adicionar um formulário **Informações do Meu Projeto** personalizado para que ele funcione com oportunidades baseadas em trabalho.</span><span class="sxs-lookup"><span data-stu-id="03efd-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="03efd-121">O mesmo processo é usado para adicionar formulário personalizados para que eles funcionem com cotações, ordens e faturas.</span><span class="sxs-lookup"><span data-stu-id="03efd-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="03efd-122">Siga estas etapas para criar uma versão personalizada do formulário **Informações do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="03efd-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="03efd-123">Na entidade Oportunidade, abra o formulário **Informações do Projeto** e salve uma cópia com o nome **Informações do Meu Projeto**.</span><span class="sxs-lookup"><span data-stu-id="03efd-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="03efd-124">Abra o novo formulário e, em seguida, nas propriedades, certifique-se de que os scripts de inicialização do formulário **Informações do Projeto** estejam presentes.</span><span class="sxs-lookup"><span data-stu-id="03efd-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="03efd-125">Não remova os scripts.</span><span class="sxs-lookup"><span data-stu-id="03efd-125">Don't remove the scripts.</span></span> <span data-ttu-id="03efd-126">Caso contrário, alguns dados podem ser inicializados incorretamente.</span><span class="sxs-lookup"><span data-stu-id="03efd-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="03efd-127">Verifique se o campo **Tipo** (**msdyn\_ordertype**) está presente no formulário.</span><span class="sxs-lookup"><span data-stu-id="03efd-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="03efd-128">Não remova esse campo.</span><span class="sxs-lookup"><span data-stu-id="03efd-128">Don't remove this field.</span></span> <span data-ttu-id="03efd-129">Caso contrário, os scripts de inicialização falharão.</span><span class="sxs-lookup"><span data-stu-id="03efd-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="03efd-130">Localize o valor **formId** do novo formulário.</span><span class="sxs-lookup"><span data-stu-id="03efd-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="03efd-131">É possível concluir essa etapa de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="03efd-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="03efd-132">Exporte o formulário **Informações do Meu Projeto** como parte de uma solução não gerenciada e pesquise o valor **formId** no arquivo customization.xml da solução exportada.</span><span class="sxs-lookup"><span data-stu-id="03efd-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="03efd-133">Abra o formulário **Informações do Meu Projeto** no editor de formulários e procure o GUID (identificador global exclusivo) ao lado do parâmetro **fromId** na URL, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="03efd-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![O valor formId do novo formulário na URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="03efd-135">Crie um mapeamento **msdyn\_ordertype** para o valor **formId** editando o recurso da Web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="03efd-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="03efd-136">Remova o código do recurso e substitua-o pelo código a seguir.</span><span class="sxs-lookup"><span data-stu-id="03efd-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="03efd-137">Salve e publique as personalizações.</span><span class="sxs-lookup"><span data-stu-id="03efd-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]