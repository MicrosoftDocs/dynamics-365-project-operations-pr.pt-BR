---
title: Criar um modelo de projeto
description: Como criar um modelo de projeto no Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749034"
---
# <a name="create-a-project-template-project-service"></a>Criar um modelo de projeto (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Os modelos de projeto economizam seu tempo se a empresa tiver lances regulares em tipos semelhantes de projetos. Oferece um conjunto de direitos padrão e as horas de um tipo estimado de projeto. Gerentes de conta e gerentes de projeto podem criar os projetos com base em um modelo do projeto, ou podem copiar o modelo e fazer o seu próprio.  
  
## <a name="components-of-project-template"></a>Componentes do modelo do projeto
 Um modelo do projeto tem três componentes:  
  
- **Estrutura de detalhamento de trabalho**: Uma estrutura de detalhamento de trabalho em um modelo do projeto com o mesmo conjunto de funções do projeto. Você pode criar uma hierarquia da tarefa de encarregar-se de funções que defina uma agenda de dependências e exiba os dados contidos no Gantt. A estrutura de detalhamento de trabalho nos modelos de projetos também oferece suporte a modos de tarefa para cada tarefa. Não há um modelo diferente entre um modelo de projeto e de um projeto para criar a agenda de trabalho.  
  
- **Estimativas e cotações de projeto**: Estimativas de projeto nos modelos funcionam do mesmo jeito que nos projetos, exceto nas listas de preço para padronizar os preços de custo e vendas como sempre o custo de padrão e listas de preço de vendas definidos no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. O restante da funcionalidade é o mesmo do projeto.  
  
- **Criação da equipe de projeto**: ao criar uma equipe de projeto para um modelo de projeto, você não pode reservar um recurso nomeado em um modelo. Você pode usar **Gerencia a equipe de projeto** na estrutura de detalhamento de trabalho para gerar um conjunto genéricos de recursos. Também é possível especificar proficiências e habilidades e obrigatórios genéricas de recursos. Não é possível fazer um recurso genérico para reservar um recurso do projeto em modelos.  
  
## <a name="create-a-project-from-a-template"></a>Criar Projeto a Partir do Modelo  
 Você pode criar um modelo do projeto de uma das seguintes maneiras:  
  
-   Ao criar um projeto com base na cotação, você poderá escolher um modelo de projeto no formulário de criação rápida de projeto.  
  
-   Como criar um projeto clicando em **Novo projeto**, o formulário é exibido de projetos antes de salvar o registro. A partir daqui, é possível clicar em um campo **Selecionar um modelo** para escolher na lista de modelos predefinidos de projeto em sua organização.  
  
-   Clique em **Criar projeto com base em um modelo** na página **Modelo de projeto** para criar um projeto com base no modelo.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Copiar componentes de um modelo a um projeto  
 Quando você copia os componentes de um projeto em um modelo, existem algumas coisas que você deve saber.  
  
 **Copiando uma estrutura de detalhamento de trabalho**: Quando você copia a estrutura de detalhamento de trabalho de um modelo do projeto, se houver um projeto do projeto do modelo que as horas de trabalho do projeto no serão aplicadas para tarefas de agendamento. A agenda ajusta isto ao calendário do projeto na forma. Da mesma forma, a primeira tarefa na estrutura de detalhamento de trabalho realiza a data de início do projeto, além o restante da agenda de trabalho da hierarquia é atualizado com base nas dependências e durações especificadas na estrutura de detalhamento de trabalho do modelo.  
  
 **Copiando estimativas e cotações de projeto**: Quando você copia nas linhas de estimativa de projeto, listas de preços são atualizadas com base nela para proprietário de projeto ao cliente e a lista de preço de custo na lista de preços das vendas. O custo da unidade e os preços de vendas são determinadas essas listas de preços de projetos associados a uma entidade de vendas.  
  
 **Um copiando a equipe de projeto**: Quando você copia a equipe de projeto de modelo para um projeto, os recursos são copiados genéricos terminar, e pelas habilidades de proficiências definidas no modelo. As atribuições genéricas de recursos também são mantidas no modelo do projeto.  
  
### <a name="see-also"></a>Consulte também  
 [Guia do gerente de projeto](../project-service/project-manager-guide.md)
