---
title: Linhas de subcontrato para hora
description: Este artigo explica como registrar linhas de subcontrato por tempo e registrar a compra de tempo de fornecedores.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ba013dd7ad023acc4f0cf077099c8c2c8d5bcd8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522217"
---
# <a name="subcontract-lines-for-time"></a>Linhas de subcontrato para hora

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Um subcontrato no Dynamics 365 Project Operations pode ter uma linha de subcontrato para tempo. As linhas de subcontrato para tempo permitem que um Gerente de Projeto compre tempo de recursos do fornecedor para tarefas do projeto e requisitos de recursos da equipe.

Para criar uma linha de subcontrato para tempo no Project Operations, conclua as etapas a seguir.

1. No painel de navegação, selecione **Subcontratos** e abra um subcontrato.
2. Na guia **Linhas de Subcontrato**, selecione **Novo** para criar uma nova linha de subcontrato.
3. Na página **Criação Rápida**, no campo **Classe de Transação**, selecione **Tempo**.
4. Insira as informações de campo restantes e selecione **Salvar**.

  A tabela a seguir fornece informações sobre os campos na página **Linha de subcontrato** e na página **Criação Rápida**.

| **Campo** | **Descrição** | **Impacto funcional** |
| --- | --- | --- |
| Name | Nome da linha do subcontrato para ajudar na identificação. | Isso será exibido como a primeira coluna em todas as pesquisas baseadas em linhas de subcontrato. |
| Descrição | Uma breve descrição dos serviços que estão sendo adquiridos na linha de subcontrato. |Nenhum(a) |
| Tipo de Linha |   Esse campo tem um valor padrão **Baseado em quantidade**.| Nenhum(a) |
| Método de Cobrança | Este é um conjunto de opções que representa os dois principais modelos de contratação com suporte do Project Operations: **Preço Fixo** e **Tempo e Material**. | Com base no método de cobrança selecionado, uma agenda de faturamento baseada em etapas é disponibilizada para linhas de subcontrato com o método de cobrança Preço Fixo. |
| Classe da Transação | O valor padrão é **Tempo**. | Isso indica que a linha de subcontrato está sendo usada para registrar uma compra de tempo do subcontratado. |
| Função | Selecione a função dos recursos subcontratados dos quais o tempo está sendo comprado. | A função dos recursos subcontratados determina o custo da compra. |
| Data de Início Solicitada | Insira a data em que os recursos subcontratados devem começar a trabalhar. | Isso é usado para escolher uma lista de preços de projeto nas listas de preços de projeto anexadas ao subcontrato. O custo da função na linha do subcontrato vem dessa lista de preços. |
| Término solicitado | Insira a data de término da atribuição do recurso subcontratado. | Isso será usado para mostrar avisos quando um gerente de projeto estiver utilizando a capacidade para requisitos de recursos que ocorrem após essa data. |
| Quantidade Encomendada | Insira o número de horas da função que está sendo comprada do fornecedor. | Isso será usado para mostrar avisos quando um gerente de projeto estiver extrapolando essa capacidade para requisitos de recursos. |
| Grupo de Unidades | O valor padrão é **Grupo de unidades de tempo**, o qual não pode ser alterado. | Nenhum(a)|
| Unidade | O padrão para este campo é a unidade básica de horas do **Grupo de unidades de tempo**. Você pode alterar esse valor para comprar qualquer unidade do **Grupo de unidades de tempo**, como dia ou semana. | A combinação de **Função** e **Unidade** será usada como o padrão ou será calculada para o preço unitário da linha do subcontrato. |
| Preço Unitário | O preço unitário padrão usa a combinação de **Função** e **Unidade** da lista de preços do projeto, aplicável para a **Data de Início Solicitada** da linha do subcontrato. | Quando a lista de preços de projeto aplicável tiver o preço configurado em uma unidade diferente da unidade na linha de subcontratação, o sistema usará a conversão de unidade para calcular o preço por unidade. |
| Subtotal |    Este é um campo somente leitura calculado como Quantidade x Preço unitário, se os valores de quantidade e preço unitário forem inseridos. Se a quantidade, o preço unitário ou ambos estiverem em branco, você poderá inserir um valor no campo. | Nenhum(a)|
| Imposto sobre Vendas |   Insira o valor do imposto sobre venda. |Nenhum(a) |
| Valor Total | O valor total da linha de subcontrato, incluindo impostos. Esse campo é calculado como Subtotal + Imposto.|Nenhum(a) |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
