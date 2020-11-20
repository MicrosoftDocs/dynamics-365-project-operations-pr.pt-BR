---
title: Gerenciar projetos e reservas no seu calendário do Office 365
description: Como gerenciar projetos e reservas no seu calendário do Office 365
author: ruhercul
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
- D365PS
- ProjectOperations
ms.openlocfilehash: 31ff541f5b817c29b162c38c282df8cfd866e375
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129034"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Gerenciar projetos e reservas em seu calendário (Project Service)

> [!Note]
> PRETERIDO: esse recurso foi preterido e não está mais disponível.

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Exibir compromissos pessoais, reservas de trabalho de projeto, e atribuições de ordem de serviço do Field Service usando o calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Com tudo em um local, é fácil gerenciar seu dia. Suas reuniões, compromissos, reservas e tarefas estão disponíveis em seu calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Se você estiver usando [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], você também pode inserir seus compromissos pessoais na visualização de entrada de tempo do Project Service. Isso permite que os gerentes de projeto saibam sua disponibilidade para projetos. Isso também poupa tempo, porque não precisa inserir informações sobre seus compromissos pessoais duas vezes. Você pode simplesmente importar seus compromissos do calendário e projetar exibição para a entrada de tempo do Project Service.  
  
 Seu calendário sincronizará os registros de pedido de trabalho e projeto nas próximas quatro semanas. Essa configuração não pode ser alterada.  
  
 A sincronização funciona somente de uma forma, do PSA para o calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Você pode sincronizar na ordem inversa. 
  
 Para saber como usar seu calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] , consulte [Calendário no Outlook na Web para negócios](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Configuração  
 Antes de poder ver e gerenciar as reservas em seu calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], será necessário configurar algumas coisas.  
  
- Você precisará ter as credenciais de Administrador Global ou Administrador do Sistema do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
- O Admin precisará configurar o perfil do servidor de email, e cada usuário precisará configurar sua caixa de e-mail. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configurar o processamento de email por meio da sincronização no servidor](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Ativar a sincronização para sua organização do (tarefa de administrador)  
  
1.  No menu principal, clique em **Configurações** > **Administração**.  
  
2.  Clique em **Configurações do Sistema**.  
  
3.  Clique na guia **Sincronização**.  
  
4.  Em **Selecionar habilitar sincronização do registro de recurso com**, marque **Sincronizar registro de recurso com Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Ative a sincronização para seu perfil de usuário (tarefa de usuário)  
  
1.  Clique no botão **Configurações** no canto superior direito da tela.  
  
2.  Clique em **Opções**.  
  
3.  Clique na guia **Sincronização**.  
  
4.  Em **Sincronização de recursos com Outlook**, marque **Sincronizar registro de recurso com Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importar seus compromissos pessoais (tarefa de usuário)  
 Somente é possível importar seus compromissos do calendário e projetar exibição para a entrada do tempo de Project Service Automation.  
  
1. Abra o calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] e clique em **Importar dados**.  
  
2. Na tela Filtros, selecione **Compromissos para troca** e então clique em **Aplicar**.  
  
3. O sistema colocará os compromissos na exibição de entrada de tempo com as entradas sugeridas da semana atual. Para adicionar entradas de outra semana, clique em **Anterior** ou **Próximo**.  
  
4. Selecione o compromisso que deseja adicionar à exibição de entrada do tempo de Project Service Automation.  
  
5. Na caixa pop-up **Entrada de hora**, selecione as opções apropriadas para converter o compromisso para uma exibição de entrada do tempo de Project Service Automation.  
  
6. Clique em **Salvar**.  
  
### <a name="see-also"></a>Consulte também  
 [Guia de tempo, despesas e colaboração](../psa/time-expense-collaboration-guide.md)
