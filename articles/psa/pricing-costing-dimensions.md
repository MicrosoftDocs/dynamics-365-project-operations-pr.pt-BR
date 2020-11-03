---
title: Home page de dimensões de preço e custo
description: Este tópico fornece uma visão geral das dimensões de preço.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071469"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Home page de dimensões de preço e custo

As dimensões usadas para definir os preços e custos de mão de obra em organizações baseadas em projetos são influenciadas pelos seguintes atributos:

- Pessoas que realizam trabalhos semelhantes à experiência, função ou geografia delas
- Trabalho a ser executado semelhante à sua complexidade ou hora do dia

Devido à natureza típica desses atributos do trabalho e as pessoas necessárias para realizar o trabalho, existem dois tipos de valores de dimensão de preços disponíveis no Project Service Automation: 

- **Conjuntos de opções** - atributos que são enumerações fixas para um conjunto de valores.
- **Valores baseados em entidades** - atributos que podem ter um conjunto variado de valores finitos, mas que podem mudar com o tempo.

## <a name="pricing-dimensions"></a>Dimensões de preço

O PSA apresenta um conjunto padrão de dimensões de preço. É possível exibi-las acessando **Project Service** > **Parâmetros**. No registro do parâmetro, na guia **Dimensões de preço baseadas em valor** , verifique se a função **msdyn_resourcecategory** e a unidade organizacional de recursos **msdyn_organizationalunit** têm os campos **Aplicável às vendas** e **Aplicável ao custo** definidos como **Sim**. Isso permitirá configurar o preço e o custo para cada combinação de função e unidade organizacional.

![Captura de tela dos parâmetros do Project Service com "Aplicável às Vendas" em destaque](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Se você vem usando os campos prontos para uso da função e da unidade organizacional como dimensões de preço antes da versão 3 do PSA, não haverá qualquer mudança significativa. Você pode continuar usando o Project Service normalmente. 

Se precisar precificar ou colocar custo para seus recursos usando atributos adicionais, você poderá criar campos, entidades e dimensões personalizados. Para obter mais informações, consulte os tópicos a seguir. No entanto, observe que você deve concluir os procedimento na ordem lista abaixo:

- [Criar campos e entidades personalizados](create-custom-fields-entities.md)
- [Adicionar campos personalizados a entidades transacionais e de configuração de preço](field-references.md)
- [Configurar campos personalizados como dimensões de precificação ](set-up-pricing-dimensions.md)
- [Atualizar os atributos de plug-in para incluir novas dimensões de preço](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Precificação do tempo do recurso humano
Como uma organização precifica o tempo do recurso humano, às vezes, é uma consideração estratégica importante que afeta diretamente a lucratividade da organização. Trabalhe com as equipes e líderes financeiros quando sua organização estiver pronta para identificar como ela quer configurar tarifas de cobrança e custo para tempo do recurso humano.

Outras considerações para preço incluem considerar a reutilização de campos ou entidades que atualmente não são dimensões de preço, mas são aplicados como uma dimensão de preço para sua organização. Campos como **Categoria de Transação** ( **msdyn_transactioncategory** ) e **Recurso Reservável** ( **bookableresource** ) são exemplos de dimensões candidatas. 

Considere se sua dimensão de preço deve ser uma tabela ou um conjunto de opções. Se houver previsão de alterações nos valores de uma dimensão que excedam 10 ou 12, e forem necessários atributos adicionais nesses valores, crie uma entidade em vez de um conjunto de opções. Manter um conjunto de opções, como adição ou remoção de valores, exige um administrador ou desenvolvedor, enquanto a adição de novas linhas a uma tabela pode ser feita por qualquer usuário empresarial.

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
