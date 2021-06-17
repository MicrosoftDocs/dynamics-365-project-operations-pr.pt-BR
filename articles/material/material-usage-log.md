---
title: Registre o uso de material em projetos e tarefas de projeto
description: Este tópico fornece informações sobre como registrar o uso de material em projetos e tarefas de projeto.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c739d7fabb96a845eaf139fcc9eab21247b0860
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001547"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Registre o uso de material em projetos e tarefas de projeto

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Como uma equipe de projeto utiliza tarefas em um projeto, eles consomem ou usam materiais. Um registro de uso de material fornece uma maneira de registrar esse uso para que possa ser aprovado pelo gerente de projeto e, por fim, faturado para o cliente. 

Para registrar o uso de catálogo ou materiais fora do catálogo e enviá-los ao aprovador, siga estas etapas: 

1. No painel de navegação, selecione **Uso de Material** e, depois, selecione **Novo**.
2. Na página **Novo Uso de Material**, insira as informações de uso do material necessárias e selecione **Salvar**.

A tabela a seguir fornece informações sobre os campos na página **Registro de Uso de Material**. 

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Descrição | Uma descrição do uso específico do material. | Não há impacto posterior para este campo. |
| Data | A data em que se espera que o material seja usado. | Não há impacto posterior para este campo. |
| Project | Uma lista de projetos que estão ativos. | Selecionar um projeto para um registro de uso de material impacta o campo **Tarefa** para mostrar apenas as tarefas que estão no projeto. |
| Tarefa | Uma lista de tarefas para o projeto, incluindo tarefas de resumo e nó folha. | Selecionar uma tarefa para um registro de uso de material impacta o custo real do material e as vendas reais do material para uma tarefa. Se este campo estiver vazio, o custo de uso do material e as vendas correspondentes serão rastreados e resumidos apenas no nível do projeto. |
| Selecionar Produto | Especifique se este uso de material é para um produto **Existente** (catálogo) ou um produto **Fora do catálogo**. | Este campo determina o tipo de produto. |
| Produto | A ID do produto do catálogo de produtos. Quando você seleciona uma ID de produto, o campo **Selecionar Produto** é atualizado automaticamente para **Produto existente**. A ID é usada para recuperar os preços de custo e venda da lista de preços. | Não há impacto posterior para este campo. |
| Descrição do Produto Fora do Catálogo | Um campo de texto para escrever o nome do produto. Este campo está disponível quando você seleciona o produto **Fora do catálogo** no campo **Selecionar produto**.| Não há impacto posterior para este campo. |
| Recurso Reservável| Recurso que utilizou este material no projeto. O padrão para este campo é o recurso reservável do usuário conectado, mas pode ser alterado para registrar o uso em nome de outros membros da equipe do projeto. | Não há impacto posterior para este campo. |
| Grupo de unidades | O valor padrão neste campo é obtido do grupo de unidades configurado como o padrão no produto do catálogo. Você pode atualizar este campo para selecionar outro grupo de unidades. | Não há impacto posterior para este campo. |
| Unidade | O valor padrão neste campo é a unidade padrão do produto selecionado. Você pode atualizar este campo para selecionar outra unidade. | Alterar a unidade resulta em um preço e custo unitário padrão diferente. |
| Quantidade | A quantidade do produto que foi usado no projeto ou na tarefa do projeto. | Não há impacto posterior para este campo. |
| Custo Unitário | O custo unitário da combinação de produto e unidade selecionados, conforme configurado na lista de preços de custo aplicável. | O custo unitário é sempre mostrado na moeda de custo do projeto. Se não houver custo unitário para a combinação de produto e unidade na lista de preços, o custo unitário padrão será de 0,00. |
| Custo Total | O valor do custo que é calculado como quantidade\*custo unitário.| O valor de custo é sempre mostrado na moeda de custo do projeto. |


## <a name="submit-material-usage-for-review-and-approval"></a>Envie o uso do material para análise e aprovação 
Após capturar todo o uso de material e quando estiver pronto para aprová-lo, envie as informações de uso para análise.

1. Acesse **Registro de Uso de Material** e selecione uma ou mais entradas. Ou selecione todos os registros de uso de material usando a caixa de seleção no cabeçalho.
2. Selecione **Enviar**. O sistema processa as entradas selecionadas e, depois, cria solicitações de aprovação de uso de material.

## <a name="recall-a-material-usage-log"></a>Recupere um registro de uso de material

Quando necessário, você pode recuperar o uso de material enviado. O tempo necessário para recuperar uma entrada de uso de material depende do estágio de aprovação.  Se o aprovador ainda não tiver aprovado a entrada, a recuperação poderá ser executada imediatamente. No entanto, se a entrada já tiver sido aprovada, o aprovador receberá uma solicitação para aprovar a recuperação e reverter as transações.

1. Acesse **Uso de Material** e, na lista de registros de uso de material, selecione o uso de material a ser recuperado.
2. Selecione **Recuperar**. Se a entrada de uso de material ainda não tiver sido aprovada, o sistema a recuperará imediatamente. Se a entrada de material já tiver sido aprovada, uma solicitação de recuperação será criada para notificar o aprovador de que você deseja cancelar o uso de material. O aprovador confirmará se a reversão poderá ser feita e a entrada será retornada.

## <a name="delete-a-material-usage-log"></a>Exclua um registro de uso de material

Você pode excluir registros de uso de material que não foram enviados. Para excluir um registro de uso de material que já foi enviado, primeiro recupere-o.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
