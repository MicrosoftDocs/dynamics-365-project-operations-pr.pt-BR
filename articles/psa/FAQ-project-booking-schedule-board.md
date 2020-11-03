---
title: Criar uma reserva de projeto no Quadro de Agendamento
description: Este tópico fornece informações sobre como criar uma reserva de projeto no quadro de agendamento.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 57fbc71681015fca73cdda4bc7d392f6be4289f3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071445"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Criar uma reserva de projeto no Quadro de Agendamento

É possível reservar um recurso em um projeto diretamente na guia **Equipe** do projeto ou gerando um requisito de recurso em uma atribuição de membro da equipe genérico e, em seguida, atendendo ao requisito com um membro da equipe de projeto.

Você também pode reservar um recurso em um projeto diretamente no Quadro de Agendamento. Isso pode ser feito de três maneiras:

- **Fazer uma reserva em um requisito de recurso gerado:** você pode gerar um requisito de recurso depois de criar um recurso genérico e atribuir tarefas em um projeto.

- **Fazer reserva no requisito principal:** os requisitos principais são mostrados no Quadro de agendamento da guia **Projeto**. 

- **Fazer reserva em um novo requisito de recurso:** você pode criar um requisito de recurso do zero e associá-lo a um projeto. No Quadro de Agendamento, o requisito de recurso é exibido na guia **Requisitos em Aberto**.

## <a name="book-from-a-generated-resource-requirement"></a>Fazer uma reserva em um requisito de recurso gerado

É possível criar um recurso genérico e atribuí-lo a uma ou várias tarefas em um projeto. Em seguida, você pode gerar um requisito de recurso de um membro da equipe genérico. 

1.  No Quadro de Agendamento, esse recurso será exibido na guia **Requisitos em Aberto** . Talvez seja necessário usar filtros de coluna na grade se você tiver muitos requisitos em aberto. 

    ![Guia Abrir Requisitos no painel Agendar](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura de tela da tabela de reservas e atribuições")

2. Selecione o requisito. A guia **Localizar Disponibilidade** aparecerá na parte superior da linha selecionada.
 
3. Quando você seleciona a guia, o modo Assistente de Agendamento do Quadro de Agendamento é aberto e filtra os recursos disponíveis que atendem ao requisito de recurso. Depois disso, você pode reservar um recurso.

4. Você também pode arrastar e soltar a linha selecionada da parte inferior do Quadro de Agendamento até uma célula do recurso na grade acima. Quando você soltá-lo, o painel **Criar reserva de recursos** abrirá à direita.

    A seleção de **Reservar** reserva o recurso na equipe de projeto.

![Painel Criar Reserva de Recursos](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Fazer reserva no Requisito principal

A criação de um projeto no Project Service cria automaticamente um requisito de recurso chamado Requisito principal. Esse é um requisito vazio usado para reservar rapidamente um recurso com o Quadro de Agendamento sem precisar gerar um requisito nem criar um do zero. Como o requisito está vazio, será necessário especificar as datas, bem como o método e as horas de alocação, se aplicáveis. 

1. Para reservar um recurso com o Requisito Principal, no Quadro de Agendamento, selecione a guia **Projeto**. Talvez seja necessário usar o filtro de coluna na coluna **Projeto** se você tiver muitos projetos.

   ![Filtros de coluna no painel Agendar](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura de tela da tabela de reservas e atribuições")

2. Selecione o requisito que tem somente o nome do projeto como seu nome e uma duração de zero (0).

3. Selecione a guia **Localizar disponibilidade** que é exibida na linha. Isso coloca o Quadro de Agendamento no modo Assistente de Agendamento e mostra os recursos disponíveis que podem ser reservados no projeto.

4. Como um **Requisito Principal** é um requisito vazio com zero (0) de duração, será necessário definir a duração no painel **Criar Reserva de Recursos** ao selecionar e reservar um recurso.

5. Você também pode selecionar o **Requisito principal do projeto** na parte inferior do Quadro de Agendamento e arrastá-lo e soltá-lo em um recurso para reservá-lo.
 
    Como o **Requisito Principal** é um requisito vazio que tem duração zero (0), será necessário definir a duração no painel **Criar Reserva de Recursos** ao selecionar e reservar um recurso.
 
    Ao reservar um recurso por meio do **Requisito Principal** no Quadro de Agendamento, você o adiciona à equipe do projeto sem nenhuma atribuição.
 
## <a name="book-from-a-new-resource-requirement"></a>Fazer reserva em um novo requisito de recurso
Complete as etapas a seguir para fazer uma reserva de um novo requisito de recurso. 

1. Vá para **Requisitos de Recurso** e selecione **Novo** para criar um novo requisito de recurso.

2. Na guia **Projeto** , selecione um projeto para associar o requisito ao projeto.
 
    No Quadro de Agendamento, esse novo requisito é mostrado como um **Requisito em Aberto** que você pode atender.

3. Reserve o recurso para adicioná-lo à equipe do projeto.

4. Agora que o recurso está reservado, é preciso atribuir tarefas manualmente.

