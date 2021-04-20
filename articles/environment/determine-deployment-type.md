---
title: Determinar o tipo de implantação
description: Este tópico fornece informações para ajudar a determinar o tipo de implantação correto do Project Operations para a sua empresa.
author: stsporen
manager: Annbe
ms.date: 03/15/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 715b117cae5418fc743ea870772278450fff5ae9
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663580"
---
# <a name="determine-your-deployment-type"></a>Determinar o tipo de implantação

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

> [!IMPORTANT]
> Após comprar a licença, comece aqui para determinar o melhor modelo de implantação do Dynamics 365 Project Operations usando o [Fluxo de instalação guiada](https://aka.ms/provisionprojectoperations).
> Depois de concluir o Fluxo de instalação guiada, você será direcionado para o portal de gerenciamento correto para concluir a instalação. Veja os detalhes de implantação para concluir a instalação.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clientes existentes de Dynamics usando Dynamics 365 Project Service Automation
O Project Operations inclui as funcionalidades fornecidas com o Project Service Automation. Um caminho de atualização será lançado para esses clientes no ciclo de lançamentos 1 de 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clientes existentes do Dynamics 365 Finance usando o Gerenciamento e contabilidade de projeto 

Os clientes existentes do Finance que usam a funcionalidade de gerenciamento e contabilidade de projeto podem continuar usando-a da mesma forma. Consulte [Project Operations para cenários de pedido baseado em estoque/produção](#pma).


## <a name="deployment-regions"></a>Regiões da implantação
Para determinar quais regiões oferecem suporte à implantação do Project Operations, consulte [Disponibilidade geográfica do Dynamics 365 e relatório do Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Selecione **Exibir Relatório** e expanda **Dynamics 365 > Aplicativos de Operações > Dynamics 365 Project Operations** para exibir as regiões compatíveis.

## <a name="deployment-types"></a>Tipos de implantação
O Project Operations oferece suporte a várias opções de implantação para atender aos seus requisitos. Seja você um cliente novo ou existente do Dynamics 365, o Project Operations pode dar suporte às suas necessidades.

Nosso [Questionário de implantação](https://aka.ms/provisionprojectoperations) ajudará você a determinar a implantação correta. Os resultados guiarão você para um dos seguintes tipos de implantação:

- [Implantação lite - gerenciar faturamento pro forma](#lite)
- [Project Operations para cenários baseados em recursos/itens sem estoque](#integrated)
- [Project Operations para cenários de pedido baseado em estoque/produção](#pma)

O Project Operations oferece suporte a cenários com estoque/ordem de produção e cenários baseados em recursos/sem estoque no mesmo ambiente por meio de configurações no nível de entidade legal. Por exemplo, Contoso pode usar os recursos em estoque/ordem de produção em sua fábrica nos EUA (entidade legal = Contoso Fabricação nos Estados Unidos). Contoso pode usar os recursos não estocados/sem estoque na instalação de atendimento Contoso Robotics Arms no Reino Unido (entidade legal = Contoso Robotics - Reino Unido).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Implantação lite – gerenciar faturamento pro forma

A implantação lite inclui as seguintes funcionalidades:

- Processo de vendas para projetos que estende as experiências do aplicativo Dynamics 365 Sales
- Planejamento de projetos usando Microsoft Project para a Web
- Precificação multidimensional
- Gerenciamento unificado de recursos
- Controle de horas
- Despesa básica
- Faturamento pro-forma para revisão e edição do gerente do Projeto 

#### <a name="deployment-steps"></a>Etapas de implantação
Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).

Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](lite-preview-subscription-sign-up.md) e [Provisionar novo ambiente](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations para cenários baseados em recursos/itens sem estoque
O Project Operations para cenários de recursos/sem estoque inclui as seguintes funcionalidades:
 
- Processo de vendas para projetos que estende o aplicativo Dynamics 365 Sales
- Planejamento de projetos usando Microsoft Project para a Web
- Precificação multidimensional
- Gerenciamento unificado de recursos
- Controle de horas
- Despesa básica
- Despesa total
- OCR de recibo
- Faturamento pro forma e voltado ao cliente 
- Reconhecimento de receita para projetos

#### <a name="deployment-steps"></a>Etapas de implantação
Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).

Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](resource-sign-up-preview-subscription.md) e [Provisionar novo ambiente](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations para cenários de pedido baseado em estoque/produção

- Planejamento de projeto usando WBS
- Gerenciamento de recursos
- Controle de horas
- Despesa total
- OCR de recibo
- Faturamento completo
- Reconhecimento de receita
- Ordens de produção
- Suporte de materiais estocados com estoque

#### <a name="deployment-steps"></a>Etapas de implantação
Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).

Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Provisionar novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
