---
title: Configurações do projeto
description: Este tópico fornece informações sobre configurações de gerenciamento do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071591"
---
# <a name="project-settings"></a>Configurações do projeto

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Use as configurações a seguir para acessar os recursos de planejamento do projeto.

## <a name="work-template"></a>Modelo de trabalho

Para criar uma agenda de projeto, crie um modelo de calendário de projeto que defina o número de horas de trabalho por dia e todos os feriados comerciais. Para criar um modelo de calendário de projeto, associe um modelo de trabalho ao campo **Modelo de calendário** do projeto. Siga estas etapas para criar um modelo de trabalho.

1. No PSA, no painel de navegação à esquerda, clique em **Recursos**. 
2. Na página de lista **Recursos** , abra um registro de usuário e selecione **Mostrar Horas de Trabalho**.

  > [!NOTE]
  > Certifique-se de permitir pop-ups na página do navegador. Isso permite ver as horas de trabalho definidas para o recurso.
  
3. Na guia **Exibição Mensal** , clique em **Configurar**. Uma lista de três opções é exibida: 

  - Nova Agenda Semanal
  - Agenda de Trabalho para Um Dia
  - Folga

> ![Configurar opções](media/project-13.png)

4. Selecione **Nova Agenda Semanal** e defina as opções para essa agenda de recurso. Você pode definir uma agenda semanal recorrente, parâmetros de hora diários, feriados comerciais e muito mais.
5. Defina um intervalo de datas, selecione **Salvar** e clique em **Fechar**. 
6. Volte para a página de lista **Recursos** e selecione o recurso para o qual você definiu as horas de trabalho. 
7. Selecione **Definir Calendário como** para definir o modelo de trabalho. 
8. Na caixa de diálogo **Modelo de Trabalho** , insira um nome para o modelo de trabalho e selecione **Aplicar**. 

Agora é possível associar o modelo de trabalho a um modelo de calendário de projeto.

## <a name="resource-roles"></a>Funções do recurso

O termo *função do recurso* se refere ao conjunto de habilidades, competências e certificações que uma pessoa deve ter para realizar um conjunto de tarefas específicas em um projeto. O PSA permite orçar e cobrar o tempo de um recurso com base na função à qual esse recurso está associado. Cada organização deve configurar essas funções usando o painel de navegação à esquerda no menu **Project Service**.

Cada organização deve configurar essas funções na página **Categorias de Recursos Ativos**. Para abrir essa página, no painel de navegação à esquerda, selecione **Funções do Recurso**.

## <a name="price-lists"></a>Listas de preços

As listas de preços permitem definir preços de custo e vendas para funções do recurso, categorias de despesa, produtos e outros elementos em uma organização. Antes de definir estimativas financeiras para o trabalho que deve ser entregue para um projeto, você deve criar uma listas de preços de custo e vendas de apoio. Na seção de parâmetros, você também deve configurar uma lista de preços de custo e vendas padrão que se aplica a todos os projetos que são criados na organização. Na página **Parâmetros do Projeto Ativos** , certifique-se de configurar uma lista de preços de custo e vendas padrão.
