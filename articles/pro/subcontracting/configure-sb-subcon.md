---
title: Configurar o Quadro de Agendamento para mostrar os trabalhadores contratados e a capacidade subcontratada
description: Este artigo descreve como configurar o Painel de Agendamento no Microsoft Dynamics 365 Project Operations para mostrar a capacidade de recursos subcontratados ao preencher os requisitos de recursos do projeto.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262202"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configurar o Quadro de Agendamento para mostrar os trabalhadores contratados e a capacidade subcontratada 

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

O Painel de Agendamento no Microsoft Dynamics 365 Project Operations pode ser usado para pesquisar recursos de duas maneiras:

- Pesquisa geral de recursos sem o contexto de qualquer requisito de recurso específico baseado em projeto.
- Pesquisa de recursos específicos do requisito em que o requisito do projeto fornecerá o contexto para os recursos sugeridos.

Para notificar o painel de agendamento de capacidade de recursos subcontratados e trabalhadores contratados, você precisa fazer atualizações nas configurações do Painel de agendamento. Essas atualizações incluem: 
- Atualize as configurações do Painel de Agendamento para pesquisa geral de recursos.
- Atualize as configurações do Painel de Agendamento para pesquisa de recursos baseada em requisitos.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Atualizar as configurações do Painel de Agendamento para pesquisa geral de recursos
### <a name="update-filters-for-general-resource-search"></a>Atualizar filtros para pesquisa geral de recursos
Ao pesquisar um recurso, os filtros disponíveis no painel de agendamento devem ser atualizados para que você também possa pesquisar recursos externos especificando um ou todos os itens a seguir:
  - Tipo de trabalhador, se os recursos mostrados devem ser trabalhadores contratados ou funcionários.
  - Empresa fornecedora à qual um recurso deve pertencer.
  - Recursos que pertencem a um subcontrato ou linha de subcontrato específico.
    
### <a name="update-retrieve-resource-query"></a>Atualizar consulta de recurso de recuperação
A consulta usada para pesquisa também deve ser atualizada para usar esses atributos de filtro adicionais. Use as etapas a seguir para atualizar a configuração do Painel de Agendamento para pesquisa geral de recursos:  
1. Abra **Configurações do Painel de Agendamento** para um Painel de Agendamento específico.
2. Abra a guia **Configurações gerais** e role até **Outras configurações**.
3. Na lista de configurações desta seção, atualize o **Layout de Filtro** para **Layout de Filtro Padrão para o Project Operations Lite**.
4. Atualize **Recuperação da Consulta de Recursos** para **Recuperação da Consulta de Recursos Padrão para o Project Operations Lite**.

![Atualizar as configurações do Painel de Agendamento para pesquisa geral de recursos](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Atualizar as configurações do Painel de Agendamento para pesquisa de recursos baseada em requisitos
### <a name="update-filters-for-requirement-specific-resource-search"></a>Atualizar filtros para pesquisa de recursos específicos de requisitos 
Ao pesquisar um recurso, os filtros disponíveis no painel de agendamento devem ser atualizados para que você também possa pesquisar recursos externos especificando um ou todos os itens a seguir:
 - Tipo de trabalhador, se os recursos mostrados devem ser trabalhadores contratados ou funcionários.
 - Empresa fornecedora à qual um recurso deve pertencer.
 - Recursos que pertencem a um subcontrato ou linha de subcontrato específico.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Atualizar consulta de recurso de recuperação para pesquisa de recurso específica do requisito 
A consulta usada para pesquisa também deve ser atualizada para usar esses atributos de filtro adicionais. Use as etapas a seguir para atualizar a configuração do Painel de Agendamento para pesquisa de recursos baseada em requisitos:

1. Abra **Configurações de Painel de Agendamento** para um Painel de Agendamento específico e selecione **Abrir Configurações Padrão** para abrir as configurações para pesquisa específica do requisito.
2. Abra a guia **Configurações gerais** e role até **Outras configurações**.
3. Na lista de configurações desta seção, atualize o **Layout de Filtro** para **Layout de Filtro Padrão para o Project Operations Lite**.
4. Atualize **Recuperação da Consulta de Recursos** para **Recuperação da Consulta de Recursos Padrão para o Project Operations Lite**.
5. Abra a guia **Tipos de Agendamento** e vá para **Projeto**.
6. Nas configurações de **Projeto**, atualize **Recuperação da Consulta de Recursos do Assistente de Agendamento** para **Recuperação da Consulta de Recursos Padrão para o Project Operations Lite** e atualize **Recuperação da Consulta de Restrições do Assistente de Agendamento** para **Recuperação da Consulta de Restrições Padrão para o Project Operations Lite**.

![Atualizar as configurações do Painel de Agendamento para pesquisa de recursos baseada em requisitos](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
