---
title: Corrija a contabilidade nas propostas de fatura do projeto de rascunho
description: Este tópico explica como ajustar as informações relacionadas à contabilidade em uma proposta de fatura de rascunho.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251174"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Corrija a contabilidade nas propostas de fatura do projeto de rascunho

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

*Detalhes operacionais* para faturas do projeto são mantidas pelo gerente de projeto em uma fatura pró-forma. Esses detalhes incluem a decisão sobre as horas, despesas, materiais ou marcos que devem ser faturados, as taxas e a aplicação de valores de adiantamento e retenção. Depois de confirmar a fatura pro forma original, você pode ajustar os detalhes operacionais criando e confirmando uma [fatura pró-forma corretiva](../proforma-invoicing/corrective-invoices.md).

*Detalhes contábeis* para as faturas do projeto são mantidas em um documento de fatura voltado para o cliente. Esses detalhes incluem o cálculo do imposto sobre vendas e as dimensões financeiras aplicadas à fatura. Este tópico fornece detalhes sobre como esses detalhes contábeis podem ser ajustados em uma proposta de fatura de projeto de rascunho.

## <a name="adjust-sales-tax"></a>Ajustar imposto

Os grupos de impostos sobre vendas de faturamento padrão e grupos de impostos sobre vendas de itens podem ser ajustados diretamente no documento de proposta de fatura. Para ajustar esses grupos, selecione **Editar** e, em seguida, em cada linha de proposta de fatura do projeto, insira um novo valor no campo **Grupo de impostos** ou **Grupo de impostos de itens**.

## <a name="adjust-financial-dimensions"></a>Ajustar dimensões financeiras

As dimensões financeiras não podem ser editadas diretamente em uma linha de proposta de fatura do projeto. Em vez disso, siga estas etapas para ajustar as dimensões financeiras em uma proposta de fatura de projeto.

1. Na proposta de fatura do projeto, selecione **Excluir tudo** para remover as linhas de proposta da fatura do projeto.

    > [!NOTE]
    > O botão **Excluir tudo** fica disponível apenas após o administrador do sistema ativar o recurso **Excluir linhas de proposta de fatura ao usar o Project Operations para cenários baseados em recursos/sem estoque** no espaço de trabalho **Gerenciamento de recursos**.

2. Ajustar as dimensões financeiras:

    - **Transações por conta (marcos de faturamento):** Vá para **Todos os projetos** \> **Gerenciar** \> **Transações por conta** e selecione o marco que requer ajuste. Em seguida, na guia **Dimensões financeiras**, atualize os valores, conforme necessário.
    - **Tempo, despesas e transações materiais:** Na página **Transações de projeto lançadas**, selecione **Ajustar contabilidade** para atualizar as dimensões financeiras.

3. Depois de terminar de ajustar os valores da dimensão financeira, vá para **Gerenciamento e contabilidade de projeto** \> **Periódico** \> **Integração do Project Operations** e selecione **Importar da tabela de preparação** para executar o processo periódico. Esse processo usa os valores de dimensão financeira atualizados para recriar as linhas de proposta de fatura do projeto. Os valores atualizados são usados no razão auxiliar e no livro razão geral do projeto quando a fatura do projeto for lançada.
