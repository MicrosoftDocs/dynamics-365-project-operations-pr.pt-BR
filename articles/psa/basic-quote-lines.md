---
title: Cotações e linhas da cotação
description: Este artigo fornece informações sobre cotações e linhas da cotação.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
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
ms.openlocfilehash: 4c59f018adc7ee439fd77a819e2fb7620941e958
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933340"
---
# <a name="quotes-and-quote-lines"></a>Cotações e linhas da cotação

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

No Dynamics 365 Project Service Automation, há dois tipos de cotação: de projeto e de vendas. Os dois tipos diferem nos seguintes aspectos:

- Em uma cotação de vendas, há apenas uma grade para itens de linha. Em uma cotação de projeto, há duas grades para itens de linha: uma para linhas de projeto e uma para linhas de produto.
- Uma cotação de vendas dá suporte à ativação e a revisões. Uma cotação do projeto não aceita esses processos.
- Você pode anexar vários ordens a uma cotação de vendas. Você pode anexar apenas um contrato de projeto a uma cotação de projeto.
- Você pode ganhar uma cotação de vendas e manter a oportunidade relacionada aberta. Depois que uma cotação de projeto é ganha, a oportunidade relacionada é fechada.
- Uma cotação de vendas não inclui alguns campos e conceitos que são incluídos em uma cotação de projeto. Os campos incluem **Unidade de Contratação**, **Gerente de Contas** e **Nome do Contato para Cobrança**.  
- As cotações de vendas e cotações de projeto também são identificadas por um campo baseado no conjunto de opções chamado **Tipo**. Para uma cotação de vendas, esse campo tem o valor **Com base no item**. Para uma cotação de projeto, ele tem o valor **Com base no trabalho**.

Este artigo focará os detalhes de cotações de projeto.

Uma cotação de projeto no PSA pode ter vários itens de linha ou linhas de cotação. Na verdade, uma cotação de projeto tem duas grades para itens de linha. Uma grade é para linhas baseadas no projeto que permitem estimativas detalhadas. A outra grade é para linhas baseadas no produto que usam um preço unitário simples e abordagem baseada em quantidade.

- **Com base no projeto** – o valor (cotado) é determinado depois que você estima o quanto de trabalho é necessário. É possível estimar o trabalho em um nível alto ou estimá-lo diretamente como detalhes de linha abaixo de cada linha da cotação. Por fim, você pode estimar o trabalho com base em estimativas detalhadas usando um projeto e plano de projeto. As linhas de cotação baseadas no projeto são encontradas na cotações baseadas em projeto que são criadas usando o Project Service Automation. Esse tipo de linha de cotação é um formulário personalizado das linhas de cotação fora do catálogo que estão disponíveis no Microsoft Dynamics 365 Sales.
- **Com base no produto** – o valor (cotado) é determinado de acordo com a quantidade de unidades que é vendida e com o preço unitário de venda do produto. O produto em uma linha baseada no produto pode vir de um catálogo de produtos em Sales ou pode ser um produto que você define. Esse tipo de linha de cotação também está disponível em cotações baseadas no projeto que são criadas usando o PSA.

O valor em uma cotação é o total nas linhas baseadas no produto e linhas baseadas no projeto.

> [!NOTE]
> As cotações e linhas de cotação não são exigidas no PSA. Você pode iniciar o processo de projeto com um contrato de projeto (projeto vendido). No entanto, uma oportunidade é sempre necessária, independentemente de você iniciar com uma cotação ou um contrato de projeto.

## <a name="project-based-quote-lines"></a>Linhas de cotação baseadas no projeto

Uma linha de cotação baseada em projeto no PSA tem os seguintes métodos de cobrança:

- Hora e material
- Preço fixo

### <a name="time-and-material"></a>Hora e material

O método de cobrança Tempo e material se baseia no consumo. Quando você seleciona esse método de cobrança, o cliente é faturado à medida que o projeto incorre em custos. As faturas são criadas em uma frequência periódica baseada em data. Durante o processo de vendas, o valor cotado de um componente de tempo e material dá apenas uma estimativa do custo final para o cliente. O fornecedor não se compromete a concluir o projeto exatamente pelo valor cotado. Os componentes de tempo e material aumentam o risco do cliente. Os clientes podem querer negociar cláusulas adicionais para minimizar o risco. O PSA não aceita a definição de cláusulas de limite máximo.

### <a name="fixed-price"></a>Preço fixo

No método de cobrança Preço fixo, um fornecedor se compromete a entregar o projeto a um custo fixo ao cliente. O valor cotado da linha de cotação de preço fixo é cobrado do cliente, independentemente dos custos em que o fornecedor incorre para entregar essa linha de cotação. O valor da linha de cotação de preço fixo é cobrado de uma destas maneiras: 

- Como um valor de quantia total no início ou término do projeto, ou quando uma etapa de projeto é atingida. 
- Na frequência baseada em data de parcelas iguais do valor fixo na linha de cotação. Essas parcelas são conhecidas como etapas periódicas.
- Em parcelas que têm um valor monetário alinhado ao andamento do trabalho ou etapas específicas que são atingidas no projeto. Nesse caso, o valor de cada parcela pode ser diferente, mas todas devem somar o valor fixo na linha de cotação.

O PSA dá suporte a três tipos de agendamento de fatura para linhas de cotação de preço fixo.

## <a name="transaction-classification"></a>Classificação da transação

As organizações de serviço profissionais geralmente cotam e faturam seus clientes por classificação de custos. No PSA, os custos são representados pelas seguintes classificações de transação:

- **Tempo** – essa classificação representa o custo de mão de obra ou tempo dos recursos humanos em um projeto.
- **Despesa**: – essa classificação representa todos os outros tipos de despesa em um projeto. Como as despesas podem ser amplamente classificadas, a maioria das organizações cria subcategorias, como viagem, aluguel de carro, hotel ou materiais de escritório.
- **Taxa** – essa classificação representa despesas diversas, multas e outros itens que são cobrados do cliente. 
- **Imposto** – essa classificação representa valores de imposto que os usuários adicionam enquanto inserem despesas.
- **Transação de material** – essa classificação representa dados reais de linhas de produto em uma fatura de projeto confirmada.
- **Etapa** – essa classificação é usada pela lógica de cobrança de preço fixo no PSA.

Uma ou mais dessas classificações de transação podem ser associadas a cada linha de cotação. Depois que uma cotação é ganha, o mapeamento entre classificação de transação e linha de cotação é transferido para a linha de contrato.
 
> ![Captura de tela dos tipos de transação de mapeamento para cotação e linhas de contrato.](media/basic-guide-5.png)
  
Por exemplo, uma cotação pode conter as duas linhas de cotação seguintes: 
- Trabalho de consultoria que usa um método de cobrança Tempo e material, onde classificações de transação de taxa e tempo são aplicáveis. Por exemplo, todas as transações de taxa e tempo para o projeto de exemplo **Implementação do Dynamics AX** são faturadas para o cliente com base no tempo e nos materiais que são usados. 
- Despesas de viagem relacionadas que usam um método de cobrança Preço fixo. Por exemplo, todas as despesas de viagem para o projeto de exemplo **Implementação do Dynamics AX** são faturadas a um valor monetário fixo.

> [!NOTE]
> A combinação das classificações de transação e projeto de **Tempo**, **Despesa** e **Taxa** que são associadas a uma linha de contato ou linha de cotação devem ser exclusivas. Se a mesma combinação de classes de transação e projeto for associada a mais de uma linha de contrato ou linha de cotação, o PSA não funcionará corretamente.

## <a name="billing-types"></a>Tipos de cobrança

O campo **Tipo de Cobrança** define o conceito de encargos no PSA. Trata-se de um conjunto de opções que tem os seguintes valores possíveis:

- **Passível de Cobrança** – o custo que é acumulado por essa função/categoria é um custo direto que impulsiona a execução do projeto, e o cliente pagará por esse trabalho. O pagamento pode ser administrado como um compromisso de tempo e material ou preço fixo. No entanto, o funcionário que gasta esse tempo receberá o crédito correspondente para suas horas trabalhadas faturáveis.
- **Não passível de cobrança** – o custo que é acumulado por essa função/categoria é considerado um custo direto que impulsiona a execução do projeto, embora o cliente não reconheça esse fato e não pagará por esse trabalho. O funcionário que gasta esse tempo não será creditado com horas trabalhadas faturáveis por isso.
- **Complementar** – o custo que é acumulado por essa função/categoria é considerado um custo direto que impulsiona a execução do projeto, e o cliente reconhece esse fato. O funcionário que gasta esse tempo será creditado pelas horas trabalhadas faturáveis. No entanto, esse custo não é cobrado do cliente.
- **Não disponível** – os custos que são incorridos em projetos internos que não exigem acompanhamento de receita são rastreados com essa opção.

## <a name="invoice-schedule"></a>Agenda de faturas

Uma agenda de fatura é quando ocorre uma série de datas ao faturar para um projeto. Se desejar, você pode criar uma agenda de faturas em uma linha de cotação no PSA. Cada linha de cotação pode ter sua própria agenda de faturas. Para criar uma agenda de faturas, é preciso fornecer os seguintes valores de atributo:

- Um data de início de cobrança 
- Uma data de entrega que representa a data de término de cobrança no projeto
- Uma frequência de fatura

O PSA usa esses três valores de atributo para gerar um conjunto temporário de datas nas quais estabelecer o faturamento.

## <a name="invoice-frequency"></a>Frequência da fatura

A frequência de fatura é uma entidade que armazena valores de atributo que ajudam a expressar a frequência da criação da fatura. Os seguintes atributos expressam ou definem a entidade Frequência de fatura:

- **Período** – são aceitos: mensalmente, quinzenalmente e semanalmente. 
- **Execuções por período** – para os períodos semanalmente e quinzenalmente, você pode definir apenas uma execução por período. Para períodos mensais, você pode definir entre uma e quatro execuções por período. 
- **Dias de execução** – os dias em que o faturamento deve ser executado. Você pode configurar esse atributo de duas maneiras:
  - **Dias da semana** – por exemplo, é possível especificar que o faturamento é executado todas as segundas-feiras ou quinzenalmente às segundas-feiras. Os clientes que devem definir o faturamento para execução em dia útil podem preferir esse tipo de configuração. 
  - **Dias de calendário** – por exemplo, você pode especificar que o faturamento é executado no sétimo e 21º dia de cada mês. Algumas organizações podem preferir esse tipo de configuração, pois isso ajuda a garantir que o faturamento seja executado em um cronograma fixo todos os mês.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Agenda de faturas para uma linha de cotação de preço fixo

Para uma linha de cotação de preço fixo, você pode usar a grade **Agenda de Faturas** para criar etapas de cobrança que igualem o valor da linha de cotação.

- Para criar etapas de cobrança que sejam igualmente divididas, selecione uma frequência de fatura, insira a data de início da cobrança na linha de cotação e selecione **Data de Conclusão Solicitada** para a cotação na seção **Resumo** do cabeçalho da cotação. Em seguida, selecione **Gerar Etapas Periódicas** para criar etapas igualmente divididas com base na frequência de fatura selecionada. 
- Para criar uma etapa de cobrança de soma total, crie uma etapa e insira o valor da linha de cotação como o valor da etapa.
- Para criar etapas de cobrança que sejam baseadas em tarefas específicas no plano de projeto, crie uma etapa e mapeie-a para o elemento de agenda do projeto na interface do usuário da etapa de cobrança.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
