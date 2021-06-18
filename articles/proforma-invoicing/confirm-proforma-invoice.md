---
title: Confirmar uma fatura pro forma baseada no projeto
description: Este tópico fornece informações sobre como confirmar uma fatura de projeto pro forma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012122"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Confirmar uma fatura pro forma baseada no projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Depois que uma fatura pro forma é confirmada, o status da fatura do projeto é atualizado para **Confirmada**. Quando uma fatura é confirmada, ela se torna somente leitura. A partir deste momento, a fatura só poderá ser corrigida se houver correções ou créditos iniciados pelo cliente.

A tabela a seguir lista os reais criados pelo sistema. Esses reais são criados quando certas operações são executadas no rascunho da fatora de projeto antes de ser confirmada.

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
Faturamento antecipado ou honorários </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma venda cobrada real do tipo <strong>Honorários</strong> é criada para o valor do adiantamento ou honorários.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
As vendas reais não faturadas com um valor negativo de retenção ou adiantamento a ser usado para reconciliação.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Depois de reconciliar totalmente honorários ou adiantamento em uma fatura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação. Este valor é positivo porque se destina a anular o valor negativo gerado no momento da faturação dos honorários ou adiantamento.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma venda cobrada real para o valor desta fatura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Depois de reconciliar parcialmente honorários ou adiantamento em uma fatura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação. Este valor é positivo porque se destina a anular o valor negativo gerado no momento da faturação dos honorários ou adiantamento.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma venda cobrada real para o valor desta fatura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma venda não cobrada real negativa do valor restante dos honorários ou adiantamento a ser usado para reconciliação em faturas futuras.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturamento de uma transação única sem nenhuma edição no rascunho da fatura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma renda cobrada real para as horas e o valor na aprovação de tempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturamento de uma transação de tempo que foi editada para reduzir a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno da venda real e uma venda cobrada real equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda real não faturada que não pode ser cobrada pelas horas e valores restantes após a dedução dos números corrigidos no detalhe da linha de fatura editada, uma reversão dos dados reais da venda e dados reais das vendas faturadas equivalentes.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturamento de uma transação de tempo que foi editada para aumentar a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda real não faturada que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturamento de uma transação de despesas sem nenhuma edição no rascunho da fatura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma venda cobrada real para a quantidade e o valor na aprovação de despesas original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturamento de uma transação de despesas que foi editada para reduzir a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que não é cobrada pela quantidade e o valor restantes após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturamento de uma transação de despesas que foi editada para aumentar a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar uma transação de material sem quaisquer edições na fatura de rascunho.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um retorno de vendas não faturadas para a quantidade e o valor na aprovação de uso de material original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
As vendas reais faturadas para a quantidade e o valor na aprovação de uso de material original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturar uma transação de material editada para reduzir a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um retorno de vendas não faturadas para a quantidade e o valor na aprovação de tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que não é cobrada pela quantidade e o valor restantes após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar uma transação de material editada para aumentar a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um retorno de vendas não faturadas para a quantidade e o valor na aprovação de uso de material original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturamento de um valor.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada pelo valor na linha do diário original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma venda cobrada real para a quantidade e o valor na linha do diário de valor original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Faturamento de um marco.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma venda cobrada real para o valor do marco original na linha de contrato do projeto.
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
