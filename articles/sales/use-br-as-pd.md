---
title: Usar um recurso reservável como uma dimensão de preço
description: Este tópico fornece informações sobre como usar um recurso reservável como uma dimensão de preço.
author: Rumant
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0c5cb85f7c43f7b2fd9c367d7f7ac9c3250e0a1
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643069"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Usar um recurso reservável como uma dimensão de preço

 _**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_ 

Este tópico fornece informações sobre como usar um recurso reservável como uma dimensão de preço. Se sua estratégia de preços for configurada de forma que cada recurso reservável tenha um preço ou taxa de custo específico, use um recurso reservável como uma dimensão de preço.

## <a name="prerequisites"></a>Pré-requisitos
Antes de concluir os procedimentos neste tópico, você deve ter uma nova solução de dimensão de preços para sua organização. Se você ainda não criou uma, consulte [Criar campos e entidades personalizadas](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Adicionar o campo Recurso Reservável a formulários e exibições
Para tornar o campo **Recurso Reservável** visível na solução de dimensão de preços, você precisa adicionar o campo a todos os formulários e exibições como uma entidade.

A tabela a seguir lista todos os formulários e exibições prontos para uso, por entidade. Você também precisará adicionar o novo campo a formulários ou exibições adicionais em entidades personalizadas.

|   Entity        | Formulários   |Modos de exibição        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preço da Função| Informação | - Preços de Categorias de Recursos Ativos<br> - Preço de Categoria de Recurso Associado |
|  Markup de Preço da Função| Informação| - Markup de Preço de Função Ativo<br>- Markup de Preço de Função Associado |
|  Detalhes da linha de cotação| - Informações do Projeto<br>- Criação Rápida do ProJeto| - Detalhe da Linha de Cotação Ativa<br>- Detalhes da Linha de Cotação Combinada<br>- Detalhe da Linha de Cotação Associada |
|  Detalhe da Linha de Contrato do Projeto| - Informações do Projeto<br>- Criação Rápida do ProJeto| - Detalhes da Linha de Contrato Combinada<br>- Detalhes da Linha de Contrato Ativa<br>- Detalhe da Linha de Contrato Associada |
|  Tarefa do Projeto| - Informações<br>- Novo Formulário| &nbsp; |
|  Membro da Equipe do Projeto| - Informações<br>- Novo Formulário| - Membros Ativos da Equipe do Projeto<br>- Membros da Equipe do Projeto<br>- Membros Associados da Equipe do Projeto |
|  Entrada de Hora| - Informações<br>- Criar Entrada de Hora| - Minhas Entradas de Hora por Data<br>- Minhas Entradas de Hora para esta Semana<br>- Entradas de Hora para Aprovação|
|  Linha do Diário| - Informações<br>- Criação Rápida| - Linhas do Diário Ativas<br>- Linha do Diário Associada |
|  Detalhe da Linha da Fatura| - Informações<br>- Criação Rápida| - Detalhes da Linha de Fatura Ativa<br>- Transações de Fatura Passíveis de Cobrança<br>- Transações de Fatura Complementares<br>- Detalhe da Linha de Fatura Associada <br>- Transações de Fatura Não Passíveis de Cobrança|
|  Real| - Informações<br>- Dados Reais Ativos| Dado Real Associado |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Configurar um recurso reservável como uma dimensão de preço
Para configurar um recurso reservável como uma dimensão de preço, siga estas etapas:

1. Vá para **Configurações** > **Parâmetros**. 
2. Na página **Parâmetro**, na guia **Dimensões de Preço Baseadas em Valor**, verifique se a grade mostra os registros na entidade **Dimensões de Preço**. 
2. Adicione **Recurso Reservável** a essa lista de dimensões de preço como **msdyn_bookableresource**. 
3. Em **Aplicável ao custo** e **Aplicável a vendas**, selecione um valor.
4. Em **Tipo de Dimensão**, selecione **Baseado em valor**. 
5. Selecione a prioridade de vendas e custo para o recurso reservável. Em geral, um recurso reservável tem a maior prioridade quando incluído como uma dimensão de preço. Defina a prioridade como **1** (ou **0** dependendo com a prioridade) para garantir esse comportamento.

## <a name="set-up-pricing-dimension-field-names"></a>Configurar nomes de campo de dimensão de preço

Quando o nome do campo de uma dimensão de preço na tabela **Preço da Função** for diferente do nome de campo em qualquer uma das outras entidades em que o preço padrão é usado, o registro de dimensão de preço deverá ser notificado dos nomes diferentes.  

Para um recurso reservável, a entidade **Membros da Equipe do Projeto** tem um nome de campo ligeiramente diferente do que é chamado na entidade **Preço da Função**: 

 - Entidade **Membros da Equipe do Projeto** = **msdyn_bookableresourceid**
 - Entidade **Preço da Função** = **msdyn_bookableresource**

O registro de dimensão de preço para **msydn_bookableresource** deve ser notificado dessa diferença.

1. Clique duas vezes na linha na grade **Dimensões de Preço** para abrir a página da dimensão de **msdyn_bookableresource**.
2. Na página da dimensão, na guia **Relacionado**, selecione **Nomes de Campos da Dimensão de Preço**.

  ![Guia Nomes de campos da dimensão de preço](media/PD-fieldname.png)

3. Na exibição associada que for aberta, selecione **Adicionar Novo Nome de Campo da Dimensão de Preço**.

  ![Adicionar Novos Nomes de Campo da Dimensão de Preço](media/Add-NewPD-fieldname.png)

  Isso abre a página **Novo nome de campo da dimensão de preço** para **msdyn_bookableresource**. 

4. Na página **Novo Nome de Campo da Dimensão de Preço**, adicione **msdyn_projectteam** ao **Nome Lógico da Entidade**.
5. Adicione **msdyn_bookableresourceid** a **Nome do Campo**.

 ![Formulário Novo nome de campo da dimensão de preço](media/PD-fieldname-Added.png)
