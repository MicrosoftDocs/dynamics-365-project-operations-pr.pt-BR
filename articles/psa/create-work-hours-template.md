---
title: Criar um modelo de horas de trabalho.
description: Como criar um modelo de horário de trabalho no Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c34634817fc8e4c993261024a8b19d45052bf5e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071438"
---
# <a name="create-a-work-hours-template-project-service"></a>Criar um modelo de horário de trabalho (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Para poder criar agendas de projetos, você precisa configurar um calendário de projeto que defina o número de horas de trabalho a serem acomodadas por dia na agenda e todos os feriados comerciais. Você faz isso com um modelo de horário de trabalho, que contém detalhes sobre o horário de trabalho por dia, folgas e outros feriados comerciais.  
  
 Ao criar um projeto, você associa um modelo de trabalho ao calendário de projeto para aplicar a agenda ao projeto.  
  
 Há duas maneiras de criar um modelo de horário de trabalho:  
  
-   Criar um modelo de horário de trabalho baseado no calendário do recurso.  
  
-   Criar um novo modelo de horário de trabalho.  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a>Para criar um modelo de horário de trabalho baseado no calendário do recurso  
  
1.  Vá para **Project Service > Recursos**.  
  
2.  Selecione o recurso no qual você deseja basear seu horário de trabalho.  
  
3.  Clique em **Salvar Calendário Como** , insira um nome para o modelo de horário de trabalho e clique em **Salvar**.  
  
4.  Ao concluir a alteração das opções, clique em **Salvar e Fechar**.  
  
5.  Clique no botão **Salvar** no canto inferior direito da tela.  
  
#### <a name="to-create-a-new-work-hours-template"></a>Para criar um novo modelo de horário de trabalho  
  
1.  Vá para **Project Service > Modelos de Horário de Trabalho**.  
  
2.  Clique em **Novo**.  
  
3.  Insira um nome para o modelo de horário de trabalho.  
  
4.  Selecione um recurso no qual basear o horário de trabalho e clique em **Salvar**.  
  
### <a name="see-also"></a>Consulte também  
 [Configurar recursos](../psa/set-up-resources.md)
