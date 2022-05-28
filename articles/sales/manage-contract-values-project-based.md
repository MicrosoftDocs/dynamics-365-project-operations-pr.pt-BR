---
title: Trabalhar com linhas de contrato baseadas em projeto
description: Este tópico fornece informações sobre linhas de contrato baseadas em projeto.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f67c0447c0b2a23d6f7d03dfc5ac7800943bbf36
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595162"
---
# <a name="work-with-projectbased-contract-lines"></a>Trabalhar com linhas de contrato baseadas em projeto

Linhas de contrato baseadas em projeto no Dynamics 365 Project Operations são projetadas para conter a estimativa e os contratos de cobrança para componentes específicos do trabalho do projeto em uma participação. A estrutura de uma linha de contrato baseada em projeto é estendida para estimativas de projeto e cenários de cobrança com os seguintes conceitos:

- Método de cobrança
- Mapeamento de projeto e tarefa
- Classes de transação incluídas
- Limite máximo
- Configuração dos encargos
- Estimativas usando detalhes da linha de contrato
- Clientes da linha de contrato

Os campos a seguir estão incluídos na guia **Geral** de linhas de contrato baseadas em projeto. Esses campos ajudam a configurar a base para uma estimativa detalhada e básica e as disposições de cobrança para o trabalho baseado em projeto.

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| **Nome** | O nome da linha do contrato que identifica o componente discreto do contrato que está sendo estimado. Para um contrato de projeto criado a partir de uma cotação, este valor é copiado de um valor correspondente da linha de cotação baseada em projeto. | O valor deste campo é copiado na linha da fatura do projeto que é criada a partir dessa linha do contrato quando a fatura é criada. |
| **Método de Cobrança** | Em um contrato de projeto criado a partir de uma cotação, este valor é copiado do campo correspondente na linha de cotação. Este é um conjunto de opções que representa os dois principais modelos de contratação com suporte do Project Operations:</br>- **Preço Fixo**</br>- **Hora e Material** | Com base no método de cobrança da linha de contrato referenciada, a transação real será processada. Se a linha do contrato referenciada pelo dado real tiver um método de cobrança por hora e material, um custo e um registro real de vendas não cobradas serão criados. Se a linha do contrato referenciada pelo real tiver um método de cobrança de preço fixo, apenas um dado real de custo será criado. |
| **Project** | Use este campo para identificar o projeto que será usado para entregar o trabalho nesta participação. | O valor neste campo é usado em conjunto com os campos **Tarefas Incluídas** e **Classes de Transação Incluídas** para resolver a referência da linha do contrato em um dado real ou em um registro de linha de estimativa. |
| **Incluir Hora** | Um sinalizador indica se as transações de hora ou custos de mão de obra no projeto selecionado estão incluídos nesta linha de contrato. Um valor **Não** indica que as transações de hora ou custos de mão de obra não serão incluídos nesta linha de contrato. Um valor **Sim** indica que serão incluídas. | Este valor de campo é usado em conjunto com o projeto para resolver a referência da linha do contrato em um dado real ou registro de linha de estimativa. |
| **Incluir Despesa** | Um sinalizador indica se custos de despesas no projeto selecionado serão incluídos nesta linha de contrato. Um valor **Não** indica que o custo de despesas não será incluído nesta linha de contrato. Um valor **Sim** indica que ele será incluído. | Este valor de campo é usado em conjunto com o projeto para resolver a referência da linha do contrato em um dado real ou registro de linha de estimativa. |
| **Incluir Taxa** | Um sinalizador indica se valores no projeto selecionado serão incluídos nesta linha de contrato. Um valor **Não** indica que os valores não serão incluídos nesta linha de contrato. Um valor **Sim** indica que serão incluídas. | Este valor de campo é usado em conjunto com o projeto para resolver a referência da linha do contrato em um dado real ou registro de linha de estimativa. |
| **Valor Contratado** | Em uma linha de contrato de preço fixo, este é o valor acordado que será faturado ao cliente por todos os componentes de trabalho associados a esta linha de contrato. Em uma linha de contrato de horas e materiais, este é um valor estimado do que será faturado ao cliente para todos os componentes de trabalho associados a esta linha de contrato. Em um contrato de projeto que é criado a partir de uma cotação, este valor é copiado do campo correspondente na linha de cotação. Quando uma linha de contrato baseada em projeto tem detalhes de linha, este campo é bloqueado para edição e é resumido a partir do valor nos detalhes da linha de contrato. | Quando a linha do contrato tem detalhes da linha, este valor pode ser modificado alterando os valores nos detalhes da linha. Em uma linha de contrato de preço fixo, esse valor é usado para gerar o valor antes do imposto em etapas de cobrança periódica. |
| **Imposto Estimado** | O usuário pode editar este campo para inserir o valor estimado do imposto na linha do contrato. Quando uma linha de contrato baseada em projeto tem detalhes de linha, este campo é bloqueado para edição e é resumido a partir do valor do imposto nos detalhes da linha de contrato. | Quando a linha do contrato tem detalhes da linha, este valor pode ser modificado alterando os valores do imposto nos detalhes da linha. Em uma linha de contrato de preço fixo, esse valor é usado para gerar impostos sobre etapas de cobrança periódica. |
| **Valor Contratado após Imposto** | O valor da linha do contrato após Imposto. Este campo é somente leitura e é calculado como **Valor Contratado + Imposto**. | Em uma linha de contrato de preço fixo, esse valor é usado para gerar etapas de cobrança periódica. |
| **Limite de NTE (limite máximo)** | O usuário pode editar este campo e ele está disponível apenas em linhas de contrato baseadas em projeto que têm um método de cobrança de horas e materiais. | O usuário pode editar este campo. Quando um dado real de hora ou despesa referencia esta linha do contrato para horas e materiais, o valor no dado real é avaliado em relação ao limite máximo nesta linha do contrato após a contabilidade dos valores já gastos e comprometidos. |
| **Orçamento do Cliente** | Este campo é editável e será copiado do campo correspondente na linha de cotação se o contrato tiver sido criado a partir de uma cotação. | Este campo é usado apenas para informações e não tem significado posterior. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regra de validação para as opções na guia Geral de linhas de contrato baseada em projeto

Regra: um projeto e certa classe de transação só podem ser incluídos em uma linha de contrato baseada em projeto em um contrato.

| Contrato | Linha de contrato | Project | Incluir hora | Incluir despesa | Incluir valor | Válido/não válido | Motivo                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Sim          | Sim             | Sim         | Não é válido       | Viola a regra. Hora, despesas e valores no projeto P1 estão incluídos em ambas as linhas de contrato, CL1 e CL2.                                                                                       |
| C1       | CL2           | P1      | Sim          | Sim             | Sim         | Não é válido       | Viola a regra. Hora, despesas e valores no projeto P1 estão incluídos em ambas as linhas de contrato, CL1 e CL2.                                                                                       |
| C1       | CL1           | P1      | Sim          | No              | Sim         | Não é válido       | Viola a regra. Hora e valores no projeto P1 estão incluídos em ambas as linhas de contrato, CL1 e CL2.                                                                                                   |
| C1       | CL2           | P1      | Sim          | Sim             | Sim         | Não é válido       | Viola a regra. Hora e valores no projeto P1 estão incluídos em ambas as linhas de contrato, CL1 e CL2.                                                                                                   |
| C1       | CL1           | P1      | Sim          | No              | Sim         | Válido           | O tempo e os valores no projeto P1 são incluídos no CL1. A despesa do projeto P1 está incluída no CL2. </br>   Não há sobreposição no que está sendo incluído em cada linha do contrato e que, portanto, é válido.  |
| C1       | CL2           | P1      | No           | Sim             | No          | Válido           | O tempo e os valores no projeto P1 são incluídos no CL1. A despesa do projeto P1 está incluída no CL2. </br>   Não há sobreposição no que está sendo incluído em cada linha do contrato e que, portanto, é válido.  |
| C1       | CL1           | P1      | Sim          | Sim             | Sim         | Não é válido       | Viola a regra. Hora, despesas e valores no projeto P1 estão incluídos nas linhas de dois contratos.                                                                                               |
| CL2      | CL2           | P1      | Sim          | Sim             | Sim         | Não é válido       | Viola a regra. Hora, despesas e valores no projeto P1 estão incluídos nas linhas de dois contratos.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]