---
title: Criar e confirmar diários de correção
description: Este tópico fornece informações sobre como criar e confirmar um diário de correção.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896942"
---
# <a name="create-and-confirm-correction-journals"></a>Criar e confirmar diários de correção

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

Ocasionalmente, uma entrada de hora ou de despesa pode ser inserida incorretamente. Por exemplo, um consultor pode selecionar a data erada ao criar uma entrada de hora ou pode transpor os números ao inserir uma despesa. Se um consultor não puder atualizar as entradas enviadas, um administrador pode corrigir a entrada de um projeto diretamente.

Para concluir os procedimentos neste tópico, será necessário ter permissões de Administrador.

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

Por exemplo, no gráfico a seguir, há dois itens de linha com uma quantidade igual a 8,00 com débitos listados na coluna Valor. Além disso, há dois itens de linha com uma quantidade igual a -8,00 que mostram quantidades creditadas na coluna Valor. Essas correções definem a quantidade como zero.

 
## <a name="correct-approved-expense-entries"></a>Corrigir entradas de despesa aprovadas

Siga as etapas para corrigir uma ou mais entradas de despesa. 

1. Na área **Vendas**, no painel de navegação à esquerda, em **Transações**, selecione **Despesas Aprovadas**.

2. Na lista **Despesas Aprovadas**, selecione o projeto que deseja corrigir e selecione **Entradas corretas**. Um novo diário de correção será criado automaticamente com o tipo de **Correção de despesa** atribuído. 

3. Na página **Novo Diário**, insira uma **Descrição** para a correção e, na guia **Correção de Despesa**, na seção **Novos Valores para Despesas**, selecione os campos de dados que deseja corrigir para as linhas de despesa selecionadas. Por exemplo, é possível atribuir a despesa a outro **Projeto** ou corrigir a **Categoria de Despesa**, **Data da Despesa** ou **Recurso Reservável**.

4. Selecione **Versão Prévia**. Na caixa de diálogo, selecione **OK**. 

5. Verifique as correções na guia **Linhas do diário**. É possível visualizar uma lista dos dados reais originais relacionados às entradas de despesa selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas.

6. Se os valores das correções aparecerem conforme o esperado, selecione **Confirmar**. Na caixa de diálogo, selecione **OK**. Se os valores não estiverem sendo exibidos conforme o esperado, selecione **Cancelar** para voltar para a lista de **Despesas Aprovadas**. Repita as etapas 2 a 5. 

> [!NOTE]
> Os dados reais corrigidos terão os mesmos valores selecionados na seção **Novos valores para Despesas**.

7. Depois de confirmar o diário de correção, navegue de volta até os projetos atualizados para exibir as alterações.  

8. Na página do projeto, na guia **Dados Reais**, revise a **Exibição Associada de Dados Reais**. As entradas originais e as entradas corrigidas serão listadas. O gráfico a seguir mostra os valores de entrada de despesa originais e os valores de entrada de despesa correspondentes corrigidos. 


