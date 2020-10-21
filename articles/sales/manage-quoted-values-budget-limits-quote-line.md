---
title: Linhas de cotação baseadas em projeto
description: Este tópico fornece informações sobre como usar linhas de cotação baseadas no projeto para o trabalho do projeto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906067"
---
# <a name="project-based-quote-lines"></a>Linhas de cotação baseadas em projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

As linhas de cotação baseadas em projeto são projetadas para ajudar a estimar o trabalho do projeto em uma participação. A estrutura de uma linha de cotação baseada em projeto é estendida para estimativas de projeto com os seguintes conceitos:

- Método de Cobrança
- Mapeamento de projeto
- Classes de transação incluídas
- Limite máximo
- Configuração dos encargos
- Estimativa usando os detalhes da linha de cotação
- Clientes da linha de cotação

A tabela a seguir fornece informações sobre os campos na guia **Geral** da linha de cotação baseada em projeto. Esses campos ajudam a estabelecer uma base para uma estimativa detalhada do trabalho do projeto.

| **Campo** | **Relevância, finalidade e orientação** | **Impacto a jusante** |
| --- | --- | --- |
| Nome | O nome da linha de cotação que deve ajudar você a identificar o componente discreto da cotação que está sendo estimada. | Copiado para a linha do contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Método de Cobrança | Em uma cotação é criada a partir de uma oportunidade, este valor é copiado do campo correspondente na oportunidade. Este campo inclui os dois modelos de contratação principais compatíveis com o Dynamics 365 Project Operations:</br>- Preço fixo</br>- Hora e material.| O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Project | Use este campo opcional para identificar o projeto que será usado para entregar o trabalho nesta participação. Quando um projeto é mapeado para uma linha de cotação, isso ajuda a configurar tarefas cobráveis e também a gerar uma estimativa baseada em projeto para a linha de cotação como detalhes da linha de cotação. Quando um projeto não é mapeado para uma linha de cotação baseada em projeto, a estimativa deve ser criada manualmente criando cada detalhe da linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Incluir Hora | Um sinalizador **Sim**/**Não** indica se as transações de tempo ou custo de mão de obra no projeto selecionado serão incluídos na estimativa nesta linha de cotação. Um valor **Não** indica que as transações de tempo ou custo de mão de obra não serão incluídos na estimativa nesta linha de cotação. Um valor **Sim** indica que as transações de tempo ou custo de mão de obra serão incluídos na estimativa nesta linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Incluir Despesa | Um sinalizador **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de cotação. Um valor **Não** indica que as despesas de custo não serão incluídas na estimativa nesta linha de cotação. Um valor **Sim** indica que as despesas de custo serão incluídas na estimativa nesta linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Incluir Taxa | Um sinalizador **Sim**/**Não** indica se os valores no projeto selecionado serão incluídos na estimativa nesta linha de cotação. Um valor **Não** indica que os valores não serão incluídos na estimativa nesta linha de cotação. Um valor **Sim** indica que os valores serão incluídos na estimativa nesta linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Valor da Cotação | Este é o valor que será cotado ao cliente para todo o trabalho previsto nesta linha de cotação baseada em projeto. Em uma cotação criada a partir de uma oportunidade, este valor é copiado do campo **Orçamento do cliente** na linha da oportunidade. Quando a linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor nos detalhes da linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Imposto Estimado | Este é um campo editável para o usuário adicionar o valor estimado do imposto na linha de cotação. Quando uma linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor do imposto nos detalhes da linha de cotação. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Valor Cotado Após Imposto | Este campo é o valor da linha de cotação após o imposto e é somente leitura. O valor neste campo é calculado como *Valor cotado + imposto*. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Limite de NTE (limite máximo) | Este campo é editável e está disponível apenas em linhas de cotação baseadas em projeto que tenham o método de cobrança **Tempo e material**. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |
| Orçamento do Cliente | Se a cotação tiver sido criada a partir de uma Oportunidade, este campo é editável e copiado a partir do campo correspondente na oportunidade. | O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regras de validação para os campos na guia Geral de linhas de cotação baseadas em projeto

**Regra 1** : uma determinada classe de transação no projeto selecionado só pode ser incluída em uma linha de cotação baseada em projeto de uma cotação.

**Regra 2** : se uma oportunidade tiver várias cotações, pode haver linhas de cotação de cotações diferentes que façam referência ao mesmo projeto e incluam a mesma classe de transação.

**Regra 3** : se as cotações não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transação.

<table border="1" cellspacing="0" cellpadding="0">
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
            <td width="48" valign="top">
                <p>
                    <strong>Incluir hora</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Incluir despesa</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Incluir</strong>
                </p>
                <p>
                    <strong>valor</strong>
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
Violação da regra nº1. Tempo, despesa e valores no projeto P1 estão incluídos em ambas as linhas de cotação, QL1 e QL2.
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
Violação da regra nº1. Tempo e valores no projeto P1 estão incluídos em ambas as linhas de cotação, QL1 e QL2.
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
Não há sobreposição no que está sendo incluído em cada linha de cotação, portanto, é válido.
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
Violação da regra nº1 acima </p>
                <p>
Q1 inclui Tempo, despesas e valores para todo o projeto P1.
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
Com base na regra nº2, Q1 e Q2 são duas cotações na mesma oportunidade, então ambos podem estimar para os mesmos componentes de um projeto.
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
QL1 em Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
Com base na regra nº3, Q1 e Q2 são duas cotações em oportunidades diferentes, então não podem estimar para os mesmos componentes do mesmo projeto.
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

