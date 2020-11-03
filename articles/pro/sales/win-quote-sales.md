---
title: Fechar cotações
description: Este tópico fornece informações sobre como fechar uma cotação no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071349"
---
# <a name="close-quotes"></a>Fechar cotações 

_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_

Uma cotação de projeto pode ser fechada como Ganha ou Perdida. As operações Ativar e Revisar nas cotações não têm suporte no Microsoft Dynamics 365 Project Operations, portanto, uma cotação de rascunho pode ser fechada.

## <a name="close-a-quote-as-won"></a>Fechar uma cotação como Ganha

Fechar uma cotação de projeto como Ganha fechará a cotação com o status definido como Fechada e a razão do status definida como Ganha. Fechar a cotação torna a cotação do projeto somente leitura e cria um contrato do projeto de rascunho que contém as informações da cotação. Como uma cotação fechada não pode ser reaberta, será exibida uma caixa de diálogo de confirmação Há uma caixa de diálogo de confirmação antes que as alterações sejam feitas, pois uma cotação fechada não pode ser reaberta e as alterações são irreversíveis.

Se a cotação for anexada a uma oportunidade, todas as outras cotações de projeto na oportunidade serão automaticamente fechadas como Perdidas.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financeiro de fechar uma cotação como Ganha

Se houver dados reais de horas registradas em um projeto enquanto ele ainda estiver anexado a uma cotação de rascunho, somente o custo do tempo ou da despesa será registrado. Depois que uma cotação for fechada como Ganha, o aplicativo vai refatorar os custos revertendo os custos reais mais antigos e recriando os novos custos reais. O aplicativo processará esses custos reais com base no Método de cobrança da linha de contrato associada do projeto. Se os valores reais de custo fizerem referência a uma linha de contrato de tempo e material, o sistema criará automaticamente os valores reais de vendas não faturados correspondentes para quando a cotação for fechada e o contrato de projeto for criado. Se os custos reais fizerem referência a uma linha de contrato de preço fixo, o aplicativo vai parar de reprocessar os custos reais com base nas regras de faturamento dividido para os clientes do contrato do projeto.

## <a name="closing-a-quote-as-lost"></a>Fechando uma cotação como perdida:

Fechar uma cotação de projeto como perdida definirá o status como Fechada e razão do status como Perdida. Fechar a cotação torna a cotação do projeto somente leitura. Como uma cotação fechada não pode ser reaberta e antes de fechar uma cotação, uma caixa de diálogo de confirmação confirmará suas alterações.

Se a cotação de projeto fechada como Perdida tiver um projeto referenciado em qualquer uma de suas linhas, esse projeto também será marcado como Fechado e todas as reservas de recursos desse dia em diante serão canceladas.

> [!NOTE]
> No Project Operations, fechar uma cotação como Ganha ou Perdida não afetará o status da Oportunidade, que permanecerá aberta até que seja fechada manualmente.
