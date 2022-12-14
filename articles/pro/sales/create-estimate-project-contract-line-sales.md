---
title: Estimar uma linha de contrato do projeto
description: Este artigo fornece informações sobre como estimar uma linha de contrato baseada em projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 86872aa58067f55243fa19dc865971f76660f594
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824753"
---
# <a name="estimate-a-project-contract-line"></a>Estimar uma linha de contrato do projeto

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

No Dynamics 365 Project Operations, uma linha de contrato do projeto tem detalhes que ajudam a estimar o custo e a receita potencial do trabalho envolvido para fornecer a linha de contrato.

Para estimar uma linha de contrato do projeto, vá para a guia **Detalhe da Linha de Contrato** na **Linha de Contrato** baseada no projeto.  Existem duas maneiras de criar uma estimativa em uma linha de contrato baseada em projeto:

   - Crie uma estimativa diretamente na linha do contrato, adicionando manualmente os detalhes da linha do contrato.
   - Crie um projeto e um plano de projeto e, em seguida, associe o projeto e as tarefas à linha de contrato do projeto. Isso permite o processo pelo qual você pode importar a estimativa do plano do projeto para a linha do contrato baseada nos componentes incluídos na linha do contrato.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Criar uma estimativa diretamente em uma linha de contrato baseada em projeto

Para criar uma estimativa diretamente em uma linha de contrato do projeto, siga estas etapas:

1. Vá para a linha do contrato e selecione a guia **Detalhe da Linha de Contrato**. As linhas que você cria nesta guia são resumidas e exibidas como o **Valor Contratado** por esta **Linha de Contrato**. 
2. Na subgrade **Detalhes da Linha do Contrato**, selecione **+ Novo Detalhe de Linha de Contrato**. Um controle deslizante de criação rápida é aberto. Os seguintes campos estão disponíveis na página **Detalhes da Linha de Contrato**.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **Descrição** | **Criação Rápida** | Uma descrição da estimativa específica. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Classe da Transação** | **Criação Rápida** | Esta é uma lista de classes de transação incluídas na guia **Geral** da linha de contrato baseada em projeto. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Selecionar Produto** | **Criação rápida** | Aplica-se quando a classe de transação é **Material**. É possível especificar se esta linha de estimativa é para um produto **Existente** (catálogo) ou um produto **Fora do Catálogo**. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Produto** | **Criação rápida** | O ID do produto do catálogo de produtos. Esse campo só estará ativado quando você selecionar **Produto existente** no campo **Selecionar Produto**. A ID é usada para recuperar o preço de venda da lista de preços do projeto no contrato. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Produto Fora do Catálogo** | **Criação rápida** | Um campo de texto para informar o nome do produto. Esse campo só estará ativado quando você selecionar **Fora do Catálogo** no campo **Selecionar Produto**.| Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Função** | **Criação Rápida** | A função da pessoa que está realizando este trabalho ou incorrendo nessa despesa. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente.|
| **Categoria** | **Criação Rápida** | A categoria do trabalho ou da despesa. |Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente.|
| **Data de Início** | **Criação Rápida** | A data de início do trabalho. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Data de Término** | **Criação Rápida** | A data de término do trabalho. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Unidade de Recursos** | **Criação Rápida** | A unidade de recursos que irá incorrer neste custo e fornecer o recurso para trabalhar nisso. |Este valor é padronizado para o detalhe da linha de contrato relacionado para o custo que é criado automaticamente e usado na recuperação do preço de custo. |
| **Agenda da unidade** | **Criação rápida** | O grupo de unidades de trabalho, produto ou despesa. As unidades pertencem a uma agenda da unidade ou a um grupo de unidades. Por exemplo, *milhas* e *quilômetros (kms)* são unidades que pertencem a um grupo de unidades que descrevem distâncias. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Unidade** | **Criação Rápida** | A unidade de trabalho, produto ou despesa. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Quantidade** | **Criação Rápida** | A quantidade de trabalho, produto ou despesa. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Preço unitário** | **Criação Rápida** | A taxa de faturamento da função que está executando o trabalho, o preço unitário do produto, ou o preço de venda do produto ou a categoria de despesa. Este campo é padronizado para **Tempo** com base na combinação de valores de dimensão de preço na linha de preço da função da lista de preços do projeto que está em vigor para a data de início. Para **Despesas**, o padrão deste campo é da configuração de preço para a categoria de transação na lista de preços do projeto que é efetiva para a data de início. Se o método de precificação da categoria de transação não for **preço por unidade**, não haverá padrão e este campo ficará em branco. Para produtos, o padrão deste campo é baseado na linha **Item da lista de preços** na lista de preços do projeto que está em vigor para a data de início.| A taxa de custo da função que está executando o trabalho ou o custo por unidade da categoria de despesas ou o custo unitário do produto. Este campo é padronizado para **Tempo** com base na combinação de valores de dimensão de preço na linha de preço da função da lista de preços de custo anexada à unidade de contratação efetiva para a data de início. Para despesas, o padrão deste campo é baseado na linha de preço da categoria da lista de preços de custo anexada à unidade de contratação efetiva para a data de início. Se o método de precificação da categoria de transação não for preço por unidade não haverá padrão e este campo ficará em branco. Para produtos, este padrão do campo é baseado na linha do **Item da lista de preços** da lista de preços de custo anexada à unidade de contratação que é efetiva para a data de início.|
| **Imposto Estimado** | **Criação Rápida** | O imposto estimado para este trabalho ou despesa. | O imposto estimado para este trabalho ou despesa. |
| **Valor** | **Criação Rápida** | Você pode adicionar o valor neste campo se os campos **Quantidade** e **Preço** ficarem em branco. Se **Quantidade** e **Preço** forem preenchidos, o campo **Valor** será somente para leitura e será calculado como **(Quantidade\*Preço unitário) + Imposto**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Atualizar os preços nos detalhes da linha do contrato

Se você alterar os preços na lista de preços do projeto anexada ao contrato ou na lista de preços de custo da unidade de contratação, poderá atualizar os preços nos detalhes da linha do contrato individual para refletir a mudança. Na página **Contrato**, selecione **Recalcular**. Um aviso aparece para informá-lo de que os preços de todas as linhas do contrato neste contrato foram redefinidos. Selecione **Sim** para atualizar os preços dos detalhes da linha do contrato de vendas e custo.

## <a name="access-contract-line-details-for-cost"></a>Acesse os detalhes da linha do contrato para custo

Na guia **Detalhes da Linha do Contrato**, selecione uma linha na grade para exibir ações na barra de ferramentas da subgrade. A primeira ação na barra de ferramentas da subgrade é **Detalhe de Custo Aberto**. Para ver a taxa de custo relacionada e o valor para este detalhe da linha de contrato, selecione **Abrir Detalhes do Custo**. 

> [!NOTE]
> Alterar a empresa de recursos, unidade de recursos, quantidade, datas, função ou valores de categoria no detalhe da linha do contrato para **Custo** também altera os valores correspondentes no detalhe da linha do contrato para **Vendas**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moeda nos detalhes da linha do contrato para custos e vendas

O detalhe da linha do contrato para **Vendas** define a moeda padrão da lista de preços do projeto efetiva na data de início do detalhe da linha do contrato.

O detalhe da linha do contrato para **Custo** define a moeda padrão da lista de preços da unidade de contratação do contrato efetiva para a data de início do detalhe da linha do contrato para **Custo**.

Os cálculos de lucratividade convertem os valores dos detalhes da linha do contrato para **Custo** e **Vendas** na moeda base do ambiente para relatar as margens reais e estimadas gerais do contrato.

> [!NOTE]
> Erros de arredondamento de moeda e margens alteradas podem ocorrer devido à falta de taxas de câmbio efetivas de data. Use esses cálculos apenas nos contratos do projeto, pois são aproximações e não são estatutários reais ou outros relatórios que exigem maior precisão de arredondamento e consciência da data efetiva para as taxas de câmbio.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
