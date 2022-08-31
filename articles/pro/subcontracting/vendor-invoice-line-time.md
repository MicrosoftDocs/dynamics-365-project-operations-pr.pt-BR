---
title: Linhas da fatura de fornecedor para tempo
description: Este artigo explica como registrar linhas da fatura de fornecedor para custos de tempo que subcontratados inserem.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261998"
---
# <a name="vendor-invoice-lines-for-time"></a>Linhas da fatura de fornecedor para tempo

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations pode ter linhas da fatura de fornecedor para tempo. Os gerentes de projeto podem usar as linhas da fatura de fornecedor para tempo para registrar os custos do tempo de subcontratados nos projetos.

As linhas da fatura do fornecedor para tempo podem ou não fazer referência a uma linha de subcontrato para tempo. Se uma linha da fatura de fornecedor para tempo fizer referência a um subcontrato, os gerentes de projeto poderão comparar e verificar o tempo que está sendo faturado pela linha da fatura de fornecedor em relação ao tempo registrado por subcontratados e aprovado por gerentes de projeto no projeto.

A tabela a seguir apresenta informações sobre os campos nas linhas da fatura de fornecedor para tempo.

| Campo | Descrição | Impacto funcional |
| --- | --- | --- |
| Nome | O nome da linha da fatura de fornecedor para ajudar na identificação. | Esse nome será exibido como a primeira coluna em todas as pesquisas baseadas em linhas da fatura de fornecedor. |
| Description | Uma breve descrição dos serviços que estão sendo faturados pelo fornecedor na linha da fatura de fornecedor. | Nenhum |
| Subcontrato | O subcontrato em que os serviços foram pedidos originalmente. | Quando um subcontrato for selecionado para a fatura de fornecedor, todas as linhas da fatura de fornecedor herdarão essa seleção. Uma fatura de fornecedor não pode ter linhas da fatura de fornecedor que fazem referência a subcontratos diferentes. |
| Linha de subcontrato | A linha de subcontrato em que os serviços foram pedidos. A lista de linhas de subcontrato que podem ser selecionadas é limitada às linhas do subcontrato selecionado. | Quando uma linha de subcontrato é selecionada em uma linha da fatura de fornecedor para tempo, os valores padrão dos campos **Projeto**, **Função** e **Recurso reservável** são inseridos a partir dos campos correspondentes na linha de subcontrato. Se a linha de subcontrato selecionada tiver valores nos campos **Projeto**, **Função** e **Reservável**, os valores dos campos correspondentes na linha da fatura de fornecedor não podem diferir desses valores. |
| Data da transação | A data em que o dado real de custo da linha da fatura de fornecedor será registrado no projeto. | Nenhum |
| Classe da transação | O valor padrão é **Tempo**. | O valor **Tempo** indica que a linha da fatura de fornecedor está sendo usada para registrar o valor da fatura de tempo do subcontratado. |
| Projeto | O nome do projeto no qual os serviços que estão sendo faturados foram usados. | Este campo é obrigatório e não pode ficar em branco. |
| Tarefa | O nome da tarefa do projeto na qual os serviços que estão sendo faturados foram usados. Este campo estará disponível somente se houver um projeto selecionado. A seleção de uma tarefa do projeto é opcional. | Se este campo estiver em branco, o gerente de projeto poderá corresponder a linha da fatura de fornecedor com o tempo registrado pelos recursos subcontratados em qualquer tarefa do projeto. Se a linha da fatura de fornecedor não fizer referência a uma linha de subcontrato e esse campo ficar em branco, o dado real de custo criado pela linha da fatura de fornecedor não será vinculado a nenhum valor real de vendas não faturado. Nesse caso, se o faturamento baseado em tarefas estiver configurado, talvez não seja possível faturar os custos para o cliente final. |
| Função | A função dos recursos subcontratados cujo tempo está sendo faturado. | Este campo especifica a função desempenhada pelos recursos subcontratados cujo tempo é faturado na fatura do fornecedor. |
| Recurso reservável | O nome do subcontratado cujo tempo está sendo faturado. A seleção de um recurso reservável é opcional. | Se este campo estiver em branco, o gerente de projeto poderá corresponder a linha da fatura de fornecedor com o tempo registrado por qualquer recurso que pertence ao fornecedor na linha da fatura de fornecedor. |
| Quantidade | Insira o número de horas do tempo que está sendo faturado pelo fornecedor na linha da fatura. |Nenhum |
| Grupo de unidades | O valor padrão é **Grupo de unidades de tempo** e ele não pode ser alterado. | Nenhum |
| Unidade | O valor padrão é unidade base de horas do grupo de unidades de tempo. Você pode alterar esse valor para comprar qualquer unidade do grupo de unidades de tempo, como dia ou semana. | A combinação dos valores de **Função** e **Unidade** será usada como valor padrão ou calculado para o campo **Preço unitário** na linha da fatura de fornecedor. |
| Preço unitário | O preço unitário padrão usa a combinação dos valores de **Função** e **Unidade** da lista de preços do projeto aplicável à data da transação da linha da fatura de fornecedor. | Se o preço da lista de preços do projeto aplicável for configurado em uma unidade diferente da unidade na linha da fatura de fornecedor, o sistema usará a conversão de unidades para calcular o preço unitário. |
| Subtotal | Este campo somente leitura será calculado como *Quantidade* &times; *Preço unitário*, se forem inseridos valores nos campos **Quantidade** e **Preço unitário**. Se um ou ambos os campos estiverem em branco, você poderá inserir um valor no campo. | Nenhum |
| Imposto sobre vendas | Insira o valor do imposto sobre venda. | Nenhum |
| Valor total | O valor total da linha da fatura de fornecedor, incluindo impostos. Esse campo é calculado como *Subtotal* + *Imposto sobre vendas*. | Nenhum |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
