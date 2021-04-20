---
title: Estimar uma linha de contrato do projeto
description: Este tópico fornece informações sobre estimativas em uma linha de contrato do projeto.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7cb7d7eccf62837ee5abf4cbe29a21dc728eb7ef
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858504"
---
# <a name="estimate-a-project-contract-line"></a>Estimar uma linha de contrato do projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_ 

No Dynamics 365 Project Operations, uma linha de contrato baseada em projeto tem detalhes que ajudam a estimar o custo e a receita potencial do trabalho envolvido para fornecer a linha de contrato.

Para estimar uma linha de contrato baseada no projeto, vá para a guia **Detalhe da Linha de Contrato** na **Linha de Contrato** baseada no projeto.  Existem duas maneiras de criar uma estimativa em uma linha de contrato baseada em projeto:

   - Crie uma estimativa diretamente na linha do contrato, adicionando manualmente os detalhes da linha do contrato.
   - Crie um projeto e um plano de projeto e, em seguida, associe o projeto e as tarefas à linha de contrato do projeto. Isso permite o processo pelo qual você pode importar a estimativa do plano do projeto para a linha do contrato baseada nos componentes incluídos na linha do contrato.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Criar uma estimativa diretamente em uma linha de contrato do projeto

Para criar uma estimativa diretamente em uma linha de contrato do projeto, siga estas etapas:

1. Vá para a linha do contrato e selecione a guia **Detalhe da Linha de Contrato**. As linhas que você cria nesta guia são resumidas e exibidas como o **Valor Contratado** por esta **Linha de Contrato**. 
2. Na subgrade **Detalhes da Linha do Contrato**, selecione **+ Novo Detalhe de Linha de Contrato**. Um controle deslizante de criação rápida é aberto. Os seguintes campos estão disponíveis na página **Detalhes da Linha de Contrato**.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **Descrição** | **Criação Rápida** | Uma descrição da estimativa específica. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Classe da Transação** | **Criação Rápida** | Esta lista de classes de transação é incluída na guia **Geral** da linha de contrato baseada em projeto. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Selecionar Produto** | **Criação rápida** | Aplica-se quando a classe de transação é **Material**. É possível optar por especificar se esta linha de estimativa é para um produto **Existente** (catálogo) ou um produto **Fora do Catálogo**. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Produto** | **Criação rápida** | A ID do produto do catálogo de produtos. Esse campo só estará ativado quando você selecionar **Produto existente** no campo **Selecionar Produto**. A ID é usada para recuperar o preço de venda da lista de preços do projeto no contrato. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Produto Fora do Catálogo** | **Criação rápida** | Um campo de texto para informar o nome do produto. Esse campo só estará ativado quando você selecionar **Fora do Catálogo** no campo **Selecionar Produto**.| Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Função** | **Criação Rápida** | A função da pessoa que está realizando este trabalho ou incorrendo nessa despesa. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente.|
| **Categoria** | **Criação Rápida** | A categoria do trabalho ou da despesa. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente.|
| **Data de Início** | **Criação Rápida** | A data de início do trabalho. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Data de Término** | **Criação Rápida** | A data de término do trabalho. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Empresa de Recursos** | **Criação Rápida** | A empresa de recursos ou entidade legal irá incorrer neste custo e fornecer o recurso para trabalhar nisso. | Este valor é padronizado para o detalhe da linha de contrato relacionado para o custo que é criado automaticamente e usado na recuperação do preço de custo. |
| **Unidade de Recursos** | **Criação Rápida** | A unidade de recursos que irá incorrer neste custo e fornecer o recurso para trabalhar nisso. | Este valor é padronizado para o detalhe da linha de contrato relacionado para o custo que é criado automaticamente e usado na recuperação do preço de custo. |
| **Agenda da unidade** | **Criação rápida** | O grupo de unidades de trabalho, produto ou despesa. As unidades pertencem a uma agenda da unidade ou a um grupo de unidades. Por exemplo, *milhas* e *quilômetros (kms)* são unidades que pertencem a um grupo de unidades que descrevem distâncias. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Unidade** | **Criação Rápida** | A unidade de trabalho, produto ou despesa. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Quantidade** | **Criação Rápida** | A quantidade de trabalho, produto ou despesa. | Este valor é padronizado para o detalhe da linha do contrato relacionado para o custo que é criado automaticamente. |
| **Preço unitário** | **Criação Rápida** | A taxa de faturamento da função que está executando o trabalho, o preço unitário do produto, ou o preço de venda do produto ou a categoria de despesa. O padrão para **Tempo** é baseado na combinação de valores de dimensão de preço na linha de preço da função da lista de preços do projeto que está em vigor para a data de início. Para **Despesas**, o padrão deste campo é da configuração de preço para a categoria de transação na lista de preços do projeto que é efetiva para a data de início. Se o método de precificação da categoria de transação não for **preço por unidade**, não haverá padrão e este campo ficará em branco. Para produtos, o padrão deste campo é baseado na linha **Item da lista de preços** na lista de preços do projeto que está em vigor para a data de início.| A taxa de custo da função que está executando o trabalho ou o custo por unidade da categoria de despesas ou o custo unitário do produto. O padrão para **Tempo** com base na combinação de valores de dimensão de preço na linha de preço da função da lista de preços de custo anexada à unidade de contratação efetiva para a data de início. Para **Despesas**, o padrão deste campo é baseado na linha de preço da categoria da lista de preços de custo anexada à unidade de contratação que é efetiva para a data de início. Se o método de precificação da categoria de transação não for preço por unidade não haverá padrão e este campo ficará em branco. Para produtos, este padrão do campo é baseado na linha do **Item da lista de preços** da lista de preços de custo anexada à unidade de contratação que é efetiva para a data de início.|
| **Imposto Estimado** | **Criação Rápida** | O imposto estimado para este trabalho ou despesa, conforme inserido pelo usuário. | &nbsp; |
| **Valor** | **Criação Rápida** | O valor neste campo pode ser adicionado se os campos **Quantidade** e **Preço** ficarem em branco. Se a **Quantidade** e o **Preço** forem preenchidos, o campo **Valor** será somente para leitura e será calculado como **(Quantidade \*Preço unitário) + Imposto**. | &nbsp; |

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
