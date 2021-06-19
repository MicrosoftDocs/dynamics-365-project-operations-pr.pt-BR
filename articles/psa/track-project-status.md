---
title: Rastrear o status de um projeto
description: Como rastrear o status de um projeto no Project Service
author: ruhercul
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014372"
---
# <a name="track-a-projects-status-project-service"></a>Rastrear o status de um projeto (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Use os recursos do [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] para acompanhar o progresso do projeto de um cliente.  

À medida que o compromisso evolui, os estágios do projeto são atualizados para refletir o estágio do compromisso:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Novo**    | Ao criar um projeto, o estágio é definido como **Novo**. Se o projeto foi criado partir de um modelo, neste estágio, o projeto pode ter um cronograma, estimativas e dados da equipe. Caso contrário, será a estrutura de tópicos do projeto, e você precisará inserir manualmente o restante dos componentes do projeto. |
|  **Cotação**   |      Ao associar um projeto a uma cotação ou criar um projeto a partir de uma cotação, o estágio do projeto é definido como **Cotação**, e a hora de início e de término estimadas são também atualizadas. Quando o projeto está no estágio de cotação, os detalhes da cotação são exibidos na guia **Vendas** na página **Projeto**.      |
|   **Plano**   |                                     Quando você vence uma cotação associada a um projeto, e quando o compromisso evolui para o estágio de contrato, o estágio do projeto é atualizado para **Plano**. Os detalhes do contrato são exibidos na guia **Vendas** na página **Projeto**.                                      |
| **Concluir** |                    Quando o trabalho do projeto é concluído, você pode mudar o estágio para **Concluído**. Quando o estágio do projeto é definido como concluído, entende-se que o trabalho foi 100% concluído, mas que o projeto será mantido aberto para o registro de horas ou entradas de despesas pendentes.                     |
|  **Fechar**   |           Quando todas as transações tiverem sido registradas no projeto e nada mais precisar ser registrado, você poderá definir manualmente o estágio como **Fechado**. Quando o projeto é definido como **Fechado**, não é possível registrar mais nenhuma transação nele, e ele será usado apenas para leitura.           |

## <a name="to-track-a-projects-status"></a>Para acompanhar o status de um projeto  

1.  Vá para **Project Service > Projetos**.  

2.  Clique no projeto no qual você deseja trabalhar.  

3.  Na barra da parte superior da tela, selecione a seta para baixo ao lado do nome do projeto e, em seguida, clique em **Acompanhamento de Projeto**.  

4.  Selecione **Acompanhamento de Esforços** ou **Acompanhamento de Custos** na lista suspensa acima da lista de tarefas.  

5.  Clique duas vezes em qualquer tarefa editá-la. Você também pode mover ou redimensionar as barras no gráfico de Gantt para alterar o tempo e o progresso da tarefa.  

### <a name="see-also"></a>Consulte também  
 [Guia do gerente de projeto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]