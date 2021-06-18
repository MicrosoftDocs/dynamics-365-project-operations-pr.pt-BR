---
title: Pedidos de vendas de projetos para projetos de tempo e material
description: Este tópico explica como criar pedidos de venda com base em projeto para projetos de tempo e material.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009647"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="a73ba-103">Pedidos de vendas de projetos para projetos de tempo e material</span><span class="sxs-lookup"><span data-stu-id="a73ba-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a73ba-104">Este tópico descreve como criar uma ordem de vendas para um projeto.</span><span class="sxs-lookup"><span data-stu-id="a73ba-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="a73ba-105">Pedidos de venda só podem ser criados para projetos do tipo **tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="a73ba-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="a73ba-106">Se um projeto de tempo e material tem várias fontes de financiamento no contrato de projeto, você deve habilitar o parâmetro **Permitir pedidos de vendas para projetos com várias fontes de financiamento** na página **Parâmetros de gerenciamento e contabilidade de projeto**.</span><span class="sxs-lookup"><span data-stu-id="a73ba-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="a73ba-107">O suporte para pedidos de vendas de projetos com várias fontes de financiamento está disponível a partir do aplicativo versão 10.0.2 e superior.</span><span class="sxs-lookup"><span data-stu-id="a73ba-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="a73ba-108">O parâmetro para habilitar o suporte para pedidos de vendas de projetos com várias fontes de financiamento será removido na onda de lançamento de abril de 2020, após a qual a funcionalidade estará sempre habilitada.</span><span class="sxs-lookup"><span data-stu-id="a73ba-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="a73ba-109">Você pode criar pedidos de venda baseados em projeto de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="a73ba-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="a73ba-110">Vá para o próprio projeto.</span><span class="sxs-lookup"><span data-stu-id="a73ba-110">Go to the project itself.</span></span> <span data-ttu-id="a73ba-111">No Painel de Ação, selecione **Gerenciar > Tarefas de item> Pedido de venda**.</span><span class="sxs-lookup"><span data-stu-id="a73ba-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="a73ba-112">As informações do projeto serão padronizadas para o pedido de venda do projeto.</span><span class="sxs-lookup"><span data-stu-id="a73ba-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="a73ba-113">Se o contrato do projeto tiver mais de uma fonte de financiamento, você precisará selecionar a fonte de financiamento para definir o cliente para o pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="a73ba-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="a73ba-114">Se houver apenas uma fonte de financiamento para o projeto, o cliente será definido automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a73ba-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="a73ba-115">Vá para a página de lista **Todos os pedidos de vendas** e crie um novo pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="a73ba-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="a73ba-116">Você precisará selecionar o projeto para o pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="a73ba-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="a73ba-117">Depois que o projeto for selecionado, o cliente será definido a partir da fonte de financiamento ou você precisará selecionar a fonte de financiamento se o contrato do projeto tiver várias fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="a73ba-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]