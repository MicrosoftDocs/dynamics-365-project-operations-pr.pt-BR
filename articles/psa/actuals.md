---
title: Visão geral dos dados reais
description: Este artigo fornece informações sobre dados reais do projeto.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 35282e6c51fff28dbbb0a5a7de760788416ed0e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929062"
---
# <a name="actuals-overview"></a>Visão geral dos dados reais

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os dados reais são o volume de trabalho que foi concluído em um projeto. Os dados reais do projeto podem ser rastreados para seus documentos de origem. Esses documentos de origem incluem hora, despesa e entradas de diário, além de faturas.

![Como os dados reais do projeto são rastreados para documentos de origem.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Enviando uma entrada de hora

No PSA, quando uma entrada de hora é enviada para um projeto que está mapeado para uma linha de contrato de tempo e materiais, são criadas duas linhas de diário. Uma linha destinada ao custo e a outra às vendas não faturadas. Quando uma entrada de hora é enviada para um projeto que está mapeado para uma linha de contrato de preço fixo, uma linha do diário é criada apenas para custo. 

A lógica para inserir preços padrão reside na linha do diário. Todos os valores de campo de uma entrada de hora são copiados para a linha do diário. Esses campos incluem a data da transação, a linha de contrato para a qual o projeto está mapeado e o resultado da moeda na lista de preços apropriada. 

Os campos que afetam preços padrão, como **Função** e **Unidades Organizacional**, fazem com que um preço apropriado seja inserido por padrão na linha do diário. Se você adicionar um campo personalizado na entrada de hora e quiser que o valor do campo seja propagado para os dados reais, crie o campo na entidade Dados Reais e use mapeamentos de campo para copiar o campo da entrada de hora para os dados reais.

## <a name="submitting-an-expense-entry"></a>Enviando uma entrada de despesa

No PSA, quando uma entrada de despesa é enviada para um projeto que está mapeado para uma linha de contrato de tempo e materiais, são criadas duas linhas de diário. Uma linha destinada ao custo e a outra às vendas não faturadas. Quando uma entrada de despesa é enviada para um projeto que está mapeado para uma linha de contrato de preço fixo, uma linha do diário é criada apenas para custo.

A lógica para inserir preços padrão para despesas se baseia na categoria da despesa que é selecionada na página **Entrada de despesa**. A data da transação, a linha de contrato para a qual o projeto é mapeado e a moeda são usados para determinar a lista de preços adequada. No entanto, para o preço em si, o valor que o usuário inseriu é definido diretamente nas linhas de diário da despesa relacionadas para custo e vendas por padrão.

Na versão atual do PSA, a entrada baseada em categoria dos preços padrão por unidade nas entradas de despesa não está disponível.

## <a name="using-entry-journals-to-record-costs"></a>Usando Diários de entrada para registrar custos

No PSA, os Diários de entrada permitem registrar o custo ou a receita nas classes de material, valor, hora, despesa ou transação de imposto. Um diário possui um cabeçalho, linhas e uma ação **Confirmar**. Veja a seguir alguns cenários onde você pode usar um diário:

- Você deve registrar os custos reais de material e as vendas em um projeto.
- Você deve mover dados reais da transação de outro sistema para o PSA.
- Você deve registrar os custos que ocorreram em outro sistema, como custos de aquisição ou subcontratação.

> [!IMPORTANT]
> O uso de Diários de entrada para criar dados reais deve ser realizado somente por um usuário totalmente ciente do impacto contábil que os Dados reais têm no projeto. Isso ocorre porque o aplicativo não valida o tipo de linha do diário, ou o preço relacionado inserido na linha do diário. Devido ao impacto desse tipo de diário, é necessário ter cautela ao determinar para quem conceder acesso para a criação de Diários de entrada.     


## <a name="recording-actuals-based-on-project-events"></a>Registrando dados reais baseados em eventos do projeto

Os PSA registra as transações financeiras que ocorrem durante um projeto. Essas transações são registradas como **dados reais**. As tabelas a seguir mostram os diferentes tipos de dados reais que são criados de acordo com o tipo de projeto; se é de preço fixo ou de tempo e materiais, se está no estágio da venda ou se está em um projeto interno.

**O recurso pertence à mesma unidade organizacional que a unidade de contratação do projeto**

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

**O recurso pertence à uma unidade organizacional que é diferente da unidade de contratação do projeto**

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
