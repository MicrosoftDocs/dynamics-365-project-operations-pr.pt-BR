---
title: Fornecer estimativas de trabalho para um projeto durante o processo de vendas
description: Como fornecer estimativas de trabalho a um projeto durante o processo de vendas no Project Service
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283534"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Fornecer estimativas de trabalho a um projeto durante o processo de vendas (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Durante o processo de vendas, você pode calcular estimativas de vendas completas com linhas de cotação. Os recursos do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] fornecem uma maneira mais científica e determinística de propor estimativas de vendas detalhando itens de trabalho e associando atributos relevantes que contribuem para as estimativas do projeto na estrutura de detalhamento de trabalho.  
  
 Depois de ganhar a venda, você pode usar a estrutura de detalhamento de trabalho associada em seu plano de projeto, refinando-a conforme necessário para a conclusão bem-sucedida do projeto.  
  
## <a name="link-a-project-to-a-quote-line"></a>Vincular um projeto a uma linha de cotação  
 Ao criar uma linha de cotação baseada em projeto, você pode criar um novo projeto a partir da linha de cotação. Você pode usar os modelos de projetos, que são planos de projetos padrão pré-configurados e estimativas financeiras comuns a sua organização ou uma cópia de um plano de projeto e das estimativas de um projeto do passado. Ao criar um projeto, a escolha de um modelo de projeto fornece uma base para restringir o plano de projeto, as estimativas e os requisitos de funções. Ao criar seu projeto a partir de uma cotação, o projeto é automaticamente associado à linha de cotação.  
  
## <a name="project-estimate-components"></a>Componentes de estimativa do projeto  
 A estrutura de detalhamento de trabalho em um projeto fornece uma maneira de detalhar o trabalho em tarefas, manter uma hierarquia de tarefas e atribuir uma estimativa do esforço necessário para executar cada tarefa. Você também pode associar funções a uma tarefa para indicar uma estimativa do tipo de recurso necessário para concluir uma tarefa e uma agenda.  
  
 A estrutura de detalhamento do trabalho ajuda você a determinar estimativas do esforço e da agenda do trabalho. Por padrão, o projeto usa listas de preços padrão que você define anteriormente. Os preços de custo e de vendas definidos nas listas de preços ajudam a determinar estimativas financeiras para detalhamento do trabalho do projeto.  
  
 Se seu projeto estiver associado a uma cotação, e a cotação tiver uma lista de preços diferente do padrão, a lista de preços da cotação será usada para estimativas financeiras.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importar estimativas de um projeto em uma cotação  
 Assim que obter as estimativas do projeto, importe essas estimativas na linha de cotação:  
  
-   Em **Detalhes da Linha de Cotação**, clique em **Importar das estimativas**. 

-   Selecione se as estimativas do projeto devem ser importadas resumidas por tipo de transação, função ou nível de nó da estrutura de detalhamento de trabalho.  
  
### <a name="see-also"></a>Consulte também  
 [Guia do gerente de projeto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]