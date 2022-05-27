---
title: Corrija a contabilidade nas propostas de fatura do projeto de rascunho
description: Este tópico explica como ajustar as informações relacionadas à contabilidade em uma proposta de fatura de rascunho.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bf0a3d6b97880920b133cb3b30389adf0c83111c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575060"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Corrija a contabilidade nas propostas de fatura do projeto de rascunho

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

*Detalhes operacionais* para faturas do projeto são mantidas pelo gerente de projeto em uma fatura pró-forma. Esses detalhes incluem a decisão sobre as horas, despesas, materiais ou marcos que devem ser faturados, as taxas e a aplicação de valores de adiantamento e retenção. Depois de confirmar a fatura pro forma original, você pode ajustar os detalhes operacionais criando e confirmando uma [fatura pró-forma corretiva](../proforma-invoicing/corrective-invoices.md).

*Detalhes contábeis* para as faturas do projeto são mantidas em um documento de fatura voltado para o cliente. Esses detalhes incluem o cálculo do imposto sobre vendas e as dimensões financeiras aplicadas à fatura. Este tópico fornece detalhes sobre como esses detalhes contábeis podem ser ajustados em uma proposta de fatura de projeto de rascunho.

## <a name="adjust-sales-tax"></a>Ajustar imposto

Os grupos de impostos sobre vendas de faturamento padrão e grupos de impostos sobre vendas de itens podem ser ajustados diretamente no documento de proposta de fatura. Para ajustar esses grupos, selecione **Editar** e, em seguida, em cada linha de proposta de fatura do projeto, insira um novo valor no campo **Grupo de impostos** ou **Grupo de impostos de itens**.

## <a name="adjust-financial-dimensions"></a>Ajustar dimensões financeiras

### <a name="header-dimensions"></a>Dimensões de cabeçalho

Por padrão, as dimensões financeiras da fatura são derivadas dos registros de transações de projeto não cobrados que estão sendo faturados. No entanto, as configurações do sistema permitem que você use dimensões financeiras no cabeçalho das propostas de fatura do projeto para lançar saldos de cliente. Para habilitar esta funcionalidade, selecione **Permitir atualizações de dimensões do projeto para contas a receber** na guia **Finanças** da página **Parâmetros de gerenciamento e contabilidade de projeto**.

As dimensões financeiras nos cabeçalhos de fatura podem ser editadas antes do lançamento da fatura. Na página **Proposta de fatura do projeto**, mude para a exibição **Cabeçalho** e, em seguida, edite os valores na guia **Dimensões financeiras**.

A exibição **Cabeçalho** só fica disponível depois que o administrador do sistema habilita o recurso **Usar Proposta de fatura do projeto e formulários do diário de faturas com a exibição Cabeçalho e Linhas** no espaço de trabalho **Gerenciamento de recursos**. Esse recurso requer a atualização do Finance 10.0.25 ou posterior.

### <a name="line-dimensions"></a>Dimensões de linha

As dimensões financeiras não podem ser editadas diretamente em uma linha de proposta de fatura do projeto. Em vez disso, siga estas etapas para ajustar as dimensões financeiras em uma proposta de fatura de projeto.

1. Na proposta de fatura do projeto, selecione **Excluir tudo** para remover as linhas de proposta da fatura do projeto.

    O botão **Excluir tudo** fica disponível apenas após o administrador do sistema ativar o recurso **Excluir linhas de proposta de fatura ao usar o Project Operations para cenários baseados em recursos/sem estoque** no espaço de trabalho **Gerenciamento de recursos**.

2. Ajustar as dimensões financeiras:

    - **Transações por conta (marcos de faturamento):** Vá para **Todos os projetos** \> **Gerenciar** \> **Transações por conta** e selecione o marco que requer ajuste. Em seguida, na guia **Dimensões financeiras**, atualize os valores, conforme necessário.
    - **Tempo, despesas e transações materiais:** Na página **Transações de projeto lançadas**, selecione **Ajustar contabilidade** para atualizar as dimensões financeiras.

3. Depois de terminar de ajustar os valores da dimensão financeira, vá para **Gerenciamento e contabilidade de projeto** \> **Periódico** \> **Integração do Project Operations** e selecione **Importar da tabela de preparação** para executar o processo periódico. Esse processo usa os valores de dimensão financeira atualizados para recriar as linhas de proposta de fatura do projeto. Os valores atualizados são usados no razão auxiliar e no livro razão geral do projeto quando a fatura do projeto for lançada.
