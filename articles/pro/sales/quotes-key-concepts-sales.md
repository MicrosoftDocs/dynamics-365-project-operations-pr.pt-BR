---
title: Principais conceitos de cotação de projeto
description: Este tópico fornece informações sobre como usar cotações de projeto no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071352"
---
# <a name="project-quote-key-concepts"></a>Principais conceitos de cotação de projeto

_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_


Esteja ciente destes conceitos-chave antes de começar a usar cotações de projeto no Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unidade de contratação

A unidade de contratação representa a divisão ou prática proprietária da entrega do projeto. Você pode configurar custos de recursos para cada unidade de contratação. Ao especificar o custo do recurso para um recurso na unidade de contratação, você também poderá definir diferentes taxas de custo para os recursos dos quais essa unidade de contratação toma emprestado, ou outra divisão ou práticas dentro da empresa. Eles são chamados de preços de transferência, empréstimo de recursos ou preços de câmbio. Ao configurar o custo do empréstimo de recursos de outras divisões, você também pode optar por configurar essas taxas de custo na moeda da divisão que faz o empréstimo.

## <a name="cost-currency"></a>Moeda do custo

A moeda de custo no Project Operations é a moeda na qual os custos são informados. Essa moeda é derivada da moeda anexada ao campo **Unidade de contratação** na cotação, contrato e projeto. Os custos podem ser registrados em qualquer moeda em um projeto. No entanto, há conversão de moeda da moeda em que os custos foram registrados para a moeda de custo do projeto.

Como as taxas de câmbio na plataforma CDS não se baseiam em data, os totais na tela para o custo poderão mudar com o tempo se você atualizar as taxas de câmbio. No entanto, os custos registrados no banco de dados permanecem inalterados porque os valores são armazenados na moeda em que foram incorridos.

## <a name="sales-currency"></a>Moeda de venda

A moeda de venda no Project Operations é a moeda em que os valores de venda estimados e reais são registrados e exibidos. Também é a moeda na qual o cliente é faturado pelo negócio. Em uma cotação de projeto, a moeda de venda é padronizada no registro do cliente ou da conta e pode ser alterada quando a cotação é criada. Depois que a cotação é salva, a moeda de venda não pode ser alterada. As listas de preços de produto e de projeto são padronizadas com base na moeda de venda da cotação.

Ao contrário dos custos, os valores de venda só podem ser registrados na moeda do Sales.

## <a name="billing-method"></a>Método de cobrança

Os projetos normalmente têm modelos de contratação baseados em taxas fixas e consumo. Isso é representado no Project Operations como **Método de Cobrança** e tem dois valores: hora e material e preço fixo.

- **Hora e material:** é um modelo de contrato baseado no consumo em que cada custo incorrido tem como contrapartida a receita correspondente. Conforme você estima ou incorre em mais custos, as vendas estimadas e reais correspondentes também aumentam. Você pode especificar limites máximos em linhas de cotação com esse método de cobrança. Isso colocará um limite na receita real. A receita estimada não é afetada pelos limites máximos.
- **Preço fixo:** é um modelo de contrato de taxa fixa que indica que os valores de venda serão independentes dos custos incorridos. O valor de venda é fixo e não muda conforme você estima ou incorre em mais custos.

## <a name="project-price-lists"></a>Listas de preços do projeto

As listas de preços do projeto são listas de preços usadas para preços padrão, não taxas de custo, para hora, despesas e outros componentes relacionados ao projeto. Pode haver várias listas de preços e cada lista pode ter sua própria data efetiva para cada cotação de projeto. O Project Operations não é compatível com sobreposição de data efetiva em listas de preços.

## <a name="product-price-lists"></a>Listas de preços de produtos

Listas de preços de produtos são listas de preços usadas para preços padrão, não taxas de custo, para linhas baseadas em produtos em uma cotação. Existe apenas uma lista de preços de produtos por cotação.

## <a name="transaction-classes"></a>Classes de transação

O Project Operations é compatível com quatro tipos de classes de transação:

- Hora
- Despesa
- Material
- Taxa

Os valores de custo e de venda podem ser estimados e incorridos nas classes de transação Hora, Despesa e Material. Taxa é uma classe de transações somente de receita.

## <a name="work-entities-and-billing-entities"></a>Entidades de trabalho e entidades de cobrança

As entidades que representam o trabalho são Projetos e Tarefas. As entidades que representam a cobrança são Linhas de cotação e Linhas de contrato. Você pode vincular diferentes entidades de trabalho a opções de cobrança, associando-as a Linhas de cotação ou de contrato.

## <a name="multi-customer-deals"></a>Negócios com vários clientes

Os negócios com vários clientes ocorrem quando há mais de um cliente para faturar. Os exemplos comuns incluem:

- **Empresas OEM e seus parceiros:** parceiros e revendedores vendem um produto com serviços de valor agregado. Normalmente, esse é um cenário em que, durante um negócio específico com um cliente, o OEM se oferece para financiar uma parte do projeto. 

- **Projetos do setor público:** vários departamentos de um governo local concordam em financiar um projeto e são faturados de acordo com uma divisão previamente acordada. Por exemplo, um distrito escolar e a cidade ou departamento do governo local concordam em financiar a construção de uma piscina.

## <a name="invoice-schedules"></a>Agendamento de faturas

Os agendamentos de faturas são específicos para cada linha de cotação e também são opcionais. Os agendamentos de faturas são criados com base em determinadas datas de início e de término e frequência de fatura. Os agendamentos de faturas são utilizados na fase do contrato, quando o processo de criação automática de faturas é configurado. Na fase de cotação, os agendamentos são opcionais. Quando os agendamentos de faturas são criados no estágio **Cotação** , eles são copiados para o contrato do projeto que é criado quando a cotação de um projeto vence.

## <a name="changes-from-dynamics-365-sales-quote"></a>Mudanças na cotação do Changes from Dynamics 365 Sales:

As cotações do Project Operations são baseadas nas cotações do Dynamics 365 Sales. No entanto, você precisa estar ciente de algumas diferenças importantes na funcionalidade:

- As ações **Revisar** e **Ativar** não são compatíveis.
- As cotações do Project Operations têm dois tipos diferentes de linhas. Uma é para projetos e a outra é para produtos.
- As cotações do Project Operations têm seu próprio formulário e elementos de interface do usuário, regras de negócios, lógica de negócios em plug-ins e scripts do lado do cliente que as tornam exclusivas das cotações do Sales.

Por esses motivos, não é recomendável usar uma cotação do Sales e uma cotação do Project Operations de forma intercambiável.
