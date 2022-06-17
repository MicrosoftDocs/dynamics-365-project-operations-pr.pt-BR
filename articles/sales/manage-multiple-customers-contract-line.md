---
title: Gerenciar vários clientes em linhas de contrato baseadas em projeto
description: Este artigo fornece informações sobre como trabalhar com linhas de contrato e contratos que contêm vários clientes.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e0652d4b9cdb0489d4f191ef0f3b251e39262f5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914848"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Gerenciar vários clientes em linhas de contrato baseadas em projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As linhas de contrato baseadas em projeto podem incluir uma lista de clientes responsáveis pelo pagamento. Esta lista de clientes na linha de contrato baseada em projeto pode ser igual à lista de clientes no contrato, mas isso não é obrigatório. Quando uma cotação de projeto é obtida e um contrato de projeto é criado, a lista de clientes na linha de cotação é copiada para a linha de contrato correspondente. Os clientes da cotação são copiados para o contrato.

Quando o contrato do projeto é faturado, a lista de clientes na linha do contrato baseada em projeto tem prioridade sobre a lista de clientes no contrato. A lista de clientes no contrato de projeto é usada apenas para definir novas linhas de contrato.

Todos os clientes do contrato na guia **Clientes** do contrato do projeto padrão como clientes da linha do contrato em quaisquer novas linhas do contrato criadas para o contrato do projeto. As linhas de contrato existentes não herdarão os novos registros de cliente de contrato criados depois delas.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Criar, atualizar ou excluir um registro de cliente de linha de contrato

Você pode criar, atualizar ou excluir um cliente de linha de contrato da guia **Clientes de Linha de Contrato** na página **Linha de Contrato baseada em Projeto**. Quando um novo cliente é adicionado à linha do contrato baseado em projeto, ele também é adicionado ao contrato geral como um cliente do contrato com uma porcentagem de divisão de cobrança padrão de zero por cento. O percentual de divisão de cobrança no contrato geral é copiado para novas linhas de contrato e para o contrato de projeto eventual. No entanto, ao faturar do contrato, é a porcentagem de divisão de cobrança no nível da linha do contrato que é usada e não a porcentagem de divisão de cobrança no nível geral do contrato. 

Abaixo estão os campos no registro de linha de cliente Contrato de uma linha de contrato baseada em projeto para saber ao trabalhar com ela:

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Conta | Grade editável na guia **Clientes da Linha de Contrato** e os formulários Principal e Criação Rápida para um cliente da linha de contrato | Todas as contas ativas. Este campo será bloqueado após a criação do registro. Para atualizar o campo, exclua o registro e crie um novo registro. Se você gravou dados reais, não poderá excluir o registro. No entanto, você pode marcar a porcentagem de divisão da cobrança como zero para essa conta. Quando o registro é marcado como zero, qualquer custo futuro e dados reais de receita atribuídos ou divididos para este cliente são afetados. | Quando você escolhe uma conta da lista mestre de contas para adicioná-la e salvá-la, o cliente da linha do contrato também é adicionado como um cliente do contrato. Os clientes da linha de contrato são usados quando faturas são geradas. |
| Percentual de cobrança dividida | Grade editável na guia **Clientes da Linha de Contrato** e os formulários Principal e Criação Rápida para um cliente da linha de contrato | Este campo representa a porcentagem de cada transação de vendas não cobrada que será atribuída a este cliente de linha de contrato. | Clientes de linha de contrato e porcentagens de divisão de cobrança são usados quando dados reais são criados após a aprovação e quando a fatura é gerada. |
| Limite máximo | Grade editável na guia **Clientes da Linha de Contrato** e os formulários Principal e Criação Rápida para um cliente da linha de contrato | Indica se há um limite negociado ou limite para o valor geral que será faturado para este cliente para a linha do contrato. | O limite máximo para o cliente da linha do contrato é usado quando dados reais são criados e as faturas são geradas. |
| Empresa Proprietária | Grade editável na guia **Clientes da Linha de Cotação** e os formulários Principal e Criação Rápida para um cliente da linha de cotação | A entidade legal na qual este cliente está configurado. Este campo é somente leitura e é definido para a empresa proprietária da cotação. A lista de clientes para adicionar no campo **Conta** já está filtrada para a lista desta empresa proprietária. | O conceito de empresa proprietária equivale ao conceito de entidade legal. Todos os custos e receitas provenientes deste projeto são registrados na Contabilidade da empresa proprietária. |
| É Arredondamento | Grade editável na guia **Clientes da Linha de Contrato** e os formulários Principal e Criação Rápida para um cliente da linha de contrato | Este campo indica se este cliente é um cliente de arredondamento padrão para esta linha de contrato baseada em projeto. | Ao gerar um valor real de acordo com a porcentagem de divisão de cobrança, podem haver algumas diferenças de arredondamento. Este cliente é atribuído às diferenças de arredondamento neste caso. |

## <a name="edit-billing-split-percentages"></a>Editar porcentagens de divisão de cobrança

As porcentagens de divisão de cobrança podem ser editadas na grade. Quando as porcentagens de divisão de cobrança não totalizarem 100%, ocorrerá um erro. Depois de editar as porcentagens de divisão de cobrança, atualize a página para remover o erro.

Você também pode tentar selecionar **Distribuir Uniformemente** na subgrade do cliente da linha de contrato. Essa ação aloca uniformemente divisões de cobrança para todos os clientes de linha de contrato. Se houver fator de arredondamento, ele será adicionado ao cliente de arredondamento. Um cliente de linha de contrato é sempre marcado como o cliente de **Arredondamento** com o sinalizador **Arredondamento** definido como **Sim**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]