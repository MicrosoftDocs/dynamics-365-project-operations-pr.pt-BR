---
title: Determinar o tipo de implantação
description: Este tópico fornece informações para ajudar a determinar o tipo de implantação correto do Project Operations para a sua empresa.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071432"
---
# <a name="determine-your-deployment-type"></a>Determinar o tipo de implantação

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

> [!IMPORTANT]
> Após comprar a licença, comece aqui para determinar o melhor modelo de implantação do Dynamics 365 Project Operations usando o [Fluxo de instalação guiada](https://aka.ms/provisionprojectoperations).
> Depois de concluir o Fluxo de instalação guiada, você será direcionado para o portal de gerenciamento correto para concluir a instalação. Veja os detalhes de implantação para concluir a instalação.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clientes existentes de Dynamics usando Dynamics 365 Project Service Automation
O Project Operations inclui as funcionalidades fornecidas com o Project Service Automation. Um caminho de atualização será lançado para esses clientes no futuro.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clientes existentes do Dynamics 365 Finance usando o Gerenciamento e contabilidade de projeto 

Os clientes existentes do Finance que usam a funcionalidade Gerenciamento e contabilidade de projeto podem continuar usando-a como tal. Consulte [Project Operations para cenários de pedido baseado em estoque/produção](#pma).


## <a name="deployment-types"></a>Tipos de implantação
O Project Operations oferece suporte a várias opções de implantação para atender aos seus requisitos. Seja você um cliente novo ou existente do Dynamics 365, o Project Operations pode dar suporte às suas necessidades.

Nosso [Questionário de implantação](https://aka.ms/provisionprojectoperations) ajudará você a determinar a implantação correta. Os resultados guiarão você para um dos seguintes tipos de implantação:

- [Implantação lite - gerenciar faturamento pro forma](#lite)
- [Project Operations para cenários baseados em recursos/itens sem estoque](#integrated)
- [Project Operations para cenários de pedido baseado em estoque/produção](#pma)

O Project Operations oferece suporte a cenários com estoque/ordem de produção e cenários baseados em recursos/sem estoque no mesmo ambiente por meio de configurações no nível de entidade legal. Por exemplo, a Contoso pode usar os recursos de pedido baseado em estoque/produção em instalações de manufatura nos EUA (entidade legal = Contoso Manufacturing Estados Unidos). A Contoso pode usar os recursos não estocados/baseados em recursos em instalações de serviço da Contoso Robotics Arms no Reino Unido (entidade legal = Contoso Robotics Reino Unido).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Implantação lite - gerenciar faturamento pro forma

A implantação lite inclui as seguintes funcionalidades:

- Planejamento de projetos usando Microsoft Project para a Web
- Precificação multidimensional
- Gerenciamento Unificado de Recursos
- Controle de horas
- Despesa Básica
- Proposta de Fatura

#### <a name="deployment-steps"></a>Etapas de implantação
Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).

Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](lite-preview-subscription-sign-up.md) e [Provisionar novo ambiente](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations para cenários baseados em recursos/itens sem estoque
O Project Operations para cenários de recursos/sem estoque inclui as seguintes funcionalidades:
  
- Planejamento de projetos usando Microsoft Project para a Web
- Precificação multidimensional
- Gerenciamento Unificado de Recursos
- Controle de horas
- Despesa Básica
- Despesa total
- OCR de recibo
- Faturamento Completo
- Reconhecimento de Receita

#### <a name="deployment-steps"></a>Etapas de implantação
Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).

Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](resource-sign-up-preview-subscription.md) e [Provisionar novo ambiente](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations para cenários de pedido baseado em estoque/produção

- Planejamento de projeto usando WBS
- Gerenciamento de Recursos
- Controle de horas
- Despesa total
- OCR de recibo
- Faturamento Completo
- Reconhecimento de Receita
- Ordens de Produção
- Suporte a materiais

#### <a name="deployment-steps"></a>Etapas de implantação
Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).

Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Provisionar novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

