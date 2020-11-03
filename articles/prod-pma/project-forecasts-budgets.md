---
title: Previsões e orçamentos de projetos
description: O Microsoft Dynamics 365 Finance fornece previsões e orçamentos de projetos para gerenciar e controlar seus projetos.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071541"
---
# <a name="project-forecasts-and-budgets"></a>Previsões e orçamentos de projetos

[!include [banner](../includes/banner.md)]

Há duas formas de gerenciar e controlar seus projetos: previsões e orçamentos de projetos. 

Use a previsão de projetos se sua organização tiver uma perspectiva operacional e se ela se concentrar em receitas e custos derivados de transações específicas. Use o orçamento de projetos se sua organização se concentrar mais nos valores financeiros. 

As previsões e os orçamentos de projetos usam modelos de previsão para controlar os valores projetados das transações. 

Cada método tem suas vantagens. Você deve considerar os seguintes pontos antes de selecionar um método para a sua organização.

|   Método de alocação       |           Previsão de projetos            |        Orçamento de projetos                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Alocação de períodos**     | Você não pode alocar transações explicitamente em um período fiscal. Na verdade, a previsão e o controle dela são feitos para a vida do projeto. Como as previsões são baseadas em uma data específica, você deverá inferir o período a partir da data. | Você não pode alocar transações para o projetos inteiros ou em um período fiscal. Se você alocar ao longo de um período, poderá transportar os valores não utilizados para o próximo período fiscal. |
| **Visualização de transações**  | Você pode visualizar as transações nos formulários de previsão, onde são exibidas as previsões para toda a empresa e para todos os projetos, independentemente da hierarquia. Para focar em um projeto específico, você deve filtrar os dados.                                       | Você pode visualizar as transações orçadas para uma única hierarquia de projeto. Portanto, é possível visualizar os detalhes da transação para um projeto pai ou seus subprojetos.                 |
| **Variáveis da transação** | Ao inserir transações de previsão, você pode usar todos os atributos existentes para uma transação real. Isso permite maiores detalhes na previsão. Por exemplo, você pode inserir detalhes para quantidades, funcionários, itens ou propriedades de linha.         | Ao inserir os detalhes do orçamento, você pode usar apenas valores, categorias e atividades.                    |
| **Segurança**              | A previsão é baseada nas transações que você insere nos formulários de previsão e não envolve mecanismos de controle do processo. Qualquer funcionário com permissão para um formulário de previsão pode revisar as informações sem aprovação.                                        | O orçamento usa o sistema de fluxo de trabalho, que permite o gerenciamento de mudanças e também manter um histórico das revisões.         |
| **Tipos de entrada**           | As entradas de transações de previsão são baseadas no número de unidades e nos preços unitários de custo e venda.  | Os detalhes do orçamento são baseados em valores, que são divididos entre custos e receitas.                                          |
| **Modelos de previsão**       | Como cada previsão deve ser associada a um modelo, você pode criar vários modelos de previsão e também configurar submodelos.           | O orçamento do projeto limita os modelos de previsão usados para o orçamento. Ter menos modelos de previsão pode ajudar a aumentar a consistência nas projeções.                           |
| **Estouro de custos**         | Você só pode permitir ou proibir a entrada de transações que causarão estouro de custos.   | O orçamento do projeto fornece opções de controle adicionais para os usuários. Você pode permitir avisos e estouro de custos.                    |
| **Controlar**               | O controle da previsão é realizado usando a redução da previsão. Os valores reais são subtraídos dos saldos das transações previstas sem qualquer trilha de auditoria. Isso pode tornar mais difícil rastrear onde as transações reais ocorreram.                   | No controle de orçamento do projeto, os valores reais são subtraídos dos valores do orçamento restante. Isso permite uma trilha de auditoria mais clara.                                   |

## <a name="project-forecasts"></a>Previsões de projetos
Ao usar a previsão de projeto, você pode inserir transações de previsão em formulários de previsão para cada tipo de transação. Cada atributo que está disponível para uma transação real pode ser usado para uma transação de previsão (por exemplo: lucratividade da linha, atributos da linha, funcionários ou descrições). Você também pode projetar quanto tempo depois de incorrer em um custo enviará a fatura ao cliente. 

As transações de previsão do projeto são baseadas em unidades e valores. 

Você deve associar cada previsão de projeto a um modelo de previsão. Quando você insere uma transação de previsão, um modelo de previsão é sugerido automaticamente. O modelo de previsão atua como um contêiner para as transações de previsão. 

Você pode designar modelos de previsão como submodelos de um modelo. Isso permite fazer previsões por região, período ou departamento. Você pode copiar as transações de previsão em um modelo para criar um novo modelo, e também transferir as transações para o razão geral. Como existe uma relação de um-para-um entre uma previsão e um modelo, cada modelo de previsão constitui um orçamento diferente para um projeto. 

Os modelos de previsão podem usar a redução de previsão como mecanismo de controle para projetos. Na redução da previsão, as transações reais reduzem os saldos das transações previstas. No entanto, como a redução da previsão é aplicada ao projeto mais alto na hierarquia, ela fornece uma visão limitada das alterações na previsão. Por exemplo, se um funcionário estiver associado a um subprojeto, as transações reais do funcionário serão postadas no projeto pai. Isso pode dificultar o rastreamento das alterações, porque você não pode determinar facilmente qual transação em qual subprojeto causou uma redução no valor previsto. Portanto, é uma boa ideia criar uma cópia de um modelo de previsão para usar na redução da previsão. Você pode então usar relatórios para visualizar o que foi originalmente previsto. 

É possível revisar, copiar, excluir ou transferir previsões do projeto para um orçamento do razão geral. No entanto, não há controle de processo. Qualquer funcionário com permissão para um formulário de previsão pode fazer revisões sem análise.

-   **Revisar** : você pode revisar uma transação de previsão nos mesmos formulários em que as entradas originais foram feitas.
-   **Copiar ou excluir** : ao copiar transações de previsão, você copia as linhas de transação de um modelo de previsão para outro. Ao excluir uma previsão, você exclui as transações de previsão de um modelo de previsão. Para limitar as transações de previsão que são copiadas ou excluídas, selecione tipos específicos de transações e de datas. Assim, você pode copiar ou excluir apenas partes específicas de uma previsão.
-   **Transferir** : ao transferir uma previsão de projeto para um orçamento do razão geral, você transfere as transações de previsão de um modelo de previsão para um orçamento do razão geral. Você pode substituir quaisquer transações transferidas anteriormente no orçamento do razão geral para o qual transferiu a previsão do projeto.

## <a name="project-budgets"></a>Orçamentos de projetos
O orçamento de projeto é um método mais simples do que a previsão, embora se integre aos modelos de previsão. Ele usa um único formulário de entrada para os detalhes e as revisões do orçamento original, e permite projeções baseadas apenas no valor, categoria ou atividade. 

No orçamento do projeto, todos os orçamentos e revisões originais devem ser enviados a um fluxo de trabalho do projeto para aprovação. Os fluxos de trabalho fornecem maior controle sobre o processo e criam um registro do histórico de alterações. 

O orçamento de projeto é semelhante ao orçamento do razão geral, mas é mais rápido e fácil de configurar. Muitas das opções no orçamento do razão geral, como sequências numéricas ou moeda, não precisam ser configuradas separadamente para projetos.

Os orçamentos do projeto são associados automaticamente a dois modelos de previsão, um para o orçamento original e outro para o orçamento restante. Portanto, os relatórios baseados em modelos de previsão podem usar dados de orçamento. Quando um orçamento de projeto é confirmado, o sistema cria transações de previsão com base nos modelos associados, que são usados para fins de relatório e controle.

## <a name="forecast-models"></a>Modelos de previsão
Os modelos de previsão possuem uma hierarquia de camada única. Isso significa que uma previsão de projeto deve ser associada a um modelo de previsão.

Se você usar a previsão de projetos, poderá identificar os modelos como submodelos. Você pode então criar previsões por departamento, período ou região. Por exemplo, você pode criar um modelo de previsão para um ano e, em seguida, criar submodelos para as previsões regionais do Nordeste, Sudeste, Noroeste e Sudoeste que os gerentes regionais enviam. Ao selecionar diferentes opções nos relatórios disponíveis, você pode visualizar as informações por previsão total ou por submodelo.



