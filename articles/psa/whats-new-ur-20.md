---
title: Novidades ou alterações na Versão de Atualização 20 do Project Service Automation V3
description: Este tópico lista os recursos e as correções disponíveis na Versão de Atualização 20 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071377"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="3b008-103">Versão de Atualização 20, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="3b008-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="3b008-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3b008-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3b008-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="3b008-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3b008-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3b008-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3b008-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="3b008-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3b008-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3b008-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3b008-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 20.</span><span class="sxs-lookup"><span data-stu-id="3b008-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="3b008-110">Esta versão apresenta o número de compilação V 3.10.31.37 e está disponível para o público em geral por meio de uma atualização automática em junho de 2020.</span><span class="sxs-lookup"><span data-stu-id="3b008-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="3b008-111">Versão de Atualização 20</span><span class="sxs-lookup"><span data-stu-id="3b008-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3b008-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="3b008-112">Bug fixes</span></span>

<span data-ttu-id="3b008-113">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="3b008-113">**Project Management**</span></span>

<span data-ttu-id="3b008-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="3b008-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3b008-115">A importação de membros da equipe do projeto com um método de alocação que requer horas resulta em uma mensagem de erro pouco clara quando as horas especificadas são zero.</span><span class="sxs-lookup"><span data-stu-id="3b008-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="3b008-116">Os usuários recebem um erro incorreto quando o número máximo de caracteres foi inserido no campo **Descrição** para uma tarefa do projeto.</span><span class="sxs-lookup"><span data-stu-id="3b008-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="3b008-117">A página de **download do suplemento do Microsoft Dynamics 365 Project Service Automation** redireciona para a página de download em inglês quando as configurações de idioma do usuário estão definidas como japonês.</span><span class="sxs-lookup"><span data-stu-id="3b008-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="3b008-118">Quando ocorre um erro no servidor, o rótulo de sincronização na guia **Agenda** do formulário **Projetos** às vezes permanece.</span><span class="sxs-lookup"><span data-stu-id="3b008-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="3b008-119">Atualizações redundantes de tarefas estão sendo enviadas ao servidor quando uma tarefa é modificada.</span><span class="sxs-lookup"><span data-stu-id="3b008-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="3b008-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3b008-120">**Sales**</span></span>

<span data-ttu-id="3b008-121">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="3b008-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="3b008-122">No formulário **Contrato** , clicar duas vezes em **Criar recibo** cria duas faturas para um único registro de dados reais.</span><span class="sxs-lookup"><span data-stu-id="3b008-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="3b008-123">No Internet Explorer 11, os usuários não conseguem criar entradas de despesas.</span><span class="sxs-lookup"><span data-stu-id="3b008-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="3b008-124">A Reversão de Custo e a reversão de Dados Reais de Vendas não Faturadas não estão vinculadas.</span><span class="sxs-lookup"><span data-stu-id="3b008-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="3b008-125">O botão **Atualizar Dados Reais** no formulário **Projeto** não atualiza **Horas Reais da Tarefa**.</span><span class="sxs-lookup"><span data-stu-id="3b008-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="3b008-126">O plug-in **PreValidateProjectTeamMemberCreate** pode criar recursos reserváveis genéricos duplicados quando o atributo **msdyn_isgenericresourceprojectscoped** está definido como **Falso**.</span><span class="sxs-lookup"><span data-stu-id="3b008-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="3b008-127">**Recalcular** limpa os custos passíveis de cobrança dos detalhes da linha de cotação baseadas em produto e dos detalhes da linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="3b008-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="3b008-128">Em cenários específicos, o plug-in **PostEstimateLineUpdate** exibe um erro de exceção de referência nula.</span><span class="sxs-lookup"><span data-stu-id="3b008-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="3b008-129">A duração da fase de tempo no **Gráfico de Análise de Lucratividade** não corresponde à duração dos custos nos detalhes da linha de cotação de preço fixo da cotação.</span><span class="sxs-lookup"><span data-stu-id="3b008-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="3b008-130">Os valores da unidade e do grupo de unidades não são padronizados corretamente para as categorias de despesas nos formulários **Detalhes da Linha do Contrato** e **Detalhes da Linha de Cotação**.</span><span class="sxs-lookup"><span data-stu-id="3b008-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="3b008-131">As listas de **Preço de Custo Unitário da Organização** permitem sobreposições na data efetiva.</span><span class="sxs-lookup"><span data-stu-id="3b008-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="3b008-132">Os usuários não têm permissão para alterar **OrgUnit** quando o tipo de ordem não for baseado no trabalho, pois levará a um erro de exceção de referência nula.</span><span class="sxs-lookup"><span data-stu-id="3b008-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="3b008-133">Ao tentar navegar do formulário **Detalhes da Linha de Cotação** de volta à guia **Cotação** , o formulário é atualizado e exibe a guia **Resumo**.</span><span class="sxs-lookup"><span data-stu-id="3b008-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
