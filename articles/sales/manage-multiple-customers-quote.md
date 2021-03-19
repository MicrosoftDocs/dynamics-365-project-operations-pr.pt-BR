---
title: Gerenciar vários clientes em uma cotação de projeto
description: Este tópico fornece informações sobre como trabalhar em cotações que envolvem vários clientes que financiarão o projeto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2b57d052d6b50ee420249cf5441077b092b4e13f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277864"
---
# <a name="manage-multiple-customers-on-a-project-quote"></a>Gerenciar vários clientes em uma cotação de projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As cotações de projeto viabilizam o cenário em que a proposta envolve vários clientes que financiarão o negócio. A guia **Resumo** da cotação tem o campo **Cliente potencial**, que identifica o cliente principal da oferta. Outros clientes do negócio podem ser configurados na guia **Clientes** da cotação do projeto.

Todos os clientes de cotação na guia **Clientes** do padrão de cotação do projeto como clientes da linha de cotação em qualquer **nova** linha de cotação baseada em projeto criada para a cotação. Quaisquer linhas de cotação baseadas em projeto existentes não herdam novos registros de cliente de cotação criados depois delas.

É possível adicionar, atualizar ou excluir clientes de cotação e clientes de linha de cotação a qualquer momento antes de a cotação ser ganha. Um cliente válido na cotação deve ser configurado como um cliente na empresa proprietária ou pessoa jurídica na página **Clientes**. As entidades legais são configuradas no módulo **Gerenciamento e contabilidade de projeto** do Dynamics 365 Project Operations e estão disponíveis como Empresas nos módulos **Vendas do Projeto e Entrega** do Project Operations.

## <a name="concept-of-a-primary-customer"></a>Conceito de cliente principal

O cliente listado na guia **Resumo** da cotação do projeto como o cliente potencial é o principal cliente da cotação. Se você tentar excluir o cliente principal da lista de clientes da cotação, receberá um erro informando que um registro do cliente principal em uma cotação não pode ser excluído.

O cliente principal não deve ser atualizado a partir da lista de clientes na cotação. No entanto, você pode influenciar o cliente principal alterando o cliente potencial na guia **Resumo** da cotação. Quando este campo é atualizado no **Resumo da Cotação**, o cliente potencial recém-selecionado é adicionado como um novo cliente da cotação com o sinalizador **Principal** definido. O antigo cliente potencial ainda será um cliente na cotação.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Criar, atualizar ou excluir um registro de cliente de linha de cotação

Um cliente de cotação pode ser criado, atualizado ou excluído na guia **Clientes da cotação** na página **Citar**. Os campos listados na seguinte tabela estão no registro do cliente da cotação de uma cotação de projeto.

| **Campo** | **Local** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Conta | Grade editável na guia **Clientes de cotação**, o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação. | Lista todas as contas ativas. Este campo será bloqueado após a criação do registro. Se você quiser atualizá-lo, exclua e recrie o registro. Se você tiver registrado quaisquer dados reais, ou se o registro do cliente da cotação for um cliente principal, você terá permissão para excluir o registro. | Quando uma linha de cotação é criada, os clientes da cotação são copiados para os clientes da linha de cotação do projeto. Quando uma cotação é ganha, os clientes da cotação são copiados para os clientes do contrato de projeto. |
| Percentual de cobrança dividida | Grade editável na guia **Clientes de cotação**, o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação. | Represente a porcentagem de cada transação de vendas não faturada que será atribuída a este cliente da cotação. | Copiado para novas linhas de cotação criadas e para clientes de contrato de projeto. |
| Nome do Contato para Cobrança | Grade editável na guia **Clientes de cotação**, o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação. | Este é um campo de texto e deve ser usado para identificar a pessoa de contato da fatura para este cliente. Eles são padronizados a partir do registro da conta relacionado | Copiado para os clientes do contrato do projeto quando uma cotação é ganha e, por sua vez, para o campo nome Contrato para Cobrança na fatura que é gerada para este cliente. |
| Nome para Cobrança | Grade editável na guia **Clientes de cotação**, o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação. | Este campo de texto deve ser usado para identificar a pessoa de contato da fatura para este cliente. | Copiado para os clientes do contrato do projeto quando uma cotação é ganha e, por sua vez, para o campo nome **Contrato para Cobrança** na fatura que é gerada para este cliente. |
| Condições de Pagamento | Grade editável na guia **Clientes de cotação**, o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação. | Este é um conjunto de opções com valores padrão do registro da conta relacionado. | Copiado para os clientes do contrato do projeto quando uma cotação é ganha e, por sua vez, para o campo nome **Contrato para Cobrança** na fatura que é gerada para este cliente. |
| É Arredondamento | Grade editável na guia **Clientes de cotação**, o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação. | Indica se este cliente é um cliente de arredondamento padrão para esta oferta. | Copiado para os clientes do contrato do projeto quando uma cotação é ganha. |
| Empresa Proprietária | Grade editável na guia **Clientes de cotação**, o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação. | A pessoa jurídica para a qual este cliente está configurado no módulo **Gestão e contabilidade de projetos**. Este campo é somente leitura e é definido para a empresa proprietária da própria cotação. A lista de clientes para adicionar no campo **Conta** já está filtrada para a lista desta empresa proprietária no módulo **Gestão e contabilidade de projetos** de Project Operations. | A empresa proprietária equipara-se ao conceito de pessoa jurídica no módulo **Gestão e contabilidade de projetos** de Project Operations. Todos os custos e receitas provenientes deste projeto são contabilizados na contabilidade da empresa proprietária, |
| Limite máximo | Grade editável na guia **Clientes de cotação**, o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação. | Indica se há um limite negociado ou limite para o valor total que será faturado a este cliente para este contrato. | Copiado para os clientes do contrato do projeto quando uma cotação é ganha. |

## <a name="editing-billing-split-percentages"></a>Editar porcentagens de divisão de cobrança

Você pode editar as porcentagens de divisão de cobrança usando a experiência de edição de grade em linha. Quando as porcentagens de divisão do cobrança não totalizam 100%, ocorre um erro. Depois de atualizar as porcentagens de divisão de cobrança, atualize a página para remover o erro.

Você também pode tentar selecionar **Distribuir Uniformemente** na subgrade dos clientes de cotação. Esta ação aloca divisões de cobrança para todos os clientes da cotação. Se houver qualquer fator de arredondamento, ele será adicionado ao cliente de arredondamento. Um dos clientes da cotação é sempre marcado como o cliente de arredondamento. Isso significa que o registro do cliente da cotação tem o sinalizador **Arredondamento** definido como **Sim**. Normalmente, este é o cliente principal da cotação, mas isso pode ser alterado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]