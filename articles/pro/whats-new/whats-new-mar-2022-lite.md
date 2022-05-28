---
title: Novidades em março de 2022 – implantação lite do Project Operations
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de março de 2022 da implantação lite do Project Operations.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583736"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Novidades em março de 2022 – implantação lite do Project Operations

_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_

Este tópico se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.30.0.99

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

- Subcontratação: experiências de criação e correspondência de faturas de fornecedor

## <a name="quality-updates"></a>Atualizações de qualidade

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Horas e despesas | 2388011 | Mostre os comentários de rejeição aos remetentes de entrada de hora durante a aprovação em massa. |
| Planejamento e acompanhamento de projeto | 2495294 | Os detalhes do projeto não devem ser editáveis na página **Detalhes da tarefa**. |
| Cobrança e preço | 2499605 | As etapas do contrato criadas com base em etapas de cotação são marcadas incorretamente como somente leitura. |
| Planejamento e acompanhamento de projeto | 2506050 | O conjunto de operações fica pendente por uma hora se não houver nenhuma alteração a ser salva. O conjunto é então falsamente marcado como **Com falha**, mas deve ser concluído de forma imediata. |
| Cobrança e preço | 2507401 | As unidades de contratação padrão são inseridas incorretamente nos projetos devido ao armazenamento em cache incorreto. |
| Cobrança e preço | 2541660 | A **Validação da Criação da Ordem de Venda** na gravação dupla deve ser apenas para ordens baseadas em projetos. |
| Cobrança e preço | 2552745 | O imposto não é dividido entre os clientes que configuraram regras de cobrança dividida. |
| Cobrança e preço | 2558859 | Aprimoradas as mensagens de erro quando as dimensões de preços são configuradas. |
| Cobrança e preço | 2558933 | **Importar de Estimativas do Projeto** falha quando **msdyn\_project** é adicionado como uma dimensão de preço. |
| Cobrança e preço | 2559101 | A exclusão de parâmetros do projeto não está bloqueada e causa problemas. |
| Gerenciamento de oportunidades | 2570390 | O plug-in de gravação dupla força o tipo de conta em cotações, ordens e oportunidades a ser **Cliente**, mesmo quando esse tipo de conta não está correto. |
| Cobrança e preço | 2586097 | Os dados reais do custo cobrado dividido não são revertidos quando um projeto é removido de uma linha de contrato de projeto. |
| Cobrança e preço | 2589619 | O imposto sobre o material fora do catálogo é propagado para os dados reais de vendas não cobradas e a fatura. |
| Gerenciamento de oportunidades | 2594015 | Uma cotação não pode ser fechada como ganha para clientes com condições de pagamento **Net60**. |
| Planejamento e acompanhamento de projeto | 2595841 | No Project for the Web, os usuários recebem uma mensagem de erro sobre um **msdyn\_actualstart** ausente quando eles criam uma nova solicitação de recurso. |
| Tempo e Despesa | 2602511 | O campo **Rejeitado por** para entradas de horas mostra **Sistema** em vez de um usuário nomeado como o rejeitador. |
| Tempo e Despesa | 2602528 | Um aprovador de projeto pode aprovar tempo em projetos nos quais ele não está listado como aprovador. |
| Cobrança e preço | 2608550 | Uma fatura de correção pode ser confirmada mesmo que não haja alterações na original. |

## <a name="removed-and-deprecated-features"></a>Recursos removidos e preteridos

O tópico [Recursos removidos ou preteridos no Project Operations](../../whats-new/removed-depreciated-features-project.md) descreve recursos que foram removidos ou preteridos no Dynamics 365 Project Operations.

- Um recurso removido não está mais disponível no produto.
- Um recurso preterido não está em desenvolvimento ativo e poderá ser removido em uma atualização futura.

Um anúncio de preterimento será exibido no tópico [Recursos removidos ou preteridos no Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 meses antes da remoção de qualquer recurso do produto.
