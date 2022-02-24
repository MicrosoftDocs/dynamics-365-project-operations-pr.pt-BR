---
title: Propor recursos de projeto
description: Este tópico fornece informações sobre como propor recursos para o projeto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 0a3eaa9929770c91523831d92744d5084aa28cb8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147504"
---
# <a name="propose-project-resources"></a>Propor recursos de projeto

[!include [banner](../includes/psa-now-project-operations.md)]

Os gerentes de recursos podem propor um recurso ao gerente de projetos usando uma solicitação de recurso.

1. Na grade de solicitações ou na própria solicitação, selecione **Localizar Recursos**.
2. Na página **Assistente de Agendamento**, selecione o recurso e, em seguida, no painel **Criar Reserva de Recursos**, no campo **Status da Reserva**, selecione **Reservar**.

    ![Recurso proposto selecionado](media/Resource-Management-image62.png)

As seguintes atualizações de status ocorrem:

- Na página **Assistente de Agendamento**, os indicadores de status são atualizados para indicar que a reserva é proposta, não fixa.

    ![Indicadores de status da reserva proposta na página Assistente de Agendamento](media/Resource-Management-image63.png)

- Na solicitação de recurso, o status é alterado para **Precisa de Revisão**.

    ![Status da solicitação de recurso alterado para Precisa de Revisão](media/Resource-Management-image64.png)

- Na guia **Equipe** do projeto, o valor **Status de Solicitação** do membro genérico da equipe é alterado para **Precisa de Revisão**.

    ![Status de solicitação do membro genérico da equipe alterado para Precisa de Revisão na guia Equipe](media/Resource-Management-image48.png)

O gerente de projetos pode aceitar ou rejeitar a proposta.

Quando os gerentes de recursos processam solicitações de recursos, eles podem usar qualquer uma das seguintes abordagens:

- Propor vários recursos para satisfazer a demanda caso não haja um recurso único disponível para atender às horas necessárias. As horas propostas então serão divididas entre vários recursos que possam satisfazer as horas necessárias. Nesse cenário, não pode haver sobreposição de horas.
- Propor menos recursos do que o necessário. Nesse cenário, a capacidade do recurso proposta é menor do que as horas necessárias especificadas pelo solicitante. Portanto, quando o solicitante aceita os recursos propostos, um requisito de recurso não atendido é criado para capturar a demanda restante.
- Reservar vários recursos para satisfazer a demanda caso não haja um recurso único disponível para concluir o trabalho.
- Reservar menos recursos do que o necessário. Nesse cenário, o número de horas reservadas é inferior ao de horas necessárias. O sistema orienta você a propor recursos em vez de reservas, para que o solicitante possa verificar e acompanhar a demanda restante.

## <a name="billable-utilization"></a>Horas trabalhadas faturáveis

Os recursos podem ter horas trabalhadas faturáveis de destino. Essas horas trabalhadas de destino são definidas como um atributo na função padrão de um recurso ou definidas no registro do recurso reservável individual. Os cálculos de horas trabalhadas se baseiam nas horas reais que os recursos relataram usando entradas de hora aprovadas.

As fórmulas a seguir são usadas para calcular as horas trabalhadas:

- Horas trabalhadas faturáveis = Horas reais passíveis de cobrança ÷ Capacidade do recurso
- Horas trabalhadas não faturáveis = Tempo real com ID do tipo de cobrança = Não passível de cobrança, Complementar ou Não disponível ÷ Capacidade do recurso
- Interno = Tempo real sem contrato de vendas ÷ Capacidade do recurso
- Capacidade do recurso = Horas de trabalho do recurso – Ausência temporária – Dias de folga

Você pode encontrar a exibição **Horas Trabalhadas do Recurso** no painel **Recursos**.

![Exibição Horas Trabalhadas do Recurso](media/Resource-Management-image65.png)

Cada célula na grade representa o percentual de horas trabalhadas faturáveis do recurso em um período, como dia, semana ou mês. As fórmulas a seguir são usadas para colorir as células:

- **Verde:** Horas trabalhadas faturáveis \>= Horas trabalhadas de destino do recurso
- **Amarelo:** Horas trabalhadas de destino – 20 \<= Horas trabalhadas faturáveis \< Horas trabalhadas de destino
- **Vermelho:** Horas trabalhadas faturáveis \< Horas trabalhadas de destino – 20

Como a exibição **Horas Trabalhadas do Recurso** é baseada no Painel de Agendamento, você pode usar as funcionalidades de filtragem dele para filtrar seus resultados.

A grade exige que você defina as horas trabalhadas de destino na função ou no recurso individual. Para definir essa configuração, vá para **Recursos** \> **Funções de recursos**.

Além disso, uma função padrão deve ser atribuída a cada recurso reservável. Vá para **Recursos** \> **Recursos**. Na guia **Project Service**, verifique se a função de um recurso está definida e se o campo **É Padrão** dela está definido como **Sim**. É possível adicionar outras funções onde **É Padrão = Não**. A função em que **É Padrão = Sim** é usada para avaliar as horas trabalhadas do recurso em relação ao destino dessa função.

![Função padrão definida](media/Resource-Management-image67.png)

Na guia **Project Service**, você também pode definir horas trabalhadas de destino individuais para o recurso. O cálculo de horas trabalhadas então usa essas horas trabalhadas de destino para avaliar o destino do recurso em vez do destino da função padrão do recurso.

As horas trabalhadas são mostradas para um recurso somente se ele tiver tempo passível de cobrança e aprovado durante o período exibido na grade.

## <a name="resource-availability"></a>Disponibilidade do recurso

É essencial que os gerentes de recursos possam visualizar a disponibilidade de recursos e atualizar as reservas. Em alguns casos, não há demanda formal (solicitação de recurso), mas um gerente de recursos deve responder a uma demanda não planejada recebida por meio de canais como email, telefonema ou mensagem instantânea. Os gerentes de recursos usam o Painel de Agendamento para atualizar recursos e reservas.

As horas de trabalho do recurso são usadas como base para calcular a disponibilidade de um recurso. As reservas de recursos consomem a capacidade dos recursos.

![Painel de Agendamento](media/Resource-Management-image68.png)

O Painel de Agendamento usa cores e sombreamento para mostrar reservas, disponibilidade e reservas em excesso, além do status das reservas. Uma das configurações do Painel de Agendamento permite mostrar uma legenda.

Se uma seta que aponta para a direita aparecer ao lado de um recurso reservável individual no Painel de Agendamento, o recurso poderá ser expandido para mostrar detalhes do trabalho no qual o recurso está reservado.

![Recurso reservável expandido no Painel de Agendamento](media/Resource-Management-image69.png)

Como o Dynamics 365 Project Service Automation usa o mecanismo Universal Resource Scheduling, se você também tiver o Dynamics 365 Field Service instalado, poderá ver os detalhes das reservas de recursos para projetos, ordens de serviço e qualquer outra entidade à qual você tenha estendido o agendamento.

![Detalhes de reservas de recursos para projetos e ordens de serviço](media/Resource-Management-image70.png)

Para exibir mais detalhes sobre um recurso individual, clique com o botão direito do mouse nele para abrir o cartão de recurso.

![Cartão de recurso](media/Resource-Management-image71.png)
