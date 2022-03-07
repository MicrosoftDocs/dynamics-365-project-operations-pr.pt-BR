---
title: Contratos de projeto - Principais conceitos - lite
description: Este tópico fornece informações sobre os principais conceitos de contratos de projeto.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a797a4fef6276f6ed008b0e58eed4c7480ba3492bcc166a362d4ff2816acf777
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991427"
---
# <a name="concepts-unique-to-project-contracts"></a>Conceitos exclusivos de Contratos de Projeto

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tópico fornece os principais conceitos que você deve conhecer antes de começar a usar os contratos do Projeto no Dynamics 365 Project Operations.

## <a name="contracting-unit"></a>Unidade de Contratação

A unidade de contratação representa a divisão ou prática proprietária da entrega do projeto. Você pode configurar custos de recursos para cada unidade de contratação. Ao especificar o custo do recurso para um recurso, você também poderá configurar diferentes taxas de custo para os recursos. Essa unidade contratante toma emprestado esses recursos de outra divisão ou práticas dentro da empresa. As taxas de custo para os recursos são chamados de preços de transferência, empréstimo de recursos ou preços de câmbio. Ao configurar as taxas de custo para empréstimo de recursos de outras divisões, use a moeda de divisão de empréstimo.

## <a name="cost-currency"></a>Moeda de Custo

A moeda de custo é a moeda na qual os custos são informados na tela. Essa moeda é derivada da moeda anexada ao campo **Unidade de Contratação** no contrato e no projeto. Os custos podem ser registrados em qualquer moeda em um projeto. No entanto, há conversão de moeda da moeda em que os custos foram registrados para a moeda de custo do projeto quando mostrada na tela.

Como as taxas de câmbio na plataforma Common Data Service (CDS) não se baseiam em data, os totais na tela para o custo poderão mudar com o tempo se você atualizar as taxas de câmbio da moeda. No entanto, os custos registrados no banco de dados permanecem inalterados porque os valores são armazenados na moeda em que foram incorridos.

## <a name="sales-currency"></a>Moeda de Venda

A moeda de venda no Project Operations é a moeda em que os valores de venda estimados e reais são registrados e exibidos. A moeda de venda também é a moeda na qual o cliente é faturado pelo negócio. Em um contrato de projeto, a moeda de venda é padronizada no registro do cliente ou da conta e pode ser alterada quando o contrato é criado. Quando um contrato é criado fechando uma cotação como ganha, a moeda do contrato é a moeda padrão da cotação.

Quando você cria um contrato de projeto do zero, o campo **Moeda de Venda** não pode ser editado. As listas de preços de produto e de projeto são padronizadas com base nessa moeda no contrato.

Ao contrário dos custos, os valores de venda só podem ser registrados na moeda de venda.

## <a name="billing-method"></a>Método de Cobrança

Geralmente, há dois tipos de modelos de contratação para projetos, de valor fixo e baseados em consumo. Esses modelos são representados nas Operações do Projeto como métodos de cobrança com dois valores possíveis:

- Tempo e Material: um modelo de contrato baseado em consumo em que cada custo incorrido tem como contrapartida a receita correspondente. Conforme você estima ou incorre em mais custos, as vendas estimadas e reais correspondentes também aumentam. Especifique os limites que não devem ser excedidos nas linhas de contrato com esse método de cobrança, que limita a receita real. A receita estimada não é afetada pelos limites máximos.
- Preço Fixo: um modelo de contrato de valor fixo que indica que os valores de venda serão independentes dos custos incorridos. O valor de venda é fixo e não muda conforme você estima ou incorre em mais custos.

## <a name="project-price-lists"></a>Listas de preços de projeto

As listas de preços do projeto são usadas para preços padrão, não taxas de custo, para hora, despesas e outros componentes relacionados ao projeto. Pode haver várias listas de preços. Cada lista de preços tem sua própria validade de data para cada contrato de projeto. O Project Operations não é compatível com sobreposição de data efetiva em listas de preços.

Quando um contrato de projeto é criado com a obtenção de uma cotação de projeto, as listas de preços do projeto são copiadas com o nome e a data do contrato incluídos. Copiar essas informações constitui o preço personalizado para os componentes do projeto neste contrato de projeto.

## <a name="product-price-lists"></a>Listas de preços de produtos

As listas de preços de produto são usadas para preços padrão, não taxas de custo, para linhas baseadas em produtos em um contrato. Existe apenas uma lista de preços de produtos por contrato.

## <a name="transaction-classes"></a>Classes de Transação

O Project Operations é compatível com quatro tipos de classes de transação:

- Hora
- Despesa
- Material
- Taxa

Os valores de custo e de venda podem ser estimados e incorridos nas classes de transação Hora, Despesa e Material. Taxa é uma classe de transação somente de receita.

## <a name="work-entities-and-billing-entities"></a>Entidades de trabalho e Entidades de cobrança

As entidades que representam o trabalho são projetos e tarefas. As entidades que representam aspectos de cobrança são linhas de contrato. Você pode vincular diferentes entidades de trabalho a opções de cobrança, vinculando-as às linhas de contrato.

## <a name="multi-customer-deals"></a>Negócios com vários clientes

Os negócios com vários clientes têm mais de um cliente para faturar em um negócio. Os exemplos comuns incluem:

- Empresas OEM e seus parceiros: os parceiros e revendedores vendem um produto com alguns serviços de valor agregado, geralmente envolvendo um negócio específico com um cliente. O OEM se oferece para financiar uma parte do projeto. 

- Projetos do setor público: vários departamentos de um governo local concordam em financiar um projeto e são faturados de acordo com uma divisão previamente acordada. Por exemplo, um distrito escolar e o governo local concordam em financiar a construção de uma piscina.

## <a name="invoice-schedules"></a>Agendas de Fatura

As agendas de fatura são específicas para cada linha do contrato e são necessárias para que o faturamento automático funcione. Os agendamentos de faturas são criados com base em determinadas datas de início e de término e frequência de fatura. As agendas são usadas no estágio do contrato, quando o processo de criação automática de faturas é configurado. Quando um contrato de projeto é criado de uma cotação, a agenda de fatura é copiada para o contrato de projeto da cotação.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Alterações do contrato do Dynamics 365 Sales

Os contratos do Project Operations são criados nos contratos do Dynamics 365 Sales. No entanto, há alguns desvios e diferentes importantes na funcionalidade da qual você deve estar ciente:

- Os contratos do Project Operations têm dois tipos diferentes de linhas, um para projetos e um para produtos.
- Os contratos do Project Operations têm seu próprio formulário e elementos de interface do usuário, regras de negócios, lógica de negócios em plug-ins e scripts do lado do cliente que as tornam exclusivas dos contratos do Sales.

Por esses motivos, você não deve usar um contrato do Sales e um contrato do Project de forma intercambiável.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
