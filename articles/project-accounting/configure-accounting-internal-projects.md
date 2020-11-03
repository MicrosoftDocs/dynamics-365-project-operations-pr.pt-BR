---
title: Configurar contabilidade para projetos internos
description: Este tópico fornece informações sobre como configurar práticas de contabilidade para projetos internos no Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071362"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="8cd36-103">Configurar contabilidade para projetos internos</span><span class="sxs-lookup"><span data-stu-id="8cd36-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="8cd36-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="8cd36-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8cd36-105">Os projetos internos permitem que as empresas rastreiem os custos relacionados às atividades que não estão sendo cobradas de um cliente.</span><span class="sxs-lookup"><span data-stu-id="8cd36-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="8cd36-106">Exemplos de projetos internos incluem:</span><span class="sxs-lookup"><span data-stu-id="8cd36-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="8cd36-107">Desenvolver um produto, como um aplicativo móvel, e monitorar o custo associado ao desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="8cd36-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="8cd36-108">Gerenciamento do tempo e de despesas de pré-venda.</span><span class="sxs-lookup"><span data-stu-id="8cd36-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="8cd36-109">Este projeto interno de pré-venda pode ser convertido posteriormente em um projeto faturável se a cotação for ganha.</span><span class="sxs-lookup"><span data-stu-id="8cd36-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="8cd36-110">Qualquer projeto não associado a um contrato no Dynamics 365 Project Operations é tratado como interno.</span><span class="sxs-lookup"><span data-stu-id="8cd36-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="8cd36-111">Os perfis de custo e de receita do projeto não são usados para determinar as regras de contabilidade para o projeto.</span><span class="sxs-lookup"><span data-stu-id="8cd36-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="8cd36-112">O custo interno do projeto é sempre lançado usando os princípios de lucros e perdas.</span><span class="sxs-lookup"><span data-stu-id="8cd36-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="8cd36-113">As contas contábeis para lançamentos são definidas na página **Configuração de lançamento do razão**.</span><span class="sxs-lookup"><span data-stu-id="8cd36-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="8cd36-114">As transações de tempo são lançadas por meio de débito da conta **Custo** e crédito na conta **Alocação de folha de pagamento**.</span><span class="sxs-lookup"><span data-stu-id="8cd36-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="8cd36-115">As transações de despesas são lançadas por meio de débito na conta **Custo** e crédito na conta **Contrapartida para despesas**.</span><span class="sxs-lookup"><span data-stu-id="8cd36-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="8cd36-116">Depois que as transações forem lançadas no projeto, se o projeto estiver associado a um contrato de projeto, o sistema reverterá todas as transações acumuladas e criará novas transações faturáveis.</span><span class="sxs-lookup"><span data-stu-id="8cd36-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="8cd36-117">As transações faturáveis seguem as regras de contabilidade definidas no respectivo perfil Custo e receita de projeto.</span><span class="sxs-lookup"><span data-stu-id="8cd36-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


