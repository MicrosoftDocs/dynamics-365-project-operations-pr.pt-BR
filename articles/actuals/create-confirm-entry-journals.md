---
title: Criar e confirmar diários de entrada
description: Este tópico fornece informações sobre como criar e confirmar diários de entrada no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584214"
---
# <a name="create-and-confirm-entry-journals"></a>Criar e confirmar diários de entrada

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Você usa os diários de entrada para registrar dados reais diretamente no Microsoft Dynamics 365 Project Operations. Ao usar diários de entrada, você não precisa inserir logs de horas, despesas e uso de material no Project Operations.

Um único diário de entrada permite criar várias linhas de diário. Quando o diário é confirmado, uma linha do diário de entrada registra os dados reais dos seguintes detalhes:

- O custo ou a receita, dependendo do tipo de transação selecionado.
- A classe de transação selecionada. As classes disponíveis são **Hora**, **Despesa**, **Material**, **Honorários**, **Etapa** e **Imposto**.
- O projeto e/ou uma tarefa selecionada na linha do diário.

Siga estas etapas para criar um diário de entrada no Project Operations.

1. Acesse **Vendas** \> **Transações** \> **Diários**.
2. Na página de listagem **Diários de entrada**, no Painel de Ações, selecione **Novo** para criar um diário.
3. Na página **Novo diário**, no campo **Descrição**, digite uma descrição do diário.
4. Verifique se o campo **Tipo de diário** está definido como **Entrada** e selecione **Salvar**. Depois que o novo diário de entrada é salvo, uma guia **Linhas do diário** deve aparecer na página do diário.
5. Na guia **Linhas do diário**, na barra de ferramentas acima da grade, selecione **Novo** para criar uma linha do diário de entrada.
6. Na caixa de diálogo **Criação rápida** para criar uma linha do diário de entrada, defina os campos conforme descrito na tabela a seguir.

    | Campo | Description | Impacto funcional |
    | --- | --- | --- |
    | Classe da Transação | A linha do diário pode ser classificada em uma das seis classes de transação: **Hora**, **Despesa**, **Material**, **Honorários**, **Etapa** ou **Imposto**. | A classe de transação **Imposto** foi desativada no Project Operations. <br> Se você criar uma classe de transação **Imposto**, ela não será processada por faturamento ou em cálculos de custo ou receita. **Etapa** é uma classe de transação somente de receita. <br>A classe de transação **Honorários** representa um adiantamento recebido de cliente. Ela sempre deve ser criada como um par de linhas do diário de vendas cobradas e não cobradas. |
    | Tipo de Transação | Os tipos de transação **Custo**, **Vendas entre organizações** e **Custo da unidade de recursos** devem ser usados para registrar o custo.<br> Os tipos de transação **Vendas Não Cobradas** e **Vendas Cobradas** devem ser usados para registrar a receita. | A classe de transação **Honorários** só funciona com os tipos de transação **Vendas Não Cobradas** e **Vendas Cobradas**.<br> A classe de transação **Etapa** só funciona com o tipo de transação **Vendas Cobradas**. <br>Os tipos de transação **Vendas entre Organizações** e **Custo da unidade de recursos** são aplicáveis apenas à classe de transação **Horas** e só estão disponíveis em diários de entrada no cenário de implantação Lite e não ao implantar o Project Operations nos cenários baseados em recursos/sem itens em estoque. |
    | Selecionar Produto | Quando a classe de transação **Material** é selecionada, esse campo permite especificar se a transação de material para a qual você está criando a linha do diário é um produto existente ou um produto fora do catálogo. | Se você selecionar **Produto fora do catálogo**, digite um nome para o produto. |
    | Produto | Uma referência ao produto do catálogo. | |
    | Description | Uma descrição da linha do diário para facilitar a identificação. | Para linhas do diário de vendas não cobradas, o valor será usado como descrição quando os detalhes da linha da fatura forem criados. |
    | Descrição externa | Uma descrição da linha do diário que pode ser usada para compartilhamento com participantes externos. | Para linhas do diário de vendas não cobradas, o valor será usado como descrição externa quando os detalhes da linha da fatura forem criados. Também pode ser exibido na fatura enviada ao cliente. |
    | Tipo de Cobrança | Um valor que indica se a linha do diário será contada como um componente passível de cobrança, complementar ou não passível de cobrança no projeto. | Em um fluxo típico, o tipo de cobrança é derivado dos termos acordados estabelecidos no contrato. No entanto, ao registrar uma linha do diário, você pode inserir um valor nesse campo. |
    | Data do documento | Use uma data em que a transação ocorreu. | |
    | Data de Início | Use a data em que a transação ocorreu. | Esse campo é usado para comparação com a data de criação da fatura para transações do tipo **Vendas Não Cobradas**. A comparação ajudará você a decidir se a data da transação é uma data futura ou se ocorreu no passado. Somente transações com datas passadas serão adicionadas à fatura. |
    | Data de Término | Use a data em que a transação ocorreu. | |
    | Data da Contabilidade | Use a data em que o impacto contábil será registrado. | |
    | Cliente da linha de contrato | Por padrão, se a linha de contrato tiver apenas um cliente, esse campo será definido como o cliente na linha de contrato quando a linha do diário for salva. Se a linha de contrato tiver vários clientes, selecione o cliente correto. | Se o sistema não puder determinar o cliente da linha de contrato na linha do diário e se estiver em branco nos dados reais do tipo **Vendas Não Cobradas** criados a partir da linha do diário, os dados reais não serão faturados. |
    | Project | Selecione o projeto para registrar os dados reais. | Com base no projeto, na classe de transação e na tarefa selecionados, o sistema tentará determinar o contrato, a linha de contrato e o cliente da linha de contrato. |
    | Tarefa | Selecione a tarefa para registrar os dados reais. | Se você associou tarefas a linhas de contrato durante a configuração do contrato, o sistema usará a tarefa selecionada, junto com um projeto e uma classe de transação, para determinar o contrato, a linha de contrato e o cliente da linha de contrato. |
    | Categoria da Transação | Selecione a categoria da transação para registrar os dados reais. | Para despesas, a categoria de transação selecionada determina o preço padrão que será especificado na linha do diário quando ela for salva. |
    | Função | Esse campo é relevante para linhas do diário de horas. Selecione a função do recurso que gastou tempo no projeto e/ou na tarefa. | Para linhas do diário de horas, se você usar a configuração inicial para a entrada de custos de recursos padrão e taxas de cobrança, a função selecionada será usada junto com a unidade de recursos para determinar o preço padrão que será informado na linha do diário quando ela for salva. Se você usar uma configuração personalizada para a entrada de preços padrão, deverá revisar essa configuração para determinar se o campo **Função** é usado para inserir valores de preço padrão. |
    | Subcontrato | Se a linha do diário representa a capacidade subcontratada ou despesas ou materiais subcontratados, selecione o subcontrato relevante. | Quando as linhas do diário de custos forem registradas, o subcontrato selecionado determinará a lista de preços usada para informar o custo de unidade padrão. |
    | Linha de subcontrato | Se a linha do diário representa a capacidade subcontratada ou despesas ou materiais subcontratados, selecione a linha do subcontrato relevante. | Quando as linhas do diário de custo forem registradas, a linha do subcontrato selecionada garantirá que os cálculos de capacidade disponível na linha do subcontrato sejam calculados corretamente. |
    | Método de Cálculo do Valor | Por padrão, esse campo é definido como **Multiplicar Quantidade Por Preço**. Quando esse método for usado, o valor será calculado como *Quantidade* × *Preço*. O outro método aceito é **Preço Fixo**. Quando esse método for usado, o preço será definido como o valor e a quantidade não será usada no cálculo. | |
    | Agendamento de Unidade e Unidade | Juntos, o agendamento de unidade e a unidade identificam a unidade da quantidade. | A combinação da unidade e da categoria de transação é usada para inserir preços padrão para despesas. Na configuração padrão do Project Operations, a combinação da unidade, da função e da unidade de recursos é usada para inserir preços padrão para hora. Se você tiver uma configuração personalizada para a entrada de preços padrão, ela será usada junto com a unidade. A combinação do produto e da unidade é usada para inserir preços padrão para materiais. |
    | Quantidade | Insira a quantidade. | |
    | Preço | Se o preço for deixado em branco quando a linha do diário for criada, os valores relevantes serão usados para inserir os preços padrão, dependendo da classe da transação. Se um preço for inserido quando a linha do diário for criada, esse preço será usado. | |
    | Imposto | Insira qualquer valor de imposto. | Dependendo do valor do imposto inserido, o valor estendido será calculado como *Valor* + *Imposto*. |

## <a name="confirm-an-entry-journal"></a>Confirmar um diário de entrada

Depois de inserir todas as linhas do diário em um diário de entrada, você poderá confirmá-lo. Esse processo registrará cada linha do diário como dados reais nos projetos apropriados.

Depois que um diário é confirmado, não é mais possível editá-lo nem suas linhas.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Dados reais criados pela confirmação do diário de entrada

Existem algumas diferenças importantes entre os dados reais que são criados pela confirmação do diário de entrada e os dados reais criados durante a aprovação dos logs de horas, despesas e uso de material e a confirmação de fatura no Project Operations:

- Os diários de entrada não usam conexões de transação para vincular os dados reais de custo aos dados reais de vendas não cobradas. Os dados reais que são criados quando os logs de horas, despesas e uso de material são aprovados sempre usam conexões de transação para vincular o custo e os dados reais de vendas não cobradas.
- Os diários de entrada não usam origens de transação para vincular os dados reais de custo e os dados reais de vendas não cobradas em nenhum registro de origem. Os dados reais que são criados quando os logs de horas, despesas e uso de material são aprovados sempre usam origens de transação para vincular o custo e os dados reais de vendas não cobradas à entrada de hora de origem.
- Quando dados reais de vendas não cobradas criados pela confirmação do diário de entrada são faturados, os dados reais de vendas cobradas criados durante a confirmação da fatura são vinculados aos dados reais de vendas não cobradas, de maneira semelhante aos dados reais de vendas não cobradas que são criados quando os logs de horas, despesas e uso de material são aprovados.
- As linhas do diário de entrada que são criadas para as horas informadas por recursos interorganizacionais não faz com que os dados reais dos tipos **Custo da unidade de recursos** e **Vendas entre Organizações** sejam criados automaticamente. Esses dados reais devem ser criados manualmente. Esse comportamento difere do comportamento para entradas de hora registradas por recursos interorganizacionais. Nesse caso, quando as horas são aprovadas, o aplicativo cria os dados reais do tipo **Custo** automaticamente no projeto e os dados reais dos tipos **Custo da unidade de recursos** e **Vendas entre Organizações** na divisão proprietária do funcionário. Em seguida, ele usa as conexões de transação para vincular esses dados reais e as origens de transação a fim de vinculá-los à entrada de hora de origem.
- Quando os diários de entrada são confirmados, eles criam dados reais. No entanto, os diários de correção não podem ser usados para corrigir esses dados reais. Esse comportamento é diferente do comportamento dos dados reais que são criados quando os logs de horas, despesas e uso de material são aprovados. Nesse caso, o aplicativo permite que você use Diários de correção para corrigir os dados reais a fim de corrigir quaisquer erros, desde que esses dados reais ainda não tenham sido faturados. Se eles já tiverem sido faturados, você ainda poderá corrigi-los se processar um crédito completo desse dado real para o cliente.

> [!NOTE]
> Os diários de entrada não impõem regras rígidas de padronização. Por isso, use esses diários de entrada o mínimo possível e tenha cuidado para não criar dados financeiros corrompidos no sistema. Sempre que puder, use os logs de horas, despesas e uso de material, a configuração de etapa e honorários em contratos de projeto e o processo de confirmação de fatura do projeto em vez de diários de entrada para criar dados reais.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
