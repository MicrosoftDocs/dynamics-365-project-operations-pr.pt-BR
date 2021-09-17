---
title: Linhas de subcontrato para hora
description: Este tópico explica como registrar linhas de subcontrato para tempo e registrar a compra de tempo de fornecedores.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323852"
---
# <a name="subcontract-lines-for-time"></a>Linhas de subcontrato para hora

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Um subcontrato no Dynamics 365 Project Operations pode ter uma linha de subcontrato para tempo. As linhas de subcontrato para tempo permitem que um Gerente de Projeto compre tempo de recursos do fornecedor para tarefas do projeto e requisitos de recursos da equipe.

Para criar uma linha de subcontrato para tempo no Project Operations, conclua as etapas a seguir.

1. No painel de navegação, selecione **Subcontratos** e abra um subcontrato.
2. Na guia **Linhas de Subcontrato**, selecione **Novo** para criar uma nova linha de subcontrato.
3. Na página **Criação Rápida**, no campo **Classe de Transação**, selecione **Tempo**.
4. Insira as informações de campo restantes e selecione **Salvar**.

  A tabela a seguir fornece informações sobre os campos na página **Linha de subcontrato** e na página **Criação Rápida**.

| **Campo** | **Descrição** |
| --- | --- |
| Name | O nome da linha de subcontrato. |
| Descrição | Uma breve descrição dos serviços que estão sendo adquiridos na linha de subcontrato. | 
| Tipo de Linha | Esse campo é um valor padrão.  |
| Método de Cobrança | Selecione o método de cobrança. Com base no método de cobrança da linha de subcontrato referenciado, uma agenda de fatura com base em marcos está disponível para o método de cobrança Preço Fixo. |
| Classe da Transação | Esse campo é um valor padrão que indica se a linha de subcontrato está sendo usada para registrar uma compra de tempo do subcontratado. |
| Função | A função dos recursos de subcontrato cujo tempo está sendo comprado. A função atribuída aos recursos do subcontrato determina o custo da compra. |
| Data de Início Solicitada | A data em que os recursos do subcontratado são necessários para começar a trabalhar. O início solicitado é usado para escolher uma lista de preços das listas de preços de projeto anexadas ao subcontrato. O custo da função na linha de subcontrato então terá o padrão saído da lista de preços. |
| Término solicitado | A data em que termina a atribuição dos recursos do subcontratado. Essa data é usada para mostrar avisos quando um Gerente de Projeto está utilizando essa capacidade para requisitos de recursos que ocorrem após essa data. |
| Quantidade Encomendada | O número de Horas de função compradas do fornecedor. Esse valor é usado para mostrar avisos quando um Gerente de Projeto está ultrapassando essa capacidade para requisitos de recursos. |
| Grupo de Unidades | O valor padrão desse campo é o grupo Unidade de tempo e não pode ser alterado.  |
| Unidade | O padrão desse campo é a unidade básica de horas do grupo Unidade de tempo. Você pode alterar esse valor para comprar qualquer grupo Unidade de tempo, como dia ou semana. A combinação de Função e Unidade é usada para calcular o preço unitário para a linha de subcontrato. |
| Preço Unitário | O preço unitário tem com padrão a combinação de Função e Unidade da lista de preços de projeto aplicável para a data de início solicitada da linha de subcontrato. Quando a lista de preços de projeto aplicável tiver o preço configurado em uma unidade diferente da unidade na linha de subcontratação, o sistema usará a conversão de unidade para calcular o preço por unidade. |
| Subtotal | Esse é um campo somente leitura que será calculado automaticamente como **Quantidade x Preço unitário** caso os valores de quantidade e preço unitário sejam inseridos. Se a quantidade, o preço unitário ou ambos estiverem em branco, você poderá inserir um valor no campo. |
| Imposto sobre Vendas |  Insira o valor do imposto sobre venda. |
| Valor Total | O valor total da linha de subcontrato após a inclusão dos impostos. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
