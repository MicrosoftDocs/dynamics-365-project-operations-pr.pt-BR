---
title: Agendar recursos para um projeto
description: Como agendar recursos de um projeto no Project Service
author: JohnPBurrows
manager: kfend
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
ms.openlocfilehash: 1479bf920be897a6ee3498aada7a6c36692a01fc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132108"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Agendar recursos de um projeto (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Você pode verificar a disponibilidade dos recursos para obter uma visão geral das reservas já feitas ou filtrar a exibição por habilidades, equipe, localização e outras opções.  
  
O painel de agendamento mostra a lista de recursos e sua disponibilidade. Selecione um modo de exibição para exibir disponibilidade por **Horas**, **Dia**, **Semana** ou **Mês**.  
  
Antes de usar o painel de agendamento, é importante configurá-lo. Para obter mais informações, consulte [Configurar o painel de agendamento (Field Service ou Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Se estiver usando uma versão mais antiga, para disponibilidade de recurso, consulte [Exibir a disponibilidade dos recursos](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Para usar a funcionalidade de agendamento de registro de agenda, geocodificação, e serviços de localização, você precisa ligar os mapas.  
> 
> 1. No menu principal, selecione **Agendamento de Recursos** > **Administração**.  
> 2. Clique em **Parâmetros de Agendamento**.  
> 3. Abra o registro e role para baixo até a seção **Resource Scheduling Optimization**.  
> 4. No campo **Conectar aos mapas**, escolha **Sim**.  
> 5. Aceite os termos e salve o registro.  
> 6. No menu principal, selecione **Project Service** > **Painel de agendamento**. Aqui, existem diversas maneiras de agendar manualmente um requisito de reserva. Selecione o método que funciona para você.
  
## <a name="find-available-resources"></a>Localizar recursos disponíveis

1.  Na lista **Requisito de Reserva**, clique com o botão direito do mouse em uma reserva não agendada e escolha uma destas opções:  
  
- Escolha **Encontrar disponibilidade - Recursos atuais** para encontrar um recurso disponível da lista de painel de agendamento.  
- Escolha **Encontrar disponibilidade - Todos recursos**, para encontrar um recurso disponível dos recursos no sistema  
   > [!NOTE]
   >  Depois que você fizer isso, os filtros mostrarão as opções para o requisito de registro selecionado.  
  
2. Quando você vir um slot disponível, clique com o botão direito do mouse no slot de tempo no painel de agendamento e escolha **Reservar Aqui**. Ou, arrastar e soltar o requisito do registro para o slot de tempo disponível.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Registre um recurso usando a exibição diária e encontre quem está agendado
  
1.  No painel de agendamento, selecione **Modo de exibição** e selecione **Dias**.  
  
    Isso mostra uma exibição em grade de quantas horas um recurso é agendado por dia e quais dias eles são livres.  
  
2.  Clique no nome do recurso que você deseja registrar, e selecione **Agendar**.  
  
3.  Na caixa de diálogo **Agendamento de recurso (criar)**, escolha o projeto que você deseja registrar o recurso ao longo com o método de agendamento e horário de início e fim.  
  
4.  Ao concluir, selecione **Reservar**.  
  
## <a name="view-to-the-schedule-board"></a>Exibir no painel de agendamento
  
1.  Selecione o requisito de reserva não agendada da lista na parte inferior.  
  
2.  Arraste a requisição de registro para um recurso/intervalo de tempo disponível no painel de agendamento.  
  
3.  Ao concluir, selecione **Reservar**.  
  
### <a name="additional-resources"></a>Recursos adicionais  
 [Guia do gerente de recursos](../psa/resource-manager-guide.md)
