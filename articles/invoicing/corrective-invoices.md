---
title: Criar faturas baseadas em projeto
description: Este tópico fornece informações sobre faturas corretivas no Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cde82bb3c5777458a63a44a131af284e6ed5d7532de6aacbb5eb860c1fcddebd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006169"
---
# <a name="create-corrective-project-based-invoices"></a>Criar faturas baseadas em projeto 

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Uma fatura de projeto confirmada pode ser corrigida para processar alterações ou créditos negociados com o cliente e o gerente de projeto.

Para fazer edições em uma fatura confirmada, abra a fatura confirmada e selecione **Corrigir esta Fatura**. 

> [!NOTE]
> Esta seleção não estará disponível a menos que uma fatura do projeto seja confirmada.

Um novo esboço de fatura é criado da fatura confirmada. Todos os detalhes da linha da fatura confirmada anteriormente são copiados para o novo rascunho. A seguir estão alguns pontos-chave para ajudá-lo a entender mais sobre os detalhes da linha na nova fatura corrigida:

- Todas as quantidades são atualizadas para zero. Isso presumo que todos os itens faturados são totalmente creditados. Se necessário, você pode atualizar manualmente essas quantidades para refletir a quantidade que está sendo faturada, e não a quantidade que está sendo creditada. Com base na quantidade inserida, o aplicativo calcula a quantidade creditada. Esse valor é refletido nos valores reais criados quando a fatura corrigida é confirmada. Se você estiver fazendo alterações no valor do imposto, deverá inserir o valor correto do imposto e não o valor do imposto que está sendo creditado.
- As correções de marcos são sempre processadas como créditos completos.
- Os valores retidos ou adiantados poderão ser corrigidos se o cliente tiver sido faturado com um valor incorreto.
- As reconciliações de retenções e adiantamentos podem ser corrigidas se um valor incorreto tiver sido usado para reconciliar com os encargos em uma fatura previamente confirmada.

> [!IMPORTANT]
> Os detalhes de linha de fatura que são correções para outros encargos já faturados têm o campo **Correção** definido como **Sim**. As faturas com os detalhes da linha da fatura corrigidos têm um campo chamado **Tem correções**, que também está definido como **Sim**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Os valores reais criados na confirmação de uma fatura corretiva

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
            <td width="216" rowspan="4" valign="top">
                <p>
Confirme a correção de um adiantamento ou honorário faturado.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação. Esse valor é positivo porque se destina a anular o valor negativo gerado no momento da faturação dos honorários ou adiantamento.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um estorno real de vendas faturadas é criado para o valor nos honorários ou adiantamento para estornar as vendas faturadas originais.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda cobrada real é criada para o valor corrigido na linha de fatura corrigida com base em honorários ou adiantamento.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma venda não cobrada real de um valor negativo da linha de fatura corrigida com base em honorários ou adiantamento, que será usada para reconciliação.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Uma confirmação da correção de honorários ou adiantamento previamente reconciliados.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação. Esse valor é positivo e se destina a anular o valor negativo gerado no momento em que a reconciliação anterior ocorreu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um estorno de venda cobrada real para o valor na fatura anterior.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda cobrada real para o valor de honorários corrigido que é aplicado na fatura corrigida.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma venda não cobrada real com um valor negativo dos honorários ou adiantamento restantes corrigidos, que será usado para reconciliação em faturas posteriores.
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
O status da fatura no marco é atualizado de <b>Fatura do cliente lançada</b> para <b>Pronto para Faturar</b>.
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
Com suporte </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
