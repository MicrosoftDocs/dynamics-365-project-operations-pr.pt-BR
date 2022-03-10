---
title: Configurar modelos de custo
description: Este tópico fornece informações sobre como criar e usar modelos de custo no Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b3a9f1e4f5ea0abe34dc860db87ef349daa46c487b03d271bfe207868c521f39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993542"
---
# <a name="set-up-cost-templates"></a>Configurar modelos de custo

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_


Este tópico fornece informações sobre como criar e usar modelos de custo no Project Operations. Um modelo de custo determina:

- As categorias do projeto para transações previstas e reais a serem incluídas em uma porcentagem do cálculo de conclusão do projeto. O valor da porcentagem concluída é usado para calcular quanta receita é reconhecida.
- Se a porcentagem de conclusão puder ser modificada se for calculada automaticamente.
- Se a porcentagem concluída for calculada com base em valores ou unidades.

## <a name="cost-template-example"></a>Exemplo de modelo de custo

Você está trabalhando em um projeto de design de site para um cliente no qual cobra uma taxa fixa de US$ 10.000. Você prevê que levará 100 horas (US$ 5.000) para concluir o projeto. Você também prevê duas passagens aéreas e quatro noites em um hotel para viagens ao local do cliente (US$ 1.800). Isso resulta em um custo total previsto de US$ 6.800.

Ao executar o processo de reconhecimento de receita de preço fixo para criar uma estimativa no final do mês, você descobre que trabalhou 35 horas no projeto. Isso ainda não inclui voos ou custos de hotel. Você também fez com que um assistente realizasse cinco horas de pesquisa para o projeto a um custo de US$ 100, algo que não havia planejado.

Ao calcular o valor total da porcentagem para este projeto, você tem as seguintes opções:

- Você deseja incluir todos os custos (horas e despesas) ou apenas horas?
- Você deseja incluir todos as horas ou apenas as horas planejadas?
- Você deseja calcular a porcentagem concluída com base no custo em dólares das horas planejadas (US$ 5.000) ou apenas no número de horas (100)?

Suas respostas a essas perguntas determinam as opções que você define no modelo de custo e as categorias que seleciona nas linhas do modelo de custo.

A tabela a seguir ilustra os resultados de diferentes métodos de cálculo do valor de porcentagem concluída para este cenário.

| Conclusão baseada em | Custo ou unidades em dólar | Porcentagem de conclusão | Cálculo |
| --- | --- | --- | --- |
| Todas as horas, sem despesas | Custo em dólar | 37% 35 x US$ 50 + US$ 100 = US$ 1.850 US$ 1.850/US$ 5.000 |
| Todas as horas, sem despesas | Unidades | 40% | 40 horas / 100 horas (incluindo cinco horas não planejadas) |
| Horas planejadas, sem despesas | Custo ou unidade em dólar | 35% | 35/100 horas ou 35 x US$ 50 / 5.000 |
| Todas as horas e despesas | Custo em dólar | 27,2% | US$ 1.850 / US$ 6.800 |

Decidir qual abordagem adotar para criar um modelo de custo pode depender de várias considerações:

- Se você incluir horas não planejadas no modelo de custo, correrá o risco de chegar a 100 por cento concluído antes do projeto ser concluído. Isso ocorre porque as horas reais serão maiores do que as horas planejadas. Se você usar um dos dois primeiros métodos listados na tabela, deverá alterar o plano (unidades previstas) quando tiver conhecimento dos desvios. Nesse caso, você adicionaria ou subtrairia horas com base no conhecimento do que é necessário para concluir o projeto. Se o projeto exigisse mais 65 horas para ser concluído, você adicionaria cinco horas ao plano para um total de 105. Se você souber que seu assistente fará mais cinco horas de pesquisa, o total será de 110 horas.
- Se você usar o terceiro método listado na tabela, deverá atualizar apenas as horas planejadas para o seu próprio tempo para manter o cálculo da porcentagem concluída preciso. Sua lucratividade mudará quando horas não planejadas forem registradas, mas você permanecerá em uma trajetória de porcentagem concluída conhecida.
- Se você usar o quarto método listado na tabela, o risco é que as despesas ocorram em momentos irregulares e não sejam refletidas no progresso de conclusão. Portanto, se as despesas forem incluídas, elas poderão levar a uma flutuação da porcentagem concluída acima do desejável. Por exemplo, como você ainda não voou, sua porcentagem concluída foi de 27%, em vez de 35% ou 37%, se você baseou o cálculo apenas no tempo. Se você tivesse feito uma viagem por duas noites e previsto custos de voo e hotel com precisão, o percentual concluído seria de 40,4% (US$ 1.850 para mão de obra e US$ 900 para despesas = US$ 2.750 / US$ 6.800 = 40,4%). Portanto, incorrer nas despesas de apenas uma viagem de avião mudaria o percentual concluído de 27% para 40%.

## <a name="create-cost-templates"></a>Criar modelos de custo
Para criar modelos de custo, siga estas etapas:

1. Para acessar modelos de custo, no ambiente do Dynamics 365 Finance, acesse **Gerenciamento e contabilidade de projetos** > **Configuração** > **Estimativas** > **Modelo de custo**.
2. Selecione **Novo** para criar um novo modelo de custo. Insira um nome e uma descrição.
3. Forneça a ID da linha de custo para cada tipo de transação.
4. Selecione um método de conclusão padrão:

  - **Automático**: a porcentagem de conclusão é calculada automaticamente em um projeto. Não é possível alterar o valor resultante.
  - **Manual**: a porcentagem de conclusão é calculada automaticamente em um projeto. Não é possível alterar o valor resultante.

  > [!NOTE]
  > Para cálculos manuais, a porcentagem de conclusão é mantida em **Cálculo manual** na guia **Geral** na página **Estimativa**.

5. Em **Conclusão baseada em**, selecione um dos seguintes valores:

  - **Valor**: o valor em moeda contábil calcula a porcentagem de conclusão.
  - **Unidade**: a quantidade calcula a porcentagem de conclusão.
  - **Linha reta**: o sistema calcula a porcentagem de conclusão em uma base proporcional usando as datas de início e término do projeto para determinar a duração do projeto.

6. Selecione **Linhas de custo** para revisar as linhas de custo do modelo de custo. É necessária pelo menos uma linha de custo para cada tipo de transação. No entanto, você pode criar várias linhas de custo para os mesmos tipos de transação e definir os atributos desejados para essas linhas.
7. Na guia **Categorias**, selecione as categorias de projeto a serem incluídas na linha do modelo de custo.
8. Na guia **Geral**, selecione se esta linha será incluída no cálculo da porcentagem de conclusão.
9. Selecione o custo para concluir o método a ser usado ao calcular a porcentagem de conclusão.


[!INCLUDE[footer-include](../includes/footer-banner.md)]