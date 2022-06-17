---
title: Usar Categoria da Transação como uma dimensão de precificação
description: Este artigo fornece informações sobre como usar o campo Categoria de Transação como uma dimensão de preço.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911680"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Usar Categoria da Transação como uma dimensão de precificação


_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


Este artigo explica como usar o campo **Categoria de Transação** como uma dimensão de preço. 

## <a name="prerequisites"></a>Pré-requisitos
Antes de concluir os procedimentos deste artigo, você deve ter uma nova solução de dimensão de preços para sua organização. Se você ainda não criou uma, consulte [Criar campos e entidades personalizadas como dimensões de preços](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Adicionar o campo Categoria de Transação a formulários e exibições
Para tornar o campo **Categoria de Transação** visível na solução de dimensão de preços, você precisa adicionar o campo a todos os formulários e exibições como uma entidade.

A tabela a seguir lista todos os formulários e exibições prontos para uso, por entidade. Você também precisará adicionar o novo campo a formulários ou exibições adicionais em entidades personalizadas.

|  Entidade        | Formulários     |Modos de exibição        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preço da Função| Informações |- Preços de Categorias de Recursos Ativos<br> - Preço de Categoria de Recurso Associado |
|  Markup de Preço da Função| Informações|- Markup de Preço de Função Ativo<br>- Markup de Preço de Função Associado |
|  Detalhe da Linha de Cotação|- Informações do Projeto<br>- Criação Rápida do ProJeto| - Detalhe da Linha de Cotação Ativa<br>- Detalhes da Linha de Cotação Combinada<br>- Detalhe da Linha de Cotação Associada |
|  Detalhe da Linha de Contrato do Projeto|- Informações do Projeto<br>- Criação Rápida do ProJeto|- Detalhes da Linha de Contrato Combinada<br>- Detalhes da Linha de Contrato Ativa<br>- Detalhe da Linha de Contrato Associada |
|  Tarefa do Projeto|- Informações<br>- Novo Formulário| &nbsp; |
|  Membro da Equipe do Projeto|- Informações<br>- Novo Formulário|- Membros Ativos da Equipe do Projeto<br>- Membros da Equipe do Projeto<br>- Membros Associados da Equipe do Projeto |
|  Entrada de Hora|- Informações<br>- Criar Entrada de Hora|- Minhas Entradas de Hora por Data<br>- Minhas Entradas de Hora para esta Semana<br>- Entradas de hora para Aprovação|
|  Linha do Diário|- Informações<br>- Criação Rápida|- Linhas do Diário Ativas<br>- Linha do Diário Associada|
|  Detalhe da Linha da Fatura|- Informações<br>- Criação Rápida|- Detalhes da Linha de Fatura Ativa<br>- Transações de Fatura Passíveis de Cobrança<br>- Transações de Fatura Complementares<br>- Detalhe da Linha de Fatura Associada <br>- Transações de Fatura Não Passíveis de Cobrança|
|  Real|- Informações<br>- Dados Reais Ativos| Dado Real Associado |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Configurar o campo Categoria de Transação como uma dimensão de preço

1. Vá para **Configurações** > **Parâmetros**. 
2. Na página **Parâmetros**, na guia **Dimensões de Preço Baseadas em Valor**, verifique se a grade mostra os registros na entidade **Dimensões de Preço**.
3. Adicione **Categoria da Transação** a essa lista e defina os campos **Aplicável ao Custo** e **Aplicável às Vendas** como **Sim**.
4. No campo **Tipo de Dimensão**, selecione **Baseado em Valor** e depois escolha a prioridade para **Categoria da Transação** pois ela está relacionada a custo e vendas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]