---
title: Determinar as estimativas de custo e receita do projeto
description: Como determinar estimativas de custo e receita de projeto no Project Service
author: ruhercul
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a91e988632d2b2cdebfe7fd17516c5d6886728fc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148809"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Determinar as estimativas de custo e receita do projeto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

As estimativas de projeto fornecem uma visão financeira do trabalho estimado e agendado na estrutura de detalhamento de trabalho do projeto. A exibição de estimativas informa você quanto ao impacto do custo e da receita do trabalho planejado. A exibição de estimativas fornece uma ferramenta para ver as informações em várias dimensões predefinidas para melhor informar sobre impacto financeiro do projeto.  
  
## <a name="cost-and-sales-value-of-the-project"></a>O valor de custo e venda do projeto  
As listas de preços de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] definem o custo e as taxas de cobrança por uso de projetos de funções. Com base nas funções associadas às tarefas na estrutura de detalhamento de trabalho do projeto, você pode determinar o impacto do custo e da receita do trabalho envolvido.  
  
## <a name="cost-price-defaulting"></a>Padronização de preço de custo  
Cada projeto pertence à uma organização (indicada em **Unidade Proprietária** no projeto). A lista de preços associada à unidade organizacional proprietária determina o preço unitário de custo. Os [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determinam os preços de custo de funções pesquisando a combinação de função, unidade e unidade organizacional na lista de preços de custo para obter o preço de custo correto para a data efetiva nas linhas de estimativa.  
  
Se a combinação de função, unidade e unidade organizacional não resultar em um preço de custo da lista de preços da unidade proprietária, a unidade será desconsiderada em favor da combinação de função e unidade organizacional. Se houver um preço de custo, o preço será convertido para a unidade escolhida na linha de estimativa.  
  
Se a combinação de função e unidade organizacional não resultar em um preço de custo, a unidade organizacional será desconsiderada em favor da combinação de função e unidade, e o preço assumirá o valor padrão depois de aplicar qualquer conversão se necessário.  
  
 Se não houver um preço para a função, o preço de custo assume como padrão 0,00 na linha de estimativa.  
  
 Todas as quantidades de custo nas linhas de estimativa de custo de projeto estão na moeda da unidade organizacional proprietária.  
  
## <a name="sales-price-defaulting"></a>Padronização de preço de venda  
A lista de preços de venda se baseia na entidade de vendas à qual projeto está associado. A lista de preços de venda associada à cotação ou ao contrato determina o preço unitário de venda. Se a cotação ou o contrato tiverem uma lista de preços personalizada, ela será a lista de preços de venda padrão para as estimativas do projeto. Se não houver nenhuma associação com as entidades de vendas, a lista de preços de venda padrão, configurada em definições de parâmetros, será a lista de preços de venda padrão para o projeto. Cada linha de estimativa tem uma unidade organizacional do recurso associada para indicar a unidade organizacional a partir da qual os recursos serão agendados para a realização da tarefa. O preço de venda das funções associadas é determinado procurando a combinação de função, unidade e unidade organizacional do recurso na lista de preços de venda para obter o preço de venda correto para a data efetiva nas linhas de estimativa.  
  
Se a combinação de função, unidade e unidade organizacional do recurso não resultar em um preço de venda da lista de preços de venda, o sistema desconsiderará a unidade e procurará a combinação de função e unidade organizacional do recurso. Se for localizado um preço de venda, ele será convertido na unidade que você escolher na linha de estimativa de vendas.  
  
Se o sistema não localizar um preço para a função, o preço de venda deve assumir o valor padrão 0,00 na linha de estimativa.  
  
A exibição de estimativas tem uma visualização de grade que exibe uma grade plana de linhas de estimativa com custo unitário e total e preço de venda.  
  
## <a name="time-phased-view-of-project-estimates"></a>Exibição de estimativas de projeto em fases de tempo  
Na exibição das estimativas do projeto em fases de tempo, os dados das estimativas na exibição de grade são por padrão dinamizados por função e mostram a extensão dos dados da estimativa em uma linha do tempo na escala de tempo escolhida.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Alocação de estimativa de esforço com base no modo de tarefa  
Na exibição em fases de tempo, o esforço total estimado para a tarefa é distribuído alocando-se um determinado número de horas de esforço por período de tempo unitário da escala de tempo escolhida. Em Project Service, o modo de tarefa determina como o esforço é alocado durante a tarefa. Os dois tipos de alocação são alocação uniforme e horas de trabalho baseadas em alocação. 
  
## <a name="work-hours-based-allocation"></a>Alocação baseada em horas de trabalho  
O modo de agendamento automático de uma tarefa determina que o número de recursos estimados para a tarefa seja estimado para ser utilizado durante todas as horas de trabalho de um dia. Isso também se aplica quando você aloca o esforço dividindo-o entre a duração das tarefas na exibição em fases de tempo também. Por exemplo, em uma escala de tempo ‘Dia’ de uma tarefa estimada para ser concluída por um recurso, o esforço alocado por dia não excederá as horas de trabalho por dia definidas no calendário do projeto. Portanto, a alocação de esforços sempre garante que os recursos sejam estimados para serem utilizados o dia inteiro.  
  
## <a name="even-distribution"></a>Distribuição uniforme  
O modo de agendamento manual de tarefa não contempla as horas de trabalho, o calendário do projeto ou o número de recursos definidos na tarefa. O agendamento da tarefa é baseado na entrada do usuário. Para essas tarefas, a alocação de esforços por período de tempo unitário da escala de tempo escolhida não têm nenhum fator de limitação. O esforço total da tarefa é dividido igualmente e alocado a cada período de tempo unitário na escala de tempo escolhida.  
  
Dessa forma, o modo de tarefa definido na tarefa determina a distribuição de esforços ou a alocação de esforços por período de tempo unitário em estimativas em fases de tempo.  
  
## <a name="grouping-and-time-phasing-options"></a>Opções de agrupamento e divisão em fases de tempo  
Essa exibição ajuda você a entender a distribuição do esforço, do custo e das estimativas de vendas em uma base diária, semanal, mensal ou anual. A opção Agrupar por permite articular dados de estimativas em duas outras dimensões: categoria e recurso. Tanto na exibição de grade quando na exibição em fases de tempo, é possível escolher os campos a serem exibidos. Os totais de cada um dos blocos de tempo são exibidos na parte inferior, indicando o total estimado para o esforço, o custo e as vendas do dia, da semana ou do ano.  
  
O preço de custo e de vendas padrão baseia-se em data. Quando as taxas das funções mudam, isso torna mais transparente na exibição dividida em fases temporárias, ao exibir dados estimados dinamizados em ‘Recurso’ e divididos em fases por semana.  
  
## <a name="expense-estimates"></a>Estimativas de despesas  
Qualquer despesa incorrida no projeto, que não esteja diretamente relacionada ao trabalho a ser gasto, pode ser registrada nas estimativas do projeto na exibição de grade. O uso da opção **Adicionar estimativa de despesa** na exibição de grade pode realizar isso. As estimativas de despesa podem ser registradas para uma tarefa específica ou para o projeto inteiro. Você pode escolher as categorias de despesas nessas linhas e escolher uma data provisória em que a despesa deverá ocorrer. Se o custo e a lista de preços de venda associados têm porcentagens de markup ou preços padrão definidos para as categorias de despesas, eles assumirão o valor padrão na linha de estimativa na associação.  
  
### <a name="see-also"></a>Consulte também  
 [Guia do gerente de projeto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]