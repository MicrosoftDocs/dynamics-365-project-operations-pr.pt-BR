---
title: Criar entrada de hora
description: Esse tópico fornece informações sobre como criar entradas de hora.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
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
ms.openlocfilehash: 8f86f69090e869bf5e6a7505a4cb1ad1c69b475b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282139"
---
# <a name="create-time-entries"></a><span data-ttu-id="2a3a2-103">Criar entrada de hora</span><span class="sxs-lookup"><span data-stu-id="2a3a2-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2a3a2-104">Em versões anteriores do Dynamics 365 Project Service Automation, as entradas de hora eram inseridas semanalmente.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="2a3a2-105">Na versão 3 do Project Service Automation, as entradas de hora são inseridas diariamente.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="2a3a2-106">No entanto, após algumas entradas terem sido criadas, é possível criar em massa ou copiá-las.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="2a3a2-107">Criar entrada de hora</span><span class="sxs-lookup"><span data-stu-id="2a3a2-107">Create a time entry</span></span>

<span data-ttu-id="2a3a2-108">Siga as etapas para criar uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="2a3a2-109">Na página **Entradas de hora**, selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="2a3a2-110">Na caixa de diálogo **Criação rápida: Entrada de hora**, insira a duração da entrada de hora em minutos, horas ou dias.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="2a3a2-111">A duração deve ser inserida no seguinte formato: *x* minutos, *x* horas ou *x* dias.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="2a3a2-112">As horas e os dias também podem ser inseridos usando decimais, como *x,x* horas ou *x,x* dias.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="2a3a2-113">Selecione o tipo de entrada de hora e o projeto no qual você está inserido a entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="2a3a2-114">No campo **Tarefa do projeto**, localize a tarefa para essa entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2a3a2-115">Se estiver criando uma entrada de hora para uma tarefa que não foi atribuída a um usuário, no campo **Tarefa do projeto**, selecione o botão **Pesquisar**, selecione **Alterar exibição** e depois **Todas as tarefas de projeto ativas** para listar todas as tarefas.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="2a3a2-116">Insira uma descrição, se necessário, e selecione **Salvar e fechar**.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="2a3a2-117">Após criar e salvar a entrada de hora, você pode editá-la na grade de entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="2a3a2-118">A grade de entrada de hora é compatível com dois formatos:</span><span class="sxs-lookup"><span data-stu-id="2a3a2-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="2a3a2-119">Você pode inserir entradas de hora no formato **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="2a3a2-120">Esse formato será convertido em horas e frações.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="2a3a2-121">Você pode inserir horas e frações diretamente.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="2a3a2-122">Observe que as frações de uma hora não são minutos.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="2a3a2-123">Portanto, 1,5 representa 1 hora e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="2a3a2-124">A mesma regra é aplicada a frações de um dia.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="2a3a2-125">Um dia é 24 horas e 0,5 dias representa 12 horas.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="2a3a2-126">Criar entradas de hora em massa</span><span class="sxs-lookup"><span data-stu-id="2a3a2-126">Bulk create time entries</span></span>

<span data-ttu-id="2a3a2-127">Após criar algumas entradas de hora, é possível copiá-las para criar entradas de hora adicionais em massa.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="2a3a2-128">Na página **Entradas de hora**, selecione **Copiar semana**.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="2a3a2-129">No grupo de campo **No período** nos campos **Data de início** e **Data de término**, defina o intervalo de datas que será usado para copiar as entradas.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="2a3a2-130">No grupo de campo **Até o período** no campo **Data de início**, especifique a data usada para criar as entradas de hora.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="2a3a2-131">Selecione **Cópia** para criar uma cópia das entradas de hora que correspondem ao dia da semana especificado no grupo de campo **Até o período**.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="2a3a2-132">Por exemplo, a entrada de hora para segunda-feira da semana passada é copiada para a segunda-feira da semana especificada no grupo de campo **Até o período**.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="2a3a2-133">Importar dados para entradas de hora</span><span class="sxs-lookup"><span data-stu-id="2a3a2-133">Import data for time entries</span></span>

<span data-ttu-id="2a3a2-134">Você pode importar dados de reservas e atribuições de projetos.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="2a3a2-135">Ao importar dados, é possível especificar o intervalo de datas das reservas a ser importado e, em seguida, explicitamente selecionar as reservas que devem ser criadas como entradas de hora **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="2a3a2-136">Recursos para agrupar por, classificar, pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="2a3a2-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="2a3a2-137">Você pode agrupar e filtrar as entradas de hora pelas dimensões especificadas nas colunas.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="2a3a2-138">No campo **Agrupar por**. selecione a dimensão a ser usada para filtrar as entradas de hora.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="2a3a2-139">Você também pode classificar os registros de entrada de hora em ordem crescente ou decrescente usando a seta de classificação nos cabeçalhos de coluna.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="2a3a2-140">Além disso, é possível mostrar ou ocultar entradas selecionando-se o botão **Filtrar** nos cabeçalhos de colunas e, em seguida, na caixa **Pesquisar**, inserindo o texto que deve ser usado para pesquisar entradas de hora por nome de projeto, tarefa de projeto, entrada de hora ou recurso.</span><span class="sxs-lookup"><span data-stu-id="2a3a2-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]