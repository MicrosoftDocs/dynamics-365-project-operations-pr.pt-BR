---
title: Linhas de oportunidade baseadas no projeto - lite
description: Este tópico fornece informações sobre linhas de oportunidade baseadas em projeto. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1978b452b84486cabd5b6b4e550261e2c8f76cd89a140709b137ac184c8967c1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998987"
---
# <a name="project-based-opportunity-lines---lite"></a>Linhas de oportunidade baseadas no projeto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

As linhas de oportunidade baseadas em projeto estão disponíveis apenas em oportunidades baseadas em projeto. Os registros de oportunidade baseados em projeto têm o valor do campo **Tipo** definido como **Baseado em trabalho**.

Linhas de oportunidade baseadas em projeto são os itens de linha que serão entregues ao cliente por meio de um projeto. No entanto, não é possível vincular um projeto a uma linha de oportunidade baseada em projeto. Os projetos podem ser vinculados a itens de linha do estágio **Cotação** em diante porque normalmente a oportunidade está em um estágio inicial no ciclo de vida de uma transação. A determinação de quantos projetos serão usados para entregar o trabalho para o cliente é uma decisão tomada posteriormente na fase de vendas. Você pode usar a fase de oportunidade para identificar os componentes discretos de entrega para o cliente. As decisões a respeito do número real de projetos usados para entregar esses componentes podem ser postergadas até que mais informações sejam conhecidas sobre o trabalho em si.

Veja abaixo os campos em uma linha de oportunidade baseada em projeto:

| **Campo** | **Local** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tipo de Produto | Guia geral (oculta) | É possível selecionar uma das seguintes opções:</br>- Serviço baseado em projeto (disponível somente quando o Dynamics 365 Project Operations está instalado)</br>- Produto (disponível apenas quando o Project Operations e o Dynamics 365 Sales estão instalados) | O valor deste campo é definido como **Serviço baseado em projeto** ao criar uma linha de oportunidade baseada em projeto a partir da grade de linhas baseadas em projeto na Oportunidade. <br> Se você alterar ou substituir este valor, a funcionalidade do projeto não será habilitada nos itens de linha baseados em projeto. |
| Oportunidade | Guia Geral | Este campo é somente leitura e faz referência ao Registro de oportunidade pai ao qual este item de linha pertence. | Não há impacto a jusante deste campo. |
| Nome | Guia Geral | Este campo de texto editável pode ser usado para fornecer uma identidade curta ao item de linha. | Este valor é transportado para a linha de cotação quando você cria uma cotação a partir desta oportunidade. |
| Orçamento do Cliente | Guia Geral | Este campo de moeda editável pode ser usado para rastrear o valor que o cliente deseja gastar neste item de linha. | Este valor é transportado para o campo correspondente na linha de cotação quando você cria uma cotação a partir desta oportunidade. |
| Método de Cobrança | Guia Geral | Este campo editável possui os valores a seguir:</br>- Hora e Material</br>- Preço Fixo | Este valor é transportado para o campo correspondente na linha de cotação quando você cria uma cotação a partir desta oportunidade. Depois que a linha de cotação é criada, o campo é bloqueado e não pode ser alterado. Atribua este valor de campo com a maior precisão possível. Se você precisar alterar o valor deste campo na linha de cotação, exclua e recrie a linha de cotação. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]