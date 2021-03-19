---
title: Criar entrada de hora
description: Esse tópico fornece informações sobre como criar entradas de hora.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8f86f69090e869bf5e6a7505a4cb1ad1c69b475b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282139"
---
# <a name="create-time-entries"></a>Criar entrada de hora

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Em versões anteriores do Dynamics 365 Project Service Automation, as entradas de hora eram inseridas semanalmente. Na versão 3 do Project Service Automation, as entradas de hora são inseridas diariamente. No entanto, após algumas entradas terem sido criadas, é possível criar em massa ou copiá-las.

## <a name="create-a-time-entry"></a>Criar entrada de hora

Siga as etapas para criar uma entrada de hora.

1. Na página **Entradas de hora**, selecione **Novo**.
2. Na caixa de diálogo **Criação rápida: Entrada de hora**, insira a duração da entrada de hora em minutos, horas ou dias. A duração deve ser inserida no seguinte formato: *x* minutos, *x* horas ou *x* dias. As horas e os dias também podem ser inseridos usando decimais, como *x,x* horas ou *x,x* dias.
3. Selecione o tipo de entrada de hora e o projeto no qual você está inserido a entrada de hora.
4. No campo **Tarefa do projeto**, localize a tarefa para essa entrada de hora.

    > [!NOTE]
    > Se estiver criando uma entrada de hora para uma tarefa que não foi atribuída a um usuário, no campo **Tarefa do projeto**, selecione o botão **Pesquisar**, selecione **Alterar exibição** e depois **Todas as tarefas de projeto ativas** para listar todas as tarefas.

5. Insira uma descrição, se necessário, e selecione **Salvar e fechar**.

Após criar e salvar a entrada de hora, você pode editá-la na grade de entrada de hora. A grade de entrada de hora é compatível com dois formatos:

- Você pode inserir entradas de hora no formato **hh:mm**. Esse formato será convertido em horas e frações.
- Você pode inserir horas e frações diretamente.

Observe que as frações de uma hora não são minutos. Portanto, 1,5 representa 1 hora e 30 minutos. A mesma regra é aplicada a frações de um dia. Um dia é 24 horas e 0,5 dias representa 12 horas.

## <a name="bulk-create-time-entries"></a>Criar entradas de hora em massa

Após criar algumas entradas de hora, é possível copiá-las para criar entradas de hora adicionais em massa.

1. Na página **Entradas de hora**, selecione **Copiar semana**.
2. No grupo de campo **No período** nos campos **Data de início** e **Data de término**, defina o intervalo de datas que será usado para copiar as entradas.
3. No grupo de campo **Até o período** no campo **Data de início**, especifique a data usada para criar as entradas de hora.
4. Selecione **Cópia** para criar uma cópia das entradas de hora que correspondem ao dia da semana especificado no grupo de campo **Até o período**. Por exemplo, a entrada de hora para segunda-feira da semana passada é copiada para a segunda-feira da semana especificada no grupo de campo **Até o período**.

## <a name="import-data-for-time-entries"></a>Importar dados para entradas de hora

Você pode importar dados de reservas e atribuições de projetos. Ao importar dados, é possível especificar o intervalo de datas das reservas a ser importado e, em seguida, explicitamente selecionar as reservas que devem ser criadas como entradas de hora **Rascunho**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Recursos para agrupar por, classificar, pesquisar e filtrar

Você pode agrupar e filtrar as entradas de hora pelas dimensões especificadas nas colunas. No campo **Agrupar por**. selecione a dimensão a ser usada para filtrar as entradas de hora. Você também pode classificar os registros de entrada de hora em ordem crescente ou decrescente usando a seta de classificação nos cabeçalhos de coluna. Além disso, é possível mostrar ou ocultar entradas selecionando-se o botão **Filtrar** nos cabeçalhos de colunas e, em seguida, na caixa **Pesquisar**, inserindo o texto que deve ser usado para pesquisar entradas de hora por nome de projeto, tarefa de projeto, entrada de hora ou recurso.


[!INCLUDE[footer-include](../includes/footer-banner.md)]