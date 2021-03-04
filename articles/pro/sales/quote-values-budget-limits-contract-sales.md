---
title: Resumo informativo de uma cotação de projeto - lite
description: Este tópico fornece informações sobre as informações e configurações que se aplicam e afetam as cotações do projeto. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f16634a87780c23d699d9ad535dd5e6d4ecb895d
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180925"
---
# <a name="summary-information-on-a-project-quote---lite"></a>Resumo informativo de uma cotação de projeto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este artigo explica as informações que se aplicam a uma cotação de projeto. Isso inclui as configurações que afetam todas as linhas de cotação e informações sobre a cotação que são resumidas em todos os itens de linha para direcionar os KPIs da cotação do projeto.

A tabela a seguir lista os campos de informações de resumo em uma cotação de projeto que são exclusivos para o Dynamics 365 Project Operations ou têm algumas mudanças importantes no comportamento das cotações do Dynamics 365 Sales.

| **Campo** | **Local** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Digitar | Guia Resumo (oculta) | O hash deste campo de conjunto de opções tem as seguintes opções:</br>- Baseado no trabalho (disponível apenas quando o Project Operations está instalado)</br>- Baseado no item (disponível apenas quando o Project Operations e Sales estão instalados)</br>- Baseado em serviço de manutenção (disponível quando o Dynamics 365 Field Service está instalado) | Quando você usa o aplicativo Project Operations, o valor deste campo é automaticamente definido como **Baseado em trabalho**. Isso classifica a cotação como uma cotação baseada em projeto. Uma cotação deve ser baseada em projeto para habilitar todas as extensões e funcionalidades específicas do projeto. |
| Cliente em Potencial | Guia Resumo | Referência à empresa do cliente ou registro de conta. Quando uma cotação é criada a partir de uma oportunidade, este campo é copiado do campo correspondente na oportunidade. | A moeda na cotação do projeto é padronizada com base na moeda do cliente. Entretanto, isso pode ser alterado antes de salvar a cotação. |
| Gerente de Contas | Guia Resumo | O nome do gerente de contas deste negócio. Quando uma cotação é criada a partir de uma oportunidade, este campo é copiado do campo correspondente na oportunidade. | O gerente de contas é responsável por gerenciar o relacionamento com o cliente até a conclusão deste projeto. Com base no registro de recurso reservável vinculado ao gerente de contas, a unidade de contratação é padronizada na cotação do projeto. |
| Unidade de Contratação | Guia Resumo | A unidade organizacional responsável pela entrega do projeto ou projetos associados a esta cotação. Quando uma cotação é criada a partir de uma oportunidade, este campo é copiado do campo correspondente na oportunidade. | A unidade de contratação é a divisão da empresa que executará os projetos após o fechamento do negócio. Cada unidade de contratação tem uma moeda, e essa moeda é usada para relatar os custos estimados e reais incorridos durante a execução do projeto. |
| Lista de preços de produtos | Guia Resumo | Esta é a lista de preços usada para os preços padrão nas linhas de cotação baseadas em produto. A lista de opções para este campo mostra várias listas de preços em que a moeda da lista de preços corresponde à moeda da cotação. Quando uma cotação é criada a partir de uma oportunidade, este campo é copiado do campo correspondente na oportunidade. Este campo na oportunidade é padronizado no registro da conta, mas pode ser alterado. | Quando uma cotação vence, o valor do campo é copiado para o contrato do projeto criado. |
| Moeda | Guia Resumo | Isso indica a moeda que será usada para relatar o valor deste negócio. Essa também é a moeda na qual o cliente será faturado se o negócio for fechado. Quando uma cotação é criada a partir de uma oportunidade, este campo é copiado do campo correspondente na oportunidade. Este campo na oportunidade é padronizado no registro da conta, mas pode ser alterado pelo usuário. | Depois que uma cotação é salva, este campo não é mais editável. Isso é usado para padronizar as listas de preços do produto e do projeto na cotação. A moeda na cotação é usada para corresponder à moeda na lista de preços. |
| Limite máximo | Guia Resumo | Indica o limite negociado no valor final com o qual o cliente concorda para este negócio. | Esse limite é avaliado durante a execução e é aplicável a todos os itens de linha e projetos associados a este negócio. |
| Data de entrega solicitada | Guia Resumo | Quando uma cotação é criada a partir de uma oportunidade, este campo é copiado do campo correspondente na oportunidade. | Esta data é usada como data de término para gerar agendamento de faturas. |

Veja abaixo as guias e KPIs disponíveis em uma cotação de projeto que são exclusivas para o Project Operations ou têm algumas mudanças importantes no comportamento de cotações do Sales:

| **Campo** | **Local** | **Descrição** |
| --- | --- | --- |
| Análise de lucratividade | Guia na Cotação | A guia mostra as seguintes métricas:</br>- Custo total passível de cobrança</br></br>- Custo total não passível de cobrança</br>- Receita total</br>- Receita total (base)</br>- Margem bruta</br>- Margem bruta ajustada|
| Comparação com Expectativas do Cliente | Guia na Cotação | Esta guia mostra as seguintes métricas:</br>- Conclusão estimada</br>- Conclusão da solicitação</br>- Orçamento do cliente</br>- Valor da cotação |
| Análise da cotação | Guia na Cotação | Esta guia resume os seguintes KPIs principais para uma cotação de projeto</br>- Comparação com as expectativas do cliente para orçamento e agenda</br>- Margem bruta</br>- Margem bruta ajustada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]