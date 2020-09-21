---
title: Reconciliar reservas e atribuições
description: Este tópico fornece informações sobre dados efetivos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 614352ba-dbd8-4fa5-8225-d54f9ec0e218
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 27fc7b6abb4c9a7a761059a2f392f13bc0dd14f9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749156"
---
# <a name="reconcile-bookings-and-assignments"></a>Reconciliar reservas e atribuições

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As reservas e atribuições de tarefas de um membro da equipe do projeto são livremente combinadas. Portanto, um recurso pode ter atribuições de tarefas que não correspondem às reservas e vice-versa. O ideal é que as reservas e atribuições do projeto estejam alinhadas, para que os recursos tenham capacidade comprometida para executar suas atribuições de tarefas. No entanto, a realidade é que as reservas podem ocorrer com base em disponibilidade e o tempo das tarefas pode mudar conforme o projeto avança em seu ciclo de vida. Portanto, a combinação livre permite a flexibilidade.

Devido à combinação livre de reservas e atribuições de tarefas do projeto, uma guia **Reconciliação** está incluída na entidade Projeto. Essa guia ajuda os gerentes de projeto a reconciliar as reservas dos membros da equipe e suas atribuições para a equipe do projeto.

Para cada membro da equipe nomeado, a guia **Reconciliação** mostra reservas e atribuições até a atribuição de tarefas individual. Ela mostra horas em células que podem representar períodos, desde meses até dias.

No campo **Escala de tempo**, você pode selecionar **Mês**, **Semana** ou **Dia**. Por padrão, a opção **Semana** é selecionada. No entanto, você pode alterar o valor padrão selecionando o botão **Configurações**. Quando a guia **Reconciliação** é aberta, ela mostra a data atual, mas é possível usar o controle de calendário para avançar ou retroceder no tempo. Quando um projeto tem uma data de início que está no futuro, a guia mostra essa data ao ser aberta. O controle de calendário também possui opções que permitem navegar até as datas de início e término do projeto.

Você pode usar os controles de expansão em cada recurso para mostrar os detalhes das reservas desse recurso. Também é possível expandir as atribuições de cada recurso até o nível da tarefa individual.

A parte inferior da guia **Reconciliação** mostra um total líquido geral para o projeto e a guia também inclui uma coluna de total. Para cada recurso, a guia calcula a diferença entre as reservas de um membro da equipe no projeto e o valor acumulado das atribuições de tarefas desse membro da equipe. O ideal é que a diferença seja 0 (zero). Em outras palavras, não deve haver nenhuma diferença entre as reservas e as atribuições de tarefas do recurso. As diferenças são indicadas por cores e sombreamento para chamar duas condições:

- **Falta de reserva** – ocorre quando um recurso tem mais atribuições do que reservas. Como essa capacidade não foi reservada, um gerente de projetos pode corrigir essa condição estendendo as reservas do recurso para cobrir a falta.
- **Reservas em excesso** – ocorrem quando um recurso é reservado para o projeto, mas não é atribuído a tarefas. Essa condição pode ser aceitável se, por exemplo, o recurso tiver sido reservado antes da atribuição de tarefas. No entanto, em outros casos, a atribuição do recurso pode não ter sido planejada. Nesses casos, o gerente de projetos deve considerar o cancelamento das reservas do recurso, para que a capacidade possa ser usada em outro projeto.

> [!NOTE]
> A legenda dessas condições pode estar oculta para deixar mais espaço para a grade. Nesse caso, é possível torná-la visível selecionando o botão **Configurações**.

Em alguns casos, quando o campo **Escala de tempo** é definido como um nível superior ao **Dia**, as diferenças podem ser calculadas como 0 (zero). Por exemplo, no nível **Mês**, a diferença líquida para um recurso pode ser 0 (zero) para indicar que as reservas são iguais às atribuições. No entanto, se você analisar o nível **Semana**, poderá ver que há atribuições de 0 (zero) horas e reservas de 40 horas na primeira semana do mês e atribuições de 40 horas e reservas de 0 (zero) horas na segunda semana desse mês. Embora o total de reservas e atribuições do mês seja igual, ele difere por semana.

Ao exibir níveis de tempo superiores, a guia **Reconciliação** mostra um indicador de células para notificá-lo sobre a existência de diferenças em níveis de tempo inferiores. Por exemplo, na ilustração a seguir, um indicador de células é exibido na célula do mês de Outubro de 2018 do recurso denominado Maria Eduarda Martins. Portanto, você pode ver que, embora as reservas e atribuições do recurso sejam iguais quando agregadas no nível **Mês**, elas não são correspondentes em níveis inferiores.

![Reservas e atribuições não correspondentes](media/reconcile-assignments-01.JPG)

Clique duas vezes em uma célula para ampliar o próximo nível inferior e visualizar a diferença. Por exemplo, se você clicar duas vezes na diferença Outubro de 2018 para Maria Eduarda Martins, será feita uma busca detalhada até o nível **Semana**. Você verá que o recurso tem reservas de 16 horas, mas nenhuma atribuição nas duas primeiras semanas de outubro e 16 horas de atribuições, mas nenhuma reserva na terceira semana desse mesmo mês.

![Reservas e atribuições não correspondentes](media/reconcile-assignments-02.JPG)

Você pode clicar com o botão direito do mouse em uma célula para reduzir o próximo nível superior. Também é possível desativar o indicador de células selecionando o botão **Configurações** . 

Além disso, você pode usar os botões **Voltar** e **Avançar** acima da grade para navegar entre quaisquer diferenças no seu projeto. Para usar esses botões, primeiro selecione um recurso. Selecione **Avançar** para navegar até a próxima diferença entre reservas e atribuições desse recurso. Selecione **Voltar** para ir até a diferença anterior.

Em situações nas quais você tem atribuições de tarefas para um recurso, mas nenhuma reserva, é possível selecionar a falta de reserva e, em seguida, selecionar **Estender Reserva**. Você poderá ver a reserva necessária para abordar a falta do recurso. Também poderá visualizar as reservas do recurso no projeto atual e em outros projetos. Selecione **OK** para criar a reserva para o recurso desconsiderando a disponibilidade atual. Em seguida, o gerente de projetos ou o gerente de recursos poderá usar o Painel de Agendamento para gerenciar situações em que um recurso é reservado em excesso além da capacidade porque suas reservas foram estendidas.

## <a name="managing-with-time-zones"></a>Gerenciando com fusos horários
Para garantir resultados precisos e previsíveis ao usar o recurso Estender Reserva, há dois pré-requisitos principais que devem ser atendidos:  

- O usuário deve configurar o fuso horário do dispositivo para corresponder ao fuso horário definido nas Configurações de Personalização do sistema.
 
  ![Configurações de fuso horário no Windows 10](media/reconcile-assignments-03.png)

  ![Configurações de fuso horário nas configurações de personalização](media/reconcile-assignments-04.png)
 
- O Recurso Reservável deve ter pelo menos um minuto de tempo de trabalho que se sobreponha aos contornos usados para definir a extensão solicitada. Por exemplo, o exemplo a seguir mostra recursos de revisão com horário de trabalho que variam entre 9:00 e 19:00. 

  ![Comparação de contornos de recursos](media/reconcile-assignments-05.png)

As listas de tabela a seguir mostra:

- Um modelo de calendário de projeto.
- Recurso A: este recurso tem o mesmo calendário e está no mesmo fuso horário do projeto. O horário de início das reservas será 9:00.
- Recursos B: este recurso está localizado em um fuso horário diferente do projeto e, portanto, inicia o trabalho às 7:00 no fuso horário. No entanto, as reservas começarão às 9h, já que é o horário de início mais cedo do contorno da tarefa.
- Recursos C e D: os recursos também estão localizados em fusos horários diferentes, diferentes entre si e o projeto, e suas reservas começam não antes dos respectivos horários de início disponíveis.

|Entidade  |Calendário  |
|-|-|
|Modelo de calendário de projeto   | ![calendário de projeto](media/reconcile-assignments-06.png) |
|Recurso A  | ![Calendário do Recurso A](media/reconcile-assignments-06.png) |
|Recurso B  |  ![Calendário do Recurso B](media/reconcile-assignments-07.png) |
|Recurso C  |  ![Calendário do Recurso C](media/reconcile-assignments-08.png) |
|Recurso D  | ![Calendário do Recurso D](media/reconcile-assignments-09.png)  |
 
Quando você navega para a visão de reconciliação, as atribuições de recursos e as faltas de reservas associadas serão exibidas.
 ![Exibição de reconciliação antes da extensão](media/reconcile-assignments-10.png)

Depois que a funcionalidade Estender Reserva for executada em cada recurso, as reservas serão estendidas com êxito para cada recurso. Isso ocorre porque as horas de trabalho de cada recurso se sobrepõem aos contornos da falta.
 ![Exibição de reconciliação após a extensão da reserva](media/reconcile-assignments-11.png) 

No entanto, uma análise mais apurada dos detalhes das reservas mostra diferenças no horário de início das reservas. As reservas começarão não antes da hora de início do contorno da atribuição e não antes da hora de início disponível do recurso.
 ![Novas reservas de recursos no quadro de horários](media/reconcile-assignments-12.png)
