---
title: Visão geral de linhas de cotação baseadas em projeto - lite
description: Este tópico fornece informações sobre como usar linhas de cotação baseadas no projeto para o trabalho do projeto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181078"
---
# <a name="project-based-quote-lines-overview---lite"></a>Visão geral de linhas de cotação baseadas em projeto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

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
| Nome | O nome da linha de cotação que deve ajudar você a identificar o componente discreto da cotação que está sendo estimada. | Copiado para a linha do contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Método de Cobrança | Em uma cotação é criada a partir de uma oportunidade, este valor é copiado do campo correspondente na oportunidade. Este campo inclui os dois modelos de contratação principais compatíveis com o Dynamics 365 Project Operations:</br>- Preço fixo</br>- Hora e material.| O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Project | Use este campo opcional para identificar o projeto que será usado para entregar o trabalho nesta participação. Quando um projeto é mapeado para uma linha de cotação, isso ajuda a configurar tarefas cobráveis e também a gerar uma estimativa baseada em projeto para a linha de cotação como detalhes da linha de cotação. Quando um projeto não é mapeado para uma linha de cotação baseada em projeto, a estimativa deve ser criada manualmente criando cada detalhe da linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.|
| Tarefas Incluídas | Indica se esta linha de cotação é usada para todas ou algumas das tarefas do projeto para o projeto selecionado. Este campo possui os valores possíveis a seguir:</br>- Todas as tarefas do projeto</br>- Somente tarefas do projeto selecionadas</br>Um valor em branco neste campo é equivalente à opção **Todas as tarefas do projeto**. | Quando **Somente tarefas selecionadas do projeto** é selecionado, na página do projeto, a guia **Configuração de cobrança de tarefas** a guia permite que você selecione tarefas específicas para associá-las a esta linha de cotação. O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Incluir Hora | Um sinalizador **Sim**/**Não** indica se as transações de tempo ou custo de mão de obra no projeto selecionado serão incluídos na estimativa nesta linha de cotação. Um valor **Não** indica que as transações de tempo ou custo de mão de obra não serão incluídos na estimativa nesta linha de cotação. Um valor **Sim** indica que as transações de tempo ou custo de mão de obra serão incluídos na estimativa nesta linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Incluir Despesa | Um sinalizador **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de cotação. Um valor **Não** indica que as despesas de custo não serão incluídas na estimativa nesta linha de cotação. Um valor **Sim** indica que as despesas de custo serão incluídas na estimativa nesta linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Incluir Taxa | Um sinalizador **Sim**/**Não** indica se os valores no projeto selecionado serão incluídos na estimativa nesta linha de cotação. Um valor **Não** indica que os valores não serão incluídos na estimativa nesta linha de cotação. Um valor **Sim** indica que os valores serão incluídos na estimativa nesta linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Valor da Cotação | Este é o valor que será cotado ao cliente para todo o trabalho previsto nesta linha de cotação baseada em projeto. Em uma cotação criada a partir de uma oportunidade, este valor é copiado do campo **Orçamento do cliente** na linha da oportunidade. Quando a linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor nos detalhes da linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Imposto Estimado | Este é um campo editável para o usuário adicionar o valor estimado do imposto na linha de cotação. Quando uma linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor do imposto nos detalhes da linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Valor Cotado Após Imposto | Este campo é o valor da linha de cotação após o imposto e é somente leitura. O valor neste campo é calculado como *Valor cotado + imposto*. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Limite de NTE (limite máximo) | Este campo é editável e está disponível apenas em linhas de cotação baseadas em projeto que tenham o método de cobrança **Tempo e material**. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Orçamento do Cliente | Se a cotação tiver sido criada a partir de uma Oportunidade, este campo é editável e copiado a partir do campo correspondente na oportunidade. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regras de validação para os campos na guia Geral de linhas de cotação baseadas em projeto

**Regra 1**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Todas as tarefas do projeto**, um projeto será incluído na linha de cotação.

**Regra 2**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Todas as tarefas do projeto**, um projeto e uma determinada classe de transação só poderão ser incluídos em uma única linha de cotação baseada em projeto de uma cotação.

**Regra 3**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Somente determinadas tarefas do projeto**, um projeto e uma determinada classe de transação só poderão ser incluídos em várias linhas de cotação baseada em projeto de uma cotação.

**Regra 4** : se uma oportunidade tiver várias cotações, pode haver linhas de cotação de cotações diferentes que façam referência ao mesmo projeto e incluam a mesma classe de transação.

**Regra 5**: se as cotações não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transação.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Oportunidade</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Cotação</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Linha de cotação</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
                <p>
                    <strong>Tarefas incluídas</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Incluir Hora</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Incluir Despesa</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Incluir</strong>
                </p>
                <p>
                    <strong>Taxa</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Válido/ Não inválido</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Razão</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violação da regra nº2. Tempo, despesa e valores no projeto P1 estão incluídos nas linhas de cotação QL1 e QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violação da regra nº2. Tempo e valores no projeto P1 estão incluídos nas linhas de cotação QL1 e QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
Tempo e valores do projeto P1 estão incluídos no QL1.
A despesa do projeto P1 está incluída no QL2.
Não há sobreposição no que está sendo incluído em cada linha de cotação e é válido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violação da regra nº2 acima </p>
                <p>
Q1 inclui Tempo, despesas e valores em um subconjunto de tarefas no projeto P1.
                </p>
                <p>
QL2 inclui Tempo, despesas e valores para todo o projeto P1 e se sobrepõe ao que está incluído em Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
De acordo com a regra nº 3 acima, </p>
                <p>
Q1 inclui Tempo, despesas e valores em um subconjunto de tarefas no projeto P1.
                </p>
                <p>
QL2 inclui Tempo, despesas e valores de um subconjunto de tarefas no projeto P1.
                </p>
                <p>
A única validação adicional é em torno do subconjunto de tarefas em QL1, que é diferente do subconjunto de tarefas em QL2. Isso garante que não haja sobreposições. Isso é feito pelo sistema quando as tarefas são associadas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="54" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Com base na regra nº5, Q1 e Q2 são duas cotações na mesma oportunidade, então ambas podem estimar para os mesmos componentes de um projeto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="54" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Com base na regra nº4, Q1 e Q2 são duas cotações em oportunidades diferentes, então não podem estimar para os mesmos componentes do mesmo projeto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="54" valign="top">
                <p>
Não é válido </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]