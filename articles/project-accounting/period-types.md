---
title: Tipos de período
description: Este tópico fornece informações sobre como configurar tipos de período para estimativa de receita.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 487e3de7895ca0752e6c9033c7bb7007ba89301c01e6205b3bc8a7d750724bc9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998762"
---
# <a name="period-types"></a>Tipos de período

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Um tipo de período define a frequência com que a receita de um projeto é estimada. Este tópico fornece informações sobre como configurar tipos de período para estimativa de receita. 

## <a name="create-and-work-with-period-types"></a>Criar e trabalhar com tipos de período
Para criar e trabalhar com tipos de período, conclua as seguintes etapas:

1. em seu ambiente do Dynamics 365 Finance, acesse **Gerenciamento e contabilidade de projeto** > **Configuração** > **Estimativas** > **Tipos de período**.
2. Selecione **Novo** para criar um tipo de período. Insira um nome e uma descrição.
3. No campo **Frequência**, selecione um valor.

    - Se você selecionar **Semana**, **Por quinzena**, **Quinzenal**, **Mês**, **Dia**, **Trimestre**, ou **Ano**, o calendário será usado para gerar os períodos. 
    - Se você selecionar **Período contábil**, os períodos contábeis da configuração da Contabilidade serão usados para gerar os períodos.
    - Se selecionar **Ilimitado**, você poderá especificar períodos personalizados.
4. Selecione o registro do tipo de período e selecione **Gerar períodos** para criar períodos para o tipo de período. Com base na frequência do período selecionado, você pode ter a opção de especificar uma data de início ou o número de períodos a serem gerados.
5. Selecione **Períodos** para revisar os períodos gerados.



[!INCLUDE[footer-include](../includes/footer-banner.md)]