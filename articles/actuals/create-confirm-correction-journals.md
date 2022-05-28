---
title: Criar e confirmar diários de correção
description: Este tópico fornece informações sobre como criar e confirmar um diário de correção.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582789"
---
# <a name="create-and-confirm-correction-journals"></a>Criar e confirmar diários de correção

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Às vezes, uma entrada de hora ou despesa pode ser inserida incorretamente. Por exemplo, um consultor pode selecionar a data errada ao criar uma entrada de hora ou selecionar o projeto errado ao inserir uma despesa. Se um consultor não conseguir atualizar as entradas enviadas, um administrador de back-end poderá corrigir os dados reais de um projeto diretamente.

## <a name="correct-approved-time-entries"></a>Corrigir entradas de hora aprovadas     

Siga as etapas para corrigir uma ou várias entradas de hora de um projeto.

1. Na área **Vendas**, selecione **Transações** e depois selecione **Hora Aprovada**. 

2. Na lista **Hora Aprovada**, localize e selecione uma ou mais entradas de hora aprovadas para corrigir. Você pode usar o filtro para localizar entradas relacionadas. Por exemplo, você pode filtrar uma ID de Projeto e selecionar todas as horas aprovadas com essa ID de Projeto.

3. Selecione **Corrigir entradas**. Um novo diário de correção é criado automaticamente com o tipo de **Correção de hora** atribuído. As entradas selecionadas são adicionadas ao diário. 

4. Na página **Novo Diário**, insira uma **Descrição** para o diário de correção e selecione a guia **Correções de Entrada de Hora**.  

5. Na seção **Novos Valores para Entradas de Hora**, atualize os campos com as informações corretas, conforme a necessidade. Por exemplo, é possível alterar o projeto atribuído ou o recurso reservável.

6. Selecione **Versão Prévia**. Na caixa de diálogo, selecione **OK**. Na guia **Linhas do diário**, é possível visualizar uma lista dos dados reais originais relacionados às entradas de hora selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas. Se forem necessárias correções adicionais, repita as etapas 5 e 6. 

    > [!NOTE]
    > Todos os dados reais corrigidos terão os mesmos valores selecionados na seção **Novos valores para Entradas de Hora**.

7. Se as correções aparecerem conforme o esperado, selecione **Confirmar**. Na caixa de diálogo, selecione **OK**.

8. Volte para a área **Vendas** e selecione **Projetos**, depois abra o projeto para o qual atualizou as entradas de hora. 

9. Na página **Projetos**, na guia **Dados Reais**, exiba as alterações feitas. 

    > [!NOTE]
    > Se a guia **Dados Reais** não estiver visível, selecione **Relacionados** > **Dados Reais**.  

10. Na lista **Exibição Associada de Dados Reais**, é possível ver que as entradas de hora originais que foram revertidas ainda estão listadas, assim como as entradas de hora corrigidas correspondentes. 

 
## <a name="correct-approved-expense-entries"></a>Corrigir entradas de despesa aprovadas

Siga as etapas para corrigir uma ou mais entradas de despesa. 

1. Na área **Vendas**, no painel de navegação à esquerda, em **Transações**, selecione **Despesas Aprovadas**.

2. Na lista **Despesas Aprovadas**, selecione o projeto que deseja corrigir e selecione **Entradas corretas**. Um novo diário de correção será criado automaticamente com o tipo de **Correção de despesa** atribuído. 

3. Na página **Novo Diário**, insira uma **Descrição** para a correção e, na guia **Correção de Despesa**, na seção **Novos Valores para Despesas**, selecione os campos de dados que deseja corrigir para as linhas de despesa selecionadas. Por exemplo, é possível atribuir a despesa a outro **Projeto** ou corrigir a **Categoria de Despesa**, **Data da Despesa** ou **Recurso Reservável**.

4. Selecione **Versão Prévia**. Na caixa de diálogo, selecione **OK**. 

5. Verifique as correções na guia **Linhas do diário**. É possível visualizar uma lista dos dados reais originais relacionados às entradas de despesa selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas.

6. Se os valores das correções aparecerem conforme o esperado, selecione **Confirmar**. Na caixa de diálogo, selecione **OK**. Se os valores não estiverem sendo exibidos conforme o esperado, selecione **Cancelar** para voltar para a lista de **Despesas Aprovadas**. Repita as etapas 2 a 5. 

7. Depois de confirmar o diário de correção, retorne ao(s) projeto(s) que você atualizou para ver as alterações.

8. Na guia **Dados reais** da página do projeto, revise a lista **Exibição Associada de Dados Reais**. As entradas originais e as entradas corrigidas serão listadas.


## <a name="correct-approved-material-usage-logs"></a>Corrigir os logs aprovados de uso de material

Realize as etapas a seguir para corrigir uma ou mais entradas de log de uso de material.

1. Na área **Vendas**, no painel de navegação esquerdo, em **Transações**, selecione **Dados reais**.

2. Na lista **Dados reais**, use filtros de coluna para selecionar a classe de transação **Material** de modo que sejam mostrados apenas os dados reais de material. Use outros filtros de coluna para limitar ainda mais os dados reais mostrados. Depois de encontrar o conjunto desejado de dados reais, selecione os dados reais e selecione **Corrigir entradas**. Um novo diário de correção é criado automaticamente e o tipo **Correção de uso do material** é atribuído.

3. Na página **Novo Diário**, no campo **Descrição**, digite uma descrição da correção. Depois, na guia **Correção de Uso do Material**, na seção **Novos Valores para Materiais**, selecione os campos de dados para corrigir as linhas de materiais selecionadas. Por exemplo, você pode atribuir o material a outro projeto ou corrigir o produto, a data do material ou o subcontrato.

4. Selecione **Versão Prévia**. Depois, na próxima caixa de diálogo, selecione **OK**.

5. Na guia **Linhas do diário**, verifique as correções. Você pode visualizar uma lista dos dados reais originais relacionados às entradas de material selecionadas que foram revertidos e as linhas correspondentes corrigidas que foram criadas.

6. Se os valores das correções aparecerem conforme o esperado, selecione **Confirmar**. Depois, na próxima caixa de diálogo, selecione **OK**. Se os valores não forem os esperados, selecione **Cancelar** para voltar à lista **Dados reais**. Em seguida, repita as etapas 2 a 5.

7. Depois de confirmar o diário de correção, retorne ao(s) projeto(s) que você atualizou para ver as alterações.

8. Na guia **Dados reais** da página do projeto, revise a lista **Exibição Associada de Dados Reais**. As entradas originais e as entradas corrigidas serão listadas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
