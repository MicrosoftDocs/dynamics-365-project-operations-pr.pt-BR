---
title: Gerenciar vários clientes em linhas de cotação baseadas em projeto
description: Este tópico fornece informações sobre como gerenciar vários clientes em linhas de cotação baseadas em projeto.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea7f0a8207fc78914783f5b9c919b3243a0bb5a4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071304"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Gerenciar vários clientes em linhas de cotação baseadas em projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

As linhas de cotação baseadas em projeto suportam cenários em que cada linha de cotação tem uma lista de clientes que estão pagando por ela. Esta lista de clientes na linha de cotação baseada em projeto pode ser igual à lista de clientes na cotação. Você também pode alterar a lista de clientes para ser diferente. Quando uma cotação de projeto é ganha, a lista de clientes na linha de cotação baseada em projeto é copiada para a linha de contrato baseada em projeto correspondente para criar o contrato de projeto eventual. Os clientes na cotação baseada em projeto são copiados para o contrato do projeto.

Quando você fatura o eventual contrato do projeto, a lista de clientes na linha do contrato com base no projeto tem prioridade sobre a lista no contrato do projeto. A lista de clientes no contrato de projeto é usada apenas para padrões em novas linhas de contrato de projeto.

Todos os clientes de cotação na guia **Clientes** do padrão de cotação do projeto como clientes da linha de cotação em qualquer nova linha de cotação baseada em projeto criada para a cotação do projeto. Quaisquer linhas de cotação baseadas em projeto existentes não herdam novos registros de cliente de cotação criados depois delas.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Criar, atualizar ou excluir um registro de cliente de linha de cotação

Você pode criar, atualizar ou excluir um cliente de linha de cotação na guia **Clientes da linha de cotação** na página **Linha de cotação baseada em projeto**. Quando você adiciona um novo cliente na linha de cotação baseada em projeto, o cliente também é adicionado à cotação geral como um cliente de cotação, com uma porcentagem de divisão de faturamento padrão na cotação geral de 0%. O percentual de divisão do faturamento na cotação geral é copiado para novas linhas de cotação e para o contrato de projeto eventual. No entanto, ao faturar do contrato, a porcentagem de divisão do faturamento no nível da linha de cotação é usada, não a porcentagem de divisão do faturamento no nível geral do contrato. 

A tabela a seguir mostra os campos no registro do cliente da linha de cotação de uma linha de cotação baseada em projeto.

| Campo | Localização | Descrição e orientação | Impacto a jusante |
| --- | --- | --- | --- |
| **Conta** | Uma grade editável na guia **Clientes da linha de cotação** , o formulário principal e o formulário de criação rápida para um cliente com linha de cotação. | Lista todas as contas ativas. Este campo será bloqueado após a criação do registro. Se você precisar atualizar o campo, exclua e recrie o registro. Se você gravou algum real, não pode deletar o registro. | Quando você escolhe uma conta da lista mestre de contas para adicionar, o cliente da linha de cotação também é adicionado como um cliente de cotação. Quando uma cotação é ganha, os clientes da linha de cotação são copiados para os clientes da linha de contrato do projeto. |
| **Percentual de cobrança dividida** | Uma grade editável na guia **Clientes da linha de cotação** , o formulário principal e o formulário de criação rápida para um cliente com linha de cotação. | Representa a porcentagem de cada transação de vendas não faturada que será atribuída a este cliente de linha de cotação. | Copiado para clientes de linha de contrato de projeto. |
| **Limite máximo** | Uma grade editável na guia **Clientes da linha de cotação** , o formulário principal e o formulário de criação rápida para um cliente com linha de cotação. | Indica se há um limite negociado para o valor total que será faturado a este cliente para esta linha de cotação. | Copiado para os clientes da linha de contrato do projeto quando uma cotação é ganha. |
| **Empresa proprietária** | Uma grade editável na guia **Clientes da linha de cotação** , o formulário principal e o formulário de criação rápida para um cliente com linha de cotação. | A pessoa jurídica para a qual este cliente está configurado no módulo **Gestão e contabilidade de projetos**. Este campo é somente leitura e é definido para a empresa proprietária da própria cotação. A lista de clientes para adicionar no campo **Conta** já está filtrada para a lista da empresa proprietária no módulo **Gestão e contabilidade de projetos** de Project Operations. | A empresa proprietária equivale ao conceito de pessoa jurídica. Todos os custos e receitas provenientes deste projeto são contabilizados na contabilidade da empresa proprietária. |
| **É arredondado** | Uma grade editável na guia **Clientes da linha de cotação** , o formulário principal e o formulário de criação rápida para um cliente com linha de cotação. | Indica se este cliente é um cliente de arredondamento padrão para esta linha de cotação baseada em projeto. | Copiado para os clientes do contrato do projeto quando uma cotação é ganha. |

## <a name="edit-billing-split-percentages"></a>Editar porcentagens de divisão de cobrança

Você pode editar as porcentagens de divisão do faturamento in-line. Quando as porcentagens de divisão do faturamento não totalizam 100%, ocorre um erro. Depois de editar as porcentagens de divisão do faturamento, atualize a página da linha de cotação para remover o erro.

Use a ação distribuir uniformemente na subgrade dos clientes da linha de cotação para alocar divisões de faturamento para todos os clientes da linha de cotação. Se houver um fator de arredondamento, ele será adicionado ao cliente de arredondamento. Um dos clientes da linha de cotação é sempre marcado como o cliente de arredondamento, o que significa que o registro do cliente da linha de cotação tem o sinalizador de arredondamento definido como **Sim**. 
