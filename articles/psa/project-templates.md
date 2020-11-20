---
title: Modelos de projeto
description: Este tópico fornece informações sobre como usar modelos de projeto para configuração rápida de projetos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122990"
---
# <a name="project-templates"></a>Modelos de projeto 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Um modelo de projeto é uma estrutura predefinida que ajuda você a iniciar um projeto com rapidez e facilidade. Você pode usar um modelo predefinido para criar um novo projeto com um único clique. Em relação aos projetos, é necessário definir os pré-requisitos dos modelos de projeto. Também é necessário definir um calendário de projeto para cada modelo, além disso, funções e listas de preços devem ser predefinidas na organização, para que os componentes do modelo tenham dados úteis.

Um modelo de projeto consiste em três componentes: uma agenda, estimativas de projeto e membros da equipe de projeto.

## <a name="schedule"></a>Agenda

Uma agenda em um modelo de projeto tem o mesmo conjunto de elementos que uma agenda em um projeto. Você pode criar uma hierarquia de tarefas, associar funções a tarefas, definir atributos de agenda e dependências. Uma agenda em um modelo de projeto também oferece suporte a modos de tarefa para cada tarefa. Portanto, ela oferece suporte ao mecanismo de agendamento. Você deve associar um calendário de projeto ao projeto. Ao criar uma agenda de trabalho, não há nenhuma diferença entre um modelo de projeto e um projeto.

## <a name="project-estimates"></a>Estimativas de projeto

Estimativas de projeto em um modelo de projeto funcionam da mesma forma que estimativas de projeto em um projeto. No entanto, os preços de custo e de vendas são obtidos das listas de preços de custo e de vendas padrão que estão definidas nos parâmetros.

## <a name="creating-a-project-from-a-template"></a>Criar um projeto com base em um modelo
 
Há várias maneiras de criar um projeto com base em um modelo:

- Ao criar um projeto com base em uma cotação, você pode selecionar um modelo de projeto na caixa de diálogo **Criação Rápida: Projeto**.

> ![Caixa de diálogo Criação Rápida: Projeto](media/project-11.png)

- Ao criar um projeto selecionando **Novo Projeto**, a página **Projeto** será exibida antes do salvamento do registro. No campo **Escolher um Modelo**, selecione um dos modelos de projeto predefinidos na organização.
- Use **Criar Projeto com base em um Modelo** na página **Entidade de Modelo** .

## <a name="copying-components-of-template-to-project"></a>Copiar componentes de um modelo para um projeto

Quando você copia os componentes de um modelo de projeto para um projeto, algumas substituições podem ocorrer, dependendo das configurações no projeto.

### <a name="copying-the-schedule"></a>Copiar a agenda

Quando você copia a agenda de um modelo de projeto, se o projeto tiver um calendário diferente do modelo, as horas de trabalho do calendário do projeto serão aplicadas à agenda de tarefas. Dessa maneira, a agenda é ajustada para corresponder ao calendário de projeto subjacente. De maneira semelhante, a primeira tarefa na agenda ocupa a data de início do projeto e a agenda do restante da hierarquia é atualizada com base na duração e nas dependências especificadas no modelo. 

### <a name="copying-project-estimates"></a>Copiar estimativas de projeto 

Quando você copia as linhas de estimativas de projeto, as listas de preços são atualizadas. Na lista de preços de custo, essas atualizações são baseadas na unidade proprietária do projeto. Na lista de preços de vendas, elas são baseadas no cliente. Em projetos associados a uma entidade de vendas, os preços de custo e de vendas da unidade são determinados com base nessas listas de preços.

### <a name="copying-a-project-team"></a>Copiar uma equipe de projeto

Quando uma equipe de projeto é copiada de um modelo de projeto para um projeto, os recursos genéricos são copiados, juntamente com as habilidades e proficiências definidas no modelo. As atribuições de recursos genéricos também são mantidas, pois estavam no modelo de projeto. Recursos nomeados não têm suporte em modelos de projeto.
