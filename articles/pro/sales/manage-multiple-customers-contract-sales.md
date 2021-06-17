---
title: Gerenciar vários clientes em contratos de projeto - lite
description: Este tópico fornece informações sobre como gerenciar vários clientes em contratos de projeto.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 31a12e44353160dde851e2b9b06148a31fbeb167
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002813"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Gerenciar vários clientes em contratos de projeto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Os contratos de projeto no Dynamics 365 Project Operations oferecem suporte ao cenário em que um contrato envolve vários clientes que estão financiando um negócio. A guia **Resumo** na página **Contrato do Projeto** inclui o campo **Cliente**. Este campo identifica o cliente principal do negócio. Outros clientes do negócio podem ser configurados na guia **Clientes** da página **Contrato do Projeto**.

Todos os clientes do contrato listados no contrato do projeto padrão como clientes da linha do contrato em quaisquer novas linhas do contrato baseadas em projeto que são criadas para o contrato do projeto. As linhas de contrato baseadas em projeto existentes não herdam novos clientes de contrato à medida que novos registros são criados.

As linhas de contrato baseadas em produto são automaticamente associadas ao cliente principal.

Os clientes de contrato e clientes de linha de contrato podem ser adicionados, atualizados ou excluídos a qualquer momento antes que o contrato seja ganho.

## <a name="primary-customer"></a>Cliente principal

O cliente listado na guia **Resumo** do contrato do projeto, pois o cliente potencial é o principal cliente do contrato. Ao tentar excluir o cliente principal da lista de clientes do contrato, você receberá uma mensagem de erro informando que o registro do cliente principal em um contrato não pode ser excluído.

O cliente principal não pode ser atualizado na lista de clientes do contrato. Em vez disso, altere o cliente potencial na guia **Resumo** do contrato. Quando este campo é atualizado na página **Resumo do Contrato**, o novo cliente é adicionado como um novo cliente do contrato com o sinalizador **Principal** definido. O cliente principal anterior ainda será um cliente no contrato.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Criar, atualizar ou excluir um registro de cliente do contrato

Um cliente do contrato pode ser criado, atualizado ou excluído da guia **Clientes** guia na página **Contrato do Projeto**. Os campos na tabela a seguir estão no registro do cliente do contrato de um contrato de projeto e devem ser mantidos em mente ao trabalhar com o contrato.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **Conta** | A grade pode ser editada na guia **Clientes de Contrato** e nos formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Lista todas as contas ativas. Este campo será bloqueado após a criação do registro. Para atualizar a conta, exclua o registro e recrie-o. Se você tiver registrado dados reais ou se o registro do cliente do contrato for um cliente principal, não será possível excluir o registro. | Os clientes do contrato são copiados como clientes da linha do contrato quando uma linha do contrato é criada. |
| **Percentual de Cobrança Dividida** | A grade pode ser editada na guia **Clientes de Contrato** e nos formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Representa a porcentagem de cada transação de vendas não cobrada que é atribuída a este cliente do contrato. | Copiado para novas linhas do contrato e para clientes da linha do contrato de projeto em novas linhas do contrato de projeto. |
| **Nome do Contato para Cobrança** | A grade pode ser editada na guia **Clientes de Contrato** e nos formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Este campo de texto deve ser usado para identificar a pessoa de contato da fatura para este cliente. Este campo é padronizado a partir do registro da conta relacionada. | Copiado para o campo **Nome do Contrato para Cobrança** na fatura que é gerada para este cliente. |
| **Nome para Cobrança** | A grade pode ser editada na guia **Clientes de Contrato** e nos formulários **Principal** e **Criação Rápida** para um cliente do contrato | Este campo de texto deve ser usado para identificar a pessoa de contato da fatura para este cliente. Este campo é padronizado a partir do registro da conta relacionada. | Copiado para o campo **Nome do Contrato para Cobrança** na fatura que é gerada para este cliente. |
| **Condições de Pagamento** | A grade pode ser editada na guia **Clientes de Contrato** e nos formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Os valores padrão a partir do registro da conta relacionada. | Copiado para o campo **Nome do Contrato para Cobrança** na fatura que é gerada para este cliente. |
| **É Arredondamento** | A grade pode ser editada na guia **Clientes de Contrato** e nos formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Indica se este cliente é um cliente de arredondamento padrão para esta oferta. Só pode haver um cliente de arredondamento em um contrato de projeto. | Quando divisões de custo e vendas não faturadas em quantidade levam a uma diferença de arredondamento, essa diferença é aplicada ao dado real que é mapeado para esse cliente. |
| **Limite de NTE (limite máximo)** | A grade pode ser editada na guia **Clientes de Contrato** e nos formulários **Principal** e **Criação Rápida** para um cliente do contrato | Indica se há um limite negociado ou limite para o valor geral que será faturado para o cliente para esta participação. | O **Limite de NTE (limite máximo)** configurada no nível do cliente do contrato será avaliado em **Dados Reais de Vendas não Cobradas** que referenciam esse cliente do contrato. |

## <a name="edit-billing-split-percentages"></a>Editar porcentagens de divisão de cobrança

As porcentagens de divisão de cobrança podem ser editadas usando a experiência de edição de grade em linha. Quando as porcentagens de divisão de cobrança não totalizarem 100%, você receberá um erro. Depois de editar as porcentagens de divisão de cobrança, atualize a página para ignorar o erro.

Você também pode selecionar **Distribuir Uniformemente** na subgrade **Clientes do Contrato** para alocar divisões de cobrança uniformemente para todos os clientes do contrato. Se houver um fator de arredondamento, ele será adicionado ao cliente de arredondamento. Um dos clientes do contrato é sempre marcado como o cliente de **arredondamento**, o que significa que o registro do cliente do contrato tem o sinalizador de arredondamento definido como **Sim**. Normalmente, esse é o cliente principal do contrato, mas também pode ser alterado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]