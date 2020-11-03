---
title: Visão geral das dimensões de preço
description: Este tópico fornece informações sobre as dimensões de preço no Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071535"
---
# <a name="pricing-dimensions-overview"></a>Visão geral das dimensões de preço

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

As dimensões que são usadas em recursos humanos para configurar preço e custos são divididas em duas categorias:

- Pessoas
- Trabalho planejado

Por isso, há dois tipos de valor de dimensão de preço disponíveis:

- **Conjuntos de opções** : dimensões que são enumerações fixas para um conjunto de valores.
- **Valores baseados em entidade** : dimensões que podem ser um conjunto variado de valores.

## <a name="pricing-dimensions"></a>Dimensões de preço

O Dynamics 365 Project Operations é fornecido com um conjunto padrão de dimensões de preços. É possível exibir essas dimensões de preços acessando **Project Operations** > **Parâmetros**. No registro do parâmetro, na guia **Dimensões de preço baseadas em valor** , verifique se a função **msdyn_resourcecategory** e a unidade organizacional de recursos **msdyn_organizationalunit** têm os campos **Aplicável às vendas** e **Aplicável ao custo** definidos como **Sim**. Com esses campos habilitados, você pode configurar o preço e o custo para cada combinação de função e unidade organizacional.

Se precisar precificar ou colocar custo para seus recursos usando atributos adicionais, você poderá criar campos, entidades e dimensões personalizados.

## <a name="pricing-human-resource-time"></a>Precificação do tempo do recurso humano
Como uma organização precifica o tempo do recurso humano, às vezes, é uma consideração estratégica importante que afeta diretamente a lucratividade da organização. Trabalhe com as equipes e líderes financeiros quando sua organização estiver pronta para identificar como ela quer configurar tarifas de cobrança e custo para tempo do recurso humano.

Outras considerações para preço incluem considerar a reutilização de campos ou entidades que atualmente não são dimensões de preço, mas são aplicados como uma dimensão de preço para sua organização. Campos como **Categoria de Transação** ( **msdyn_transactioncategory** ) e **Recurso Reservável** ( **bookableresource** ) são exemplos de dimensões candidatas. 

Considere se sua dimensão de preço deve ser uma tabela ou um conjunto de opções. Se houver previsão de alterações nos valores de uma dimensão que excedam 10 ou 12, e forem necessários atributos adicionais nesses valores, você poderá criar uma entidade em vez de um conjunto de opções. Manter um conjunto de opções, como adição ou remoção de valores, exige um administrador ou desenvolvedor, enquanto a adição de novas linhas a uma tabela pode ser feita por qualquer usuário.

O exemplo a seguir mostra taxas de cobrança que são configuradas com base na função e na unidade organizacional de recursos à qual o recurso pertence. As taxas de custo geralmente se baseiam na faixa salarial do funcionário e na unidade organizacional a que ele pertence. Nesse exemplo, as tabelas de taxa de cobrança e taxa de custo serão parecidas com as que se seguem.

**Taxas de cobrança de exemplo**

| Função        | Unidades Organizacionais    |Unidade      |Preço      |Moeda  |
| ------------|-------------|----------|----------:|----------|
| Desenvolvedor   | Cabral EUA  |Hour | 200|USD     |
| Desenvolvedor   | Cabral India |Hour|   112|USD     |


**Taxas de custo de exemplo**

| Faixa Salarial     | Unidades Organizacionais    |Unidade      |Preço      |Moeda  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Cabral EUA  |Hour | 145|USD     |
| My company_Band2 | Cabral India |Hour|   67|USD     |
