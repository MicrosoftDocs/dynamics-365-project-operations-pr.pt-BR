---
title: Visão geral de linhas de cotação baseadas em projeto
description: Este tópico fornece informações sobre como usar linhas de cotação baseadas no projeto para o trabalho do projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369857"
---
# <a name="project-based-quote-lines-overview"></a>Visão geral de linhas de cotação baseadas em projeto 

_**Aplica-se a:** Implantação lite - gerenciar faturamento pro forma, Project Operations para cenários com base em recursos/sem estoque_

As linhas de cotação baseadas em projeto são projetadas para ajudar a estimar o trabalho do projeto em uma participação. A estrutura de uma linha de cotação baseada em projeto é estendida para estimativas de projeto com os seguintes conceitos:

- Método de Cobrança
- Mapeamento de projeto e tarefa
- Classes de transação incluídas
- Limite máximo
- Configuração dos encargos
- Estimativa usando os detalhes da linha de cotação
- Clientes da linha de cotação

A tabela a seguir fornece informações sobre os campos na guia **Geral** da linha de cotação baseada em projeto. Esses campos ajudam a estabelecer uma base para uma estimativa detalhada do trabalho do projeto.

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Nome | O nome da linha de cotação que ajuda a identificar o componente discreto da cotação que está sendo estimada. | Copiado para a linha do contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Método de Cobrança | Em uma cotação é criada a partir de uma oportunidade, este valor é copiado do campo correspondente na oportunidade. Este campo inclui os dois principais modelos de contratação compatíveis com o Dynamics 365 Project Operations:</br>- Preço fixo</br>- Hora e material.| Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |
| Project | Use este campo opcional para identificar o projeto que será usado para entregar o trabalho nesta participação. Quando um projeto é mapeado para uma linha de cotação, isso ajuda a configurar tarefas cobráveis e também a gerar uma estimativa baseada em projeto para a linha de cotação como detalhes da linha de cotação. Quando um projeto não é mapeado para uma linha de cotação baseada em projeto, a estimativa deve ser criada manualmente criando cada detalhe da linha de cotação. | Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.|
| Tarefas Incluídas | Indica se esta linha de cotação é usada para todas ou algumas das tarefas do projeto para o projeto selecionado. Este campo possui os valores possíveis a seguir:</br>- Todas as tarefas do projeto</br>- Somente tarefas do projeto selecionadas</br>Um valor em branco neste campo é equivalente à opção **Todas as tarefas do projeto**. | Quando **Somente tarefas do projeto selecionadas** é selecionado na página do projeto, a guia **Configuração de cobrança da tarefa** permite selecionar tarefas específicas para associá-las a esta linha de cotação. Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |
| Incluir Hora | Um valor **Sim**/**Não** indica se as transações de tempo ou custos de mão de obra no projeto selecionado serão incluídas na estimativa nesta linha de cotação. Um valor **Não** indica que as transações de tempo ou custo de mão de obra não serão incluídos na estimativa nesta linha de cotação. Um valor **Sim** indica que as transações de tempo ou custo de mão de obra serão incluídos na estimativa nesta linha de cotação. | Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |
| Incluir Despesa | Um valor **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de cotação. Um valor **Não** indica que as despesas de custo não serão incluídas na estimativa nesta linha de cotação. Um valor **Sim** indica que as despesas de custo serão incluídas na estimativa nesta linha de cotação. | Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |
| Material Incluso | Um valor **Sim**/**Não** indica se os custos de material no projeto selecionado serão incluídos na estimativa nesta linha de cotação. Um valor **Não** indica que os custos de material não serão incluídos na estimativa nesta linha de cotação. Um valor **Sim** indica que os custos de material serão incluídos na estimativa nesta linha de cotação. | Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |
| Incluir Taxa | Um valor **Sim**/**Não** indica se valores no projeto selecionado serão incluídos na estimativa nesta linha de cotação. Um valor **Não** indica que os valores não serão incluídos na estimativa nesta linha de cotação. Um valor **Sim** indica que os valores serão incluídos na estimativa nesta linha de cotação. | Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |
| Valor da Cotação | Este é o valor que será cotado ao cliente para todo o trabalho previsto nesta linha de cotação baseada em projeto. Em uma cotação criada a partir de uma oportunidade, este valor é copiado do campo **Orçamento do cliente** na linha da oportunidade. Quando a linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor nos detalhes da linha de cotação. | Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |
| Imposto Estimado | Este é um campo editável para o usuário adicionar o valor estimado do imposto na linha de cotação. Quando uma linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor do imposto nos detalhes da linha de cotação. | Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |
| Valor Cotado Após Imposto | Este campo é o valor da linha de cotação após o imposto e é somente leitura. O valor neste campo é calculado como *Valor cotado + imposto*. | Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |
| Limite de NTE (limite máximo) | Este campo é editável e está disponível apenas em linhas de cotação baseadas em projeto que tenham o método de cobrança **Tempo e material**. | Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |
| Orçamento do Cliente | Se a cotação tiver sido criada a partir de uma Oportunidade, este campo é editável e copiado a partir do campo correspondente na oportunidade. | Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regras de validação para os campos na guia Geral de linhas de cotação baseadas em projeto

**Regra 1**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Todas as tarefas do projeto**, um projeto será incluído na linha de cotação.

**Regra 2**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Todas as tarefas do projeto**, um projeto e uma determinada classe de transação só poderão ser incluídos em uma única linha de cotação baseada em projeto de uma cotação.

**Regra 3**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Somente determinadas tarefas do projeto**, um projeto e uma determinada classe de transação só poderão ser incluídos em várias linhas de cotação baseada em projeto de uma cotação.

**Regra 4** : se uma oportunidade tiver várias cotações, pode haver linhas de cotação de cotações diferentes que façam referência ao mesmo projeto e incluam a mesma classe de transação.

**Regra 5**: se as cotações não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transação.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Oportunidade</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Cotação</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Linha de cotação</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Tarefas incluídas</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Incluir Hora</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Incluir Despesa</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Material Incluso</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Incluir</strong>
                </p>
                <p>
                    <strong>Taxa</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Válido/ Não inválido</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Razão</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violação da regra Nº 2. Tempo, Despesa e Valores no projeto P1 estão incluídos nas linhas de cotação QL1 e QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violação da regra Nº 2. Tempo, Material e Valores no projeto P1 estão incluídos nas linhas de cotação QL1 e QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Tempo, Material e Valores no projeto P1 estão incluídos em QL1 <br>
A despesa do projeto P1 está incluída em QL2 <br>
Nenhuma sobreposição no que está sendo incluído em cada linha da cotação e, portanto, ela é válida.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violação da regra Nº 2 </p>
                <p>
Q1 inclui Tempo, Material, Despesas e Valores em um subconjunto de tarefas no projeto P1 </p>
                <p>
QL2 inclui Tempo, Despesas e Valores para todo o projeto P1 e, portanto, se sobrepõe ao que está incluído em Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Por regra nº 3, </p>
                <p>
Q1 inclui Tempo, Material, Despesas e Valores em um subconjunto de tarefas no projeto P1.
                </p>
                <p>
QL2 inclui Tempo, Material, Despesas e Valores para um subconjunto de tarefas no projeto P1.
                </p>
                <p>
A única validação adicional é o subconjunto de tarefas no QL1 que difere do subconjunto de tarefas no QL2 para garantir que não haja sobreposições. Isso é feito pelo sistema quando as tarefas são associadas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
De acordo com a regra nº 5, Q1 e Q2 são duas cotações na mesma oportunidade; portanto, ambos podem estimar para os mesmos componentes de um projeto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
De acordo com a regra nº 4, Q1 e Q2 são duas cotações em oportunidades diferentes; portanto, eles não podem fazer estimativa para os mesmos componentes do mesmo projeto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
