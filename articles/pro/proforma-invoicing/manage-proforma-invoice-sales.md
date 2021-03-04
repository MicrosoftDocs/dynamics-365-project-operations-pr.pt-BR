---
title: Gerenciar uma fatura pro forma - lite
description: Este tópico fornece informações sobre como trabalhar com faturas pro forma.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cd56b99c3ed455848edbd9ff4419afa58d782a3e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181528"
---
# <a name="manage-a-proforma-invoice---lite"></a>Gerenciar uma fatura pro forma - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

No Dynamics 365 Project Operations, as faturas pro forma são criadas como uma extensão das faturas no Dynamics 365 Sales. No entanto, existem muitas diferenças no processo de faturamento entre o Sales e o Project Operations quando se trata de faturamento. Por exemplo, não é possível criar uma nova fatura a partir da página **Lista de Faturas** no Project Operations, mas é possível fazer isso em Sales. Essas diferenças e extensões existem para oferecer suporte aos processos de faturamento para projetos que são diferentes de uma fatura típica para um pedido de venda.

> [!IMPORTANT]
> Por causa das diferenças, não use faturas em Sales e Project Operations de forma alternadamente.

## <a name="invoice-header"></a>Cabeçalho da fatura

As informações a seguir estão disponíveis em um cabeçalho de fatura pro forma no Project Operations.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **ID da Fatura** | Guia **Resumo** | A ID gerada automaticamente quando uma fatura pro forma é criada. Um campo somente leitura que está bloqueado para edição. | Este campo é usado como referência para cada fatura pro forma. |
| **Nome** | Guia **Resumo** | Defina como o nome do contrato do projeto por padrão. Este campo pode ser editado pelo usuário. | &nbsp;  |
| **Moeda** | Guia **Resumo** | Defina como a moeda do contrato do projeto por padrão. Um campo somente leitura que está bloqueado para edição. |&nbsp; |
| **Lista de preços** | Guia **Resumo** | Defina como a lista de preços do contrato do projeto por padrão. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Oportunidade** | Guia **Resumo** | A referência à oportunidade vinculada. Um campo somente leitura que está bloqueado para edição. | &nbsp;  |
| **Contrato** | Guia **Resumo** | A referência ao contrato do projeto vinculado. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Cliente** | Guia **Resumo** | A referência ao contrato do projeto vinculado. Um campo somente leitura que está bloqueado para edição. |&nbsp;  |
| **Descrição** | Guia **Resumo** | O campo de texto que descreve a fatura. Este campo pode ser editado pelo usuário. | &nbsp; |
| **Para Cobrança** e campos relacionados | Guia **Resumo** | Os padrões são definidos a partir do cliente do contrato do projeto. Este campo pode ser editado pelo usuário.  | &nbsp; |
| **Status** | Guia **Resumo** | Define as seguintes opções: **Ativo**, **Fechado**, **Pago** e **Cancelado**, e pode ser editado pelo usuário. | Os status sem suporte para o Project Operations incluem **Fechado** e **Cancelado**. </br> O status está definido como **Ativo** quando a fatura é criada. </br>O status deve ser definido como **Pago** somente após a confirmação da fatura. |
| **Status da Fatura do Projeto** | Guia **Resumo** | Define as seguintes opções: **Rascunho**, **Em análise**, and **Confirmado**, e pode ser editado pelo usuário. | Nos status **Rascunho** e **Em Análise**, a fatura pode ser editada. A fatura não pode ser editada depois de confirmada. |
| **Valor Detalhado** | Guia **Resumo** | A soma dos valores em todas as linhas da fatura após adiantamentos e deduções. Um campo somente leitura que está bloqueado para edição. | Este campo é usado para calcular o valor final. |
| **Desconto (%)** | Guia **Resumo** | Este campo pode ser editado para inserir uma porcentagem de desconto. Este campo não é compatível com a funcionalidade do Project Operations. | Este campo não tem suporte. |
| **Valor do Desconto** | Guia **Resumo** | Este campo pode ser editado para inserir o valor do desconto. Este campo não é compatível com a funcionalidade do Project Operations. | Este campo não tem suporte. |
| **Valor sem Frete** | Guia **Resumo** | O valor total da fatura após a aplicação dos descontos. Um campo somente leitura que está bloqueado para edição. | Este campo é usado para calcular o valor final. |
| **Valor do Frete** | Guia **Resumo** | Este campo pode ser editado para inserir o valor do frete. Este campo não é compatível com a funcionalidade do Project Operations. | Este campo não tem suporte. |
| **Total de Impostos** | Guia **Resumo** | O imposto total de todas as linhas da fatura. Um campo somente leitura que está bloqueado para edição. | Nenhum. |
| **Valor Total** | Guia **Resumo** | A soma do valor após descontos e impostos. | A soma é o valor que o cliente precisa pagar. |
## <a name="project-based-invoice-lines"></a>Linhas da fatura baseadas em projeto

No Project Operations, há sempre uma linha de fatura para cada linha de contrato de projeto. A linha da fatura será criada mesmo se não houver dados reais. As informações a seguir estão disponíveis em uma linha da fatura pro forma.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **ID da Fatura** | Guia **Geral** | A referência à ID da fatura. Um campo somente leitura que está bloqueado para edição. | O link do ID da fatura pode ser usado para navegar de volta ao cabeçalho da fatura. |
| **Nome** | Guia **Geral** | O nome da linha da fatura definido por padrão a partir do nome da linha do contrato. Este campo pode ser editado pelo usuário. | &nbsp; |
| **Project** | Guia **Geral** | O projeto na linha de contrato de projeto relacionada. Um campo somente leitura que está bloqueado para edição. | O link do projeto pode ser usado para navegar até o projeto. |
| **Método de Cobrança** | Guia **Geral** | O método de cobrança na linha de contrato de projeto relacionada. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Valor da Linha de Contrato** | Guia **Geral** | O valor do contrato na linha de contrato do projeto relacionado. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Faturado até Hoje** | Guia **Geral** | A soma dos valores em todos os detalhes da linha de fatura desta fatura. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Valor** | Guia **Geral** | A soma dos valores em todos os detalhes da linha de fatura cobráveis desta fatura. Um campo somente leitura que está bloqueado para edição. | Este campo é usado para calcular o valor final no cabeçalho da fatura. |
| **Imposto** | Guia **Geral** | A soma dos valores de impostos em todos os detalhes da linha de fatura desta linha de fatura. Um campo somente leitura que está bloqueado para edição. | Este campo é usado para calcular o valor do imposto final no cabeçalho da fatura. |
| **Valor Ampliado** | Guia **Geral** | A soma de valores totais (**Imposto + Valores**) em todos os detalhes da linha de fatura cobrável desta linha de fatura. Um campo somente leitura que está bloqueado para edição. | Este campo é usado para calcular o valor final no cabeçalho da fatura. |


## <a name="invoice-line-details"></a>Detalhes da linha da fatura

Cada linha da fatura em uma fatura do projeto inclui detalhes da linha da fatura. Estes detalhes da linha estão relacionados aos dados reais e etapas de vendas não cobradas associados à linha de contrato referenciada pela linha da fatura. Todas essas transações são marcadas como **Pronto para Faturar**.

Para a linha **Fatura de Tempo e Material**, os detalhes da linha da fatura são agrupados em **Cobrável**, **Não cobrável** e **Complementar** na página **Linha de Fatura**. Os detalhes de **Linha de Fatura Cobrável** somam-se ao total da linha da fatura. **Complementar** e **Dados Reais Não Cobráveis** não são adicionados ao total da linha de fatura.

Para a linha **Fatura de Preço Fixo**, os detalhes da linha de fatura são criados a partir de etapas marcadas como **Pronto para faturar** na linha de contrato relacionada. Depois que o detalhe da linha da fatura é criado a partir de uma etapa, o status de faturamento na etapa é atualizado para **Fatura do Cliente Criada**.

### <a name="edit-invoice-line-details"></a>Editar detalhes de linha de fatura

Os seguintes campos estão disponíveis no detalhe de uma linha da fatura com suporte de dado real de vendas não cobradas:

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| **Linha da fatura** | Uma referência à **ID da Linha da Fatura**. Campo somente leitura, bloqueado para edição. | Este link pode ser usado para navegar de volta ao cabeçalho da fatura. |
| **Descrição** | Uma descrição do detalhe da linha de fatura. Definido por padrão no campo **Comentários Internos** na **Entrada de Hora** e no campo **Descrição** em **Entrada de Despesa**. O campo pode ser editado pelo usuário.| &nbsp; |
| **Descrição Externa** | Uma descrição do detalhe da linha de fatura. Definido por padrão no campo **Comentários Externos** na **Entrada de Hora** e no campo **Descrição** em **Entrada de Despesa**. O campo pode ser editado pelo usuário. | Essa descrição pode ser usada para determinar o que deve constar na fatura impressa que será enviada ao cliente. No Project Operations, uma fatura pro forma não tem todas as funcionalidades necessárias para definir as configurações de impressão de uma fatura. |
| **Data de Início** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | Este campo pode ser editado em um novo detalhe de linha de fatura que não é apoiado por uma fonte real. |
| **Project** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | Defina por padrão como o projeto na linha de contrato relacionada. |
| **Tarefa** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | O campo pode ser editado em um novo detalhe de linha de fatura que não é apoiado por uma fonte real. Uma lista suspensa mostra todas as tarefas associadas à linha de contrato do projeto relacionado.  |
| **Categoria da transação** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | O campo pode ser editado em um novo detalhe de linha de fatura que não é apoiado por uma fonte real. |
| **Função** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | O campo pode ser editado em um novo detalhe de linha de fatura que não é apoiado por uma fonte real. |
| **Recurso Reservável** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | O campo pode ser editado em um novo detalhe de linha de fatura que não é apoiado por uma fonte real. |
| **Unidade de Recursos** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | O campo pode ser editado em um novo detalhe de linha de fatura que não é apoiado por uma fonte real. |
| **Quantidade** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | O campo pode ser editado em um novo detalhe de linha de fatura que não é apoiado por uma fonte real. |
| **Agenda da Unidade** | Para detalhes de linha de fatura por hora, isso é sempre definido como hora e não pode ser editado. Para despesas, isso é definido por padrão a partir da despesa real de origem. Um campo somente leitura que está bloqueado para edição. | Definido por padrão como **Hora** em um novo detalhe de linha de fatura que não é apoiado por um dado real. |
| **Unidade** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | O campo pode ser editado em um novo detalhe de linha de fatura que não é apoiado por um dado real de origem |
| **Preço** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | O campo pode ser editado em um novo detalhe de linha de fatura que não é apoiado por uma fonte real. Se nenhum valor for inserido, ele será definido por padrão após **Salvar**. |
| **Moeda** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | Definido por padrão no cabeçalho da fatura ao criar um novo detalhe da fatura sem o apoio real.  Um campo somente leitura que está bloqueado para edição. |
| **Valor** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | Calculado como **Quantidade \* Preço** ao criar um novo detalhe de fatura sem um dado real de apoio. Ele é calculado após **Salvar**. Um campo somente leitura que está bloqueado para edição. |
| **Imposto** | Definido por padrão a partir da fonte real. O campo pode ser editado pelo usuário | O campo pode ser editado pelo usuário ao criar um novo detalhe de linha de fatura sem um dado real de apoio. |
| **Valor Ampliado** | Um campo calculado, calculado como **Valor + Imposto**. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Tipo de Cobrança** | Definido por padrão a partir da fonte real. O campo pode ser editado pelo usuário. | Selecionar **Cobrável** adiciona a linha ao total da linha da fatura. **Complementar** e **Não cobrável** irá excluí-lo do total da linha da fatura. |
| **Tipo de Transação** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | Definido por padrão como **Vendas Cobradas** e bloqueado ao criar um novo **Detalhe da linha de fatura** sem um dado real de apoio.  |
| **Classe da Transação** | Definido por padrão a partir da fonte real. Um campo somente leitura que está bloqueado para edição. | Definido por padrão com base na opção do usuário em criar um detalhe da linha de fatura **Hora**, **Despesa** ou **Taxa**, além de criar um novo **Detalhe da linha de fatura** sem um dado real de apoio. Bloqueado para edição. |

Os seguintes campos estão disponíveis em um detalhe de linha da fatura com suporte de uma etapa:

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| **Linha da fatura** | Referência à **ID da Linha da Fatura**. Um campo somente leitura que está bloqueado para edição. | O link pode ser usado para navegar de volta ao cabeçalho da fatura. |
| **Descrição** | Descrição do detalhe da linha de fatura. Definido por padrão a partir da descrição da etapa de origem. | &nbsp; |
|**Descrição Externa** | Descrição do detalhe da linha da fatura que é definido por padrão a partir da descrição da etapa de origem. | Esse campo pode ser usado para determinar o que deve constar na fatura impressa que será enviada ao cliente. Uma fatura pro forma no Project Operations não tem todas as funcionalidades necessárias para definir as configurações de impressão de uma fatura. |
| **Data de Início** | Definido por padrão na data da **Etapa** na etapa de origem. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Projeto** | Definido por padrão a partir da etapa de origem. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Tarefa** | Definido por padrão a partir da etapa de origem. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Categoria da transação** | Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Função** | Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Recurso Reservável** | Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Unidade de Recursos** | Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Agenda da Unidade** | Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Unidade** | Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Preço** | Definido por padrão a partir do valor na etapa de origem. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Moeda** | Definido por padrão a partir da etapa de origem. Um campo somente leitura que está bloqueado para edição. |&nbsp; |
| **Valor** | Definido por padrão a partir do valor na etapa de origem. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Imposto** | Definido por padrão a partir do valor de imposto na etapa de origem. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Valor Ampliado** | Definido por padrão a partir do valor total na etapa de origem. O campo pode ser editado pelo usuário | &nbsp; |
| **Tipo de Cobrança** | Sempre definido por padrão como **Cobrável**. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Tipo de Transação** | Definido por padrão a partir da etapa de origem. Um campo somente leitura que está bloqueado para edição. | &nbsp; |
| **Classe da Transação** | Definido por padrão a partir da etapa de origem. Um campo somente leitura que está bloqueado para edição. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Criar novos detalhes da linha de fatura

Nas linhas de hora e material da fatura, você pode criar novos detalhes da linha de fatura. Esses detalhes da linha de fatura não têm suporte de um dado real. Na linha da fatura de uma linha de hora e material da fatura, você pode selecionar **Novo** para criar um novo detalhe da linha de fatura para as classes de transações que são incluídas na linha do contrato.

## <a name="refresh-invoice-transactions"></a>Atualizar transações da fatura

Se houver dados reais recebidos após a criação da fatura, você poderá incluí-los na fatura.

1. Na **Exibição do Backlog de Cobrança**, marque os dados como **Pronto para Faturamento**.   
2. Abra a fatura pro forma de rascunho e, na faixa de opções **Ações**, clique em **Atualizar Transações de Linha de Fatura**.

  Isso cria detalhes da linha de fatura para qualquer dado real com data anterior e marcado como **Pronto para Faturamento**; mas não está incluído na fatura.

## <a name="product-based-invoice-lines"></a>Linhas da fatura baseadas em produto

No Project Operations, você pode criar linhas de fatura para produtos que não se aplicam a projetos ou para todos os projetos junto com linhas de fatura baseadas em projeto. Essas linhas de fatura são criadas como linhas de contrato baseadas em produto e, após serem marcadas como prontas para faturamento, são adicionadas como linhas de fatura baseadas em produto.

Após você adicionar as linhas de fatura baseadas em produto, elas não poderão ser alteradas. No entanto, elas poderão ser excluídas da fatura pro forma de rascunho.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]