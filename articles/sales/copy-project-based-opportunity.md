---
title: Copiar oportunidades baseadas em projeto
description: Este tópico fornece informações sobre a cópia de oportunidades com base em projeto no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071367"
---
# <a name="copy-project-based-opportunities"></a>Copiar oportunidades baseadas em projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_


As oportunidades de projeto podem ser facilmente copiadas para criar novas oportunidades de projeto. 

1. Vá para a página de listagem **Oportunidades de Projeto** e selecione uma oportunidade na lista. Ou abra a página de detalhes de uma oportunidade específica. 
2. Em qualquer uma das páginas, selecione **Copiar**. Uma página de diálogo será aberta contendo as seguintes informações de campo. Dependendo dos valores selecionados nesse diálogo, o processo de cópia poderá mudar.

    | **Campo** | **Relevância, finalidade e orientação** | **Impacto a jusante** |
    | --- | --- | --- |
    | Tópico | Insira o tópico relevante da oportunidade de destino. Quando o diálogo for aberto, o sistema irá configurá-lo para o tópico da oportunidade de origem com **copy** acrescentado. | Não há impacto posterior para esse campo. |
    | Conta | Referências à empresa do cliente ou registro da conta. Quando o diálogo for aberto, o sistema irá configurá-lo para a conta na oportunidade de origem. | Esse campo é o cliente principal da oportunidade. |
    | Unidade de Contratação | A unidade organizacional responsável pela entrega dos projetos ou projetos associados a este negócio. Quando o diálogo for aberto, o sistema irá configurá-lo para a unidade de contratação na oportunidade de origem. | A unidade de contratação é a divisão da empresa que executa os projetos após o fechamento do negócio. Cada unidade de contratação tem uma moeda, e essa moeda é usada para relatar os custos estimados e reais incorridos durante o projeto. |
    | Moeda | A moeda de transação do negócio. Quando a página de diálogo for aberta, o sistema irá configurá-lo para a moeda na oportunidade de origem. | A moeda é usada como padrão para uma lista de preços e criar estimativas financeiras na cotação. Eventualmente, a moeda é usada para faturar o cliente quando o negócio é ganho. |
    | Copiar precificação | Um valor Sim/Não que indica se o preço da oportunidade deve ser copiado da oportunidade de origem. | Se **Sim** for selecionado, as listas de preços serão copiadas da oportunidade de origem para a oportunidade de destino. Se **Não** for selecionado, as listas de preços serão padronizadas novamente com base nas listas de preços mais recentes que foram configuradas. |

3. Selecione **OK**. O sistema cria uma cópia da oportunidade de projeto com base nos parâmetros selecionados e a nova oportunidade de projeto é aberta.
