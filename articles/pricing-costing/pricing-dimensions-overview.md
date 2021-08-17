---
title: Visão geral das dimensões de precificação
description: Esse tópico fornece informações sobre as dimensões de precificação no Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 4b3b71c0b64a24f6914c70c4383eee654e7d4947ececaf9b4e6394f45a081a4c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001957"
---
# <a name="pricing-dimensions-overview"></a>Visão geral das dimensões de precificação

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As dimensões que são usadas em recursos humanos para configurar preço e custos são divididas em duas categorias:

- Pessoas
- Trabalho planejado

Por isso, há dois tipos de valor de dimensão de preço disponíveis:

- **Conjuntos de opções**: dimensões que são enumerações fixas para um conjunto de valores.
- **Valores baseados em entidade**: dimensões que podem ser um conjunto variado de valores.

## <a name="pricing-dimensions"></a>Dimensões de precificação

O Dynamics 365 Project Operations apresenta um conjunto padrão de dimensões de precificação. É possível exibir essas dimensões de precificaçãos acessando **Project Operations** > **Parâmetros**. No registro do parâmetro, na guia **Dimensões de precificação baseadas em valor**, verifique se a função **msdyn_resourcecategory** e a unidade organizacional de recursos **msdyn_organizationalunit** têm os campos **Aplicável às vendas** e **Aplicável ao custo** definidos como **Sim**. Com esses campos habilitados, você pode configurar o preço e o custo para cada combinação de função e unidade organizacional.

![Captura de tela dos parâmetros do Project Service com "Aplicável às Vendas" em destaque.](media/PS-OOB-parameters.png)

Se precisar precificar ou colocar custo para seus recursos usando atributos adicionais, você poderá criar campos, entidades e dimensões personalizados. Para obter mais informações, consulte os seguintes tópicos. 
  
  > [!NOTE]
  > Os procedimentos devem ser concluídos na ordem em que estão listados.

1. [Criar uma solução para dimensões de precificação personalizadas](../sales/create-solution-custompd.md)
2. [Criar campos e entidades personalizados](create-custom-fields-entities-pricing-dimensions.md)
3. [Adicionar campos personalizados a entidades transacionais e de configuração de preço ](add-custom-fields-price-setup-transactional-entities.md)
4. [Configurar campos personalizados como dimensões de precificação ](set-up-custom-fields-pricing-dimensions.md)
5. [Atualizar os atributos de plug-in para incluir novas dimensões de precificação](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Precificação do tempo do recurso humano
Como uma organização precifica o tempo do recurso humano, às vezes, é uma consideração estratégica importante que afeta diretamente a lucratividade da organização. Trabalhe com as equipes e líderes financeiros quando sua organização estiver pronta para identificar como ela quer configurar tarifas de cobrança e custo para tempo do recurso humano.

Outras considerações para preço incluem considerar a reutilização de campos ou entidades que atualmente não são dimensões de precificação, mas são aplicados como uma dimensão de preço para sua organização. Campos como **Categoria de Transação** (**msdyn_transactioncategory**) e **Recurso Reservável** (**bookableresource**) são exemplos de dimensões candidatas. 

Considere se sua dimensão de preço deve ser uma tabela ou um conjunto de opções. Se houver previsão de alterações nos valores de uma dimensão que excedam 10 ou 12, e forem necessários atributos adicionais nesses valores, você poderá criar uma entidade em vez de um conjunto de opções. Manter um conjunto de opções, como adição ou remoção de valores, exige um administrador ou desenvolvedor, enquanto a adição de novas linhas a uma tabela pode ser feita por qualquer usuário.

O exemplo a seguir mostra taxas de cobrança que são configuradas com base na função e na unidade organizacional de recursos à qual o recurso pertence. As taxas de custo geralmente se baseiam na faixa salarial do funcionário e na unidade organizacional a que ele pertence. Nesse exemplo, as tabelas de taxa de cobrança e taxa de custo serão parecidas com as que se seguem.

**Taxas de cobrança de exemplo**

| Função        | Unidades Organizacionais    |Unidade      |Preço      |Moeda  |
| ------------|-------------|----------|----------:|----------|
| Desenvolvedor   | Contoso US  |Hora | 200|USD     |
| Desenvolvedor   | Contoso Índia |Hora|   112|USD     |


**Taxas de custo de exemplo**

| Faixa Salarial     | Unidades Organizacionais    |Unidade      |Preço      |Moeda  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso US  |Hora | 145|USD     |
| My company_Band2 | Contoso Índia |Hora|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]