---
title: Sincronizar contratos de projeto e projetos diretamente do Project Service Automation para o Finance
description: Este tópico descreve o modelo e as tarefas subjacentes usadas para sincronizar contratos de projeto e projetos diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85722f61a672cc55cd2b511dc80ebfbe4807b957
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950385"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Sincronizar contratos de projeto e projetos diretamente do Project Service Automation para o Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tópico descreve o modelo e as tarefas subjacentes usadas para sincronizar contratos de projeto e projetos diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.

> [!NOTE] 
> Se estiver usando o Enterprise Edition 7.3.0, você precisará instalar o KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de dados do Project Service Automation para o Finance

> [!NOTE]
> Para usar a solução de integração do Project Service Automation para o Finance, familiarize-se primeiro com o recurso de integração de dados do Dynamics 365.

A solução de integração do Project Service Automation ao Finance usa o recurso de integração de dados para sincronizar dados entre instâncias do Project Service Automation e do Finance. O modelo de integração disponível com o recurso de integração de dados permite transferir dados sobre contratos de projeto, projetos, linhas de contrato de projetos e respectivas etapas do Project Service Automation para o Finance.

A ilustração a seguir mostra como os dados são sincronizados entre o Project Service Automation e o Finance.

[![Fluxo de dados para a integração do Project Service Automation ao Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Modelos e tarefas

Para acessar os modelos disponíveis, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.

Os seguintes modelos e as tarefas subjacentes são usados para sincronizar contratos de projeto e projetos do Project Service Automation para o Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integração com o Dynamics 365 Project Service Automation v2.x
- **Nome do modelo na integração de dados:** Projetos e contratos (Project Service Automation para o Finance)
- **Nome das tarefas no projeto:**

    - Contratos de projeto Project Service Automation para o Finance
    - Projetos Project Service Automation para o Finance
    - Linhas de contrato do projeto Project Service Automation para o Finance
    - Marcos de linhas de contrato do projeto Project Service Automation para o Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integração com o Dynamics 365 Project Service Automation v3.x
Há uma alteração de esquema no Project Service Automation que impacta o modelo de etapas de linhas de contrato de projeto, e o uso da versão v2 do modelo é obrigatório para integrar o Project Service Automation v3.x ao Dynamics 365.

- **Nome do modelo na integração de dados:** Projetos e contratos (Project Service Automation 3.x para o Finance) - v2
- **Nome das tarefas no projeto:**

    - Contratos de projeto Project Service Automation para o Finance
    - Projetos Project Service Automation para o Finance
    - Linhas de contrato do projeto Project Service Automation para o Finance
    - Marcos de linhas de contrato do projeto Project Service Automation para o Finance

É necessário primeiro sincronizar as contas para que ocorra a sincronização de contratos de projeto e projetos.

## <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation       | Financeiro                                                |
|----------------------------------|--------------------------------------------------------|
| Pedidos                           | Entidade de integração para contrato de projeto                |
| Projetos                         | Entidade de integração para projeto                         |
| Linhas da ordem                      | Entidade de integração para linha de contrato de projeto           |
| Etapas da linha de contrato de projeto | Entidade de integração para etapa de linha de contrato de projeto |

## <a name="entity-flow"></a>Fluxo da entidade

Os contratos de projeto são gerenciados no Project Service Automation e são sincronizados com o Finance como contratos de projeto. Como parte do modelo de integração, você pode definir a origem de integração no Finance para o contrato de projeto.

Projetos de tempo, material e preço fixo são gerenciados no Project Service Automation e sincronizados com o Finance como projetos. Como parte da integração do modelo, você pode definir a origem de integração do projeto no Finance. Atualmente, apenas projetos de tempo e material e de preço fixo são compatíveis.


As linhas de contrato de projeto são gerenciadas no Project Service Automation e são sincronizadas com o Finance como regras de cobrança de contrato de projeto. Se o método de cobrança for diferente do tipo de projeto padrão, a sincronização atualiza o tipo de projeto para o projeto de linha de contrato e grupo de projetos.

As etapas de linhas de contrato de projeto são gerenciados no Project Service Automation e são sincronizadas com o Finance como etapas de regras de cobrança de contrato de projeto.

## <a name="project-service-automation-to-finance-integration-solution"></a>Solução de integração do Project Service Automation ao Finance

O campo **ID do contrato de projeto** está disponível na página **Contratos de projeto**. Esse campo se tornou uma chave natural e única para dar suporte à integração.

Quando um novo contrato de projeto é criado, se ainda não existir um valor de **ID do contrato de projeto**, ele será gerado automaticamente usando uma sequência numérica. O valor consiste em **ORD** seguido por uma sequência numérica crescente e um sufixo de seis caracteres. Veja um exemplo: **ORD-01022-Z4M9Q0**.

O campo **Número do projeto** está disponível na página **Projetos**. Esse campo se tornou uma chave natural e única para dar suporte à integração.

Quando um novo contrato de projeto é criado, se ainda não existir um valor de **Número do projeto**, ele será gerado automaticamente usando uma sequência numérica. O valor consiste em **PRJ** seguido por uma sequência numérica crescente e um sufixo de seis caracteres. Veja um exemplo: **PRJ-01049-CCNID0**.

Quando a solução de integração do Project Service Automation ao Finance é aplicada, um script de atualização define o campo **ID do contrato de projeto** para contratos de projeto existentes e o campo **Número do projeto** para projetos existentes no Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Pré-requisitos e configuração de mapeamento

- É necessário primeiro sincronizar as contas para que ocorra a sincronização de contratos de projeto e projetos.
- No conjunto de conexões, adicione um mapeamento de campo-chave de integração de **msdyn\_organizationalunits** para **msdyn\_name \[Name\]**. Talvez antes seja necessário adicionar um projeto ao conjunto de conexões. Para mais informações, consulte [Integrar dados no Common Data Service para Aplicativos](/powerapps/administrator/data-integrator).
- No conjunto de conexões, adicione um mapeamento de campo-chave de integração de **msdyn\_projects** para **msdynce\_projectnumber \[Project Number\]**. Talvez antes seja necessário adicionar um projeto ao conjunto de conexões. Para mais informações, consulte [Integrar dados no Common Data Service para Aplicativos](/powerapps/administrator/data-integrator).
- O campo **SourceDataID** para contratos de projeto e projetos pode ser atualizado com um valor diferente ou ser removido do mapeamento. O valor padrão do modelo é **Project Service Automation**.
- O mapeamento de **PaymentTerms** deve ser atualizado para refletir os termos válidos de pagamento no Finance. Você também pode remover o mapeamento da tarefa do projeto. O mapa de valores padrão possui valores padrão para dados de demonstração. A tabela a seguir mostra os valores no Project Service Automation.

    | Valor | Descrição   |
    |-------|---------------|
    | 0     | Líquido 30        |
    | 2     | 2% 10, Líquido 30 |
    | 3     | Líquido 45        |
    | 4     | Líquido 60        |

## <a name="power-query"></a>Power Query

Use o Microsoft Power Query para Excel para filtrar dados se as seguintes condições forem atendidas:

- Você tem pedidos de venda no Dynamics 365 Sales.
- Você tem várias unidades organizacionais no Project Service Automation e essas unidades organizacionais serão mapeadas para várias entidades legais no Finance.

Se você precisar usar o Power Query, siga estas diretrizes:

- O modelo de projetos e contratos (PSA para Fin and Ops) tem um filtro padrão que inclui apenas pedidos de venda do tipo **Item de trabalho (msdyn\_ordertype = 192350001)**. Esse filtro ajuda a garantir que os contratos de projeto não sejam criados para pedidos de venda no Finance. Se você criar seu próprio modelo, deverá adicionar esse filtro.
- Crie um filtro Power Query que inclua apenas as organizações de contrato que devem ser sincronizadas com a entidade legal do conjunto de conexão de integração. Por exemplo, contratos de projeto que você tem com a unidade organizacional de contrato da Contoso US devem ser sincronizados com a entidade legal USSI, mas os contratos de projeto que você tem com a unidade organizacional de contrato da Contoso Global devem ser sincronizados com a entidade legal da USMF. Se você não adicionar esse filtro ao mapeamento de tarefas, todos os contratos de projeto serão sincronizados com a entidade legal definida para o conjunto de conexões, independentemente da unidade organizacional do contrato.

## <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na integração de dados

> [!NOTE] 
> Os campos **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** e **AddressZipCode** não são incluídos no mapeamento padrão para contratos de projeto. Você pode adicionar os mapeamentos se precisar que esses dados sejam sincronizados para contratos de projeto.
>
> Os campos **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** e **ProjectType** não são incluídos no mapeamento padrão para projetos. Você pode adicionar os mapeamentos se precisar que esses dados sejam sincronizados para projetos.

As ilustrações a seguir mostram exemplos de mapeamentos de tarefas do modelo na integração de dados. O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.

[![Mapeamento de modelo de contrato de projeto](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mapeamento de modelo de projeto](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mapeamento de modelo de linhas de contrato de projeto](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mapeamento de modelo de marco de linha de contrato de projeto](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Mapeamento de etapas de linha de contrato de projeto em Projetos e contratos (PSA 3.x para Dynamics) – modelo v2:

[![Mapeamento de marco de linha de contrato de projeto com modelo de versão dois](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]