---
title: Fechar uma cotação – lite
description: Este artigo fornece informações sobre como fechar uma cotação no Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e3a199843f379dc53d63372f91e8be2e1bcbf4e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916918"
---
# <a name="close-a-quote---lite"></a>Fechar uma cotação – lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Uma cotação de projeto pode ser fechada como Ganha ou Perdida. Um rascunho de cotação pode ser fechado porque as operações Ativar e Revisar nas cotações não são compatíveis com o Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Fechar uma cotação como Ganha

Quando você fecha uma cotação de projeto como Vencida, o status é definido como Fechado e a razão do status é Vencida. Fechar a cotação torna a cotação do projeto somente leitura e cria um contrato do projeto de rascunho que contém as informações da cotação. Como uma cotação fechada não pode ser reaberta, uma caixa de diálogo de confirmação confirmará suas alterações.

Se a cotação for anexada a uma oportunidade, todas as outras cotações de projeto na oportunidade serão automaticamente fechadas como Perdidas.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financeiro de fechar uma cotação como Ganha

Se houver algum valor real para o tempo em um projeto enquanto ele ainda está vinculado a uma cotação preliminar, apenas o custo do tempo ou despesa é registrado. Depois que uma cotação for fechada como Ganha, o aplicativo vai refatorar os custos revertendo os custos reais mais antigos e recriando os novos custos reais. O aplicativo processará esses custos reais com base no Método de cobrança da linha de contrato associada do projeto. Se os custos reais fizerem referência a uma linha de contrato de tempo e material, os valores reais de vendas não faturados correspondentes serão criados para quando a cotação for fechada e o contrato de projeto criado. Se os custos reais fizerem referência a uma linha de contrato de preço fixo, o aplicativo irá parar de reprocessar os custos reais que são baseados nas regras de faturamento dividido para os clientes do contrato do projeto.

## <a name="closing-a-quote-as-lost"></a>Fechando uma cotação como perdida:

Quando você fecha uma cotação de projeto como Perdida, o status é definido como Fechado e a razão do status é Perdida. Fechar a cotação torna a cotação do projeto somente leitura. Como uma cotação fechada não pode ser reaberta e antes de fechar uma cotação, uma caixa de diálogo de confirmação confirmará suas alterações.

Se a cotação de projeto fechada como Perdida fizer referência a um projeto em qualquer uma de suas linhas, esse projeto também será marcado como Fechado. Todas as reservas de recursos desse dia em diante serão canceladas.

> [!NOTE]
> No Project Operations, fechar uma cotação como Ganha ou Perdida não afetará o status da Oportunidade, que permanecerá aberta até que seja fechada manualmente.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]