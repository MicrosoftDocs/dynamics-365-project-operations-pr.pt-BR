---
title: Configurar categorias de projeto
description: Este tópico fornece informações sobre como configurar categorias de projeto.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895952"
---
# <a name="configure-project-categories"></a>Configurar categorias de projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

O Project Operations oferece funcionalidades robustas para categorizar a receita e as despesas em projetos. As categorias fornecem a capacidade de relatar e analisar as transações do projeto, além de conduzir o lançamento na contabilidade.

O diagrama a seguir ilustra a correlação entre categorias de transação, categorias compartilhadas e categorias de projeto. 

As categorias de transação são o agrupamento básico para transações de projeto. Dentro desse agrupamento, há um conjunto de categorias compartilhadas que podem ser compartilhadas entre aplicativos e módulos. Ao se aprofundar ainda mais nas especificidades, as categorias de projeto são o nível mais granular de categorias. As categorias de projeto são específicas para entidade legal, módulo e aplicativo.

![Correlação entre categorias de transação, categorias compartilhadas e categorias de projeto](media/project-categories.png)

## <a name="transaction-categories"></a>Categorias de transação

As categorias de transação representam o agrupamento básico de transações de projeto e não são específicas da empresa ou do tipo de transação. Por exemplo, a Contoso Robotics usa as categorias Design, Viagem, Instalação e Transação de Serviço para agrupar as Transações do projeto.

As categorias de transação são definidas no módulo do Project Operations. 
1. Vá para **Configurações** \> **Categorias de Transação** para abrir o formulário. 
2. Crie uma nova categoria de transação selecionando **Novo** ou **Importar do Excel**.

## <a name="shared-categories"></a>Categorias compartilhadas

O Dynamics 365 usa o conceito de Categorias compartilhadas para categorizar despesas em aplicativos diferentes, como Dynamics 365 Finance, Dynamics 365 Supply Chain e Dynamics 365 Project Operations. Para cada Categoria de transação criada, o Project Operations automaticamente cria quatro Categorias compartilhadas relacionadas: Horas, Despesa, Taxas e Item. Você pode revisar e ajustar as categorias compartilhadas acessando **Gerenciamento e contabilidade de projeto** \> **Configurar** \> **Categorias** \> **Categorias Compartilhadas**.

## <a name="project-categories"></a>Categorias de produto

As categorias de projeto representam o nível mais granular da configuração de categoria e devem ser configuradas separadamente e, para cada empresa, por um Contador do projeto.

1. Vá para **Gerenciamento e Contabilidade de Projeto** \> **Configurar** \> **Categorias** \> **Categorias de projeto**.
2. Selecione **Novo**.
3. Selecione a **ID da Categoria** da Categoria compartilhada que você criou na seção anterior. O Project Operations permite usar somente as categorias compartilhadas que estão associadas às categorias de transação.
4. Selecione um grupo de categorias.

## <a name="category-groups"></a>Grupos de categoria

Os grupos de categorias são usados para compartilhar propriedades, principalmente perfis de lançamentos, entre Categorias de projeto relacionadas. Deve haver pelo menos um grupo de categorias para cada tipo de transação e cada categoria de projeto é atribuído a um grupo.

As especificações de lançamento no Project Operations são definidas pelo custo do projeto e regras do perfil da receita, categorias de projeto e grupos de categorias. Você pode configurar grupos de categorias acessando **Gerenciamento e contabilidade de projeto** \> **Configuração** \> **Categorias** \> **Grupos de categorias**.
