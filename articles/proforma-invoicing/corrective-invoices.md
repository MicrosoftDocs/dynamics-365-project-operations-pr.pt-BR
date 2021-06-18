---
title: Faturas corretivas baseadas em projeto
description: Este tópico fornece informações sobre como criar e confirmar faturas corretivas baseadas em projeto no Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012257"
---
# <a name="corrective-project-based-invoices"></a>Faturas corretivas baseadas em projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Uma fatura de projeto confirmada pode ser corrigida para processar alterações ou créditos negociados com o cliente e o gerente de projeto.

Para fazer edições em uma fatura confirmada, abra a fatura confirmada e selecione **Corrigir esta Fatura**. 

> [!NOTE]
> Esta seleção não está disponível a menos que uma fatura do projeto seja confirmada ou a fatura baseada no projeto tenha adiantamentos ou honorários ou reconciliações de adiantamentos ou honorários.

Um novo esboço de fatura é criado da fatura confirmada. Todos os detalhes da linha da fatura confirmada anteriormente são copiados para o novo rascunho. A seguir estão alguns dos pontos-chave para entender sobre os detalhes da linha na nova fatura corrigida:

- Todas as quantidades são atualizadas para zero. O Dynamics 365 Project Operations assume que todos os itens faturados são totalmente creditados. Se necessário, você pode atualizar manualmente essas quantidades para refletir a quantidade que está sendo faturada, e não a quantidade que está sendo creditada. Com base na quantidade inserida, o aplicativo calcula a quantidade creditada. Esse valor é refletido nos valores reais criados quando a fatura corrigida é confirmada. Se você estiver fazendo alterações no valor do imposto, deverá inserir o valor correto do imposto e não o valor do imposto que está sendo creditado.
- As correções de marcos são sempre processadas como créditos completos.


> [!IMPORTANT]
> Para detalhes de linha de fatura que são correções para outros encargos já faturados, o campo **Correção** está definido como **Sim**. Para faturas que têm detalhes da linha da fatura corrigidos, o campo **Tem correções** é definido como **Sim**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Os valores reais quando uma fatura corretiva é confirmada

A tabela a seguir lista os valores reais criados quando uma fatura corretiva é confirmada.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Cenário</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Reais criados na confirmação</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturamento do crédito total de uma transação de tempo faturada anteriormente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda cobrada pelas horas e o valor no detalhe da linha de fatura original para tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real pelas horas e o valor no detalhe da linha de fatura original para tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturamento do crédito parcial em uma transação de tempo.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda cobrada pelas horas e o valor faturado no detalhe da linha de fatura original para tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda real não faturada que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno disso e um valor real das vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que é passível de cobrança pelas horas e valores restantes após a dedução dos números corrigidos no detalhe da linha da fatura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturamento do crédito total de uma transação de despesa faturada anteriormente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda cobrada pela quantidade e o valor no detalhe da linha de fatura original para a despesa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real pela quantidade e o valor no detalhe da linha de fatura original para a despesa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturamento do crédito parcial de uma transação de despesa faturada anteriormente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda cobrada pela quantidade e o valor faturados no detalhe da linha de fatura original para uma despesa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda real não faturada que é passível de cobrança pela quantidade e o valor no detalhe da linha da fatura corrigida, um estorno disso e um valor real das vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que é passível de cobrança pela quantidade e valores restantes após a dedução dos números corrigidos no detalhe da linha da fatura.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar o crédito total de uma transação de material faturada anteriormente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de vendas faturadas para a quantidade e o valor no detalhe da linha da fatura original do material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor de vendas não faturado para a quantidade e o valor no detalhe da linha da fatura original do material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturamento do crédito parcial em uma transação de material.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de vendas faturadas para a quantidade e o valor faturado no detalhe da linha da fatura original do material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturadas que é cobrado pela quantidade e valor no detalhe da linha da fatura editada, um estorno disso e um valor real de vendas faturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que é passível de cobrança pela quantidade e valores restantes após a dedução dos números corrigidos no detalhe da linha da fatura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturamento do crédito total de uma transação de valor faturada anteriormente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda cobrada pela quantidade e o valor no detalhe da linha de fatura original para o valor.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real pela quantidade e o valor no detalhe da linha de fatura original para o valor.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturamento do crédito parcial de uma transação de valor faturada anteriormente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda cobrada pela quantidade e o valor faturados no detalhe da linha de fatura original para o valor.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que é passível de cobrança pela quantidade e o valor no detalhe da linha da fatura corretiva editada, um estorno disso e um valor real das vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Faturamento do crédito total de um marco faturado anteriormente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda cobrada pelas horas e o valor no detalhe da linha de fatura original para o marco.
                </p>
                <p>
O status da fatura no marco é atualizado de <b>Fatura do Cliente Lançada</b> para <b>Pronto para Faturamento</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Faturamento do crédito parcial de um marco faturado anteriormente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Este não é suportado.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
