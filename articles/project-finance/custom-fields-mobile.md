---
title: Implementar campos personalizados para o aplicativo móvel Microsoft Dynamics 365 Project Timesheet no iOS e Android
description: Este tópico fornece padrões comuns para usar extensões para implementar campos personalizados.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749035"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="0f605-103">Implementar campos personalizados para o aplicativo móvel Microsoft Dynamics 365 Project Timesheet no iOS e Android</span><span class="sxs-lookup"><span data-stu-id="0f605-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f605-104">Este tópico fornece padrões comuns para usar extensões para implementar campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="0f605-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="0f605-105">Os tópicos a seguir são abordados:</span><span class="sxs-lookup"><span data-stu-id="0f605-105">The following topics are covered:</span></span>

- <span data-ttu-id="0f605-106">Os vários tipos de dados que a estrutura de campos personalizados oferece suporte</span><span class="sxs-lookup"><span data-stu-id="0f605-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="0f605-107">Como mostrar campos personalizados editáveis ou somente leitura em entradas de folha de pagamento e salvar valores fornecidos pelo usuários de volta ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="0f605-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="0f605-108">Como mostrar campos personalizados somente leitura no cabeçalho da folha de pagamento</span><span class="sxs-lookup"><span data-stu-id="0f605-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="0f605-109">Como integrar outra lógica de negócios personalizada para inserir valores padrão em campos e fazer validações adicionais</span><span class="sxs-lookup"><span data-stu-id="0f605-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="0f605-110">Público-alvo</span><span class="sxs-lookup"><span data-stu-id="0f605-110">Audience</span></span>

<span data-ttu-id="0f605-111">Este tópico destina-se a desenvolvedores que estão integrando seus campos personalizados ao aplicativo móvel Microsoft Dynamics 365 Project Timesheet que está disponível para Apple iOS e Google Android.</span><span class="sxs-lookup"><span data-stu-id="0f605-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="0f605-112">Pressupõe-se que os leitores estejam familiarizados com o desenvolvimento em X++ e com a funcionalidade de folha de ponto do projeto.</span><span class="sxs-lookup"><span data-stu-id="0f605-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="0f605-113">Contrato de dados — classe TSTimesheetCustomField de X++</span><span class="sxs-lookup"><span data-stu-id="0f605-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="0f605-114">A classe **TSTimesheetCustomField** é o contrato de dados de X+ que representa as informações sobre um campo personalizado para a funcionalidade de folha de ponto.</span><span class="sxs-lookup"><span data-stu-id="0f605-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="0f605-115">Lista os objetos do campo personalizado no contrato de dados TSTimesheetDetails e no contrato de dados TSTimesheetEntry para mostrar campos personalizados no aplicativo móvel.</span><span class="sxs-lookup"><span data-stu-id="0f605-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="0f605-116">**TSTimesheetDetails** — o contrato do cabeçalho da folha de ponto.</span><span class="sxs-lookup"><span data-stu-id="0f605-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="0f605-117">**TSTimesheetEntry** — o contrato de transação da folha de ponto.</span><span class="sxs-lookup"><span data-stu-id="0f605-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="0f605-118">Grupos desses objetos que tenham as mesmas informações do projeto e o valor **timesheetLineRecId** constituem um linha,</span><span class="sxs-lookup"><span data-stu-id="0f605-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="0f605-119">fieldBaseType (Tipos)</span><span class="sxs-lookup"><span data-stu-id="0f605-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="0f605-120">A propriedade **FieldBaseType** no objeto **TsTimesheetCustom** determina o tipo de campo que é exibido no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="0f605-121">Ha suporte aos seguintes valores de **Tipos**:</span><span class="sxs-lookup"><span data-stu-id="0f605-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="0f605-122">Valor de tipos</span><span class="sxs-lookup"><span data-stu-id="0f605-122">Types value</span></span> | <span data-ttu-id="0f605-123">Digitar</span><span class="sxs-lookup"><span data-stu-id="0f605-123">Type</span></span>              | <span data-ttu-id="0f605-124">Anotações</span><span class="sxs-lookup"><span data-stu-id="0f605-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="0f605-125">0</span><span class="sxs-lookup"><span data-stu-id="0f605-125">0</span></span>           | <span data-ttu-id="0f605-126">Cadeia de Caracteres (e Enumeração)</span><span class="sxs-lookup"><span data-stu-id="0f605-126">String (and Enum)</span></span> | <span data-ttu-id="0f605-127">O campo é exibido como um campo de texto.</span><span class="sxs-lookup"><span data-stu-id="0f605-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="0f605-128">0</span><span class="sxs-lookup"><span data-stu-id="0f605-128">1</span></span>           | <span data-ttu-id="0f605-129">Integer</span><span class="sxs-lookup"><span data-stu-id="0f605-129">Integer</span></span>           | <span data-ttu-id="0f605-130">O valor é exibido como um número sem casas decimais.</span><span class="sxs-lookup"><span data-stu-id="0f605-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="0f605-131">2</span><span class="sxs-lookup"><span data-stu-id="0f605-131">2</span></span>           | <span data-ttu-id="0f605-132">Real</span><span class="sxs-lookup"><span data-stu-id="0f605-132">Real</span></span>              | <span data-ttu-id="0f605-133">O valor é exibido como um número com casas decimais.</span><span class="sxs-lookup"><span data-stu-id="0f605-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="0f605-134">Para mostrar o valor real como uma moeda no aplicativo, use a propriedade **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="0f605-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="0f605-135">Você pode usar a propriedade **numberOfDecimals** para definir o número de casas decimais exibidas.</span><span class="sxs-lookup"><span data-stu-id="0f605-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="0f605-136">3</span><span class="sxs-lookup"><span data-stu-id="0f605-136">3</span></span>           | <span data-ttu-id="0f605-137">Data</span><span class="sxs-lookup"><span data-stu-id="0f605-137">Date</span></span>              | <span data-ttu-id="0f605-138">Os formatos de data são definidos pela configuração **formato de data, hora e número** do usuário, que está especificada em **Preferência de idioma e país/região** em **Opções do usuário**.</span><span class="sxs-lookup"><span data-stu-id="0f605-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="0f605-139">4</span><span class="sxs-lookup"><span data-stu-id="0f605-139">4</span></span>           | <span data-ttu-id="0f605-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="0f605-140">Boolean</span></span>           | |
| <span data-ttu-id="0f605-141">15</span><span class="sxs-lookup"><span data-stu-id="0f605-141">15</span></span>          | <span data-ttu-id="0f605-142">GUID</span><span class="sxs-lookup"><span data-stu-id="0f605-142">GUID</span></span>              | |
| <span data-ttu-id="0f605-143">16</span><span class="sxs-lookup"><span data-stu-id="0f605-143">16</span></span>          | <span data-ttu-id="0f605-144">Int64</span><span class="sxs-lookup"><span data-stu-id="0f605-144">Int64</span></span>             | |

- <span data-ttu-id="0f605-145">Se a propriedade **stringOptions** não for fornecida no objeto **TSTimesheetCustomField**, um campo de texto livre será fornecido ao usuário.</span><span class="sxs-lookup"><span data-stu-id="0f605-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="0f605-146">A propriedade **stringLength** pode ser usada para definir o tamanho máximo da cadeia de caracteres que os usuário poderão inserir.</span><span class="sxs-lookup"><span data-stu-id="0f605-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="0f605-147">Se a propriedade **stringOptions** for fornecida no objeto **TSTimesheetCustomField**, os valores dessa lista de elementos serão os únicos que os usuários poderão selecionar usando os botões de opção.</span><span class="sxs-lookup"><span data-stu-id="0f605-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="0f605-148">Nesse caso, o campo de cadeia de caracteres pode agir como um valor de enumeração para fins de entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="0f605-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="0f605-149">Para salvar o valor de um banco de dados como uma enumeração, mapeie manualmente o valor da cadeia de caracteres de volta ao valor da enumeração antes de salvar no banco de dados usando a cadeia de comando (consulte a seção "Usar cadeia de comando na classe TSTimesheetEntryService para salvar uma entrada de folha de ponto do aplicativo de volta no banco de dados" posteriormente neste tópico para obter um exemplo).</span><span class="sxs-lookup"><span data-stu-id="0f605-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="0f605-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="0f605-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="0f605-151">Você pode usar essa propriedade para formatar valores reais como moeda.</span><span class="sxs-lookup"><span data-stu-id="0f605-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="0f605-152">Essa abordagem é aplicável somente quando o valor **fieldBaseType** for **Real**.</span><span class="sxs-lookup"><span data-stu-id="0f605-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="0f605-153">**TSCustomFieldExtendedType:None** — nenhuma formatação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="0f605-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="0f605-154">**TSCustomFieldExtendedType::Currency** — formata o valor como moeda.</span><span class="sxs-lookup"><span data-stu-id="0f605-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="0f605-155">Quando a formatação da moeda está ativa, o campo **stringValue** pode ser usado para passar o código da moeda que deve ser exibido no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="0f605-156">O valor é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0f605-156">The value is a read-only value.</span></span>

    <span data-ttu-id="0f605-157">O campo **realValue** contém o valor monetário que deve ser salvo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f605-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="0f605-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="0f605-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="0f605-159">Você pode usar essa propriedade para especificar quando o campo personalizado deve ser exibido no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="0f605-160">**TSCustomFieldSection::Header** — o campo será exibido na seção **Exibir mais detalhes** no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="0f605-161">Esses campos sempre são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0f605-161">These fields are always read-only.</span></span>
- <span data-ttu-id="0f605-162">**TSCustomFieldSection::Line** — o campo será exibido após todos os campos de linha prontos para uso nas entradas da folha de ponto.</span><span class="sxs-lookup"><span data-stu-id="0f605-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="0f605-163">Esses campos podem ser editáveis ou somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0f605-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="0f605-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="0f605-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="0f605-165">Essa propriedade identifica o campo quando os valores que o aplicativo fornece são salvos de volta no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f605-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="0f605-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="0f605-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="0f605-167">Essa propriedade identifica o campo quando os valores que o aplicativo fornece são salvos de volta no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f605-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="0f605-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="0f605-168">isEditable (NoYes)</span></span>

<span data-ttu-id="0f605-169">Defina essa propriedade como **Sim** para especificar que o campo na seção de entrada da folha de ponto deve ser editável pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="0f605-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="0f605-170">Defina a propriedade como **Não** para fazer com que o campo seja somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0f605-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="0f605-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="0f605-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="0f605-172">Defina essa propriedade como **Sim** para especificar que o campo na seção de entrada da folha de ponto deve ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0f605-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="0f605-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="0f605-173">label (str)</span></span>

<span data-ttu-id="0f605-174">Essa propriedade especifica o rótulo que é exibido ao lado do campo no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="0f605-175">stringOptions (Lista de Cadeias de Caracteres)</span><span class="sxs-lookup"><span data-stu-id="0f605-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="0f605-176">Essa propriedade é aplicável somente quando **fieldBaseType** é definido como **Cadeia de Caracteres**.</span><span class="sxs-lookup"><span data-stu-id="0f605-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="0f605-177">Se a propriedade **stringOptions** estiver definida, os valores de cadeia de caracteres que estão disponíveis para seleção por meio dos botões de opção serão especificados pelas cadeias de caracteres na lista.</span><span class="sxs-lookup"><span data-stu-id="0f605-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="0f605-178">Se nenhuma cadeia de caracteres for fornecida, a entrada de texto livre no campo de cadeia de caracteres será permitida (consulte a seção "Usar a cadeia de comando na classe TSTimesheetEntryService para salvar uma entrada de folha de ponto do aplicativo de volta no banco de dados" posteriormente neste tópico para obter um exemplo).</span><span class="sxs-lookup"><span data-stu-id="0f605-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="0f605-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="0f605-179">stringLength (int)</span></span>

<span data-ttu-id="0f605-180">Essa propriedade especifica o tamanho máximo de um campo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0f605-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="0f605-181">Ela é aplicável somente quando **fieldBaseType** é definido como **Cadeia de Caracteres**.</span><span class="sxs-lookup"><span data-stu-id="0f605-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="0f605-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="0f605-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="0f605-183">Essa propriedade especifica o número de casas decimais exibidas para um campo real.</span><span class="sxs-lookup"><span data-stu-id="0f605-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="0f605-184">Ela é aplicável somente quando **fieldBaseType** é definido como **Real**.</span><span class="sxs-lookup"><span data-stu-id="0f605-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="0f605-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="0f605-185">orderSequence (int)</span></span>

<span data-ttu-id="0f605-186">Essa propriedade controla a ordem na qual os campos personalizados são exibidos no aplicativo quando mais de um campo personalizado é especificado.</span><span class="sxs-lookup"><span data-stu-id="0f605-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="0f605-187">Campos com números mais baixos são exibidos primeiro.</span><span class="sxs-lookup"><span data-stu-id="0f605-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="0f605-188">booleanValue (booliano)</span><span class="sxs-lookup"><span data-stu-id="0f605-188">booleanValue (boolean)</span></span>

<span data-ttu-id="0f605-189">Para campos do tipo **Booliano**, essa propriedade passa o valor booliano do campo entre o servidor e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="0f605-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="0f605-190">guidValue (guid)</span></span>

<span data-ttu-id="0f605-191">Para campos do tipo **GUID**, essa propriedade passa o valor do identificador global exclusivo (GUID) do campo entre o servidor e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="0f605-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="0f605-192">int64Value (int64)</span></span>

<span data-ttu-id="0f605-193">Para campos do tipo **Int64**, essa propriedade passa o valor de Int64 do campo entre o servidor e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="0f605-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="0f605-194">intValue (int)</span></span>

<span data-ttu-id="0f605-195">Para campos do tipo **Int**, essa propriedade passa o valor de int do campo entre o servidor e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="0f605-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="0f605-196">realValue (real)</span></span>

<span data-ttu-id="0f605-197">Para campos do tipo **Real**, essa propriedade passa o valor real do campo entre o servidor e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="0f605-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="0f605-198">stringValue (str)</span></span>

<span data-ttu-id="0f605-199">Para campos do tipo **Cadeia de Caracteres**, essa propriedade passa o valor da cadeia de caracteres do campo entre o servidor e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="0f605-200">Ela também é usada para campos do tipo **Real** que são formatados como moeda.</span><span class="sxs-lookup"><span data-stu-id="0f605-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="0f605-201">Para esses campos, a propriedade é usada para passar o código de moeda para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="0f605-202">dateValue (data)</span><span class="sxs-lookup"><span data-stu-id="0f605-202">dateValue (date)</span></span>

<span data-ttu-id="0f605-203">Para campos do tipo **Data**, essa propriedade passa o valor de data do campo entre o servidor e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="0f605-204">Mostrar e salvar um campo personalizado na seção de entrada de folha de ponto</span><span class="sxs-lookup"><span data-stu-id="0f605-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="0f605-205">Abaixo encontra-se uma captura de tela do aplicativo móvel de uma criação de entrada de folha de ponto.</span><span class="sxs-lookup"><span data-stu-id="0f605-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="0f605-206">Ela mostra os campos prontos para uso e um campo personalizado na seção "Entrada de horas" chamado "Cadeia de caracteres de teste" com um valor de enumeração de "Segunda opção" já definido.</span><span class="sxs-lookup"><span data-stu-id="0f605-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Campo Cadeia de caracteres de teste no aplicativo](media/timesheet-entry.jpg)



<span data-ttu-id="0f605-208">Abaixo encontra-se uma captura de tela do usuário do aplicativo móvel selecionando uma das opções de enumeração disponíveis para o campo personalizado "Cadeia de caracteres de teste".</span><span class="sxs-lookup"><span data-stu-id="0f605-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="0f605-209">As duas opções são "Primeira opção" e Segunda opção", exibidas como botões de opção.</span><span class="sxs-lookup"><span data-stu-id="0f605-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="0f605-210">A segunda opção está selecionada.</span><span class="sxs-lookup"><span data-stu-id="0f605-210">The second option is currently selected.</span></span>

![Botões de opção para o campo personalizado Cadeia de caracteres de teste](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="0f605-212">Estender a tabela TSTimesheetLine para que ela tenha um campo personalizado</span><span class="sxs-lookup"><span data-stu-id="0f605-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="0f605-213">Em cenários típicos, é provável que os dados de um campo personalizado na seção de entrada da folha de ponto sejam salvos na tabela TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="0f605-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="0f605-214">No entanto, outras tabelas podem ser usadas se os dados puderem se recuperados com base em um registro de TSTimesheetTrans que seja fornecido, ou se não tiverem um contexto de registro específico (por exemplo, se o campo for definido como somente leitura nos parâmetros do projeto).</span><span class="sxs-lookup"><span data-stu-id="0f605-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="0f605-215">Observe que os campos personalizados não têm nenhum registro de banco de dados de backup.</span><span class="sxs-lookup"><span data-stu-id="0f605-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="0f605-216">Eles podem ser gerados dinamicamente com base na lógica de X++.</span><span class="sxs-lookup"><span data-stu-id="0f605-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="0f605-217">Essa abordagem é útil em cenários somente leitura (consulte a seção "Usar a cadeia de comando na classe TSTimesheetDetails, método buildCustomFieldListForHeader para preencher detalhes da folha de ponto" para obter um exemplo de valores de campos personalizados gerados dinamicamente).</span><span class="sxs-lookup"><span data-stu-id="0f605-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="0f605-218">Abaixo encontra-se uma captura de tela do Visual Studio da árvore de objetos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="0f605-219">Ela mostra uma extensão da tabela TSTimesheetLine com o campo TestLineString adicionado como um campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="0f605-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Cadeia de caracteres de linha](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="0f605-221">Usar a cadeia de comando no método buildCustomFieldList da classe TSTimesheetSettings para mostrar um campo na seção de entrada de folha de ponto</span><span class="sxs-lookup"><span data-stu-id="0f605-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="0f605-222">Esse código controla as configurações de exibição do campo no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="0f605-223">Por exemplo, ele controla o tipo de campo, o rótulo, se o campo é obrigatório e em qual seção o campo é exibido.</span><span class="sxs-lookup"><span data-stu-id="0f605-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="0f605-224">O exemplo a seguir mostra um campo de cadeia de caracteres em entradas de horas.</span><span class="sxs-lookup"><span data-stu-id="0f605-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="0f605-225">Esse campo tem duas opções, **Primeira opção** e **Segunda opção**, que estão disponíveis por meio dos botões de opção.</span><span class="sxs-lookup"><span data-stu-id="0f605-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="0f605-226">O campo no aplicativo está associado ao campo **TestLineString**, que está adicionado à tabela TSTimesheetLine table.</span><span class="sxs-lookup"><span data-stu-id="0f605-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="0f605-227">Observe o uso do método **TSTimesheetCustomField::newFromMetatdata()** para simplificar a inicialização das propriedades do campo personalizado: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** e **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="0f605-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="0f605-228">Você também pode definir esses parâmetros manualmente, como preferir.</span><span class="sxs-lookup"><span data-stu-id="0f605-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="0f605-229">Usar a cadeia de comando no método buildCustomFieldListForEntry da classe TSTimesheetEntry para inserir valores em uma entrada de folha de ponto</span><span class="sxs-lookup"><span data-stu-id="0f605-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="0f605-230">O método **buildCustomFieldListForEntry** é usado para inserir valores nas linhas salvas da folha de ponto em um aplicativo móvel.</span><span class="sxs-lookup"><span data-stu-id="0f605-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="0f605-231">Ele pega um registro de TSTimesheetTrans como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0f605-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="0f605-232">Campos desse registro podem ser usados para preencher o valor do campo personalizado no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="0f605-233">Usar a cadeia de comando na classe TSTimesheetEntryService para salvar uma entrada de folha de ponto do aplicativo de volta no banco de dados</span><span class="sxs-lookup"><span data-stu-id="0f605-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="0f605-234">Para salvar um campo personalizado de volta no banco de dados em uso típico, você deve estender vários métodos:</span><span class="sxs-lookup"><span data-stu-id="0f605-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="0f605-235">O método **timesheetLineNeedsUpdating** é usado para determinar se o registro da linha foi alterado pelo usuário no aplicativo e deve ser salvo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f605-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="0f605-236">Se o desempenho for uma preocupação, esse método pode ser simplificado para que ele sempre retorne **true**.</span><span class="sxs-lookup"><span data-stu-id="0f605-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="0f605-237">Os métodos **populateTimesheetLineFromEntryDuringCreate** e **populateTimesheetLineFromEntryDuringUpdate** podem ser estendidos para que eles insiram valores no registro do banco de dados TSTimesheetLine a partir do registro do contrato de dados que é fornecido.</span><span class="sxs-lookup"><span data-stu-id="0f605-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="0f605-238">No exemplo a seguir, observe como o mapeamento entre o campo do banco de dados e o campo de entrada é feito manualmente por meio de código X++.</span><span class="sxs-lookup"><span data-stu-id="0f605-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="0f605-239">O método **populateTimesheetWeekFromEntry** também poderá ser estendido se o campo personalizado que é mapeado para o objeto **TSTimesheetEntry** tiver que gravar de volta na tabela TSTimesheetLineweek do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f605-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="0f605-240">O exemplo a seguir salva o valor de **firstOption** ou de **secondOption** que o usuário selecionar no banco de dados como um valor de cadeia de caracteres bruto.</span><span class="sxs-lookup"><span data-stu-id="0f605-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="0f605-241">Se o campo do banco de dados for um campo do tipo **Enumeração**, esses valores podem ser mapeados manualmente para um valor de enumeração e depois salvos no campo de enumeração na tabela do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f605-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="0f605-242">Mostrar um campo personalizado na seção do cabeçalho da folha de ponto</span><span class="sxs-lookup"><span data-stu-id="0f605-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="0f605-243">Abaixo encontra-se uma captura de tela do aplicativo móvel de um usuário exibindo uma folha de ponto.</span><span class="sxs-lookup"><span data-stu-id="0f605-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="0f605-244">O botão "Mais informações" foi selecionado no canto superior direito para mostrar a opção "Exibir mais detalhes".</span><span class="sxs-lookup"><span data-stu-id="0f605-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Comando Exibir mais detalhes](media/show-more.png)

<span data-ttu-id="0f605-246">Abaixo encontra-se uma captura de tela do aplicativo móvel exibindo a seção "Mais" de uma folha de ponto.</span><span class="sxs-lookup"><span data-stu-id="0f605-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="0f605-247">Um campo personalizado chamado "Taxa de utilização desta folha de ponto (campo personalizado calculado) foi adicionado à seção do cabeçalho da folha de ponto.</span><span class="sxs-lookup"><span data-stu-id="0f605-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="0f605-248">Um valor somente leitura de "0,667" é definido no campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="0f605-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Seção Mais](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="0f605-250">Estender a tabela TSTimesheetTable para que ela tenha um campo personalizado</span><span class="sxs-lookup"><span data-stu-id="0f605-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="0f605-251">Em cenários típicos, é provável que os dados de um campo personalizado na seção do cabeçalho sejam extraídos da tabela TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="0f605-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="0f605-252">No entanto, outras tables podem ser usadas se os dados puderem se recuperados com base em um registro de TSTimesheetTable que seja fornecido, ou se não tiverem um contexto de registro específico (por exemplo, se o campo for definido como somente leitura nos parâmetros do projeto).</span><span class="sxs-lookup"><span data-stu-id="0f605-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="0f605-253">Observe que os campos personalizados não têm nenhum registro de banco de dados de backup.</span><span class="sxs-lookup"><span data-stu-id="0f605-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="0f605-254">Eles podem ser gerados dinamicamente com base na lógica de X++.</span><span class="sxs-lookup"><span data-stu-id="0f605-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="0f605-255">O exemplo a seguir mostra essa abordagem.</span><span class="sxs-lookup"><span data-stu-id="0f605-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="0f605-256">Os campos na seção do cabeçalho são sempre somente leitura no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="0f605-257">Usar a cadeia de comando no método buildCustomFieldList da classe TSTimesheetSettings para mostrar um campo na seção do cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0f605-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="0f605-258">Esse código controla as configurações de exibição do campo no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="0f605-259">Por exemplo, ele controla o tipo de campo, o rótulo, se o campo é obrigatório e em qual seção o campo é exibido.</span><span class="sxs-lookup"><span data-stu-id="0f605-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="0f605-260">O exemplo a seguir mostra um valor calculado na seção do cabeçalho no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="0f605-261">Usar a cadeia de comando no método buildCustomFieldListForHeader da classe TSTimesheetDetails para preencher os detalhes em uma folha de ponto</span><span class="sxs-lookup"><span data-stu-id="0f605-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="0f605-262">O método **buildCustomFieldListForHeader** é usado para preencher os detalhes do cabeçalho em uma folha de ponto no aplicativo móvel.</span><span class="sxs-lookup"><span data-stu-id="0f605-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="0f605-263">Ele pega um registro de TSTimesheetTable como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0f605-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="0f605-264">Campos desse registro podem ser usados para preencher o valor do campo personalizado no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="0f605-265">O exemplo a seguir não lê qualquer valor do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f605-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="0f605-266">Em vez disso, ele usa a lógica de X++ para gerar uma valor calculado que então é exibido no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f605-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="0f605-267">Outras oportunidades de capacidade de configuração/extensão</span><span class="sxs-lookup"><span data-stu-id="0f605-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="0f605-268">Adicionando outras validações para o aplicativo</span><span class="sxs-lookup"><span data-stu-id="0f605-268">Adding additional validation for the app</span></span>

<span data-ttu-id="0f605-269">A lógica existente para a funcionalidade de folha de ponto no nível do banco de dados funcionará como o esperado.</span><span class="sxs-lookup"><span data-stu-id="0f605-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="0f605-270">Para interromper a conclusão de operações de salvamento ou envio e exibir uma mensagem de erro específica, você pode adicionar **throw error("mensagem para o usuário")** ao código por meio de uma extensão de cadeia de comando.</span><span class="sxs-lookup"><span data-stu-id="0f605-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="0f605-271">Veja três exemplos de métodos extensíveis úteis:</span><span class="sxs-lookup"><span data-stu-id="0f605-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="0f605-272">Se **validateWrite** na tabela TSTimesheetLine retornar **false** durante uma operação de salvamento de uma linha da folha de ponto, uma mensagem de erro será exibida no aplicativo móvel.</span><span class="sxs-lookup"><span data-stu-id="0f605-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="0f605-273">Se **validateSubmit** na tabela TSTimesheetTable retornar **false** durante uma operação de envio no aplicativo, uma mensagem de erro será exibida ao usuário.</span><span class="sxs-lookup"><span data-stu-id="0f605-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="0f605-274">A lógica que preenche os campos (por exemplo, **Line Property**) durante o método **insert** na tabela TSTimesheetLine ainda será executado.</span><span class="sxs-lookup"><span data-stu-id="0f605-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="0f605-275">Ocultando e marcando campos prontos para uso como somente leitura por meio de configuração</span><span class="sxs-lookup"><span data-stu-id="0f605-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="0f605-276">Nos parâmetros do projeto, você pode tornar campos prontos para uso em somente leitura ou em campos ocultos no aplicativo móvel.</span><span class="sxs-lookup"><span data-stu-id="0f605-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="0f605-277">Defina as opções na seção **Folhas de ponto móveis** na guia **Folhas de ponto** da página **Parâmetros de gerenciamento e contabilidade de projeto**.</span><span class="sxs-lookup"><span data-stu-id="0f605-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parâmetros do projeto](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="0f605-279">Alterar as atividades disponíveis para seleção por meio de extensões</span><span class="sxs-lookup"><span data-stu-id="0f605-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="0f605-280">As atividades disponíveis para seleção de um projeto são preenchidas por meio dos métodos **getActivitiesForProject()** e **getActivityQuery()** na classe **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="0f605-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="0f605-281">Você pode usar a cadeia de comando para alterar esse comportamento para corresponder ao seu cenário comercial para as atividades que estão disponíveis para seleção para um projeto específico.</span><span class="sxs-lookup"><span data-stu-id="0f605-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="0f605-282">Inserindo uma categoria de projeto padrão nas entradas de folha de ponto</span><span class="sxs-lookup"><span data-stu-id="0f605-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="0f605-283">A entrada de uma categoria de projeto padrão nas entradas de o quadro de folha de ponto ocorre em três níveis.</span><span class="sxs-lookup"><span data-stu-id="0f605-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="0f605-284">Você pode usar a cadeia de comando para estender o comportamento em qualquer um ou todos esses níveis para atingir o comportamento desejado.</span><span class="sxs-lookup"><span data-stu-id="0f605-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="0f605-285">A seguinte hierarquia é usada:</span><span class="sxs-lookup"><span data-stu-id="0f605-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="0f605-286">O aplicativo tenta colocar a categoria padrão a partir do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="0f605-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="0f605-287">Essa categoria padrão é definida nos métodos **getCurrentUserResource** e **getDelegatedResourcesForCurrentUser** na classe **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="0f605-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="0f605-288">Se a categoria padrão não for fornecida no nível do recurso do projeto, o aplicativo tentará extraí-la da atividade do projeto.</span><span class="sxs-lookup"><span data-stu-id="0f605-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="0f605-289">Esta categoria padrão é definida no método **getActivitiesForProject** na classe **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="0f605-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="0f605-290">Se a categoria padrão não for fornecida no nível da atividade do projeto, a categoria padrão será extraída dos parâmetros do projeto.</span><span class="sxs-lookup"><span data-stu-id="0f605-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="0f605-291">Essa categoria padrão é definida no método **getProjectDetailsbyRule** na classe **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="0f605-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
