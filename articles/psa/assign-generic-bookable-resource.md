---
title: Atribuir recursos reserváveis genéricos a uma tarefa e equipe de projeto
description: Este artigo fornece informações sobre como reservar recursos genéricos para tarefas e equipes de projeto.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9f67ab7381747e5d780f8b0024dd98ae8420d05f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923542"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recurso 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Além de reservar e atribuir recursos nomeados ou reais ao seu projeto, você pode atribuir recursos genéricos a tarefas do projeto. Esses recursos podem atuar como espaços reservados para recursos nomeados até você estar pronto para montar a equipe do seu projeto com recursos nomeados. 

1. No PSA (Project Service Automation), abra a página **Projeto** e, na guia **Agendar**, insira o nome da posição do recurso genérico na célula **Recurso** da agenda. Ou, clique no ícone **Recurso** da célula a fim de abrir o seletor de recursos e insira o nome do recurso genérico que deseja criar.

![Criando e atribuindo um membro de equipe genérico.](media/RM-how-to-9.png)

Isso abrirá o painel **Criação rápida: membro da equipe do projeto**. 

2. Insira a função e a unidade organizacional do membro da equipe de recurso genérico e clique em **Salvar**.

![Criação rápida do membro da equipe genérico.](media/RM-how-to-10.png)

3. Depois de criar o novo membro da equipe de recurso genérico, ele é atribuído à tarefa. Você pode continuar atribuindo esse recurso genérico a outras tarefas na agenda de tarefas.

![Atribuindo membro da equipe genérico existente a tarefas.](media/RM-how-to-11.png)

4. Depois de atribuir o recurso genérico, você pode gerar um requisito de recurso e preenchê-lo diretamente reservando ou enviando uma solicitação de recurso a um gerente de recursos.

![Gerando um requisito para um membro da equipe genérico.](media/RM-how-to-12.png)

Na grade do membro da equipe, além de poder usar o seletor de recursos como mencionado acima, você pode adicionar recursos genéricos diretamente. Os recursos são adicionados com um requisito de recurso que se baseia nas datas de início/término e um método de alocação especificado no painel **Criação Rápida: Membro da Equipe do Projeto**.

É possível ver a diferença se você adicionar o membro da equipe genérico diretamente e atribuir mais tarefa ao recurso genérico do que as horas exigidas. Clique em **Gerar Requisito** para regenerar o requisito a fim de equilibrar as horas exigidas em relação às atribuições.

Também é possível clicar no link **Requisito de recurso** na grade da equipe para abrir o requisito e adicionar habilidades, recursos preferidos, etc.

![Requisito de recurso.](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
