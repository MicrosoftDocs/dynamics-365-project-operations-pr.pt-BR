---
title: Estimar vendas e custos do projeto quando um recurso reservável preencher várias funções para um projeto
description: Este artigo fornece informações sobre como usar dimensões de preços para dar suporte a preços e custos para um recurso que preenche várias funções em um projeto.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5adaa7b83aae69c15aa268e723417172f1b56f42
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916136"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Estimar vendas e custos do projeto quando um recurso reservável preencher várias funções para um projeto 

[!include [banner](../includes/psa-now-project-operations.md)]

As empresas que têm como base projetos frequentemente precisam de um recurso para realizar várias funções em um projeto. Cada uma dessas funções pode ter um preço e um custo diferentes, o que significa que a hora do mesmo recurso no projeto pode ter uma estimativa financeira diferente, dependendo da cobrança e das taxas de custo de cada uma das funções. O Project Service Automation permite a configuração dos valores no registro do membro da equipe para o recurso nomeado e permite diferentes substituições em cada uma das tarefas às quais o membro da equipe está atribuído.

O exemplo a seguir explica como a substituição simples desse valor permite que um recurso tenha várias funções em um projeto com diferentes custos e taxas de cobrança.

## <a name="create-tasks"></a>Criar tarefas
Crie duas tarefas de projeto de 40 horas cada, Tarefa A e Tarefa B. Selecione a Tarefa A como predecessora da Tarefa B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurar a Função e a Unidade Organizacional para um membro genérico da equipe do projeto

1. Na página **Agenda**, selecione a linha **Tarefa** para a Tarefa A. 
2. No campo **Recursos**, selecione **Criar** na lista suspensa.
3. Na página **Criação Rápida de Membro de Equipe**, especifique os atributos do membro genérico da equipe que poderá executar essa tarefa.
4. Selecione a função e a unidade organizacional apropriadas e, em seguida, selecione **Salvar e Fechar**. Um membro genérico da equipe é criado e atribuído à tarefa. 

Repita estas etapas para a Tarefa B e certifique-se de que a função e a unidade organizacional no membro genérico da equipe criado para a Tarefa B sejam diferentes da Tarefa A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Configurar a função e a unidade organizacional para uma tarefa de projeto

1. Depois de criar a Tarefa A, selecione a tarefa e, em seguida, selecione **Editar tarefa**.
2. Na página **Detalhes da Tarefa**, localize os campos **Função** e **Unidade Organizacional**, adicione os valores exigidos de um recurso que executaria esta tarefa. 

  > [!NOTE]
  > Se você estiver concluindo estes cenários usando dados de demonstração do Project Service Automation, selecione **Líder de Consultoria** como a função e **Fabrikam US** como a unidade organizacional.

3. Selecione a Tarefa B e, em seguida, **Editar tarefa**.
4. Na página **Detalhes da Tarefa**, localize os campos **Função** e **Unidade Organizacional**, adicione os valores exigidos de um recurso que executaria esta tarefa. Certifique-se de que os valores nos campos **Função** e **Unidade organizacional** sejam diferentes entre a Tarefa B e a Tarefa A. 

  > [!NOTE]
  > Se você estiver concluindo estes cenários usando dados de demonstração do Project Service Automation, selecione **Técnico de Rede** como a função e **Fabrikam US** como a unidade organizacional.

5. Salve e feche a página **Detalhes da Tarefa**. 

## <a name="team-member-and-estimates-behavior"></a>Membro da equipe e comportamento de estimativas 

1. Na página **Detalhes da Tarefa**, em **Membro da Equipe**, selecione os dois Membros genéricos da equipe e, em seguida, selecione **Gerar Requisitos**. 
2. Selecione a linha do membro da equipe de **Líder de Consultoria** e então selecione **Reservar**. O quadro de horários é aberto e reserva um recurso para esse requisito.
3. Selecione a linha do membro da equipe de **Técnico de Rede** e então selecione **Reservar**. O quadro de horários é aberto e reserva o mesmo recurso nesse requisito.

### <a name="team-member-grid"></a>Grade Membro da Equipe 
Na grade **Membro da Equipe**, observe que os dois registros genéricos do membro da equipe foram excluídos e um recurso foi substituído. Há um conjunto de valores para esse recurso que mostra um conjunto padrão de valores para **Função** e **Unidade Organizacional**.
Ao expandir a linha desse registro Membro da Equipe, você poderá ver atribuições distintas no registro do membro da equipe para ambas as tarefas. Cada linha de atribuição tem valores específicos de tarefa para **Função** e **Unidade Organizacional**. 

### <a name="estimates-grid"></a>Grade Estimativas 
Quando navegar para a grade **Estimativas**, você notará que ambas as atribuições para o mesmo recurso têm preços diferentes.
O preço da atribuição para o recurso na Tarefa A foi estimado usando o valor do atributo **Função** de **Líder de Consultoria**. O preço da atribuição para o mesmo recurso na Tarefa B foi estimado usando o valor do atributo **Função** de **Técnico de Rede**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
