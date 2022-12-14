---
title: Conceitos exclusivos para cotações baseadas no projeto
description: Este artigo fornece informações sobre cotações de projetos no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824313"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Conceitos exclusivos para cotações baseadas no projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Antes de começar a usar cotações de projetos no Microsoft Dynamics 365 Project Operations, você deve estar ciente dos seguintes conceitos básicos:

## <a name="owning-company"></a>Empresa proprietária

A empresa proprietária representa a entidade legal proprietária da entrega do projeto. O cliente na cotação deve ser um cliente válido nessa entidade legal em aplicativos de finanças e operações. A moeda da empresa proprietária e a moeda da unidade contratante selecionada em uma cotação baseada em projeto devem corresponder.

## <a name="contracting-unit"></a>Unidade de contratação

Uma unidade de contratação representa a divisão ou prática proprietária da entrega do projeto. Você pode configurar custos de recursos para cada unidade de contratação. Ao especificar custos de recursos para um recurso em uma unidade de contratação, você pode configurar diferentes taxas de custo para recursos dos quais a unidade de contratação toma emprestado ou para outras divisões ou práticas na empresa. Essas taxas de custo são chamadas de preços de transferência, empréstimo de recursos ou preços de câmbio. Ao configurar o custo do empréstimo de recursos de outras divisões, é possível configurar as taxas de custo na moeda da divisão de empréstimo.

## <a name="cost-currency"></a>Moeda do custo

A moeda de custo no Project Operations é a moeda em que os custos são informados. Essa moeda é derivada da moeda anexada ao campo **Unidade de contratação** na cotação, contrato e projeto. Os custos de um projeto podem ser registrados em qualquer moeda. No entanto, há conversão de moeda da moeda em que os custos foram registrados para a moeda de custo do projeto.

Como as taxas de câmbio na plataforma Dataverse não se baseiam em data, os totais na tela para o custo poderão mudar com o tempo se você atualizar as taxas de câmbio da moeda. No entanto, os custos registrados no banco de dados permanecem inalterados porque os valores são armazenados na moeda em que foram incorridos.

## <a name="sales-currency"></a>Moeda de venda

A moeda de venda no Project Operations é a moeda em que os valores de venda estimados e reais são registrados e exibidos. Também é a moeda na qual o cliente é faturado pelo negócio. Em uma cotação de projeto, uma moeda de venda padrão é definida no registro do cliente ou da conta e pode ser alterada quando a cotação é criada. Contudo, a moeda de venda não pode ser alterada depois que a cotação é salva. As listas de preços de produto e de projeto padrão são definidas com base na moeda de venda da cotação.

Ao contrário dos custos, os valores de vendas podem ser registrados **somente** na moeda de vendas.

## <a name="billing-method"></a>Método de cobrança

Os projetos normalmente têm modelos de contratação baseados em taxas fixas e consumo. No Project Operations, o modelo de contratação de um projeto é representado pelo método de cobrança. O método de cobrança tem dois valores: tempo e material e preço fixo.

- **Hora e material**: um modelo de contratação baseado no consumo em que cada custo incorrido tem como contrapartida a receita correspondente. Conforme você estima ou incorre em mais custos, as vendas estimadas e reais correspondentes também aumentam. Você pode especificar limites máximos em linhas de cotação com esse método de cobrança. Dessa forma, você pode limitar a receita real. A receita estimada não é afetada pelos limites máximos.
- **Preço fixo**: um modelo de contrato de valor fixo em que os valores de venda são independentes dos custos incorridos. O valor de venda é fixo e não muda conforme você estima ou incorre em mais custos.

## <a name="project-price-lists"></a>Listas de preços do projeto

As listas de preços do projeto são listas de preços usadas para inserir preços padrão, não taxas de custo, para hora, despesas e outros componentes relacionados ao projeto. Pode haver várias listas de preços e cada lista pode ter sua própria data efetiva para cada cotação de projeto. O Project Operations não permite a sobreposição de data efetiva para listas de preços de projetos.

## <a name="product-price-lists"></a>Listas de preços de produtos

Listas de preços de produtos são listas de preços usadas para inserir preços padrão, não taxas de custo, para linhas baseadas em produtos em uma cotação. Existe apenas uma lista de preços de produtos por cotação.

## <a name="transaction-classes"></a>Classes de transação

O Project Operations é compatível com quatro tipos de classes de transação:

- Hora
- Despesa
- Material
- Taxa

Os valores de custo e de venda podem ser estimados e incorridos em classes de transações de **Hora**, **Despesa** e **Material**. **Taxa** é uma classe de transação somente de receita.

## <a name="work-entities-and-billing-entities"></a>Entidades de trabalho e entidades de cobrança

Projetos e Tarefas são entidades que representam o trabalho. Linhas de cotação e linhas de contrato são entidades que representam o faturamento. Você pode vincular diferentes entidades de trabalho a opções de cobrança, associando-as a Linhas de cotação ou de contrato.

## <a name="multi-customer-deals"></a>Negócios com vários clientes

Os negócios com vários clientes ocorrem quando há mais de um cliente por fatura. Aqui estão alguns exemplos típicos:

- **Empresas de fabricantes de equipamentos originais (OEM) e seus parceiros**: parceiros e revendedores vendem um produto que inclui serviços de valor agregado. Durante um acordo com um cliente, o OEM geralmente se oferece para financiar parte do projeto.
- **Projetos do setor público**: vários departamentos de um governo local concordam em financiar um projeto e são faturados de acordo com uma divisão previamente acordada. Por exemplo, um distrito escolar e a cidade ou departamento do governo local concordam em financiar a construção de uma piscina.

## <a name="invoice-schedules"></a>Agendamento de faturas

Os agendamentos de faturas são específicos para cada linha de cotação e são opcionais. Os agendamentos de faturas são criados com base em datas de início e término específicas e em uma frequência de faturas. São utilizados na fase de contrato, quando o processo de criação automática de faturas é configurado. Durante a fase de cotação, os agendamentos de faturas são opcionais. Se eles forem criados durante a fase de cotação, eles serão copiados para o contrato do projeto que é criado quando uma cotação do projeto é ganha.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Diferenças das cotações do Dynamics 365 Sales

As cotações do Project Operations são baseadas nas cotações do Dynamics 365 Sales. No entanto, você precisa estar ciente de algumas diferenças importantes na funcionalidade:

- As cotações do Project Operations têm dois tipos diferentes de linhas: uma para projetos e outra para produtos.
- As cotações do Project Operations têm sua própria página e elementos de interface do usuário (UI), regras de negócios, lógica de negócios em plug-ins e scripts do cliente que as tornam exclusivas das cotações do Sales.
- No Sales, você pode anexar vários pedidos a uma única cotação de venda. No Project Operations, você pode anexar apenas um contrato de projeto a uma cotação de projeto.
- Quando você ganha uma cotação de venda, a oportunidade relacionada pode permanecer aberta. Depois que uma cotação de projeto é ganha, a oportunidade relacionada é fechada.
- Uma cotação de venda não inclui alguns campos e conceitos que são incluídos em uma cotação de projeto. Os campos incluem **Unidade de Contratação**, **Gerente de Contas** e **Nome do Contato para Cobrança**.
- Cotações de vendas e cotações de projetos são identificadas pelo campo **Tipo** baseado no conjunto de opções. Para uma cotação de venda, o valor deste campo é **Com base no item**. Para uma cotação de projeto, o valor é **Com base no trabalho**.

Por causa dessas diferenças, não recomendamos que você use cotações de vendas e cotações do Project Operations de forma intercambiável.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
