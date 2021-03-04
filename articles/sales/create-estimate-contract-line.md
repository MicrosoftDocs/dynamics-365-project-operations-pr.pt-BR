---
title: Estimar uma linha de contrato baseada em projeto
description: Este tópico fornece informações sobre como fazer uma estimativa de uma linha de contrato baseada no projeto.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180448"
---
# <a name="estimate-a-projectbased-contract-line"></a>Estimar uma linha de contrato baseada em projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_ 

No Dynamics 365 Project Operations, uma linha de contrato baseada em projeto tem detalhes que ajudam a estimar o custo e a receita potencial do trabalho envolvido para fornecer a linha de contrato.

Para estimar uma linha de contrato baseada no projeto, vá para a guia **Detalhe da Linha de Contrato** na **Linha de Contrato** baseada no projeto.  Existem duas maneiras de criar uma estimativa em uma linha de contrato baseada em projeto:

   - Crie uma estimativa diretamente na linha do contrato, adicionando manualmente os detalhes da linha do contrato.
   - Crie um projeto e um plano de projeto e, em seguida, associe o projeto e as tarefas à linha de contrato do projeto. Isso permite o processo pelo qual você pode importar a estimativa do plano do projeto para a linha do contrato baseada nos componentes incluídos na linha do contrato.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Criar uma estimativa diretamente em uma linha de contrato baseada em projeto

1. Vá para a linha do contrato e selecione a guia **Detalhe da Linha de Contrato**. As linhas que você cria nesta guia são resumidas e exibidas como o **Valor Contratado** por esta **Linha de Contrato**. 
2. Na subgrade **Detalhes da Linha do Contrato**, selecione **+ Novo Detalhe de Linha de Contrato**. Um controle deslizante de criação rápida é aberto. Os seguintes campos estão disponíveis no formulário **Detalhes da Linha de Contrato**:

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **Descrição** | **Criação Rápida** | Uma descrição da estimativa específica. | Este campo assume como padrão o detalhe da linha do contrato relacionado para custos que são criados automaticamente. |
| **Classe da Transação** | **Criação Rápida** | Esta lista suspensa é uma lista de classes de transação incluídas na guia **Geral** da linha de contrato baseado em projeto. | Este campo assume como padrão o detalhe da linha do contrato relacionado para custos que são criados automaticamente. |
| **Função** | **Criação Rápida** | A função da pessoa que está realizando este trabalho ou incorrendo nessa despesa. | Este campo assume como padrão o detalhe da linha do contrato relacionado para custos que são criados automaticamente. |
| **Categoria** | **Criação Rápida** | A categoria do trabalho ou da despesa. | Este campo assume como padrão o detalhe da linha do contrato relacionado para custos que são criados automaticamente. |
| **Data de Início** | **Criação Rápida** | A data de início do trabalho. | Este campo assume como padrão o detalhe da linha do contrato relacionado para custos que são criados automaticamente. |
| **Data de Término** | **Criação Rápida** | A data de término do trabalho. | Este campo assume como padrão o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Empresa de Recursos** | **Criação Rápida** | A empresa de recursos ou entidade legal que está incorrendo neste custo e fornecendo o recurso para trabalhar nisso. | Este campo assume como padrão o detalhe da linha do contrato relacionado para custos que são criados automaticamente. Este campo também é usado na recuperação do preço de custo. |
| **Unidade de Recursos** | **Criação Rápida** | A unidade de recursos que incorre nesse custo e fornece o recurso para trabalhar nisso. | Este campo assume como padrão o detalhe da linha do contrato relacionado para custos que são criados automaticamente. Este campo também é usado na recuperação do preço de custo. |
| **Agenda da unidade** | **Criação rápida** | O grupo de unidades do trabalho ou da despesa. As unidades pertencem a uma agenda da unidade ou a um grupo de unidades. Por exemplo, *milhas* e *quilômetros (Kms)* são unidades que pertencem a um grupo de unidades que descrevem distâncias. | Este campo assume como padrão o detalhe da linha do contrato relacionado para custos que são criados automaticamente. |
| **Unidade** | **Criação Rápida** | A unidade do trabalho ou da despesa. | Este campo assume como padrão o detalhe da linha do contrato relacionado para custos que são criados automaticamente. |
| **Quantidade** | **Criação Rápida** | A quantidade de trabalho ou da despesa. | Este campo assume como padrão o detalhe da linha do contrato relacionado para custos que são criados automaticamente. |
| **Preço unitário** | **Criação Rápida** | A taxa de cobrança da função que está realizando o trabalho ou o preço de venda da categoria de despesas. Este campo é padronizado para **Hora** baseado na combinação de função e unidade de recursos na lista de preços do projeto efetiva para a data de início. Para despesas, o padrão deste campo é da configuração de preço para a categoria de transação na lista de preços do projeto que é efetiva para a data de início. Se o método de precificação da categoria de transação não for **preço por unidade**, não haverá padrão e este campo ficará em branco. | A taxa de custo da função que está realizando o trabalho ou o custa por unidade da categoria de despesas. Este campo é padronizado para **Tempo com base na função** e a combinação da unidade de recurso na linha de preço da função da lista de preços de custo anexada à unidade de contratação efetiva para a data de início. Para despesas, o padrão deste campo é baseado na linha de preço da categoria da lista de preços de custo anexada à unidade de contratação efetiva para a data de início. Se o método de precificação da categoria de transação não for preço por unidade não haverá padrão e este campo ficará em branco. |
| **Imposto Estimado** | **Criação Rápida** | O imposto estimado para este trabalho ou despesa, conforme inserido pelo usuário. | O imposto estimado para este trabalho ou despesa, conforme inserido pelo usuário. |
| **Valor** | **Criação Rápida** | Este valor neste campo pode ser adicionado pelo usuário se os campos **Quantidade** e **Preço** ficarem em branco. Se **Quantidade** e **Preço** forem preenchidos, o campo **Valor** será somente para leitura e será calculado como **(Quantidade \* Preço unitário) + Imposto**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Atualizar os preços nos detalhes da linha do contrato

Se você alterar os preços na lista de preços do projeto anexada ao contrato ou na lista de preços de custo da unidade de contratação, poderá atualizar os preços nos detalhes da linha do contrato individual para refletir a mudança. Na página **Contrato**, selecione **Recalcular**. Um aviso é aberto para informá-lo de que os preços de todas as linhas do contrato neste contrato foram redefinidos. Selecione **Sim** para atualizar os preços dos detalhes da linha do contrato de vendas e custo.

## <a name="access-contract-line-details-for-cost"></a>Acesse os detalhes da linha do contrato para custo

Na guia **Detalhes da Linha do Contrato**, selecione uma linha na grade para exibir ações na barra de ferramentas da subgrade. A primeira ação na barra de ferramentas da subgrade é **Detalhe de Custo Aberto**. Para ver a taxa de custo relacionada e o valor para este detalhe da linha de contrato, selecione **Abrir Detalhes do Custo**. 

> [!NOTE]
> Alterar a empresa de recursos, unidade de recursos, quantidade, datas, função ou valores de categoria no detalhe da linha do contrato para **Custo** também altera os valores correspondentes no detalhe da linha do contrato para **Vendas**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moeda nos detalhes da linha do contrato para custos e vendas

O detalhe da linha do contrato para **Vendas** define a moeda padrão da lista de preços do projeto efetiva na data de início do detalhe da linha do contrato.

O detalhe da linha do contrato para **Custo** define a moeda padrão da lista de preços da unidade de contratação do contrato efetiva para a data de início do detalhe da linha do contrato para **Custo**.

Os cálculos de lucratividade convertem os valores dos detalhes da linha do contrato para **Custo** e **Vendas** na moeda base do ambiente para relatar as margens reais e estimadas gerais do contrato.

> [!NOTE]
> Erros de arredondamento de moeda e margens alteradas podem ocorrer devido à falta de taxas de câmbio efetivas de data. Use esses cálculos em contratos de projeto apenas como aproximações e não para relatórios estatutários reais ou outros relatórios que requeiram maior precisão de arredondamento e consciência da validade de data para taxas de câmbio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]