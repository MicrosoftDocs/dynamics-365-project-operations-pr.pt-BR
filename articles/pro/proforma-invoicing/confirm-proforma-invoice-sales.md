---
title: Confirmar uma fatura pro forma (lite)
description: Este tópico fornece informações sobre a confirmação de faturas pro forma no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274264"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Confirmar uma fatura pro forma (lite)

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_


Depois que uma fatura pro forma é confirmada, o status da fatura do projeto é atualizado para **Confirmada**. Quando uma fatura é confirmada, ela se torna somente leitura. A partir de agora, a fatura só poderá ser corrigida se houver correções ou créditos iniciados pelo cliente ou se a fatura estiver marcada como paga.

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
Uma venda não cobrada real de um valor negativo dos honorários ou adiantamento a serem usados para reconciliação.
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
Uma nova venda não cobrada real que não é cobrada pelas horas restantes e o valor após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda real e uma venda cobrada real equivalente.
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
Uma venda cobrada real para a quantidade e o valor na aprovação de despesas original </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Faturamento de uma linha de contrato baseada em produto.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma venda cobrada real para a linha de produto com a quantidade e o valor provenientes da linha de contrato baseada em produto.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]