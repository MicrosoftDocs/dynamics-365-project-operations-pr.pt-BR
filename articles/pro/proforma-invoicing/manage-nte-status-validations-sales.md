---
title: Gerenciar status e validações que não devem ser excedidos
description: Este tópico fornece informações sobre as verificações de limite de NTE (limite máximo) realizadas no Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d51a61e441b004ae836037aefa172fdd20ac83ed
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003887"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Gerenciar status e validações que não devem ser excedidos 

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

## <a name="not-to-exceed-on-approvals"></a>Limite de NTE (limite máximo) em aprovações

Ao enviar uma entrada de tempo, despesa ou uso de material, é criado um registro de aprovação. Se a aprovação for cobrável e mapeada para uma linha de contrato de tempo e material, o sistema concluirá uma verificação de validação NTE (limite máximo) nos seguintes níveis:

  - Verifique o limite configurado para o cliente na linha do contrato do projeto
  - Verifique o limite configurado na linha do contrato
  - Verifique o limite configurado para o cliente
  - Verifique o limite configurado no contrato

As verificações em cada nível envolvem a garantia de que o valor das vendas nesta aprovação não violará o NTE (limite máximo) nesse nível, após contabilizar a quantidade de lista de pendências de cobrança já registrada e a quantidade faturada até a data nesse nível.

Se a verificação for aprovada, a aprovação receberá um status de validação **Êxito**.

Se a verificação falhar, a aprovação receberá um status de validação **Falha**. O detalhe de validação NTE (limite máximo) informará ao usuário o nível em que a validação falhou.

Quando a entrada de tempo, despesa ou uso de material enviada é considerada não passível de cobrança, o status de validação que não deve ser excedido é definido como **Não aplicável** com o detalhe de validação equivalente a **Não aplicável**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>NTE (limite máximo) em dados reais de vendas não cobradas

Quando uma entrada de tempo, despesa ou uso de material é aprovada, são criados registros reais de custo e vendas não faturadas. Se o dado real de vendas não cobráveis criado for cobrável e mapeado para uma linha de contrato de tempo e material, o aplicativo executará uma verificação de validação NTE (limite máximo) nos seguintes níveis:

  - Verifique o limite configurado para o cliente da linha do contrato do projeto
  - Verifique o limite configurado na linha do contrato
  - Verifique o limite configurado para o cliente
  - Verifique o limite configurado no contrato

As verificações em cada nível garantem que o valor das vendas no dado real não violará o NTE (limite máximo) nesse nível, após contabilizar a quantidade de lista de pendências de cobrança já registrada e a quantidade faturada até a data nesse nível.

Se a verificação for aprovada, o dado real de vendas não cobradas receberá um status de NTE (limite máximo) **Confirmado**.

Se a verificação falhar, o dado real de vendas não cobradas receberá um status de NTE (limite máximo) **Falha**. O detalhe de validação informa ao usuário o nível em que a validação falhou.

Quando o dado real de vendas não cobradas for considerado não cobrável ou complementar, se não houver limite NTE (limite máximo) em qualquer um dos quatro níveis, ou se o dado real criado for Custo, Retenção, Unidade de Recursos ou Vendas Interorganizacionais, os campos **Status de NTE (limite máximo)** e **Detalhe da Validação do NTE (limite máximo)** deverão ser definidos como **Não Aplicável**.

## <a name="reset-the-not-to-exceed-status"></a>Redefinir o status de NTE (limite máximo)

Você pode fazer uma redefinição em massa do status de NTE (limite máximo). Os gerentes de projeto podem ajustar a validação que não deve ser excedida para priorizar o faturamento de determinado corpo de trabalho, tempo, despesa ou uso de material em relação a outros já comprometidos com o valor disponível que não deve ser excedido.

Após o status de NTE (limite máximo) ser redefinido em dados reais de vendas não cobradas, o valor confirmado será reduzido. O gerente de projeto pode selecionar outra entrada de trabalho, tempo, despesa ou uso de material que antes falhou na validação e reavaliação de não excedido. Com a redução do valor comprometido, esses dados reais passam a ser validados, o que auxilia o gerente de projetos a exercer maior influência e controle sobre as transações faturáveis desse período.

Para redefinir o status de NTE (limite máximo), selecione um ou mais dados reais da exibição **Lista de Pendências de Cobrança de Hora e Materiais** ou **Dados Reais** e selecione **Redefinir Status de NTE (limite máximo)**.

O status de NTE (limite máximo) é redefinido como **Não Avaliado** em todos os dados reais selecionados relevantes. Os dados reais com o status de NTE (limite máximo) redefinido são dados reais de vendas não cobradas que ainda não foram faturadas, não em uma fatura de rascunho, e são marcadas como cobráveis. Outros dados reais selecionados são ignorados.

## <a name="reevaluate-not-to-exceed-status"></a>Reavaliar status de NTE (limite máximo)

Você pode fazer uma reavaliação em massa do status de NTE (limite máximo). A reavaliação do status de NTE (limite máximo) é útil quando:

  - Houve uma renegociação de limites de NTE (limite máximo) com o cliente e será necessário reavaliar os dados reais.
  - O gerente de projeto deseja ajustar a lista de pendências de vendas não cobradas priorizando um corpo de trabalho em detrimento de outro.

Para reavaliar o status de NTE (limite máximo), selecione um ou mais dados reais da exibição **Lista de Pendências de Cobrança de Hora e Materiais** ou **Dados Reais** e selecione **Reavaliar Status de NTE (limite máximo)**.

Todos os dados reais selecionados relevantes com um limite de NTE (limite máximo) serão avaliados em relação à configuração de NTE (limite máximo). Os dados reais que são relevantes para reavaliar o status de NTE (limite máximo) são dados reais de vendas não cobradas que não são faturadas, não em uma fatura de rascunho, e são marcadas como cobráveis. Outros dados reais selecionados.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
