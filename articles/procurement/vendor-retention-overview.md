---
title: Visão geral da retenção de fornecedores
description: Este tópico fornece uma visão geral dos recursos de retenção do fornecedor.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594561"
---
# <a name="vendor-retention-overview"></a>Visão geral da retenção de fornecedores

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Sua organização pode querer reter uma parte dos pagamentos a fornecedores que trabalham em projetos para sua organização. Por exemplo, antes de pagar seu fornecedor, você pode querer ter certeza de que os itens e serviços fornecidos atendam às suas expectativas.

Ao negociar compras para projetos com fornecedores, você pode especificar os termos de retenção do fornecedor que incluam a porcentagem ou o valor a ser retido. À medida que o fornecedor entrega itens e serviços, você deduz a porcentagem ou valor de retenção especificado do seu pagamento ao fornecedor. Quando o projeto for concluído ou atingir um estágio intermediário conforme especificado no contrato do fornecedor, você libera o valor retido e cria um pagamento para o fornecedor.

## <a name="vendor-retention-example"></a>Exemplo de retenção de fornecedor

O exemplo a seguir mostra como uma porcentagem do valor da fatura de um fornecedor é retida com base na porcentagem concluída de um projeto.

A Contoso Robotics USA contratou o fornecedor Fabrikam para fornecer 100 horas de treinamento para o projeto de renovação de equipamentos. O valor total do contrato é de USD 30.000 com um preço de compra acordado de USD 300 por hora.

O treinamento será realizado em três fases com a seguinte agenda:

- Fase 1: 50 horas ou 50% do projeto
- Fase 2: 30 horas ou 80% do projeto no total
- Fase 3: 20 horas ou 100% do projeto

A tabela a seguir lista os termos de retenção.

| **Porcentagem de unidades entregues** | **Porcentagem a ser retida** | **Porcentagem a ser liberada** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

As transações resultam nos seguintes valores:

- Fase 1:
  - O valor a pagar é 50 x 300, ou 15.000.
  - 20% do valor, ou 3.000, são retidos e serão liberados em um estágio posterior.
  - O valor pago ao fornecedor é de 12.000.
- Fase 2:
  - O valor a pagar é 30 x 300, ou 9.000.
  - 10% do valor, ou 900, são retidos.
  - 10% dos 3.000 que foram retidos na Fase 1, ou 300, são liberados.
  - O valor pago ao fornecedor é de 8.400. Esse valor é de 9.000 menos a retenção de 900 mais os 300 que foram liberados da retenção da Fase 1.
- Fase 3:
  - O valor a pagar é 20 x 300, ou 6.000.
  - Nenhum valor é retido.
  - O valor liberado é de 3.600. Este valor consiste nos 3.000 que foram retidos na Fase 1, menos os 300 da Fase 1 que foram liberados na Fase 2, mais os 900 que foram retidos na Fase 2.
  - O valor pago ao fornecedor é de 9.600. Este valor consiste no valor retido de 3.600 mais os 6.000 para a conclusão da Fase 3.

O valor total pago ao fornecedor após a conclusão das três fases é de 30.000, que é o valor total do pedido de compra (15.000 + 9.000 + 6.000).
