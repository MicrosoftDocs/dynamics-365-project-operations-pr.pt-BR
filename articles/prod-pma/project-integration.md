---
title: Integração com o Microsoft Project Client
description: O planejamento e a manutenção da agenda de um projeto podem ser complexos; portanto, os gerentes de projeto precisam usar ferramentas que os ajudem a gerenciar essa tarefa. A integração com o Microsoft Project Client fornece suporte para abrir e gerenciar uma estrutura de detalhamento de trabalho do projeto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d2994195ba916ac7a128e8bdd53bea6acb7bd0ba
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684950"
---
# <a name="microsoft-project-client-integration"></a>Integração com o Microsoft Project Client

[!include [banner](../includes/banner.md)]

O planejamento e a manutenção da agenda de um projeto podem ser complexos; portanto, os gerentes de projeto precisam usar ferramentas que os ajudem a gerenciar essa tarefa. A integração com o Microsoft Project Client fornece suporte para abrir e gerenciar uma estrutura de detalhamento de trabalho do projeto. O gerente do projeto pode publicar as alterações novamente na estrutura de detalhamento de trabalho do projeto do Dynamics 365 Finance.

> [!NOTE]
> Se estiver usando a atualização de julho (versão 10.0.4), você deverá instalar o KB 4054797 e 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Configurar o suplemento do Microsoft Project Client
Para habilitar a integração com o Microsoft Project Client, um suplemento do Microsoft Dynamics 365 deverá ser instalado no aplicativo cliente do Microsoft Project do usuário. Isso é feito abrindo o **Espaço de trabalho de gerenciamento de projetos**.

•   Clique em **Configurar o suplemento de cliente do projeto** na seção **Links** > **Configuração** do espaço de trabalho.

•   Clique em **Abrir** e, em seguida, em **Executar** quando solicitado.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Abrir e editar um rascunho existente da estrutura de detalhamento de trabalho no Microsoft Project Client
Se um projeto no Dynamics 365 Finance já tiver uma estrutura de detalhamento de trabalho criada, ela poderá ser aberta no aplicativo Microsoft Project Client, se tiver status de rascunho. Para abrir na página **Projeto**, clique no link **Abrir no Microsoft Project** na guia **Planejar**. Essa página também pode ser aberta no aplicativo Microsoft Project Client clicando em **Abrir** na guia **Microsoft Dynamics 365**. Selecione **Entidade legal** e **Projeto** na lista.

> [!NOTE]
> Se você estiver usando o Internet Explorer como navegador, precisará clicar em **Salvar** para abrir manualmente a partir do local em que o arquivo foi baixado. Ou clique em **Salvar e abrir** para abrir o arquivo no Microsoft Project Client. Não mude o nome do arquivo ao salvá-lo.

Antes de fazer qualquer edição no arquivo usando o Microsoft Project Client, você precisa fazer o check-out dele. Clique em **Check-out** na guia **Microsoft Dynamics 365**. Isso impedirá que outros usuários editem ao mesmo tempo a estrutura de detalhamento de trabalho no Finance. Para publicar a estrutura de detalhamento de trabalho após concluir as edições, clique em **Check-in** na guia **Microsoft Dynamics 365**.

Se uma equipe de projeto já tiver sido adicionada ao projeto no Finance, a lista de recursos será preenchida com os membros da equipe. Se uma equipe de projeto ainda não tiver sido adicionada ao projeto, você poderá selecionar recursos e criar a equipe dentro do Microsoft Project Client clicando no botão **Recursos** na guia **Microsoft Dynamics 365**. 

Os dados a seguir serão sincronizados de volta com o Finance como parte do processo de check-in:

•   Nome da tarefa

•   Data de início

•   Data de término

•   Antecessores

•   Nomes dos recursos

•   Categoria

•   Categoria do recurso

•   Horas de trabalho

•   Observações

•   Prioridade

> [!NOTE]
> Se você adicionar quaisquer outras colunas ao arquivo do Microsoft Project Client, elas não serão salvas no arquivo e não serão exibidas quando o arquivo for aberto novamente.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Criar a estrutura de detalhamento de trabalho para um projeto existente usando o Microsoft Project Client
Siga estas etapas para criar uma nova estrutura de detalhamento de trabalho usando o Microsoft Project Client:


1.  Abra o Microsoft Project Client.

2.  Na guia **Microsoft Dynamics 365**, clique em **Abrir**.

3.  Selecione a **Entidade legal** para o projeto.

4.  Selecione o **Projeto**.

5.  Clique em **Check-out** na guia **Microsoft Dynamics 365**.

6.  Quando estiver pronto para publicar no Finance, clique em **Check-in** na guia **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Substituir a estrutura de detalhamento de trabalho existente de um projeto existente usando o Microsoft Project Client
Para criar uma nova estrutura de detalhamento de trabalho usando o Microsoft Project Client e substituir uma estrutura existente para um projeto existente, siga estas etapas:

1.  Abra o Microsoft Project Client.

2.  Crie a agenda no Microsoft Project Client.

3.  Na guia **Microsoft Dynamics 365**, clique em **Salvar alterações** > **Substituir projeto existente**.

4.  Selecione a **Entidade legal** para o projeto.

5.  Selecione o **Projeto**.

6.  Clique em **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Criar um novo projeto de dentro do Microsoft Project Client


1.  Abra o Microsoft Project Client.

2.  Crie a agenda no Microsoft Project Client.

3.  Na guia **Microsoft Dynamics 365**, clique em **Salvar alterações** > **Salvar em novo projeto**.

4.  Selecione a **Entidade legal** para o projeto.

5.  Insira a **ID do projeto**, se necessário.

6.  Informe o **Nome do projeto**.

7.  Selecione o **Tipo de projeto**, o **Grupo do projeto** e a **ID do contrato de projeto**. Também é possível criar um novo contrato de projeto clicando em **Novo**.

8.  Selecione o **Calendário** a ser usado para obter recursos.

11. Clique no **OK**.

> [!NOTE]
> O suplemento Project Client não oferece suporte aos seguintes caracteres no formato de ID do projeto:
> 
>   - Sublinhado
>   - Ponto
>   - Espaço
>   - Barra

[!INCLUDE[footer-include](../includes/footer-banner.md)]
