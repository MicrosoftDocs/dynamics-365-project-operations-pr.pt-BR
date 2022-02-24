---
title: Espaço de trabalho móvel de entrada de hora de projeto
description: Esse tópico fornece informações sobre o espaço de trabalho móvel da entrada de hora de projeto. Este espaço de trabalho permite que os usuários entrem e economizem tempo em um projeto usando seu dispositivo móvel.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 23a5a9f25cfdd6df74257b3500c7a035d711b5f6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071409"
---
# <a name="project-time-entry-mobile-workspace"></a>Espaço de trabalho móvel de entrada de hora de projeto

[!include [banner](../includes/banner.md)]

Esse tópico fornece informações sobre o espaço de trabalho móvel da **entrada de hora de projeto**. Este espaço de trabalho permite que os usuários entrem e economizem tempo em um projeto usando seu dispositivo móvel.

Esse espaço de trabalho móvel deve ser usado com o aplicativo móvel Dynamics 365 Unified Ops. 

## <a name="overview"></a>Visão Geral
Como parte de seu trabalho diário, os recursos do projeto costumam estar no local ou em viagem. O espaço de trabalho móvel **Entrada de tempo do projeto** permite que os usuários insiram seu tempo faturável ou não faturável em um projeto no dispositivo móvel de sua escolha. Portanto, os recursos do projeto podem registrar entradas de tempo a qualquer hora e em qualquer lugar. Eles também podem ver as entradas de tempo que já foram registradas. 

Especificamente, no espaço de trabalho móvel **Entrada de tempo do projeto**, os usuários podem executar estas tarefas:

-   Para qualquer data selecionada, insira o número de horas que você gastou em uma tarefa específica.
-   Pesquise por nome do projeto ou cliente para encontrar o projeto para o qual inserir o tempo.
-   Especifique a categoria e atividade para o tempo que você gastou.
-   Registre o tempo como faturável ou não faturável para o projeto.
-   Opcionalmente, insira qualquer comentário externo ou interno.

## <a name="prerequisites"></a>Pré-requisitos
Os pré-requisitos diferem, com base na versão do Microsoft Dynamics 365 que foi implantado para sua organização.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Pré-requisitos se você usar Dynamics 365 Finance
Se o Finance foi implantado para sua organização, o administrador do sistema deve publicar o espaço de trabalho móvel **Entrada de tempo do projeto**. Para obter instruções, veja [Publicar um espaço de trabalho móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Pré-requisitos se você usar a versão 1611 com atualização de plataforma 3 ou posterior
Se a versão 1611 com atualização da plataforma 3 ou posterior foi implantada para sua organização, o administrador do sistema deve preencher os seguintes pré-requisitos. 

<table>
<thead>
<tr class="header">
<th>Pré-requisito</th>
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implemente o KB 4018050.</td>
<td>Administrador do sistema</td>
<td>KB 4018050 é uma atualização X++ ou hotfix de metadados que contém o espaço de trabalho móvel <strong>Entrada de tempo do projeto</strong>. Para implementar o KB 4018050, o administrador do sistema deve seguir estas etapas.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Baixe o hotfix de metadados de Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instale o hotfix de metadados</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Crie um pacote implantável</a> que contém os modelos <strong>ApplicationSuite</strong> e <strong>ProjectMobile</strong> e, em seguida, carregue o pacote implantável no LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Aplique o pacote implantável</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publicar o Espaço de trabalho móvel de <strong>entrada de hora de projeto</strong>.</td>
<td>Administrador do sistema</td>
<td>Consulte <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicar um espaço de trabalho móvel</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Baixe e instale o aplicativo móvel

Baixe e instale o aplicativo móvel Finance and Operations:

-   [Para telefones Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Para iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Entre no aplicativo móvel
1.  Inicie o aplicativo no dispositivo móvel.
2.  Insira o URL do Dynamics 365.
3.  Na primeira vez que você efetuar login, será solicitado seu nome de usuário e senha. Insira suas credenciais.
4.  Depois de fazer login, os espaços de trabalho disponíveis para sua empresa são mostrados. Observe que se o administrador do sistema publicar uma nova área de trabalho posteriormente, você terá que atualizar a lista de áreas de trabalho móveis.

[![Deslizar para atualizar](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Insira o tempo usando o espaço de trabalho móvel de entrada de tempo do projeto
1.  No seu dispositivo móvel, selecione o espaço de trabalho **Entrada de tempo do projeto**.
2.  Selecione **Entrada de hora**. As datas do calendário para a semana atual serão exibidas.
3.  Para uma data selecionada, selecione **Ações** &gt; **Nova entrada**.
4.  Insira o número de horas para registrar.
5.  Selecione o projeto para a entrada de hora. Uma lista mostra os projetos que são carregados em seu aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, consulte [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Se o seu projeto não estiver na lista, selecione **Pesquisar**. Pesquise por nome ou alterne para pesquisar por nome de projeto ou cliente.
7.  Selecionar uma categoria. Uma lista mostra as categorias que são carregadas em seu aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, consulte [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Se a sua categoria não estiver na lista, selecione **Pesquisar**. Pesquise por categoria ou mude para pesquisar por nome de categoria.
9.  Selecione uma atividade. Uma lista mostra as atividades que são carregadas em seu aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, consulte [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Se a sua atividade não estiver na lista, selecione **Pesquisar**. Pesquise por número de atividade ou alterne para pesquisar por objetivo.

11. Selecione a propriedade de linha.
12. Opcional: insira quaisquer comentários externos e internos.
13. Escolha **Concluído**.
