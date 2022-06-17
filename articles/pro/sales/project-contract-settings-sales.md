---
title: Configurações de contrato do projeto - lite
description: Este artigo fornece informações sobre os campos que afetam as linhas do contrato e as informações sobre o contrato resumidas em todos os itens de linha.
author: rumant
ms.date: 03/08/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6123cbc028cf49cc198173697969f415b0789256
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917056"
---
# <a name="header-details-for-project-contracts"></a>Detalhes do cabeçalho para contratos de projeto

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este artigo fornece informações sobre campos que se aplicam a todo o contrato do projeto, incluindo configurações que afetam todas as linhas do contrato. As informações sobre o contrato resumidas em todos os itens de linha para direcionar os KPIs do contrato do projeto também estão incluídas.

A tabela a seguir lista os campos em um contrato de projeto que são exclusivos do Dynamics 365 Project Operations ou que tenham algumas alterações importantes no comportamento das ordens de venda do Dynamics 365 Sales.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Digitar | Guia **Resumo** (oculta) | Este é um campo de conjunto de opções com as seguintes opções:</br>- **Baseado no trabalho** (disponível apenas quando o Project Operations está instalado)</br>- **Baseado no item** (disponível apenas quando o Project Operations e Sales estão instalados)</br>- **Baseado em serviço de manutenção** (disponível quando o Dynamics 365 Field Service está instalado) | No Project Operations, o valor desse campo é padronizado como **Baseado em trabalho** e classifica o contrato como um contrato baseado em projeto. Um contrato deve ser baseado em projeto para habilitar todas as extensões e funcionalidades específicas do projeto. |
| Cliente em Potencial | Guia **Resumo** | A referência à empresa do cliente ou ao registro da conta. Quando um contrato é criado a partir de uma cotação, este campo é copiado do campo correspondente no registro de cotação. | A moeda no contrato do projeto é padronizada com base na moeda do cliente. Isso pode ser alterado antes de salvar o contrato. |
| Gerente de Contas | Guia **Resumo** | O nome do gerente de contas deste negócio. Quando um contrato é criado a partir de uma cotação, este campo é copiado do campo correspondente no registro de cotação. | O gerente de contas é responsável por gerenciar o relacionamento com o cliente até a conclusão do projeto. Com base no registro de recurso reservável vinculado ao gerente de contas, a unidade de contratação é padronizada no contrato do projeto. |
| Unidade de Contratação | Guia **Resumo** | A unidade organizacional responsável pela entrega dos projetos ou projetos associados a este contrato. Quando um contrato é criado a partir de uma cotação, este campo é copiado do campo correspondente no registro de cotação. | A unidade de contratação é a divisão da empresa que executa os projetos. Cada unidade de contratação tem uma moeda, e essa moeda é usada para relatar os custos estimados e reais incorridos durante o projeto. |
| Lista de Preços de Produtos | Guia **Resumo** | Esta lista de preços é usada para preços padrão em linhas de contrato baseadas em produto. A lista de opções suspensas para este campo mostra uma lista de listas de preços em que a moeda da lista de preços corresponde à moeda do contrato. Quando um contrato é criado a partir de uma cotação, este campo é copiado do campo correspondente no registro de cotação. No contrato de projeto, este campo assumirá o padrão no registro da conta, mas pode ser alterado. | Não há relevância posterior para este campo. |
| Moeda | Guia **Resumo** | A moeda usada para relatar o valor dessa transação e a moeda na qual o cliente será faturado. Quando um contrato é criado a partir de uma cotação, este campo é copiado do campo correspondente no registro de cotação. No contrato de projeto, este campo é padronizado no registro da conta, mas pode ser alterado. | Depois que um contrato é salvo, este campo não é mais editável. O campo é usado para padronizar as listas de preços do produto e do projeto no contrato. A moeda no contrato é usada para corresponder à moeda na lista de preços. |
| Limite máximo | Guia **Resumo** | Este campo indica o limite negociado no valor final com o qual o cliente concordou para este negócio. | O limite é avaliado durante a execução e é aplicável a todos os itens de linha e projetos associados a este negócio. |
| Data de Entrega da Solicitação | Guia **Resumo** | Quando um contrato é criado a partir de uma cotação de projeto, este campo é copiado do campo correspondente na cotação de projeto. | Esta data é usada como data de término para gerar programações de faturas. |

Os seguintes KPIs estão disponíveis na guia **Desempenho do Contrato** de um contrato de projeto. 

>[!NOTE]
>Todos os valores na guia **Desempenho do Contrato** são expressos na moeda padrão do ambiente.

| Campo | Localização | Description |
| --- | --- | --- |
| Valor do Contrato | Contrato geral | O valor total do contrato do projeto.|
| Valor Cobrado | Contrato geral | A soma dos valores em todas as faturas deste contrato.|
| Custo Incorrido | Contrato geral | A soma de todos os custos reais registrados em todos os projetos mapeados para o contrato. |
| Margem Bruta | Contrato geral | Valor faturado - Custo incorrido até a data/valor faturado |
| Margem Esperada | Contrato geral | (Valor do contrato - Custos estimados)/valor do contrato Custos estimados = A soma de todos os custos estimados em todos os projetos mapeados para o contrato.|
| Valor do Contrato | Linhas baseadas em projeto | O valor da linha do contrato. |
| Valor faturado | Linhas baseadas em projeto | Para a linha de contrato de preço fixo: a soma dos valores em todos os valores reais do marco de vendas faturadas em relação a esta linha de contrato em várias faturas criadas para este contrato. Para a linha de contrato de tempo e material: a soma dos valores em todos os valores reais de vendas faturadas passíveis de cobrança em relação a esta linha de contrato em várias faturas criadas para este contrato. |
| Custo Incorrido | Linhas baseadas em projeto | A soma de todos os custos reais registrados em todos os projetos mapeados para a linha de contrato. |
| Margem Bruta | Linhas baseadas em projeto | (Valor faturado - Custo incorrido até a data)/valor faturado |
| Margem Esperada | Linhas baseadas em projeto | (Valor da linha do contrato na moeda base - Custos estimados para a linha do contrato na moeda base)/valor da linha do contrato na moeda base |
| Custo Incorrido | Detalhes de uma linha baseada em projeto | Tempo: a soma do valor nos dados reais de custo de hora registrados para esta função no projeto mapeado para a linha do contrato. Despesas: a soma do valor em todos os custos reais de despesas registrados para esta categoria no projeto mapeado para a linha do contrato. |
| Quantidade Registrada | Detalhes de uma linha baseada em projeto | Tempo: o valor nos dados reais de custo de hora total para uma função no projeto que é mapeada para esta linha de contrato. Despesas: todos os valores para esta categoria de despesas nos custos reais das despesas no projeto são mapeadas para esta linha de contrato. |
| Valor Cobrado | Detalhes de uma linha baseada em projeto | Para uma linha de contrato de preço fixo, este campo é deixado em branco no nível de detalhe e só é mostrado no nível da linha de contrato. Para uma linha de contrato de tempo e material, os cálculos são concluídos no nível de detalhes. Os detalhes mostram a soma do valor em todas as linhas de receita faturadas nesta linha de contrato que são cobráveis. |
| Quantidade Cobrada | Detalhes de uma linha baseada em projeto | Para uma linha de contrato de preço fixo, este campo é deixado em branco no nível de detalhe e só é mostrado no nível da linha de contrato. Para uma linha de contrato de tempo e material, os cálculos são concluídos no nível de detalhes para tempo e despesas. Tempo: a soma das horas em todas as linhas de receita faturadas para esta função em relação a esta linha de contrato que são cobráveis. Despesas: todos os valores para esta categoria de despesas nos custos reais das despesas no projeto são mapeadas para esta linha de contrato. |
| Valor do Contrato | Linhas baseadas em produto | O valor da linha de contrato desta linha de contrato baseada em produto. |
| Valor Cobrado | Linhas baseadas em produto | A soma dos valores em todas as linhas da fatura em relação a esta linha do contrato com base no produto em várias faturas criadas para este contrato. |
| Custo Incorrido | Linhas baseadas em produto | A soma de todos os custos reais registrados para a linha de contrato baseada em produto. |
| Margem Bruta | Linhas baseadas em projeto | Valor faturado - Custo incorrido até a data/valor faturado |
| Margem Esperada | Linhas baseadas em produto | (Valor da linha do contrato - Custos estimados para a linha do contrato)/valor da linha do contrato |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
