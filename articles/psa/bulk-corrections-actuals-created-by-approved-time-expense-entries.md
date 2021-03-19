---
title: Correções em massa de valores criados por entradas de hora e despesa aprovadas
description: Este tópico explica como um administrador pode realizar correções separadamente ou em massa a entradas de hora e despesa aprovadas anteriormente se o faturamento não tiver sido concluído.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 17d6648840e27a4e573985af2cdd74c4adf878e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290885"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Correções em massa de valores criados por entradas de hora e despesa aprovadas

[!include [banner](../includes/psa-now-project-operations.md)]

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

![Lista de exibição associada de dados reais](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
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

![Dados reais de despesa](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]