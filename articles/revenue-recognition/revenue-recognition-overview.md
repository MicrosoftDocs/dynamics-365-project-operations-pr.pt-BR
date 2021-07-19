---
title: Visão geral do reconhecimento de receita
description: Este tópico fornece informações sobre o reconhecimento de receita no Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368012"
---
# <a name="revenue-recognition-overview"></a>Visão geral do reconhecimento de receita

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

No Dynamics 365 Project Operations, os princípios de reconhecimento de receita variam com base no método de faturamento selecionado para um projeto ou parte do projeto. Este tópico fornece informações sobre o reconhecimento de receita no Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transações contabilizadas usando o método de cobrança de hora e material

- O custo e o reconhecimento da receita estão conectados. O custo das transações e as vendas não cobradas são lançados usando o [Diário de integração do Project Operations](../project-accounting/project-operations-integration-journal.md).
- O custo do projeto e o perfil de receita determinam se as transações de vendas não cobradas são lançadas na contabilidade. Se a opção **Acumular receita** estiver selecionada, o sistema usa as contas **Valor de vendas de WIP** e **Valor de vendas da receita acumulada** durante o lançamento. Veja a seguir um exemplo deste método.  

  | Tipo de transação | Débito/crédito | Valor |
  | --- | --- | --- |
  | Valor de venda de WIP | Débito | 100 |
  | Valor de venda da receita acumulada | Crédito | 100 |

- A receita é reconhecida durante o faturamento. O sistema usa a conta **Receita faturada** durante o lançamento. Veja a seguir um exemplo deste método.  

  | Tipo de transação | Débito/crédito | Valor |
  | --- | --- | --- |
  | Saldo do cliente | Débito | 120 |
  | Imposto a pagar | Crédito | 20 |
  | Receita Faturada | Crédito | 100 |

- Se a receita foi acumulada quando as vendas não cobradas foram lançadas, o sistema reverterá a receita acumulada no faturamento.

  | Tipo de transação | Débito/crédito | Valor |
  | --- | --- | --- |
  | Valor de venda de WIP | Crédito | 100 |
  | Valor de venda da receita acumulada | Débito | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transações contabilizadas usando o método de cobrança de preço fixo

- O custo e o reconhecimento da receita são separados. O custo das transações é lançado usando o [Diário de integração do Project Operations](../project-accounting/project-operations-integration-journal.md). As transações de vendas não cobradas não são criadas.
- A receita pode ser reconhecida durante o faturamento se o custo do projeto e o perfil de receita tiver a opção **Princípio usado para cálculos de conclusão do projeto** definida como **Sem WIP**. Use este método somente para projetos simples de curto prazo.
- A receita pode ser reconhecida usando estimativas de receita de preço fixo, com os métodos **Contrato concluído** ou **Reconhecimento de receita da porcentagem de conclusão**.

## <a name="additional-resources"></a>Recursos adicionais
[Artigo Configurar contabilidade para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md)

[Projetos de estimativa de receita de preço fixo](rev-rec-percentage-completion-method.md)

[Gerenciar estimativas de receita](rev-rec-completed-contract-method.md)

[Custo para concluir os métodos](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]