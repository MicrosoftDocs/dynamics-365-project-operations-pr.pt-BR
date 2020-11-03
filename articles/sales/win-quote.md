---
title: Fechar uma cotação
description: Este tópico fornece informações sobre como fechar cotações no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071326"
---
# <a name="close-a-quote"></a>Fechar uma cotação

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Uma cotação de projeto pode ser fechada como Ganha ou Perdida. Como as funções Ativar e Revisar nas cotações não têm suporte no Microsoft Dynamics 365 Project Operations, portanto, você pode fechar uma cotação de rascunho.

## <a name="close-a-quote-as-won"></a>Fechar uma cotação como Ganha

Fechar uma cotação de projeto como Ganha definirá o status da cotação como **Fechada** e a razão do status definida como **Ganha**. Fechar as cotações faz com que elas se tornem somente leitura e cria um contrato do projeto de rascunho com todas as informações da cotação. Como uma cotação fechada não pode ser reaberta, antes de fechar uma cotação, uma caixa de diálogo de confirmação confirmará suas alterações.

O contrato de projeto criado a partir de uma cotação de projeto também será disponibilizado no módulo Gestão e contabilidade de projetos do Project Operations. Se um contrato de projeto não estiver mapeado para um projeto em nenhuma de suas linhas, esse contrato de projeto será disponibilizado como um contrato de projeto inativo e se tornará ativo assim que um projeto for mapeado para pelo menos uma de suas linhas de contrato.

Se a cotação for anexada a uma oportunidade, todas as outras cotações de projeto na oportunidade serão automaticamente fechadas como Perdidas.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financeiro de fechar uma cotação como Ganha

Se houver dados reais de horas registradas em um projeto enquanto ele ainda estiver anexado a uma cotação de rascunho, somente o custo do tempo ou da despesa será registrado. Depois que uma cotação for fechada como Ganha, o aplicativo vai refatorar os custos revertendo os custos reais mais antigos e recriando os novos custos reais. O aplicativo processará esses custos reais com base no Método de cobrança da linha de contrato associada do projeto. Se os valores reais de custo fizerem referência a uma linha de contrato de tempo e material, o sistema criará automaticamente os valores reais de vendas não faturados correspondentes para quando a cotação for fechada e o contrato de projeto for criado. Se os custos reais fizerem referência a uma linha de contrato de preço fixo, o aplicativo vai parar de reprocessar os custos reais com base nas regras de faturamento dividido para os clientes do contrato do projeto.

Todos os valores reais reprocessados estão disponíveis no módulo Gestão e contabilidade de projetos para que o contador do projeto revise, atualize e publique na Contabilidade. 

## <a name="close-a-quote-as-lost"></a>Fechar uma cotação como Perdida

Fechar uma cotação de projeto como Perdida definirá o status como **Fechada** e razão do status como **Perdida**. Fechar a cotação faz com ela se torne somente leitura. Como uma cotação fechada não pode ser reaberta e antes de fechar uma cotação, uma caixa de diálogo de confirmação confirmará suas alterações.

Se a cotação de projeto fechada como Perdida tiver um projeto referenciado em qualquer uma de suas linhas, esse projeto também será marcado como Fechado e todas as reservas de recursos desse dia em diante serão canceladas.

> [!NOTE]
> No Project Operations, fechar uma cotação como Ganha ou Perdida não afetará o status da Oportunidade, que permanecerá aberta até que seja fechada manualmente.
