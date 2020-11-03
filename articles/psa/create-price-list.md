---
title: Crie uma lista de preços
description: Como criar uma lista de preços no Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bf75286fd1837e27a9b6053ccb21b60771ee197d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071464"
---
# <a name="create-a-price-list-project-service"></a>Criar uma lista de preços (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

As listas de preços fornecem um modelo que os gerentes de conta podem usar para criar cotações e projetos e para estabelecer os custos de um projeto. Elas fornecem uma lista de itens de linha de funções e despesas, e o preço que será cobrado para cada um. É possível criar várias listas de preços para que você possa manter estruturas de preços separadas para diferentes regiões que você vende seus produtos ou diferentes canais de vendas. É uma boa ideia criar pelo menos uma lista de preços para cada moeda na qual você planeja cobrar os clientes.  
  
Para criar estimativas financeiras para o trabalho a ser entregue, verifique se cada projeto tem um custo de suporte e uma lista de preços de venda. Configure um custo e uma lista de preços de venda padrão que se apliquem a todos os projetos criados em sua organização.  
  
As listas de preços se baseiam em funções e em categorias de despesas, portanto, antes de criar uma lista de preços, verifique se você já configurou as funções e as categorias de despesas que deseja usar ao criar a lista de preços.  
  
1.  Vá para **Project Service > Listas de Preços**.  
  
2.  Clique em **Novo**.  
  
3.  Em **Contexto** , selecione se a lista de preços é de **Custo** , de **Compra** ou de **Venda**.  
  
4.  Em **Nome** , insira um nome para a lista de preços.  
  
5.  Em **Moeda** , selecione a moeda que você usará para cobrança ou avaliação de custo.  
  
6.  Em **Unidade de Tempo** , especifique o período ao qual o preço se aplica, como dia ou hora.  
  
7.  Preencha a **Data de Início** , a **Data de término** e a **Descrição** conforme necessário.  
  
8.  Clique em **Salvar** para criar o registro para poder continuar a editá-lo.  
  
9. Para adicionar um preço da função à lista de preços, clique em **+** em **Preços da função**.  
  
10. No painel **Preço de Função** , preencha os detalhes e clique em **Salvar**. Continue a adicionar preços de função conforme necessário. Ao terminar, clique em **Salvar** no canto inferior direito da tela.  
  
11. Para adicionar um preço de categoria de despesas à lista de preços, clique em **+** em **Preços de categoria**.  
  
12. No painel **Preço de Categoria de Transação** , preencha os detalhes e clique em **Salvar**. Continue a adicionar preços de categorias conforme necessário. Ao terminar, clique em **Salvar** no canto inferior direito da tela.  
  
13. Para adicionar itens da lista de preços à lista de preços, clique em **+** em **Itens da Lista de Preços**.  
  
14. No painel **Item da Lista de Preços** , preencha os detalhes e clique em **Salvar**. Continue a adicionar itens da lista de preços conforme necessário. Ao terminar, clique em **Salvar** no canto inferior direito da tela.  
  
15. Para adicionar relacionamentos de regiões à lista de preços, clique em **+** **Relacionamentos de Regiões**.  
  
16. Na janela **Nova Conexão** , preencha os detalhes e clique em **Salvar**. Continue a adicionar relacionamentos de regiões conforme necessário. Ao terminar, clique em **Salvar** no canto inferior direito da tela.  
  
### <a name="see-also"></a>Consulte também  
 [Configurar Project Service Automation](../psa/configure.md)
