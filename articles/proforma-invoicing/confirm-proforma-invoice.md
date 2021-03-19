---
title: Confirmar uma fatura pro forma
description: Este tópico fornece informações sobre como confirmar uma fatura pro forma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287854"
---
# <a name="confirm-a-proforma-invoice"></a>Confirmar uma fatura pro forma

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Depois que uma fatura pro forma é confirmada, o status da fatura do projeto é atualizado para **Confirmada**. Quando uma fatura é confirmada, ela se torna somente leitura. A partir de agora, a fatura só poderá ser corrigida se houver correções ou créditos iniciados pelo cliente ou quando for marcada como paga.

A tabela a seguir lista os reais criados pelo sistema. Esses reais são criados quando certas operações são executadas no rascunho da fatora de projeto antes de ser confirmada.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Cenário</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Reais criados na confirmação</strong>
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
Uma nova venda real não faturada que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda real não faturada que não é cobrada pelas horas e o valor restantes após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda real não faturada e uma venda real faturada equivalente.
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
Uma nova venda não cobrada real que não é cobrada pela quantidade e o valor restantes após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda não cobrada real e um equivalente da venda cobrada real.
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