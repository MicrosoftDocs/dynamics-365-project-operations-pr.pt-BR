---
title: Gerenciar vários clientes em contratos de projeto
description: Este tópico fornece informações sobre como gerenciar vários clientes em um contrato de projeto.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5554cb062710c3587d81b1a29771a7af84d2d05f
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643142"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Gerenciar vários clientes em contratos de projeto

Este tópico fornece informações sobre como gerenciar vários clientes em um contrato de projeto. Você pode usar um contrato de projeto quando um acordo contratual para vários clientes é necessário para financiar um negócio. Na página **Contrato do Projeto**, a guia **Resumo** inclui informações sobre o cliente principal de um negócio. Outros clientes que participam do negócio podem ser adicionados à guia **Clientes**.

Todos os clientes do contrato na guia **Clientes** do contrato do projeto serão usados por padrão como clientes da linha do contrato em quaisquer novas linhas do contrato baseadas no projeto criadas para o contrato do projeto. As linhas de contrato baseadas no projeto existentes não herdarão novos registros de clientes de contrato que forem criados posteriormente.

Você pode adicionar, atualizar ou excluir clientes de contrato e clientes de linha de contrato a qualquer momento antes que o contrato seja ganho. Um cliente no contrato do projeto deve ser configurado como um cliente na empresa proprietária ou na entidade legal na página **Clientes**. As entidades legais são configuradas no módulo **Gerenciamento e contabilidade de projeto** do Dynamics 365 Project Operations e estão disponíveis como empresas nos módulos **Vendas do Projeto** e **Entrega** do Project Operations.

## <a name="primary-customers"></a>Clientes principais

O cliente potencial na guia **Resumo** do contrato do projeto é o cliente principal do contrato. Você não pode atualizar o cliente principal na lista de clientes do contrato. Se tentar excluir o cliente principal de uma lista de clientes do contrato, você receberá uma mensagem de erro informando que o registro do cliente principal em um contrato não pode ser excluído. Em vez disso, altere o cliente no campo **Cliente potencial** na guia **Resumo** do contrato do projeto. Quando você atualiza esse campo, o cliente recém-selecionado é adicionado como um novo cliente do contrato com o sinalizador **Principal** definido como **Sim**. O cliente principal anterior ainda será um cliente no contrato. No entanto, ele não será mais o cliente principal.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Criar, atualizar ou excluir um registro de cliente do contrato

Você pode criar, atualizar ou excluir um cliente do contrato na guia **Clientes do Contrato** guia na página **Contrato**. Os campos a seguir estão incluídos no registro de cliente do contrato de um contrato de projeto.

| **Campo** | **Local** | **Descrição** | 
| --- | --- | --- | 
| Conta | Grade editável na guia **Clientes do Contrato** e as páginas principal e de criação rápida para um cliente do contrato. | Lista todas as contas ativas. Este campo será bloqueado após a criação do registro. Para atualizar o registro, você deve excluí-lo e, em seguida, recriá-lo. Se você tiver registrado dados reais ou se o registro do cliente do contrato for um cliente principal, não será possível excluir o registro. Quando uma linha do contrato é criada, os clientes do contrato são copiados como clientes da linha do contrato. |
| Percentual de Cobrança Dividida | Grade editável na guia **Clientes do Contrato** e as páginas principal e de criação rápida para um cliente do contrato. | Representa a porcentagem de cada transação de vendas não cobrada atribuída ao cliente do contrato. Quando novas linhas de contrato do projeto são criadas, a porcentagem de divisão de cobrança é copiada nas novas linhas de contrato criadas e nos clientes de linha de contrato do projeto. |
| Nome do Contato para Cobrança | Grade editável na guia **Clientes do Contrato** e as páginas principal e de criação rápida para um cliente do contrato. | Este campo de texto deve ser usado para identificar a pessoa de contato da fatura para o cliente. Os valores padrão são provenientes do registro da conta relacionada. O nome do contato é copiado no campo **Nome do Contrato para Cobrança** na fatura que é gerada para o cliente. |
| Nome para Cobrança | Grade editável na guia **Clientes do Contrato** e as páginas principal e de criação rápida para um cliente do contrato. | Use esse campo para identificar a pessoa de contato da fatura para o cliente. Os valores padrão são provenientes do registro da conta relacionada. O nome é copiado no campo **Nome do Contrato para Cobrança** na fatura gerada para o cliente. |
| Condições de Pagamento | Grade editável na guia **Clientes do Contrato** e as páginas principal e de criação rápida para um cliente do contrato. | Os valores padrão são provenientes do registro da conta relacionada. Os termos são copiados no campo **Nome do Contrato para Cobrança** na fatura que é gerada para o cliente. |
| Empresa Proprietária | Grade editável na guia **Clientes do Contrato do Projeto** e as páginas principal e de criação rápida para um cliente do contrato do projeto. | A entidade legal na qual o cliente está configurado no módulo **Gerenciamento e contabilidade de projeto**. Este campo é somente leitura e está definido como a empresa proprietária do contrato do projeto.</br>A lista de clientes para adicionar no campo **Conta** já está filtrada para a lista da empresa proprietária no módulo **Gestão e contabilidade de projetos** de Project Operations. A empresa proprietária é igual à entidade legal no módulo **Gerenciamento e contabilidade de projeto** do Project Operations. Todos os custos e receitas provenientes do projeto são registrados na Contabilidade da empresa proprietária. |
| É Arredondamento | Grade editável na guia **Clientes do Contrato** e as páginas principal e de criação rápida para um cliente do contrato. | Indica se o cliente é um cliente de arredondamento padrão para o negócio. Só pode haver um cliente de arredondamento em um contrato de projeto. Quando divisões de custo e vendas não faturadas em quantidade e levam a uma diferença de arredondamento, essa diferença é aplicada aos dados reais que são mapeados para esse cliente. |
| Limite de NTE (limite máximo) | Grade editável na guia **Clientes do Contrato** e as páginas principal e de criação rápida para um cliente do contrato. | Indica se há um limite negociado ou limite para o valor geral que será faturado para o cliente para a participação. O Limite de NTE (limite máximo) configurado no nível do cliente do contrato é avaliado com base nos dados reais de vendas não cobradas que fazem referência ao cliente do contrato. |

## <a name="edit-billing-split-percentages"></a>Editar porcentagens de divisão de cobrança

Você pode editar as porcentagens de divisão de cobrança editando a grade. Quando as porcentagens de divisão de cobrança não totalizarem 100%, ocorrerá um erro. Depois de editar uma porcentagem de divisão de cobrança, atualize a página **Contrato do Projeto** para remover o erro.

Você também pode selecionar **Distribuir Uniformemente** na subgrade do cliente do contrato do projeto. As divisões de cobrança são alocadas uniformemente entre todos os clientes no contrato do projeto. Se houver fator de arredondamento, ele será adicionado ao cliente de arredondamento. Um dos clientes do contrato sempre terá o sinalizador **Arredondamento** definido como **Sim**. Esse cliente é o cliente de arredondamento. Normalmente, o cliente de arredondamento também é o cliente principal do contrato, mas isso não é obrigatório.


[!INCLUDE[footer-include](../includes/footer-banner.md)]