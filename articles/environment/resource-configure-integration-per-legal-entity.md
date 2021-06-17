---
title: Configurar a integração do Project Operations por entidade legal
description: Este tópico fornece informações sobre como configurar a integração por entidade legal no Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000062"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurar a integração do Project Operations por entidade legal 

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico orienta você ao longo das etapas necessárias para configurar o Dynamics 365 Project Operations por entidade legal.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Habilitar teclas de função no Dynamics 365 Finance

Conclua as etapas a seguir para habilitar os recursos necessários.

1. No Dynamics 365 Finance, acesse o espaço de trabalho **Gerenciamento de Recursos**.
2. Na **Lista de recursos**, encontre e ative os seguintes recursos:
  
    - **Habilitar várias linhas de contrato para um projeto**
    - **Habilitar o Project Operations no Dynamics 365 Customer Engagement**

> [!NOTE]
> Se você não vir **Teclas de recursos** listadas, verifique se sua versão do Finance atende ao requisito de versão mínima (versão do aplicativo 10.0.13 com todas as atualizações de qualidade aplicadas ou superior). Selecione **Verificar se há atualizações** para atualizar a lista de recursos.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definir o cenário de implantação do Project Operations para uma entidade legal

Você pode habilitar o Project Operations no Dynamics 365 Customer Engagement em um nível de entidade legal. Você pode ter uma entidade legal usando o Project Operations no Dynamics 365 Customer Engagement para cenários baseados em recursos/sem estoque. No mesmo ambiente, você pode ter outra entidade legal usando o Project Operations para cenários com estoque/ordem de produção.

1. No Dynamics 365 Finance, acesse **Gerenciamento e contabilidade de projeto** > **Configuração** > **Parâmetros globais de gerenciamento e contabilidade de projeto**.
2. Na lista de entidades legais disponíveis, selecione as entidades onde várias linhas de contrato e recursos do Project Operations no Dynamics 365 Customer Engagement serão habilitados. Deixe desmarcadas as entidades legais que usarão o Project Operations para cenários com estoque/ordem de produção.

> [!NOTE]
> Uma entidade legal pode ser selecionada apenas se não tiver nenhum projeto existente.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurar parâmetros de gerenciamento e contabilidade de projeto

Cada entidade legal que usa o Project Operations no Dynamics 365 Customer Engagement precisa de um conjunto de parâmetros padrão. Esses parâmetros são configurados na guia **Project Operations** da página **Parâmetros de gerenciamento e contabilidade de projeto**. Os parâmetros são:

  - **Padrões de tipo de cobrança**: o Project Operations usa um conjunto fixo de padrões de tipo de cobrança que deve ser mapeado para as propriedades de linha Finance. Crie um registro para cada tipo de cobrança: **Não especificado**, **Passível de Cobrança**, **Não Passível de Cobrança**, **Complementar** e **Não disponível**.
  - **Padrões de categoria de projeto**: selecione as categorias de projeto padrão a serem usadas para cada tipo de transação. Esses padrões serão usados no **Diário de integração de operações do projeto** e em estimativas onde nenhuma categoria de transação é especificada para o projeto real.
  - **Previsões**: selecione o modelo de previsão a ser usado para estimativas de tempo e despesas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]