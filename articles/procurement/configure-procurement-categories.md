---
title: Usar categorias de compras com ordens de compra do projeto e faturas de fornecedor pendentes
description: Este artigo descreve como configurar categorias de compras que podem ser usadas com ordens de compra do projeto e faturas de fornecedor pendentes.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028596"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Usar categorias de compras com ordens de compra do projeto e faturas de fornecedor pendentes

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Os profissionais de compras podem criar e manter catálogos de itens e serviços que podem ser usados em ordens de compra e faturas de fornecedor pendentes. [Catálogos de compras](/dynamics365/supply-chain/procurement/procurement-catalogs) são uma maneira fácil de categorizar compras sem precisar configurar e usar um catálogo de produtos lançados. Cada categoria de compras pode ser mapeada para uma categoria de projeto para transações de horas, despesas ou itens. Depois que uma fatura de fornecedor pendente que usa uma categoria de compras for lançada, o sistema criará os dados reais de horas, despesas ou material do projeto, as transações do projeto e as entradas do razão auxiliar.

## <a name="minimum-version-requirements"></a>Requisitos mínimos de versão

As seguintes versões são necessárias para usar categorias de compras com ordens de compra do projeto em cenários baseados em recursos/itens sem estoque do Microsoft Dynamics 365 Project Operations:

- Solução Project Operations Dataverse versão 4.41.0.45 ou posterior
- Ambiente de finanças e operações versão 10.0.26 ou posterior

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Executar mapas de gravação dupla para suporte a categorias de compras

Certifique-se de que o mapeamento para **Entidade de exportação de linha de fatura de fornecedor do projeto de integração do Project Operations msdyn\_projectvendorinvoicelines** usa a versão 1.0.0.4 ou posterior.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Habilitar a chave de recurso para categorias de compras

Siga estas etapas para habilitar a funcionalidade para usar categorias de compras com ordens de compra do projeto.

1. No Dynamics 365 Finance, abra o espaço de trabalho **Gerenciamento de recursos**.
1. Na lista de recursos, encontre o recurso **Usar categorias de compras em cenários baseados em recursos/itens sem estoque do Project Operations** e selecione **Habilitar**.

> [!IMPORTANT]
> Como pré-requisito, você também deve habilitar o recurso **Habilitar faturas de fornecedor pendentes no Project Operations para cenários baseados em recursos/itens sem estoque**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapear categorias de projeto na hierarquia de categorias de compras

Siga estas etapas para mapear categorias de projeto para categorias de compras na hierarquia **Categoria de compras**:

1. Acesse **Compras e fornecimento > \> Categorias de compras**.
1. Selecione **Editar hierarquia de categoria**.
1. Selecione o nó de hierarquia de categoria desejado e, na guia **Atribuir categorias de projeto**, associe o nó à categoria de projeto da categoria **Hora**, **Despesa** ou **Projeto de Item** (isto é, a categoria **Tempo Padrão** ou **Despesa Padrão**).
1. Selecione **Salvar**.
1. Feche a página.

> [!NOTE]
> O mapeamento de uma categoria de compras para uma categoria de projeto é opcional. Se a categoria de compras não for mapeada, o sistema usará o valor definido no campo **Item** da seção **Padrões de categoria do projeto** na guia **Project Operations no Dynamics 365 Customer Engagement** da página **Parâmetros de gerenciamento e contabilidade de projeto**.
