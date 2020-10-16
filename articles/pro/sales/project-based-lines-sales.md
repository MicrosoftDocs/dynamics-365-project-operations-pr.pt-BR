---
title: Linhas de oportunidade baseadas em projeto (Pro)
description: Este tópico fornece informações sobre linhas de oportunidade baseadas em projeto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896357"
---
# <a name="project-based-opportunity-lines-pro"></a>Linhas de oportunidade baseadas em projeto (Pro)

_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_

As linhas de oportunidade baseadas em projeto estão disponíveis apenas em oportunidades baseadas em projeto. Os registros de oportunidade baseados em projeto têm o valor do campo **Tipo** definido como **Baseado em trabalho**.

Linhas de oportunidade baseadas em projeto são os itens de linha que serão entregues ao cliente por meio de um projeto. No entanto, não é possível vincular um projeto a uma linha de oportunidade baseada em projeto. Os projetos podem ser vinculados a itens de linha do estágio **Cotação** em diante porque normalmente a oportunidade está em um estágio inicial no ciclo de vida de uma transação. A determinação de quantos projetos serão usados para entregar o trabalho para o cliente é uma decisão tomada posteriormente na fase de vendas. Você pode usar a fase de oportunidade para identificar os componentes discretos de entrega para o cliente. As decisões a respeito do número real de projetos usados para entregar esses componentes podem ser postergadas até que mais informações sejam conhecidas sobre o trabalho em si.

Veja abaixo os campos em uma linha de oportunidade baseada em projeto:

| **Campo** | **Local** | **Relevância, finalidade e orientação** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tipo de Produto | Guia geral (oculta) | É possível selecionar uma das seguintes opções:</br>- Serviço baseado em projeto (disponível apenas quando o Dynamics 365 Project Operations está instalado)</br>- Produto (disponível apenas quando o Project Operations e o Dynamics 365 Sales estão instalados) | O valor deste campo é definido como **Serviço baseado em projeto** ao criar uma linha de oportunidade baseada em projeto a partir da grade de linhas baseadas em projeto na Oportunidade. <br> Se você alterar ou substituir este valor, a funcionalidade do projeto não será habilitada nos itens de linha baseados em projeto. |
| Oportunidade | Guia Geral | Este campo é somente leitura e faz referência ao Registro de oportunidade pai ao qual este item de linha pertence. | Não há impacto a jusante deste campo. |
| Nome | Guia Geral | Este campo de texto editável pode ser usado para fornecer uma identidade curta ao item de linha. | Este valor é transportado para a linha de cotação quando você cria uma cotação a partir desta oportunidade. |
| Orçamento do Cliente | Guia Geral | Este campo de moeda editável pode ser usado para rastrear o valor que o cliente deseja gastar neste item de linha. | Este valor é transportado para o campo correspondente na linha de cotação quando você cria uma cotação a partir desta oportunidade. |
| Método de Cobrança | Guia Geral | Este campo editável possui os valores a seguir:</br>- Hora e Material</br>- Preço Fixo | Este valor é transportado para o campo correspondente na linha de cotação quando você cria uma cotação a partir desta oportunidade. Depois que a linha de cotação é criada, o campo é bloqueado e não pode ser alterado. Atribua este valor de campo com a maior precisão possível. Se você precisar alterar o valor deste campo na linha de cotação, exclua e recrie a linha de cotação. |
