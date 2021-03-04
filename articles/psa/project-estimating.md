---
title: Custos e receita de projetos
description: Este tópico fornece informações sobre como estimar custos e receita de projeto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 279c1119d334a7f60906e33b3fc7ca22ff9a360d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148314"
---
# <a name="project-costs-and-revenue"></a>Custos e receita de projetos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As estimativas de projeto fornecem a visão financeira do trabalho estimado e programado na agenda do projeto. A guia **Estimativas** na página **Projetos** mostra o impacto de custo e receita do trabalho que você está planejando. Ela também fornece informações sobre muitas dimensões predefinidas. 

> ![Guia Estimativas](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Os valores de custo e vendas do projeto

As listas de preços definem o custo e as taxas de cobrança para funções em um projeto. É possível determinar o impacto de custo e receita do trabalho com base nas funções associadas ao nome da posição e ao recurso nomeado que é atribuído a uma tarefa. Se houver tarefas que não tenham atribuições (genéricas ou nomeadas), não será possível obter as estimativas de custo ou vendas. Os valores de custo e vendas consideram a data que é definida nas listas de preços.

### <a name="default-cost-price"></a>Preço de custo padrão  

Cada projeto pertence a uma organização. Essa organização é mostrada no campo **Unidade de Contratação** do projeto. A lista de preços associada à unidade de contratação é usada para determinar o preço de custo da unidade. Para determinar os preços de custo corretos em funções para a data definida nas linhas de estimativa, procure a combinação de função, unidade e unidade organizacional na lista de preços de custo. 

Para que seus preços de custo possam ser calculados, todas as tarefas devem ser atribuídas a um recurso. Todas as tarefas não atribuídas terão um preço de custo de 0,00.

Se a combinação de função, unidade e unidade organizacional não retornar um preço de custo da lista de preços da unidade de contratação, o sistema vai ignorar a unidade. Em vez disso, ele vai procurar a combinação apenas de função e unidade organizacional. Se um preço de custo for encontrado, os fatores de conversão serão usados para convertê-lo na unidade que você selecionou na linha de estimativa.

Se a combinação de função e unidade organizacional não retornar um preço de custo, o sistema vai ignorar a unidade organizacional. Em vez disso, ele vai procurar a combinação de função e unidade para definir o preço padrão (após a aplicação de qualquer conversão).

Se o sistema não encontrar um preço para a função, o preço de custo na linha de estimativa será definido para um valor padrão de **0,00**. Todos os valores de custo nas linhas de estimativa de custo do projeto são registrados na moeda da unidade de contratação.

> [!NOTE]
> Por padrão, o Microsoft Dynamics 365 armazena valores de custo em sua moeda base. Entretanto, os valores de custo que são mostrados na guia **Estimativas** estão na moeda da unidade de contratação.  

### <a name="default-sales-price"></a>Preço de vendas padrão 

A lista de preços de vendas é determinada pela entidade de vendas à qual o projeto está anexado ou pelo cliente do projeto. Quando uma entidade de vendas, como oportunidade, cotação ou contrato, é associada ao projeto, o preço de vendas da entidade de vendas é determinado pela lista de preços associada à cotação ou ao contrato. Se a cotação ou o contrato tiver uma lista de preços personalizada, essa lista de preços será usada como a lista de preços de vendas padrão para as estimativas do projeto. Se não houver associação às entidades de vendas, a lista de preços de vendas padrão dos parâmetros será usada como a lista de preços de vendas padrão do projeto correspondida pela moeda do cliente que é definida no projeto.

Cada linha de estimativa tem uma unidade de recursos associada a ela. A unidade de recursos indica a unidade organizacional da qual os recursos são reservados para concluir a tarefa. A fim de determinar o preço de vendas para as funções associadas, procure a combinação de função, unidade e unidade de recursos na lista de preços de vendas. Se não houver atribuições na tarefa, o preço de vendas para a tarefa será 0,00.

Se a combinação de função, unidade e unidade de recursos não retornar um preço de vendas da lista de preços da venda, o sistema vai ignorar a unidade. Em vez disso, ele vai procurar a combinação apenas de função e unidade de recursos. Se um preço de vendas for encontrado, os fatores de conversão serão usados para convertê-lo na unidade que você selecionou na linha de estimativa de vendas. 

Se a combinação de função e unidade de recursos não retornar um preço de vendas da lista de preços da venda, o sistema vai ignorar a unidade de recursos. Em vez disso, ele vai procurar a combinação de função e unidade para definir o preço padrão (após a aplicação de qualquer conversão).

Se o sistema não encontrar um preço para a função, o preço de vendas na linha de estimativa será definido para um valor padrão de **0,00**.

A guia **Estimativas** tem uma exibição de grade que mostra as linhas de estimativa. A grande inclui colunas para a unidade, o preço de custo total e o preço de vendas total, conforme mostrado na ilustração a seguir. 

> ![Exibição de grade na guia Estimativas](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Exibição de estimativas de projeto em fases de tempo

A visão em fases de tempo das estimativas do projeto mostra os dados de estimativa da exibição de grade na linha do tempo, em uma escala de tempo selecionada por você. Por padrão, os dados da estimativa são dinamizados na dimensão **Função**.

> ![Exibição em fases de tempo das estimativas do projeto](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Alocando esforço estimado com base no modo de tarefa

Na exibição em fases de tempo, você distribui o esforço total estimado para a tarefa alocando as horas de esforço por período de tempo unitário na escala de tempo selecionada. O modo de tarefa determina como o esforço é alocado durante a tarefa. Os dois tipos de alocação são **Uniforme** e **Baseada em horas de trabalho**.

### <a name="work-hours-based-allocation"></a>Alocação baseada em horas de trabalho
 
No modo de tarefa de agendamento automático, as horas diárias padrão para recursos da tarefa são definidas na taxa completa de hora de trabalho. Esse comportamento se aplica quando o esforço é alocado dividindo-o pela duração da tarefa na exibição em fases de tempo. Por exemplo, se a sua estimativa é de que uma tarefa seja concluída por um recurso na escala de tempo **Dia**, o esforço que é alocado por dia não excederá as horas de trabalho por dia definidas no calendário do projeto. Portanto, a alocação de esforços sempre garante que os recursos sejam estimados para serem usados o dia inteiro.

### <a name="even-allocation"></a>Alocação uniforme

No modo de tarefa agendada manualmente, as horas de trabalho no calendário do projeto não são usadas. Em vez disso, o agendamento da tarefa se baseia na entrada do usuário. Para essas tarefas, a alocação de esforço por período de tempo unitário na escala de tempo selecionada não têm qualquer fator de limitação. O esforço total da tarefa é dividido igualmente e alocado a cada período de tempo unitário na escala de tempo selecionada. Portanto, o modo de tarefa definido na tarefa determina a distribuição de esforço ou a alocação de esforço por período de tempo unitário em estimativas em fases de tempo.

## <a name="grouping-and-time-phasing-options"></a>Opções de agrupamento e divisão em fases de tempo

A exibição em fases de tempo mostra a distribuição das estimativas de vendas, custo e esforço diária, semanal, mensal ou anualmente. Por padrão, os dados da estimativa são dinamizados na dimensão **Função**. No entanto, você pode usar a opção **Agrupar por** para dinamizar em duas outras dimensões: **Categoria** e **Recurso**.

Em ambas, na exibição de grade e na exibição em fases de tempo, você pode selecionar quais campos serão mostrados. Os totais para cada bloco de tempo são mostrados na parte inferior do projeto. Eles mostram o total estimado de esforço, custo e vendas para dia, semana, mês ou ano. O preço de custo padrão e preço de vendas se baseia em data. Em outras palavras, eles mudam para cada recurso, com base na exibição em fases de tempo que você seleciona.

## <a name="expense-estimates"></a>Estimativas de despesas

O botão **Adicionar uma Nova Estimativa de Despesa** na exibição de grade permite registrar as despesas que são incorridas no projeto, mas que não se relacionam diretamente à mão de obra. Você pode registrar as estimativas de despesa para uma tarefa específica ou para o projeto inteiro. Selecione as categorias de despesa e a data provisória quando você espera incorrer em despesa. Se a lista de preços de custo e a lista de preços de vendas associadas tiverem preços padrão (ou se as porcentagens de markup forem definidas para categorias de despesa), eles serão inseridos automaticamente na linha de estimativa quando ocorrer a associação.


[!INCLUDE[footer-include](../includes/footer-banner.md)]