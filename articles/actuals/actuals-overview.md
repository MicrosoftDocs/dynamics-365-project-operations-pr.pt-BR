---
title: Dados reais
description: Este tópico oferece informações sobre como trabalhar com dados reais no Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852530"
---
# <a name="actuals"></a>Dados Reais 

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os dados reais representam o progresso financeiro revisado e aprovado e da agenda em um projeto. Eles são criados como resultado de aprovação de tempo, despesas, entradas de uso de material e entradas de diário e faturas.

## <a name="journal-lines-and-time-submission"></a>Linhas do diário e envio de horas

Para obter mais informações sobre a entrada de hora, consulte [Visão geral de entrada de hora](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tempo e materiais

Quando uma entrada de hora enviada está vinculada a um projeto mapeado para uma linha de contrato de tempo e materiais, o sistema cria duas linhas de diário, uma para custo e a outra para vendas não faturadas.

### <a name="fixed-price"></a>Preço fixo

Quando uma entrada enviada está vinculada a um projeto que está mapeado para uma linha de contrato de preço fixo, o sistema cria uma linha de diário para custo.

### <a name="default-pricing"></a>Preço padrão

A lógica para criar preços padrão reside na linha do diário. Os valores de campo da entrada de hora são copiados para a linha do diário. Esses valores incluem a data da transação, a linha de contrato para a qual o projeto está mapeado e o resultado da moeda na lista de preços apropriada.

Os campos que afetam preços padrão, como **Função** e **Unidade de Recursos**, são usados para determinar o preço apropriado na linha do diário. Você pode adicionar um campo personalizado à entrada de hora. Se quiser que o valor do campo seja propagado para reais, crie o campo nas tabelas **Dados Reais** e **Linha do Diário**. Use o código personalizado para propagar o valor do campo selecionado de Entrada de Hora para Dados Reais pela linha de diário usando origens de transação. Para obter mais informações sobre origens de transação e conexões, consulte [Vinculando Dados Reais a registros originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Linhas de diário e envio de despesas básicas

Para obter mais informações sobre a entrada de despesa, consulte [Visão geral de despesas](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tempo e materiais

Quando uma entrada de despesa básica enviada está vinculada a um projeto mapeado para uma linha de contrato de tempo e materiais, o sistema cria duas linhas de diário, uma para custo e a outra para vendas não faturadas.

### <a name="fixed-price"></a>Preço fixo

Quando uma entrada de despesa básica enviada é vinculada a um projeto que está mapeado para uma linha de contrato de preço fixo, o sistema cria uma linha do diário para custo.

### <a name="default-pricing"></a>Preço padrão

A lógica para inserir preços padrão para despesas é baseada na categoria de despesas. A data da transação, a linha de contrato para a qual o projeto é mapeado e a moeda são usados para determinar a lista de preços adequada. Os campos que afetam preços padrão, como **Categoria da Transação** e **Unidade**, são usados para determinar o preço apropriado na linha do diário. No entanto, isso funciona somente quando o método de precificação na lista de preços for **Preço por unidade**. Se o método de precificação for **A preço de custo** ou **Markup sobre custo**, o preço inserido quando a entrada de despesa é criada é usado para o custo e o preço na linha de diário de vendas é calculado com base no método de precificação. 

Você pode adicionar um campo personalizado na entrada de despesa. Se quiser que o valor do campo seja propagado para reais, crie o campo nas tabelas **Dados Reais** e **Linha do Diário**. Use o código personalizado para propagar o valor do campo selecionado de Entrada de Hora para Dados Reais pela linha de diário usando origens de transação. Para obter mais informações sobre origens de transação e conexões, consulte [Vinculando Dados Reais a registros originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Linhas de diário e envio de log de uso de material

Para obter mais informações sobre entrada de despesa, consulte [Log de Uso de Material](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Tempo e materiais

Quando uma entrada de log de uso de material enviada for vinculada a um projeto mapeado para uma linha de contrato de tempo e material, o sistema criará duas linhas de diário, uma para custo e outra para vendas não faturadas.

### <a name="fixed-price"></a>Preço fixo

Quando uma entrada de uso de material enviada é vinculada a um projeto que está mapeado para uma linha de contrato de preço fixo, o sistema cria uma linha do diário para custo.

### <a name="default-pricing"></a>Preço padrão

A lógica para inserir preços padrão para material é baseada na combinação de produto e unidade. A data da transação, a linha de contrato para a qual o projeto é mapeado e a moeda são usados para determinar a lista de preços adequada. Os campos que afetam preços padrão, como **ID do Produto** e **Unidade**, são usados para determinar o preço apropriado na linha do diário. No entanto, isso funciona apenas para produtos do catálogo. Para produtos fora do catálogo, o preço inserido quando a entrada de log de uso de material é criada é usado para o custo e o preço de vendas nas linhas do diário. 

Você pode adicionar um campo personalizado na entrada **Log de Uso de Material**. Se quiser que o valor do campo seja propagado para reais, crie o campo nas tabelas **Dados Reais** e **Linha do Diário**. Use o código personalizado para propagar o valor do campo selecionado de Entrada de Hora para Dados Reais pela linha de diário usando origens de transação. Para obter mais informações sobre origens de transação e conexões, consulte [Vinculando Dados Reais a registros originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Usar diários de entrada para registrar custos

Você pode usar diários de entrada para registrar o custo ou receita nas classes de material, valor, hora, despesa ou transação de imposto. Os diários podem ser usados para as seguintes finalidades:

- Mova os dados reais de transações de outro sistema para o Microsoft Dynamics 365 Project Operations.
- Registre os custos que ocorreram em outro sistema. Esses custos podem incluir custos de aquisição ou subcontratação.

> [!IMPORTANT]
> O aplicativo não valida o tipo de linha do diário ou o preço relacionado inserido na linha do diário. Portanto, somente um usuário que está totalmente ciente do impacto contábil que os dados reais têm no projeto devem usar diários de entrada para criar os dados reais. Devido ao impacto deste tipo de diário, é necessário escolher cuidadosamente quem tem acesso para criar diários de entrada.

## <a name="record-actuals-based-on-project-events"></a>Registrar dados reais baseados em eventos do projeto

O Project Operations registra as transações financeiras que ocorrem durante um projeto. Essas transações são registradas como dados reais. As tabelas a seguir mostram os diferentes tipos de dados reais que são criados de acordo com o tipo de projeto; se é de preço fixo ou de tempo e materiais, se está no estágio da venda ou se está em um projeto interno.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>O recurso pertence à mesma unidade organizacional que a unidade de contratação do projeto

<table>
<thead>
<tr>
<th rowspan="3">Evento</th>
<th colspan="4">Projeto faturável ou vendido</th>
<th rowspan="3">Projeto no estágio de pré-venda</th>
<th rowspan="3">Projeto interno</th>
</tr>
<tr>
<th colspan="2">Tempo e materiais</th>
<th colspan="2">Preço fixo</th>
</tr>
<tr>
<th>Dados Efetivos</th>
<th>Moeda da transação</th>
<th>Preço fixo</th>
<th>Moeda da transação</th>
</tr>
</thead>
<tbody>
<tr>
<td>Uma entrada de hora é criada.</td>
<td colspan="6">Nenhuma atividade na entidade Dados Reais</td>
</tr>
<tr>
<td>Uma entrada de hora é enviada.</td>
<td colspan="6">Nenhuma atividade na entidade Dados Reais</td>
</tr>
<tr>
<td rowspan="2">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</td>
<td>Custo real</td>
<td>Moeda da unidade de contratação</td>
<td rowspan="2">Custo real</td>
<td rowspan="2">Moeda da unidade de contratação
<td rowspan="2">Custo real</td>
<td rowspan="2">Custo real</td>
</tr>
<tr>
<td>Vendas reais não cobradas – passível de cobrança</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td rowspan="3">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</td>
<td>Custo real</td>
<td>Moeda da unidade de contratação</td>
<td rowspan="3">Custo real</td>
<td rowspan="3">Moeda da unidade de contratação</td>
<td rowspan="3">Custo real</td>
<td rowspan="3">Custo real</td>
</tr>
<tr>
<td>Vendas reais não cobradas – passível de cobrança para a nova quantidade</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td>Vendas reais não cobradas – não passível de cobrança para a diferença</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td rowspan="2">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</td>
<td>Reversão de vendas não cobradas</td>
<td>Moeda de contrato de projeto</td>
<td rowspan="2">Vendas cobradas por etapa</td>
<td rowspan="2">Moeda de contrato de projeto</td>
<td rowspan="2">Não aplicável</td>
<td rowspan="2">Não aplicável</td>
</tr>
<tr>
<td>Vendas cobradas</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td rowspan="3">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</td>
<td>Reversão de vendas não cobradas</td>
<td>Moeda de contrato de projeto</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
</tr>
<tr>
<td>Vendas cobradas – passível de cobrança para a nova quantidade</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td>Vendas cobradas – não passível de cobrança para a diferença</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td rowspan="2">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</td>
<td>Vendas cobradas – estorno</td>
<td>Moeda de contrato de projeto</td>
<td rowspan="5">
<ul>
<li>Estorno de vendas cobradas por etapa</li>
<li>Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></li>
</ul>
</td>
<td rowspan="5">Moeda de contrato de projeto</td>
<td rowspan="5">Não aplicável</td>
<td rowspan="5">Não aplicável</td>
</tr>
<tr>
<td>Vendas cobradas</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td rowspan="3">Uma fatura é corrigida para redução da quantidade passível de cobrança.</td>
<td>Vendas cobradas – estorno</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td>Vendas cobradas para a nova quantidade</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td>Vendas não cobradas – passível de cobrança para a diferença</td>
<td>Moeda de contrato de projeto</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>O recurso pertence à uma unidade organizacional que é diferente da unidade de contratação do projeto

<table>
<thead>
<tr>
<th rowspan="3">Evento</th>
<th colspan="4">Projeto faturável ou vendido</th>
<th rowspan="3">Projeto no estágio de pré-venda</th>
<th rowspan="3">Projeto interno</th>
</tr>
<tr>
<th colspan="2">Tempo e materiais</th>
<th colspan="2">Preço fixo</th>
</tr>
<tr>
<th>Dados Efetivos</th>
<th>Moeda da transação</th>
<th>Preço fixo</th>
<th>Moeda da transação</th>
</tr>
</thead>
<tbody>
<tr>
<td>Uma entrada de hora é criada.</td>
<td colspan="6">Nenhuma atividade na entidade Dados Reais</td>
</tr>
<tr>
<td>Uma entrada de hora é enviada.</td>
<td colspan="6">Nenhuma atividade na entidade Dados Reais</td>
</tr>
<tr>
<td rowspan="4">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</td>
<td>Custo real</td>
<td>Moeda da unidade de contratação</td>
<td rowspan="4">Custo real</td>
<td rowspan="4">Moeda da unidade de contratação</td>
<td rowspan="4">Custo real</td>
<td rowspan="4">Custo real</td>
</tr>
<tr>
<td>Vendas reais não cobradas – passível de cobrança</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td>Custo da unidade de recursos</td>
<td>Moeda da unidade de recursos</td>
</tr>
<tr>
<td>Vendas entre organizações</td>
<td>Moeda da unidade de contratação</td>
</tr>
<tr>
<td rowspan="5">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</td>
<td>Custo real</td>
<td>Moeda da unidade de contratação</td>
<td rowspan="5">Custo real</td>
<td rowspan="5">Moeda da unidade de contratação</td>
<td rowspan="5">Custo real</td>
<td rowspan="5">Custo real</td>
</tr>
<tr>
<td>Custo da unidade de recursos</td>
<td>Moeda da unidade de recursos</td>
</tr>
<tr>
<td>Vendas entre organizações</td>
<td>Moeda da unidade de contratação</td>
</tr>
<tr>
<td>Vendas reais não cobradas – passível de cobrança para a nova quantidade</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td>Vendas reais não cobradas – não passível de cobrança para a diferença</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td rowspan="2">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</td>
<td>Reversão de vendas não cobradas</td>
<td>Moeda de contrato de projeto</td>
<td rowspan="2">Vendas cobradas por etapa</td>
<td rowspan="2">Moeda de contrato de projeto</td>
<td rowspan="2">Não aplicável</td>
<td rowspan="2">Não aplicável</td>
</tr>
<tr>
<td>Vendas cobradas</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td rowspan="3">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</td>
<td>Reversão de vendas não cobradas</td>
<td>Moeda de contrato de projeto</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
</tr>
<tr>
<td>Vendas cobradas – passível de cobrança para a nova quantidade</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td>Vendas cobradas – não passível de cobrança para a diferença</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td rowspan="2">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</td>
<td>Vendas cobradas – estorno</td>
<td>Moeda de contrato de projeto</td>
<td rowspan="5">
<ul>
<li>Estorno de vendas cobradas por etapa</li>
<li>Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></li>
</ul>
</td>
<td rowspan="5">Moeda de contrato de projeto</td>
<td rowspan="5">Não aplicável</td>
<td rowspan="5">Não aplicável</td>
</tr>
<tr>
<td>Vendas cobradas</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td rowspan="3">Uma fatura é corrigida para redução da quantidade passível de cobrança.</td>
<td>Vendas cobradas – estorno</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td>Vendas cobradas para a nova quantidade</td>
<td>Moeda de contrato de projeto</td>
</tr>
<tr>
<td>Vendas não cobradas – passível de cobrança para a diferença</td>
<td>Moeda de contrato de projeto</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
