---
title: Moeda
description: Este tópico fornece informações sobre como adicionar e remover tipos de moeda no Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9c2c6f98e48c5ee251d44131d0c05c705faf1459
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011267"
---
# <a name="currency"></a>Moeda

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

As moedas determinam os preços dos produtos no catálogo de produtos e o custo das transações, como ordens de vendas. Se os clientes estão dispersos por regiões geográficas, adicione suas moedas para gerenciar suas transações. Adicione as moedas mais apropriadas às suas necessidades de negócios atuais e futuras.  

> [!NOTE]
> Se o seu ambiente for um ambiente do Common Data Service, você estiver no centro de administração do Power Platform e selecionar a página **Moedas** (**Ambientes** > [selecionar ambiente] > **Configurações** > **Negócios** > **Moedas**), a página ficará em branco. Isso ocorre porque não há suporte para a definição de moedas em ambientes do Common Data Service.

## <a name="add-a-currency"></a>Adicionar uma moeda  
Antes de iniciar este procedimento, verifique se o seu direito de acesso inclui permissões de administrador do sistema. 

1. No centro de administração do Power Platform, selecione um ambiente. 
2. Selecione **Configurações** > **Negócios**.
3. Selecione **Moedas**.  
4. Selecione **Novo**.  
5. Preencha as informações, conforme necessário.  


   |          Campo          |                                                                                                                                                                                                                                                                                                                                                                            Descrição                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Tipo de Moeda**    | - **Sistema** - Selecione esta opção se quiser usar as moedas disponíveis nos aplicativos baseados em modelo do Dynamics 365. Para procurar uma moeda, selecione **Pesquisa**. Quando você seleciona um código de moeda, **Nome da Moeda** e **Símbolo de Moeda** são automaticamente adicionados à moeda selecionada.<br />- **Personalizado** - Selecione esta opção se quiser adicionar uma moeda que não está disponível nos aplicativos baseados em modelo do Dynamics 365. Nesse caso, você deve inserir manualmente os valores de **Código da Moeda**, **Precisão da Moeda**, **Nome da Moeda**, **Símbolo da Moeda** e **Conversão de Moeda**. |
   |    **Código da Moeda**    |                                                                                                                                                                                                                                                                                                                                            Forma abreviada para a moeda. Por exemplo, **USD** para dólares americanos.                                                                                                                                                                                                                                                                                                                                            |
   | **Número de casas decimais da moeda**  |                                                                                                                                                                                  Digite o número de decimais que você deseja usar para a moeda.  Você pode adicionar um valor entre 0 e 4. **Observação:** se você definir um valor de precisão na caixa de diálogo **Configurações do Sistema**, esse valor será exibido aqui.                                                                                                                                                                                  |
   |    **Nome da Moeda**    |                                                                                                                                                                                                                                         Se você tiver selecionado um código de moeda na lista de moedas disponíveis dos aplicativos baseados em modelo do Dynamics 365, o nome da moeda para o código selecionado será exibido aqui. Se você tiver selecionado **Personalizado** como o tipo de moeda, digite o nome da moeda.                                                                                                                                                                                                                                          |
   |   **Símbolo de moeda**   |                                                                                                                                                                                                                                                                      Se você tiver selecionado um código de moeda na lista de moedas disponíveis, o símbolo da moeda selecionada será exibido aqui. Se você tiver selecionado **Personalizado** como o tipo de moeda, insira o símbolo da nova moeda.                                                                                                                                                                                                                                                                       |
   | **Conversão de moeda** |                                                                                                                                                                                                                                     Digite o valor da moeda selecionada em termos de um dólar americano. Esse é o valor no qual a moeda selecionada é convertida na moeda base. **Importante:** atualize esse valor com a frequência necessária para evitar cálculos imprecisos em suas transações.                                                                                                                                                                                                                                      |


6. Ao terminar, na barra de comando, selecione **Salvar** ou **Salvar e fechar**.  

   > [!TIP]
   >  Para editar uma moeda, selecione a moeda e insira ou selecione os novos valores.  

## <a name="delete-a-currency"></a>Excluir uma moeda  

1. No centro de administração do Power Platform, selecione um ambiente. 
2. Selecione **Configurações** > **Negócios**.
3. Selecione **Moedas**.  
4. Na lista de moedas exibida, selecione a moeda a ser excluída.  
5. Selecione **Excluir**.  
6. Confirme a exclusão.  

> [!IMPORTANT]
>  Você não pode excluir moedas que estejam sendo usadas por outros registros, mas pode desativá-las. A desativação dos registros de moeda não remove as informações sobre moeda dos registros existentes, como oportunidades ou pedidos. Entretanto, você não poderá selecionar a moeda desativada para novas transações.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]