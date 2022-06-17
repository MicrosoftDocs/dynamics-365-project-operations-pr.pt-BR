---
title: Usar categoria de transação como uma dimensão de precificação
description: Este artigo fornece informações sobre o uso de uma categoria de transação como uma dimensão de preço.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 1a1c2dc17c2092e5364d90e7efc1f13aee80703e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915722"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Usar categoria de transação como uma dimensão de precificação

[!include [banner](../includes/psa-now-project-operations.md)]

Este artigo mostra como usar uma categoria de transação como uma dimensão de preço. Antes de começar, se você ainda não criou uma solução de dimensão de precificação, será necessário criar uma. Se você já possui uma solução de dimensão de precificação, poderá fazer suas alterações nessa solução. Se você não criou uma solução de dimensão de preço para sua organização, conclua os procedimentos no artigo [Criar campos e entidades personalizados](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Adicionar categoria de transação a formulários e exibições
Para tornar a categoria de transação visível na interface do usuário na solução de dimensão de precificação, você precisará passar por todos os formulários e exibições das principais entidades e adicionar esses campos aos formulários e exibições dessas entidades.
A tabela a seguir é uma lista abrangente de formulários e exibições prontos para uso, listados por entidade, que precisarão ser atualizados com os novos campos. Se houver qualquer exibição ou formulário adicional em suas personalizações nessas entidades, adicione os novos campos a eles também.

|  Entidade        | Formulários     |Exibições        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preço da Função|• Informações |• Preços Ativos de Categorias de Recursos<br> • Exibição Associada de Preços de Categorias de Recursos|
|  Markup de Preço da Função|• Informações|• Markup de Preço da Função Ativo<br>• Exibição Associada do Markup de Preço da Função|
|  Detalhes da linha de cotação|• Informações do Projeto<br>• Criação Rápida do ProJeto|• Detalhes da Linha de Cotação Ativos<br>• Detalhes Combinados da Linha de Cotação<br>• Exibição Associada de Detalhes da Linha de Cotação|
|  Detalhe da Linha de Contrato do Projeto|• Informações do Projeto<br>• Criação Rápida do ProJeto|• Detalhes Combinados da Linha de Contrato<br>• Detalhes da Linha de Contrato Ativa<br>• Exibição Associada de Detalhes da Linha de Contrato|
|  Tarefa do Projeto|• Informações<br>• Novo Formulário||
|  Membro da Equipe do Projeto|• Informações<br>• Novo Formulário|• Membros Ativos da Equipe do Projeto<br>• Membros da Equipe do Projeto<br>• Exibição Associada de Membros da Equipe do Projeto|
|  Entrada de Horas|• Informações<br>• Criar Entrada de Hora|• Minhas Entradas de Hora por Data<br>• Minhas Entradas de Horas para Esta Semana<br>• Entradas de hora para aprovação|
|  Linha do Diário|• Informações<br>• Criação rápida:|• Linhas de diário ativas<br>• Exibição Associada de Linhas de Diário|
|  Detalhes da Linha da Fatura|• Informações<br>• Criação rápida:|• Detalhes de Linha de Fatura Ativos<br>• Transações de Fatura Passíveis de Cobrança<br>• Transações de Fatura Complementares<br>• Exibição Associada de Detalhes de Linha de Fatura<br>• Transações de Fatura Não Passíveis de Cobrança|
|  Real|• Informações<br>• Dados Reais Ativos|• Exibição Associada de Dados Reais|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Configurar categoria de transação como uma dimensão de precificação

1. Na interface da Web, vá para **Project Service** > **Configurações** > **Parâmetros**. 
2. Na página **Parâmetros**, na guia **Dimensões de Preço Baseadas em Valor**, observe que a grade na guia mostra os registros na entidade **Dimensões de Precificação**.
3. Adicione **Categoria da Transação** a essa lista e defina os campos **Aplicável ao Custo** e **Aplicável às Vendas** como **Sim**.
4. No campo **Tipo de Dimensão**, selecione **Baseado em Valor** e depois escolha a prioridade para **Categoria da Transação** relacionada a custo e vendas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
