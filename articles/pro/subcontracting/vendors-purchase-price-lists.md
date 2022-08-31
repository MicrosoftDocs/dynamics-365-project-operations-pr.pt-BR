---
title: Gerenciamento de fornecedores e de listas de preços de compra no Project Operations
description: Este artigo fornece informações que o ajudarão a criar e manter dados de fornecedores e listas de preços de compra para subcontratação.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3cd883fed8a59f1c54c39e2d051b9748833ba692
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261873"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Gerenciamento de fornecedores e de listas de preços de compra no Project Operations


_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

## <a name="vendors-in-project-operations"></a>Fornecedores no Project Operations

No Microsoft Dynamics 365 Project Operations, contas de fornecedores têm um tipo de relacionamento de **Fornecedor** ou **Provedor**. Você pode selecionar apenas um registro de conta que tenha um desses tipos de relacionamento como fornecedor em um subcontrato.

Você pode associar uma ou mais listas de preços de compra a um registro de fornecedor. No entanto, cada lista de preços de compra associada a um registro de fornecedor deve ter uma data efetiva diferente. O Project Operations não permite a sobreposição de data efetiva para listas de preços de compra.

Por padrão, os seguintes campos e conceitos em um registro de fornecedor são usados para qualquer subcontrato criado para o fornecedor:

- Condições de pagamento
- Contato para cobrança
- Contato principal

    > [!NOTE]
    > Por padrão, o contato principal do fornecedor é usado como o gerente de contas do fornecedor do subcontrato.

- Moeda
- Listas de preços de compra atuais

## <a name="purchase-price-lists-in-project-operations"></a>Listas de preços de compra no Project Operations

Uma lista de preços em que o campo **Contexto** está definido como **Compra** é considerada uma lista de preços de compra. Listas de preços de compra podem ser definidas para representar um catálogo de taxas de compra para hora, despesas e materiais. As listas de preços de compra se assemelham às listas de preços de custo e venda no Project Operations. Os seguintes conceitos se aplicam às listas de preços de compra da mesma forma que se aplicam às listas de preços de custo e venda:

- **Data efetiva** – As listas de preços de compra têm uma data efetiva. A data efetiva é representada pelos campos de data de início e data de término em cada lista de preços. O tempo entre a data de início e a data de término é o período da data efetiva.
- **Moeda** – A moeda no cabeçalho da lista de preços é usada como a moeda em que os preços de compra são expressos para mão de obra, categorias de despesas e produtos no catálogo.
- **Unidade de tempo padrão** – A unidade de tempo padrão expressa os preços de mão de obra para compras. O campo de unidade de tempo em uma lista de preços é usado apenas para fornecer um valor padrão. Esse valor pode ser alterado em linhas de preços de funções individuais.

As listas de preços de compra podem ser anexadas a registros de fornecedor como associações conhecidas como listas de preços do projeto. Essas listas de preços são usadas para inserir preços padrão nas linhas de subcontrato. Por padrão, quando várias listas de preços de compra estão anexadas a um registro de fornecedor, a lista de preços mais atual é usada para subcontratos criados para o fornecedor. Apenas listas de preços em que o campo **Contexto** está definido como **Compra** podem ser anexadas a registros de fornecedor.

### <a name="subcontract-specific-purchase-price-lists"></a>Listas de preços de compra específicas de subcontrato

As listas de preços de compra também podem ser anexadas a subcontratos como associações conhecidas como listas de preços do projeto. Essas listas de preços são usadas para inserir preços padrão nas linhas de subcontrato. Por padrão, quando várias listas de preços de compra são anexadas a um subcontrato, cada uma deve ter uma data efetiva diferente. O Project Operations não permite listas de preços de compra com sobreposição de data efetiva. Apenas listas de preços em que o campo **Contexto** está definido como **Compra** podem ser anexadas a subcontratos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
