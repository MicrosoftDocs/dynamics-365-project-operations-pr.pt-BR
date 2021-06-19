---
title: Considerações sobre a atualização – Microsoft Dynamics 365 Project Service Automation versão 2.x ou 1.x para a versão 3
description: Este tópico fornece informações sobre as considerações que você deve fazer ao fazer upgrade da versão 2.x ou 1.x para a versão 3 do Project Service Automation.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 04ae6aa3ef6a14a6f85dce3eaa5af01e0adce9ba
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014867"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Considerações de atualização - PSA versão 2.x ou 1.x para a versão 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation e Field Service
O Dynamics 365 Project Service Automation e o Dynamics 365 Field Service usam a solução URS (Universal Resourcing Scheduling) para agendamento de recursos. Se você tiver o Project Service Automation e Field Service na sua instância, atualize ambas as soluções para a última versão. Para o Project Service Automation, é a versão 3.x. Para o Field Service, é a versão 8.x. A atualização do Project Service Automation ou Field Service instalará a versão mais recente do URS. Se as soluções do Project Service Automation e Field Service na mesma instância não forem atualizadas para a versão mais recente, pode haver algum comportamento inconsistente.

## <a name="resource-assignments"></a>Atribuições de recursos
No Project Service Automation versão 2 e versão 1, as atribuições de tarefas eram armazenadas como tarefas filho (também chamadas de tarefas de linha) na **entidade Tarefa** e estavam indiretamente relacionadas à entidade **Atribuição de Recurso**. A tarefa de linha ficava visível na janela pop-up de atribuição da WBS (estrutura de detalhamento de trabalho).

![Linha de tarefas na WBS no Project Service Automation versão 2 e versão 1](media/upgrade-line-task-01.png)

Na versão 3 do Project Service Automation, o esquema subjacente de atribuição de recursos reserváveis às tarefas foi alterado. A tarefa de linha foi preterida e há um relacionamento 1:1 direto entre a tarefa na **entidade Tarefa** e o membro da equipe na entidade **Atribuição de Recurso**. As tarefas atribuídas a um membro da equipe do projeto agora são armazenadas diretamente na entidade Atribuição de Recurso.  

Essas alterações causam impacto na atualização dos projetos existentes que possuem atribuições de recursos para recursos reserváveis nomeados e recursos genéricos em uma equipe de projeto. Este tópico descreve as considerações que você deve fazer em relação aos projetos ao atualizar para a versão 3. 

### <a name="tasks-assigned-to-named-resources"></a>Tarefas atribuídas a recursos nomeados
Ao usar a entidade de tarefa subjacente, as tarefas na versão 2 e na versão 1 permitem que os membros da equipe desempenhem uma função diferente de suas funções padrão definidas. Por exemplo, Clara Gomes, que recebeu, por padrão, a função de Gerente de Programa, pode receber a atribuição de uma tarefa com a função de Desenvolvedor. Na versão 3, a função dos membros de uma equipe nomeada é sempre o padrão, de modo que qualquer tarefa que seja atribuída a Gracie George use sua função padrão de Gerente de programa.

Se tiver atribuído a um recurso uma tarefa fora de sua função padrão nas versões 2 e 1, ao atualizar, a função padrão será atribuída ao recurso nomeado para todas as atribuições de tarefas, independentemente da atribuição de função na versão 2. Essa atribuição resulta em diferenças nas estimativas calculadas da versão 2 ou versão 1 em relação à versão 3, pois as estimativas são calculadas com base na função do recurso, e não na atribuição da tarefa de linha. Por exemplo, na versão 2, duas tarefas foram atribuídas a Vitória Cavalcante. A função na tarefa de linha da tarefa 1 era Desenvolvedor e, na tarefa 2, Gerente de Programa. A função padrão de Vitória Cavalcante é Gerente de Programa.

![Várias funções atribuídas a um recurso](media/upgrade-multiple-roles-02.png)

Como as funções de Desenvolvedor e Gerente de Programa são diferentes, as estimativas de custo e vendas são as seguintes:

![Estimativas de custo para as funções do recurso](media/upggrade-cost-estimates-03.png)

![Estimativas de vendas para as funções do recurso](media/upgrade-sales-estimates-04.png)

Ao atualizar para a versão 3, as tarefas de linha são substituídas por atribuições de recursos na tarefa do membro da equipe de recurso reservável. A atribuição usará a função padrão do recurso reservável. Na imagem a seguir, Vitória Cavalcante, que possui a função de Gerente de Programa, é o recurso.

![Atribuições de recursos](media/resource-assignment-v2-05.png)

Como as estimativas baseiam-se na função padrão do recurso, as estimativas de custo e vendas podem ser alteradas. Na imagem a seguir, a função **Desenvolvedor** não é mais exibida, pois a função agora é obtida da função padrão do recurso reservável.

![Estimativas de custo para funções padrão](media/resource-assignment-cost-estimate-06.png)
![Estimativas de vendas para funções padrão](media/resource-assignment-sales-estimate-07.png)

Depois que a atualização for concluída, você poderá editar a função de um membro da equipe como algo diferente do padrão atribuído. Entretanto, se você modificar a função de membros da equipe, ela será alterada em todas as suas tarefas atribuídas, pois não é mais permitido atribuir várias funções aos membros da equipe na versão 3.

![Atualizando uma função de recurso](media/resource-role-assignment-08.png)

Isso também é válido para as tarefas de linha atribuídas a recursos nomeados quando você altera a unidade organizacional do recurso de padrão para outra unidade organizacional. Após a conclusão da atualização da versão 3, a atribuição usará a unidade organizacional padrão do recurso, em vez da unidade definida na tarefa de linha.

### <a name="tasks-assigned-to-generic-resources"></a>Tarefas atribuídas a recursos genéricos
Na versão 2 e na versão 1, você pode definir a função e a unidade organizacional em uma tarefa e, depois, usar o recurso **Gerar equipe** para gerar recursos genéricos com base nos atributos definidos na tarefa. Na versão 3, você cria os membros da equipe genéricos com função e unidade organizacional e, em seguida, atribua os membros da equipe às tarefas.

Na versão 2 e na versão 1, os projetos com recursos genéricos podem estar em dois estados ou em uma combinação de ambos no nível da tarefa. Por exemplo, é possível ter os seguintes cenários:

- Tarefas com funções e unidades organizacionais definidas, mas nenhuma atribuição de recurso afiliado foi gerada.
- Tarefas com recursos de membros da equipe genéricos atribuídos por meio da criação de um recurso genérico usando o recurso **Gerar equipe**.

Antes de iniciar a atualização, é recomendável gerar novamente a equipe para cada projeto que possui tarefas atribuídas a recursos genéricos ou que ainda tem de executar o processo nelas.

Para as tarefas atribuídas a membros da equipe genéricos que foram gerados usando **Gerar equipe**, a atualização irá manter o recurso genérico na equipe e, também, a atribuição a esse membro da equipe genérico. Recomendamos que você gere o requisito de recurso para o membro da equipe genérico após a atualização, mas antes de reservar ou enviar uma solicitação de recurso. Isso preservará todas as atribuições de unidade organizacional dos membros da equipe genéricos que forem diferentes da unidade organizacional de contratação do projeto.

Por exemplo, no Projeto Z, a unidade organizacional de contratação Contoso Estados Unidos. No plano do projeto, as tarefas de teste na fase de implementação receberam a função de Consultor Técnico e a unidade organizacional atribuída é Contoso Índia.

![Atribuição de organização na fase de implementação](media/org-unit-assignment-09.png)

Após a fase de implementação, a tarefa de teste de integração é atribuída à função Consultor Técnico, mas a organização é definida como Contoso Estados Unidos.  

![Atribuição de organização da tarefa de teste de integração](media/org-unit-generate-team-10.png)

Ao gerar uma equipe para o projeto, dois membros da equipe genéricos são criados devido às unidades organizacionais diferentes nas tarefas. O consultor técnico 1 receberá as tarefas da Contoso Índia e o consultor técnico 2 receberá as tarefas da Contoso Estados Unidos.  

![Membros da equipe genéricos gerados](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> No Project Service Automation versões 2 e 1, o membro da equipe não mantém a unidade organizacional, ela é mantida na tarefa de linha.

![Tarefas de linha de versão 2 e da versão 1 no Project Service Automation](media/line-tasks-12.png)

Você pode ver a unidade organizacional no modo de exibição de estimativas. 

![Estimativas da unidade organizacional](media/org-unit-estimates-view-13.png)
 
Quando a atualização é concluída, a unidade organizacional na tarefa de linha que corresponde ao membro da equipe genérico é adicionada a esse membro e a tarefa de linha é removida. Por isso, recomendamos que, antes de atualizar, você gere a equipe em cada projeto que contém recursos genéricos, ou gere-a novamente.

Para as tarefas atribuídas a uma função com uma unidade organizacional diferente daquela do projeto de contratação e sem uma equipe gerada, a atualização criará um membro da equipe genérico para a função, mas usará a unidade de contratação do projeto para a unidade organizacional do membro da equipe. Voltando ao exemplo do Projeto Z, a unidade organizacional de contratação da Contoso Reino Unido e as tarefas de teste do plano do projeto na fase de implementação receberam a função Consultor técnico com a unidade organizacional atribuída à Contoso Índia. A tarefa de teste de integração concluída após a fase de implementação foi atribuída à função Consultor Técnico. A unidade organizacional é a Contoso Estados Unidos e uma equipe não foi gerada. A atualização criará um membro da equipe genérico, um Consultor técnico que possui as horas atribuídas das três tarefas e uma unidade organizacional da unidade da Contoso Estados Unidos, a unidade organizacional de contratação do projeto.   
 
Alteração no padrão de unidades organizacionais de recursos diferentes em membros de equipe não gerados é o motivo pelo qual recomendamos que você gere novamente a equipe em cada projeto que contém recursos genéricos antes da atualização, de modo que as atribuições da unidade organizacional não sejam perdidas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]