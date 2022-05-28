---
title: Gerenciar contratos de projeto
description: Este tópico fornece informações sobre a exibição de contratos baseados em projeto.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 64e81593065d97272af6261e17175c76bd8dca7a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590470"
---
# <a name="manage-project-contracts"></a>Gerenciar contratos de projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os contratos de projeto no Dynamics 365 Project Operations capturam e gerenciam os compromissos contratualmente acordados e detalhes de cobrança de um projeto. A estrutura de um contrato de projeto no Project Operations é adaptada para o trabalho baseado em projeto com os seguintes componentes:

- Linhas de contrato que identificam os componentes distintos do trabalho que serão apresentados como componentes de alto nível em uma fatura do projeto.
- Detalhes da linha de contrato que identificam e estimam o trabalho para cada componente de alto nível ou linha de contrato. A estimativa inclui o cronograma e os aspectos financeiros do trabalho vinculado à linha do contrato.
- Modelos de contratação e componentes cobráveis são configurados para cada linha de contrato que contém o acordo de faturamento para cada linha de contrato e o contrato geral.

## <a name="view-all-project-based-contracts"></a>Exibir todos os contratos baseados em projeto

Uma lista de todos os contratos do projeto pode ser vista na página de listagem **Contratos**. 

1. Vá para **Vendas** > **Contratos**. É exibida uma lista de todos os contratos de projeto no sistema. 
2. Selecione **Exibir seletor** (a seta suspensa ao lado do nome da exibição) para selecionar outras exibições filtradas. Você pode criar suas próprias exibições com critérios de filtro personalizados.

Os contratos podem ser criados ou excluídos desta página de listagem ou de páginas de detalhes.

> [!NOTE]
> Os contratos que têm projetos, tarefas, estimativas, diários e/ou dados reais associados a eles não podem ser excluídos. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
