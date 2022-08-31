---
title: Linhas da fatura de fornecedor para etapas
description: Este artigo explica como criar linhas da fatura de fornecedor para etapas em um subcontrato.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9260981"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Linhas da fatura de fornecedor para etapas

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations pode ter linhas da fatura de fornecedor para etapas que são definidas em uma linha de subcontrato. Os gerentes de projeto podem usar linhas da fatura de fornecedor para etapas para registrar os custos de serviços adquiridos como custos baseados em etapas incorridos em serviços ou produtos adquiridos para o projeto.

As linhas da fatura de fornecedor para etapas devem sempre fazer referência a uma linha de subcontrato com um método de cobrança Preço fixo. Quando uma linha da fatura de fornecedor para etapas fizer referência a uma linha de subcontrato, os gerentes de projeto poderão comparar e verificar os custos subjacentes de horas, despesas ou materiais que fazem referência a essa linha de subcontrato em relação à etapa que está sendo faturada pelo fornecedor.

A tabela a seguir apresenta informações sobre os campos nas linhas da fatura de fornecedor para etapas.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | O nome da linha da fatura de fornecedor para ajudar na identificação. | Esse nome será exibido como a primeira coluna em todas as pesquisas baseadas em linhas da fatura de fornecedor. |
| Description | Uma breve descrição dos serviços que estão sendo faturados pelo fornecedor na linha da fatura de fornecedor. | Nenhum |
| Subcontrato | O subcontrato em que os serviços foram pedidos originalmente. | Quando um subcontrato for selecionado para a fatura de fornecedor, todas as linhas da fatura de fornecedor herdarão essa seleção. Uma fatura de fornecedor não pode ter linhas da fatura de fornecedor que fazem referência a subcontratos diferentes. |
| Linha de subcontrato | A linha de subcontrato em que os serviços foram pedidos. A lista de linhas de subcontrato que podem ser selecionadas é limitada às linhas do subcontrato selecionado. | Quando uma linha de subcontrato é selecionada em uma linha da fatura de fornecedor para etapas, os campos **Função** e **Categoria de transação** e os campos relacionados ao produto são irrelevantes e não estão disponíveis. Os campos **Quantidade**, **Unidade** e **Grupo de unidades** também não são relevantes para linhas da fatura de fornecedor baseadas em etapas. |
| Data da transação | A data em que o dado real de custo da linha da fatura de fornecedor será registrado no projeto. | Nenhum |
| Classe da transação | Selecione **Etapa** para registrar uma fatura de fornecedor para uma etapa concluída que foi definida em uma linha de subcontrato. | Nenhum |
| Etapa | Selecione a etapa definida na linha de subcontrato relacionada marcada como **Pronto para Faturamento**. | É possível selecionar as etapas da linha de subcontrato com status **Pronto para faturamento** em uma linha da fatura de fornecedor. |
| Projeto | O nome do projeto no qual os serviços que estão sendo faturados foram usados. | Este campo é obrigatório e não pode ficar em branco. |
| Tarefa | O nome da tarefa do projeto na qual os serviços que estão sendo faturados foram usados. Este campo estará disponível somente se houver um projeto selecionado. A seleção de uma tarefa do projeto é opcional. | Se este campo estiver em branco, o gerente de projeto poderá corresponder a linha da fatura de fornecedor com a classe de transações na linha de subcontrato relacionada registrada em qualquer tarefa do projeto. Se a linha da fatura de fornecedor não fizer referência a uma linha de subcontrato e esse campo ficar em branco, o dado real de custo criado pela linha da fatura de fornecedor não será vinculado a nenhum valor real de vendas não faturado. Nesse caso, se o faturamento baseado em tarefas estiver configurado, talvez não seja possível faturar os custos para o cliente final. |
| Valor do marco | Insira o valor da etapa definida na linha de subcontrato que está pronta para ser faturada. | Nenhum |
| Imposto sobre vendas | Insira o valor do imposto sobre venda. | Nenhum |
| Valor total | O valor total da linha da fatura de fornecedor, incluindo impostos. O campo é calculado como *Valor da etapa* + *Imposto sobre vendas*. | Nenhum |

> [!NOTE]
> Quando uma linha da fatura de fornecedor que faz referência a uma etapa de linha de subcontrato é criada, o status da etapa de subcontrato é atualizado para **Fatura de fornecedor criada**. Então, quando essa fatura de fornecedor é confirmada, o status da etapa da linha de subcontrato é atualizado para **Fatura de fornecedor confirmada**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
