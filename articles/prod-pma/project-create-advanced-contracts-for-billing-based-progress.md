---
title: Criar contratos avançados para cobrança baseada no andamento
description: Este tópico explica como criar contratos de projeto para que você possa gerar faturas para clientes, com base em uma porcentagem do trabalho concluído.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071557"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Criar contratos avançados para cobrança baseada no andamento
[!include [banner](../includes/banner.md)]

Este tópico explica como criar contratos de projeto para que você possa criar faturas para clientes, com base em uma porcentagem do trabalho concluído. Os valores da fatura são calculados automaticamente para as categorias de orçamento de trabalho que você configurou para um projeto. O tempo da fatura é definido quando você negocia o contrato do projeto com o cliente.

Use os procedimentos neste tópico para configurar um contrato, um projeto associado e as regras de cobrança que calculam os valores das faturas para as categorias de orçamento de trabalho que você configurou para o projeto.

Depois de criar o contrato e o projeto, você pode configurar os detalhes do projeto. Por exemplo, você pode definir atividades e atribuir trabalhadores ao projeto.

## <a name="example"></a>Exemplo

Sua organização é uma empresa de desenvolvimento de software. Você concorda em desenvolver um pacote de contabilidade da folha de pagamento para um cliente por uma taxa total de 20.000 dólares americanos (USD). Sua organização concorda em faturar o cliente à medida que você completa porcentagens específicas do projeto. Você configura as seguintes categorias de projeto para o trabalho, de modo que possa usá-las no processo de faturamento:

- Consultoria
- Criar
- Instalação

Você também configura regras de cobrança que calculam automaticamente os valores das faturas para a porcentagem do trabalho do projeto concluído em cada categoria.

O gerente de orçamento cria um orçamento para as categorias do projeto. A quantidade de trabalho concluído é calculada automaticamente como uma porcentagem do trabalho real em comparação com os valores orçados.

## <a name="prerequisites"></a>Pré-requisitos

Antes de criar um projeto que usa regras de cobrança, você deve configurar as sequências numéricas para regras de cobrança e um diário de taxas que é usado para lançar cobranças em andamento.

1. Vá para **Gerenciamento e contabilidade de projeto** \> **Configuração** \> **Parâmetros de gerenciamento e contabilidade de projeto**.
2. Na página **Parâmetros de gerenciamento e contabilidade de projeto**, na guia **Número de sequências**, configure a sequência numérica que deseja usar quando as regras de faturamento são criadas.
3. Vá para **Gerenciamento e contabilidade de projeto** \> **Diários** \> **Taxa**.
4. Na página **Diário de taxas**, selecione **Novo** e digite o nome do diário.

## <a name="create-a-contract-for-progress-billings"></a>Criar um contrato para faturamento em andamento

Use este procedimento para criar um contrato de projeto para um projeto de preço fixo. Você cria uma fatura de projeto quando o trabalho concluído no projeto atinge uma porcentagem especificada.

1. Acesse **Gerenciamento e contabilidade de projeto** \> **Projetos** \> **Contratos do projeto**.
2. Na página **Contratos do projeto**, selecione **Novo**.
3. Na caixa de diálogo **Novo contrato de projeto**, defina os seguintes campos:

    - **Nome**
    - **Tipo de financiamento**
    - **Fonte de financiamento**
    - **Moeda de venda** – Por padrão, esta moeda é usada para faturas de clientes associadas ao contrato do projeto. Entretanto, você pode alterar a moeda de venda em uma fatura de cliente específica.

4. Selecione **OK**. As informações são copiadas para o cabeçalho da página **Contratos do projeto**.
5. Na página **Contratos do projeto**, preencha o restante das informações necessárias para o projeto.

## <a name="create-a-project-for-progress-billings"></a>Criar um projeto para faturamento em andamento

Siga estas etapas para criar um projeto e quaisquer subprojetos associados a um contrato de projeto.

1. Acesse **Gerenciamento e contabilidade de projeto** \> **Projetos** \> **Todos os projetos**.
2. Na página **Todos os projetos**, selecione **Novo**.
3. Na caixa de diálogo **Novo projeto**, no campo **Tipo de projeto**, selecione **Hora e material**.
4. Selecione um grupo de projetos. Um grupo de projetos define as informações de postagem dos projetos atribuídos ao grupo.
5. Selecione **Criar projeto**.
6. Depois que o projeto for criado, defina o estágio do projeto para **Em andamento**.

## <a name="create-a-budget-for-a-project"></a>Criar um orçamento para um projeto

Categorias de orçamento são usadas para calcular automaticamente os valores da fatura para a porcentagem de trabalho concluído em cada categoria. Siga estas etapas para criar categorias de orçamento para os custos estimados.

1. Acesse **Gerenciamento e contabilidade de projeto** \> **Projetos** \> **Todos os projetos**.
2. Na página **Todos os projetos**, selecione e abra o projeto que deseja.
3. Na página **Projetos**, no Painel de Ações, na guia **Plano**, no grupo **Orçamento**, selecione **Orçamento do projeto**.
4. Na página **Orçamento do projeto**, insira um custo estimado para cada categoria do projeto.

## <a name="create-billing-rules-for-progress-billings"></a>Criar regras de cobrança para cobranças em andamento

1. Acesse **Gerenciamento e contabilidade de projeto** \> **Projetos** \> **Contratos do projeto**.
2. Na página **Contratos do projeto**, selecione e abra um contrato de projeto.
3. Na página do contrato do projeto, na FastTab **Regras de cobrança**, selecione **Adicionar**.
4. Na página **Regra de cobrança**, no campo **Tipo de Linha**, selecione **Progresso**.
5. Na FastTab **Detalhes da linha de regra de cobrança**, no campo **Valor do contrato**, insira o valor total do contrato.
6. No campo **Categoria**, selecione a categoria para postar a transação de taxa.
7. No campo **Projeto**, selecione o projeto que usa esta regra de cobrança.
8. Opcional: atribua a regra de cobrança a projetos adicionais. Na FastTab **Projeto**, na seção **Projetos disponíveis**, selecione um projeto e, em seguida, selecione o botão de seta para a direita para adicioná-lo à seção **Projetos selecionados**.
9. Opcional: calcule o valor percentual que o cliente retém dos pagamentos de uma fatura. Na FastTab **Termos de retenção de pagamento**, selecione a fonte de financiamento e, em seguida, no campo **Porcentagem de retenção**, insira a porcentagem de retenção.
10. Repita essas etapas para criar regras de cobrança adicionais para o contrato do projeto.
