---
title: Consulta sobre agendamento de despesas de prêmios federais
description: Este tópico fornece informações sobre a consulta sobre agendamento de despesas de prêmios federais.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010052"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Consulta sobre agendamento de despesas de prêmios federais

[!include [banner](../includes/banner.md)]

De acordo com a Circular A-133 do Office of Management and Budget, as agências que recebem fundos federais estão sujeitas a exigências de auditoria, também conhecidas como auditorias únicas. O processo de auditoria é usado para relatar as receitas e despesas dos subsídios federais de maneira recorrente. Parte do relatório de auditoria única inclui o agendamento de despesas de prêmios federais (Schedule of Expenditures of Federal Awards, SEFA).

A consulta sobre agendamento de despesas de prêmios federais inclui o título e número do catálogo de assistência doméstica federal (Catalog of Federal Domestic Assistance, CFDA), o número da concessão, o ano da concessão, o nome da agência federal que fornece os fundos e o nome da entidade de passagem. A consulta ocorre por um período específico. Geralmente, esse período é igual ao período das demonstrações financeiras, que é um ano fiscal.

A consulta inclui concessões que têm datas de projeção no intervalo de datas selecionado. A coluna **Agência concedente** da consulta mostra o cliente da concessão ou, para uma concessão de passagem, a agência concedente. Para uma concessão de passagem, a coluna **Agência de passagem** mostra o cliente da concessão. Se a concessão não for uma concessão de passagem, a coluna **Agência de passagem** ficará em branco.

## <a name="set-up-the-cfda-clusters"></a>Configurar os clusters do CFDA

Você deve configurar os clusters do CFDA que podem ser associados aos números do CFDA na consulta sobre agendamento de despesas de prêmios federais.

1. Acesse **Gerenciamento e contabilidade de projeto \> Configuração \> Concessões \> Clusters do catálogo de assistência doméstica federal**.
2. Selecione **Novo** para criar um cluster do CFDA.
3. Insira o nome do cluster.
4. Selecione **Salvar** para salvar suas alterações.

## <a name="set-up-cfda-numbers"></a>Configurar os números do CFDA

Você deve configurar os números do CFDA que podem ser adicionados às concessões e incluídos na consulta sobre agendamento de despesas de prêmios federais.

1. Acesse **Gerenciamento e contabilidade de projeto \> Configuração \> Concessões \> Números do catálogo de assistência doméstica federal**.
2. Selecione **Novo** para criar um número do CFDA.
3. Na coluna **Número**, insira o número do CFDA.
4. Pressione a tecla **Tab**.
5. Na coluna **Descrição**, insira o título do CFDA.
6. Pressione a tecla **Tab**.
7. Opcional: no campo **Cluster de programas**, inclua o cluster do CFDA apropriado.
8. Selecione **Salvar** para salvar suas alterações.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Configurar concessões para relatar para a consulta sobre agendamento de despesas de prêmios federais

1. Acesse **Gerenciamento e contabilidade de projeto \> Concessões \> Concessões** e selecione uma concessão existente.
2. Na FastTab **Configuração**, no campo **Catálogo de assistência doméstica federal**, atribua o número do CFDA. O número do CFDA na concessão determina o cluster do CFDA para relatórios.
3. Na FastTab **Informações de contato**, insira as informações do concedente seguindo estas etapas:

    1. No campo **Cliente da concessão**, insira o cliente que é responsável pela concessão. Para uma concessão existente, essas informações podem já ter sido inseridas.
    2. Indique se o cliente da concessão é o financiador. Se o cliente da concessão for o financiador, deixe a caixa de seleção **Passagem** desmarcada. Se outro cliente for o financiador e o cliente da concessão for responsável por gastar e rastrear o dinheiro, marque a caixa de seleção **Passagem**.

4. Se você marcou a caixa de seleção **Passagem** na etapa anterior, no campo **Agência concedente**, insira o cliente que forneceu a concessão. A agência concedente e o cliente da concessão não podem ser o mesmo cliente.

Aqui está um exemplo de concessão de passagem:

O governo federal financiou um projeto de infraestrutura para um estado. O governo federal deu o dinheiro para o estado gastar. Nesse caso, o governo federal é a agência concedente e o estado é o cliente da concessão.

> [!NOTE] 
> Quando você ativa o recurso pela primeira vez, os números do CFDA iniciais serão inseridos usando os números existentes nas concessões.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Excluir concessões de relatórios do SEFA com base no tipo de concessão

1. Acesse **Gerenciamento e contabilidade de projeto \> Configuração \> Concessões \> Tipos de concessão**.
2. Na FastTab **Informações padrão**, marque a caixa de seleção **Excluir do agendamento de despesas de prêmios federais**.
3. Selecione **Salvar** para salvar suas alterações.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Executar a consulta sobre agendamento de despesas de prêmios federais

1. Acesse **Gerenciamento e contabilidade de projeto \> Consultas e relatórios \> Consulta de concessão \> Agendamento de despesas de prêmios federais**.
2. Na seção **Parâmetros**, siga estas etapas:

    1. No campo **Intervalo de data**, selecione o código para o intervalo de data. Se desejar, nos campos **Data inicial** e **Data final**, defina o intervalo de data.
    2. Opcional: para incluir apenas transações cobradas como receita na consulta, defina a opção **Incluir somente receitas cobradas** como **Sim**.

## <a name="columns"></a>Colunas

A consulta sobre agendamento de despesas de prêmios federais inclui as seguintes colunas:

- Nome do cluster do catálogo de assistência doméstica federal
- Agência concedente
- Agência de passagem
- Nome da concessão
- ID da concessão
- ID do pedido de concessão
- Catálogo de assistência doméstica federal
- Recibos
- Despesas


[!INCLUDE[footer-include](../includes/footer-banner.md)]