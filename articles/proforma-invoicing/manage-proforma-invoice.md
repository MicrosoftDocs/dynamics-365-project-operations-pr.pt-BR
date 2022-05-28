---
title: Gerenciar uma fatura pro forma baseada em projeto
description: Este tópico fornece informações sobre como gerenciar e trabalhar com faturas pro forma baseadas em projeto.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c61b0d887ae35988f1765d40de0447aa5fd7efd4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593736"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Gerenciar uma fatura pro forma baseada em projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

No Dynamics 365 Project Operations, as faturas pro forma são criadas como uma extensão das faturas no Dynamics 365 Sales. No entanto, existem muitas diferenças no processo de faturamento entre o Sales e o Project Operations quando se trata de faturamento. Por exemplo, não é possível criar uma nova fatura a partir da página **Lista de Faturas** no Project Operations, mas é possível fazer isso em Sales. Essas diferenças e extensões existem para oferecer suporte aos processos de faturamento para projetos que são diferentes de uma fatura típica para um pedido de venda.

> [!IMPORTANT]
> Por causa das diferenças, não use faturas em Sales e Project Operations de forma alternadamente.

## <a name="invoice-header"></a>Cabeçalho da fatura

As informações a seguir estão disponíveis em um cabeçalho de fatura pro forma no Project Operations.

| Campo | Localização | Descrição |
| --- | --- | --- | 
| **ID da fatura** | Guia **Resumo** | A ID gerada automaticamente quando uma fatura pro forma é criada. Um campo somente leitura que está bloqueado para edição. Este campo é usado como referência para cada fatura pro forma. |
| **Nome** | Guia **Resumo** | Defina como o nome do contrato do projeto por padrão. Este campo pode ser editado. | 
| **Moeda** | Guia **Resumo** | Defina como a moeda do contrato do projeto por padrão. Um campo somente leitura que está bloqueado para edição. |
| **Lista de preços** | Guia **Resumo** | Defina como a lista de preços do contrato do projeto por padrão. Um campo somente leitura que está bloqueado para edição. | 
| **Oportunidade** | Guia **Resumo** | A referência à oportunidade vinculada. Um campo somente leitura que está bloqueado para edição. | 
| **Contrato** | Guia **Resumo** | A referência ao contrato do projeto vinculado. Um campo somente leitura que está bloqueado para edição. | 
| **Cliente** | Guia **Resumo** | A referência ao contrato do projeto vinculado. Um campo somente leitura que está bloqueado para edição. |
| **Descrição** | Guia **Resumo** | O campo de texto que descreve a fatura. Este campo pode ser editado. | 
| **Para Cobrança** e campos relacionados | Guia **Resumo** | Os padrões são definidos a partir do cliente do contrato do projeto. Este campo pode ser editado.  | 
| **Status** | Guia **Resumo** | Define as seguintes opções: **Ativo**, **Fechado**, **Pago** e **Cancelado**, e pode ser editado. Os status sem suporte para o Project Operations incluem **Fechado** e **Cancelado**. </br> O status está definido como **Ativo** quando a fatura é criada. </br>O status deve ser definido como **Pago** somente após a confirmação da fatura.  | 
| **Status da Fatura do Projeto** | Guia **Resumo** | Define as seguintes opções: **Rascunho**, **Em análise** e **Confirmado**, e pode ser editado. Nos status **Rascunho** e **Em Análise**, a fatura pode ser editada. A fatura não pode ser editada depois de confirmada. | 
| **Valor Detalhado** | Guia **Resumo** | A soma dos valores em todas as linhas da fatura após adiantamentos e deduções. Um campo somente leitura que está bloqueado para edição.  Este campo é usado para calcular o valor final. | 
| **Desconto (%)** | Guia **Resumo** | Este campo pode ser editado para inserir uma porcentagem de desconto. Este campo não é compatível com a funcionalidade do Project Operations. Este campo não tem suporte.|  
| **Valor do Desconto** | Guia **Resumo** | Este campo pode ser editado para inserir o valor do desconto. Este campo não é compatível com a funcionalidade do Project Operations. Este campo não tem suporte. |  
| **Valor sem Frete** | Guia **Resumo** | O valor total da fatura após a aplicação dos descontos. Um campo somente leitura que está bloqueado para edição. Este campo é usado para calcular o valor final.  | 
| **Valor do Frete** | Guia **Resumo** | Este campo pode ser editado para inserir o valor do frete. Este campo não é compatível com a funcionalidade do Project Operations. Este campo não tem suporte. |
| **Total de Impostos** | Guia **Resumo** | O imposto total de todas as linhas da fatura. Um campo somente leitura que está bloqueado para edição. | 
| **Valor Total** | Guia **Resumo** | A soma do valor após descontos e impostos. A soma é o valor que o cliente precisa pagar. | 

## <a name="project-based-invoice-lines"></a>Linhas da fatura baseadas em projeto

No Project Operations, há sempre uma linha de fatura para cada linha de contrato de projeto. A linha da fatura será criada mesmo se não houver dados reais. As informações a seguir estão disponíveis em uma linha da fatura pro forma.

| Campo | Localização | Descrição | 
| --- | --- | --- |
| **ID da fatura** | Guia **Geral** | A referência à ID da fatura. Um campo somente leitura que está bloqueado para edição. O link do ID da fatura pode ser usado para navegar de volta ao cabeçalho da fatura. | 
| **Nome** | Guia **Geral** | O nome da linha da fatura definido por padrão a partir do nome da linha do contrato. Este campo pode ser editado. |
| **Project** | Guia **Geral** | O projeto na linha de contrato de projeto relacionada. Um campo somente leitura que está bloqueado para edição. O link do projeto pode ser usado para navegar até o projeto. | 
| **Método de Cobrança** | Guia **Geral** | O método de cobrança na linha de contrato de projeto relacionada. Um campo somente leitura que está bloqueado para edição. |
| **Valor da Linha de Contrato** | Guia **Geral** | O valor do contrato na linha de contrato do projeto relacionado. Um campo somente leitura que está bloqueado para edição. | 
| **Faturado até Hoje** | Guia **Geral** | A soma dos valores em todos os detalhes da linha de fatura desta fatura. Um campo somente leitura que está bloqueado para edição. | 
| **Valor** | Guia **Geral** | A soma dos valores em todos os detalhes da linha de fatura cobráveis desta fatura. Um campo somente leitura que está bloqueado para edição. Este campo é usado para calcular o valor final no cabeçalho da fatura. | 
| **Imposto** | Guia **Geral** | A soma dos valores de impostos em todos os detalhes da linha de fatura desta linha de fatura. Um campo somente leitura que está bloqueado para edição. Este campo é usado para calcular o valor do imposto final no cabeçalho da fatura. | 
| **Valor Ampliado** | Guia **Geral** | A soma de valores totais (**Imposto + Valores**) em todos os detalhes da linha de fatura cobrável desta linha de fatura. Um campo somente leitura que está bloqueado para edição. Este campo é usado para calcular o valor final no cabeçalho da fatura. |

## <a name="invoice-line-details"></a>Detalhes da linha da fatura

Cada linha da fatura em uma fatura do projeto inclui detalhes da linha da fatura. Estes detalhes da linha estão relacionados aos dados reais e etapas de vendas não cobradas associados à linha de contrato referenciada pela linha da fatura. Todas essas transações são marcadas como **Pronto para Faturar**.

Para uma linha **Fatura de Tempo e Material**, os detalhes da linha da fatura são agrupados em **Cobrável**, **Não cobrável** e **Complementar** na página **Linha de Fatura**. Os detalhes de **Linha de Fatura Cobrável** somam-se ao total da linha da fatura. **Complementar** e **Dados Reais Não Cobráveis** não são adicionados ao total da linha de fatura.

Para uma linha **Fatura de Preço Fixo**, os detalhes da linha da fatura são criados a partir de etapas marcadas como **Pronto para faturamento** na linha de contrato relacionada. Depois que o detalhe da linha da fatura é criado a partir de uma etapa, o status de faturamento na etapa é atualizado para **Fatura do Cliente Criada**.

### <a name="edit-invoice-line-details"></a>Editar detalhes de linha de fatura

Os campos a seguir estão disponíveis no detalhe da linha da fatura com suporte de valor real de vendas não cobradas.

| Campo | Descrição |
| --- | --- | 
| **Linha da fatura** | Uma referência à **ID da Linha da Fatura**. Este campo é somente leitura e bloqueado para edição. Este link pode ser usado para navegar de volta ao cabeçalho da fatura. | 
| **Descrição** | Uma descrição do detalhe da linha de fatura. Definido por padrão no campo **Comentários Internos** na **Entrada de Hora** e no campo **Descrição** em **Entrada de Despesa**. O campo pode ser editado.| 
| **Descrição Externa** | Uma descrição do detalhe da linha de fatura. Definido por padrão no campo **Comentários Externos** na **Entrada de Hora** e no campo **Descrição** em **Entrada de Despesa**. O campo pode ser editado. Essa descrição pode ser usada para determinar o que deve constar na fatura impressa que será enviada ao cliente. No Project Operations, uma fatura pro forma não tem todas as funcionalidades necessárias para definir as configurações de impressão de uma fatura. | 
| **Data de Início** | Este é um campo somente leitura definido por padrão a partir de dados reais de origem. |
| **Project** | Este é um campo somente leitura que é definido por padrão a partir de dados reais de origem para o projeto na linha de contrato relacionada. |  
| **Tarefa** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. |
| **Categoria da transação** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | 
| **Função** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. |  
| **Recurso Reservável** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | 
| **Empresa de Recursos** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | 
| **Unidade de Recursos** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | 
| **Quantidade** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. |  
| **Agenda da Unidade** | Para detalhes de linha de fatura por hora, isso é sempre definido como hora e não pode ser editado. Para despesas, isso é definido por padrão a partir da despesa real de origem. Um campo somente leitura que está bloqueado para edição. | 
| **Unidade** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. |  
| **Preço** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. |
| **Moeda** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | 
| **Valor** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | 
| **Imposto** | Definido por padrão a partir da fonte real. O campo pode ser editado.| 
| **Valor Ampliado** | Um campo calculado, calculado como **Valor + Imposto**. Um campo somente leitura que está bloqueado para edição. | 
| **Tipo de Cobrança** | Definido por padrão a partir da fonte real. O campo pode ser editado. Selecionar **Cobrável** adiciona a linha ao total da linha da fatura. **Complementar** e **Não cobrável** irá excluí-lo do total da linha da fatura.| 
| **Selecionar Produto** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. |
| **Produto** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | 
| **Nome do Produto** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. |  
| **Descrição da Gravação** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. |
| **Tipo de Transação** | Este é um campo somente leitura, que é definido por padrão a partir de dados reais de origem como **Vendas Cobradas**. |  
| **Classe da Transação** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | 

Os campos a seguir estão disponíveis em um detalhe de linha da fatura com suporte de uma etapa.

| Campo | Descrição |
| --- | --- | 
| **Linha da fatura** | Referência à **ID da Linha da Fatura**. Um campo somente leitura que está bloqueado para edição. O link pode ser usado para navegar de volta ao cabeçalho da fatura.  | 
| **Descrição** | Descrição do detalhe da linha de fatura. Definido por padrão a partir da descrição da etapa de origem. | 
|**Descrição Externa** | Descrição do detalhe da linha da fatura que é definido por padrão a partir da descrição da etapa de origem. Esse campo pode ser usado para determinar o que deve constar na fatura impressa que será enviada ao cliente. Uma fatura pro forma no Project Operations não tem todas as funcionalidades necessárias para definir as configurações de impressão de uma fatura. | 
| **Data de Início** | Definido por padrão na data da **Etapa** na etapa de origem. Um campo somente leitura que está bloqueado para edição. | 
| **Project** | Definido por padrão a partir da etapa de origem. Um campo somente leitura que está bloqueado para edição. |
| **Tarefa** | Definido por padrão a partir da etapa de origem. Um campo somente leitura que está bloqueado para edição. | 
| **Categoria da transação** | Um campo somente leitura que está bloqueado para edição. |
| **Função** | Um campo somente leitura que está bloqueado para edição. | 
| **Recurso Reservável** | Um campo somente leitura que está bloqueado para edição. | 
| **Unidade de Recursos** | Um campo somente leitura que está bloqueado para edição. | 
| **Agenda da Unidade** | Um campo somente leitura que está bloqueado para edição. | 
| **Unidade** | Um campo somente leitura que está bloqueado para edição. | 
| **Preço** | Definido por padrão a partir do valor na etapa de origem. Um campo somente leitura que está bloqueado para edição. |
| **Moeda** | Definido por padrão a partir da etapa de origem. Um campo somente leitura que está bloqueado para edição. |
| **Valor** | Definido por padrão a partir do valor na etapa de origem. Um campo somente leitura que está bloqueado para edição. | 
| **Imposto** | Definido por padrão a partir do valor de imposto na etapa de origem. Um campo somente leitura que está bloqueado para edição. |
| **Valor Ampliado** | Definido por padrão a partir do valor total na etapa de origem. O campo pode ser editado. | 
| **Tipo de Cobrança** | Sempre definido por padrão como **Cobrável**. Um campo somente leitura que está bloqueado para edição. |
| **Tipo de Transação** | Definido por padrão a partir da etapa de origem. Um campo somente leitura que está bloqueado para edição. | 
| **Classe da Transação** | Definido por padrão a partir da etapa de origem. Um campo somente leitura que está bloqueado para edição. | 

## <a name="refresh-invoice-transactions"></a>Atualizar transações da fatura

Se houver dados reais recebidos após a criação da fatura, você poderá incluí-los na fatura.

1. Na **Exibição do Backlog de Cobrança**, marque os dados como **Pronto para Faturamento**.   
2. Abra o rascunho da fatura pro forma e, na faixa de opções **Ações**, selecione **Atualizar Transações de Linha de Fatura**.

  Os detalhes da linha de fatura são criados para qualquer data real no passado e marcada como **Pronto para Faturamento**, mas não estão incluídos na fatura.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
