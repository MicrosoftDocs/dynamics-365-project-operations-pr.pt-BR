---
title: Atualizar os atributos de plug-in para incluir novas dimensões de preço
description: Este artigo fornece informações sobre a atualização de atributos de plug-in para dimensões de preço.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 459aefb510cc9a9ec55a86ca7e362db98ccabb70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913192"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Atualizar os atributos de plug-in para incluir novas dimensões de preço

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Se você não estiver usando os recursos de cotação e contratação do Project Service Automation (PSA), poderá ignorar este artigo.

Este artigo supõe que os procedimentos nos artigos foram concluídos, [Criar campos personalizados e entidades](create-custom-fields-entities.md), [Adicionar campos personalizados para configuração de preço e entidades transacionais](field-references.md) e [Configurar campos personalizados como dimensões de preço](set-up-pricing-dimensions.md). Se você não concluiu esses procedimentos, volte e conclua-os e retorne a este artigo.

Quando um detalhe da linha de cotação é criado na página **Linha de Cotação** para uma linha de cotação do projeto, o sistema cria duas linhas de estimativa em segundo plano – uma linha para o lado do custo da estimativa e outra para o lado das vendas. O mesmo se aplica às linhas de contrato do projeto.

Quando você altera uma quantidade ou um campo no lado do custo, essa alteração é propagada para o lado das vendas. Isso é possível por causa dos plug-ins a seguir que devem ser registrados novamente após uma alteração nas dimensões de precificação.

- PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.

As etapas a seguir orientam você no processo de registro dos plug-ins.

1. Abra **PluginRegistrationTool** e conecte-se à sua instância online
2. Clique em **Pesquisar** e procure o plug-in a ser atualizado.

 ![Captura de tela da árvore de pesquisa.](media/PRT-1.png)

3. Depois que o plug-in for encontrado, selecione-o e clique em **Selecionar no Formulário Principal**.

4. Selecione a etapa do plug-in a ser atualizado, clique com o botão direito do mouse e selecione **Atualizar**.

 ![Captura de tela do plug-in a ser atualizado.](media/PRT-2.png)
 
5. Na janela de atualização, clique nas reticências (**...**) nos atributos de filtragem.

 ![Captura de tela das informações de configuração Atualizar etapa existente.](media/PRT-3.png)
 
6. Marque as caixas de seleção do atributo de precificação.

 ![Captura de tela mostrando a marcação das caixas de seleção de atributos de precificação.](media/PRT-4.png)

7. Clique em **OK** para fechar a página e selecione **Atualizar Etapa**.

 ![Captura de tela mostrando o botão “Atualizar Etapa”.](media/PRT-5.png)
 
8. Repita esse processo para o segundo plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.

9. Feche a ferramenta de registro de plug-in.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
