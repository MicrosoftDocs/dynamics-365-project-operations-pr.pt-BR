---
title: Visão geral de linhas de contrato baseadas em projeto
description: Este tópico fornece informações sobre como trabalhar com linhas de contrato baseadas em projeto.
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 436079a166b102590863c5df6734d21dd83b83fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593138"
---
# <a name="project-based-contract-lines-overview"></a>Visão geral de linhas de contrato baseadas em projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Linhas de contrato baseadas em projeto no Dynamics 365 Project Operations são projetadas para conter a estimativa e os contratos de cobrança para componentes específicos do trabalho do projeto em uma participação. A estrutura de uma linha de contrato baseada em projeto é estendida para estimativas de projeto e cenários de cobrança com os seguintes conceitos:

- Método de cobrança
- Mapeamento de projeto e tarefa
- Classes de transação incluídas
- Limite máximo
- Configuração dos encargos
- Estimativas usando detalhes da linha de contrato
- Clientes da linha de contrato

A tabela a seguir inclui os campos na guia **Geral** de linhas de contrato baseadas em projeto que ajudam a configurar a base para uma estimativa detalhada básica e disposições de cobrança para o trabalho baseado em projeto.

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| **Nome** | Nome da linha do contrato. Isso identifica o componente discreto do contrato que está sendo estimado. Para um contrato de projeto criado a partir de uma cotação, este valor é copiado de um valor correspondente da linha de cotação baseada em projeto. | O nome copiado na linha da fatura do projeto que é criada a partir dessa linha do contrato quando a fatura é criada. |
| **Método de Cobrança** | Em um contrato de projeto criado a partir de uma cotação, este valor é copiado do campo correspondente na linha de cotação. Este é um conjunto de opções que representa os dois principais modelos de contratação com suporte do Project Operations:</br>- **Preço Fixo**</br>- **Hora e Material** | Com base no método de cobrança da linha de contrato referenciada, a transação real será processada. Se a linha do contrato referenciada pelo dado real tiver um método de cobrança por hora e material, serão criados registros de custos e dado real de vendas não cobradas. Se a linha do contrato referenciada pelo real tiver um método de cobrança de preço fixo, apenas um dado real de custo será criado. |
| **Project** | Use este campo para identificar o projeto que será usado para entregar o trabalho nesta participação. | Este valor será usado junto com **Tarefas Incluídas** e **Classes de Transação Incluídas** para resolver a referência da linha do contrato em um registro de linha real ou estimado. |
| **Tarefas Incluídas** | Indica se esta linha de contrato inclui todas as tarefas do projeto para o projeto selecionado ou apenas um subconjunto das tarefas. Este é um conjunto de opções que tem os seguintes valores possíveis:</br>- **Todas as Tarefas do Projeto**</br>- **Tarefas do Projeto Selecionadas Somente**. Um valor em branco neste campo equivale a selecionar **Todas as Tarefas do Projeto**. | Se **Tarefas Selecionadas Somente** for selecionado, você poderá selecionar tarefas específicas e associá-las a esta linha de contrato na guia **Configuração de Cobrança da Tarefa** na página **Projeto**. O valor será usado em conjunto com as classes **Projeto** e **Transação Incluída** para resolver a referência da linha do contrato em um dado real ou em um registro de linha de estimativa. |
| **Incluir Hora** | Um valor **Sim**/**Não** indica se as transações de tempo ou custos de mão de obra no projeto selecionado serão incluídas nesta linha de contrato. Um valor **Não** indica que as transações de hora ou custo de mão de obra não serão incluídas nesta linha de contrato. Um valor **Sim** indica que serão incluídas. | Este valor é usado junto com o projeto para resolver a referência da linha do contrato em um registro real ou de linha de estimativa. |
| **Incluir Despesa** | Um valor **Sim**/**Não** indica se custos de despesa no projeto selecionado serão incluídos nesta linha de contrato. Um valor **Não** indica que o custo de despesas não será incluído nesta linha de contrato. Um valor **Sim** indica que ele será incluído. | Este valor é usado junto com o projeto para resolver a referência da linha do contrato em um registro real ou de linha de estimativa. |
| **Incluir Materiais** | Um valor **Sim**/**Não** indica se custos de material no projeto selecionado serão incluídos nesta linha de contrato. Um valor **Não** indica se os custos de material não serão incluídos nesta linha de contrato. Um valor **Sim** indica que ele será incluído. | Este valor é usado junto com o projeto para resolver a referência da linha do contrato em um registro real ou de linha de estimativa. |
| **Incluir Taxa** | Um valor **Sim**/**Não** indica se valores no projeto selecionado serão incluídos nesta linha de contrato. Um valor **Não** indica que os valores não serão incluídos nesta linha de contrato. Um valor **Sim** indica que serão incluídas. | Este valor é usado junto com o projeto para resolver a referência da linha do contrato em um registro real ou de linha de estimativa. |
| **Valor Contratado** | Em uma linha de contrato de preço fixo, este é o valor acordado que será faturado ao cliente para todos os componentes de trabalho associados a esta linha de contrato. Em uma linha de contrato de horas e materiais, este é um valor estimado do que será faturado ao cliente para todos os componentes de trabalho associados a esta linha de contrato. Em um contrato de projeto que é criado a partir de uma cotação, este valor é copiado do campo correspondente na linha de cotação. Quando uma linha de contrato baseada em projeto tem detalhes de linha, este campo é bloqueado para edição e é resumido a partir do valor nos detalhes da linha de contrato. | Quando a linha do contrato tem detalhes da linha, este valor pode ser modificado alterando os valores nos detalhes da linha. Em uma linha de contrato de preço fixo, esse valor é usado para gerar o valor antes do imposto em etapas de cobrança periódica. |
| **Imposto Estimado** | O usuário pode editar este campo para inserir o valor estimado do imposto na linha do contrato. Quando uma linha de contrato baseada em projeto tem detalhes de linha, este campo é bloqueado para edição e é resumido a partir do valor do imposto nos detalhes da linha de contrato. | Quando a linha do contrato tem detalhes da linha, este valor pode ser modificado alterando os valores do imposto nos detalhes da linha. Em uma linha de contrato de preço fixo, esse valor é usado para gerar os impostos sobre etapas de cobrança periódica. |
| **Valor Contratado após Imposto** | O valor da linha do contrato após Imposto. Este campo é somente leitura e é calculado como **Valor Contratado + Imposto**. | Em uma linha de contrato de preço fixo, esse valor é usado para gerar etapas de cobrança periódica. |
| **Limite de NTE (limite máximo)** | O usuário pode editar este campo e ele está disponível apenas em linhas de contrato baseadas em projeto que têm um método de cobrança definido como horas e materiais. | O usuário pode editar este campo. Quando um dado real de horas e materiais referencia esta linha do contrato para horas e materiais, o valor no dado real é avaliado em relação ao limite máximo na linha do contrato. Essa avaliação é concluída após a contabilização dos valores já gastos e comprometidos. |
| **Orçamento do Cliente** | Este campo é editável e será copiado do campo correspondente na linha de cotação se o contrato tiver sido criado a partir de uma cotação. | Este campo é usado apenas para informações e não tem significado posterior. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regras de validação para as opções na guia Geral de linhas de contrato baseadas em projeto

Regra 1: se o campo **Tarefas Incluídas** estiver em branco ou definido como **Todas as Tarefas do Projeto**, todas as tarefas do projeto serão incluídas na linha do contrato.

Regra 2: quando o campo **Tarefas Incluídas** estiver em branco ou explicitamente definido como **Todas as Tarefas do Projeto**, um projeto e uma certa classe de transação só poderão ser incluídos em uma linha de contrato baseada em projeto de um contrato.

Regra 3: quando o campo **Tarefas Incluídas** estiver definido como **Tarefas do Projeto Selecionadas Somente**, um projeto e uma certa classe de transação poderão ser incluídos em várias linhas de contrato baseadas em projeto de um contrato.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Contrato</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Linha de contrato</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
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
                    <strong>Incluir Materiais</strong>
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
            <td width="53" valign="top">
                <p>
                    <strong>Válido/ Não inválido</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Razão</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violação da regra Nº 2. Tempo, Despesas, Materiais e Valores no projeto P1 estão incluídos nas linhas de contrato CL1 e CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violação da regra Nº 2. Tempo, Materiais e Valores no projeto P1 estão incluídos nas linhas de contrato CL1 e CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Tempo, Materiais e Valores no projeto P1 estão incluídos no CL1.
                </p>
                <ul>
                    <li>
A despesa do projeto P1 está incluída no CL2.
                    </li>
                </ul>
                <p>
Nenhuma sobreposição no que está sendo incluído em cada linha do contrato e, portanto, ele é válido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violação da regra Nº 2 </p>
                <p>
C1 inclui Tempo, Materiais, Despesas e Valores em um subconjunto de tarefas no projeto P1.
                </p>
                <p>
CL2 inclui Tempo, Materiais, Despesas e Valores para todo o projeto P1 e, portanto, se sobrepõe ao que está incluído em C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Por regra nº 3 </p>
                <p>
C1 inclui Tempo, Despesas, Materiais e Valores em um subconjunto de tarefas no projeto P1.
                </p>
                <p>
CL2 inclui Tempo, Despesas, Materiais e Valores para um subconjunto de tarefas no projeto P1.
                </p>
                <p>
A única validação adicional é que o subconjunto de tarefas no CL1 é diferente do subconjunto de tarefas no CL2 para garantir que não haja sobreposições. Isso é feito pelo sistema quando as tarefas são associadas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
