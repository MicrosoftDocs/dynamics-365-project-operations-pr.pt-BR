---
title: Espaço de trabalho móvel do gerenciamento de despesas
description: Esse tópico fornece informações sobre o espaço de trabalho móvel Gerenciamento de despesas. Este espaço de trabalho permite que os usuários capturem e carreguem um recibo para que possam anexá-lo a um relatório de despesas posteriormente. Os usuários também podem criar rapidamente uma linha de despesas usando um recibo anexado, além de criar e gerenciar relatórios de despesas.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2d257ced3dadb320c501bfd5f64dcd8f21c1a4d3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272014"
---
# <a name="expense-management-mobile-workspace"></a>Espaço de trabalho móvel do gerenciamento de despesas

Esse tópico fornece informações sobre o espaço de trabalho móvel **Gerenciamento de despesas**. Este espaço de trabalho permite que os usuários capturem e carreguem um recibo para que possam anexá-lo a um relatório de despesas posteriormente. Os usuários também podem criar rapidamente uma linha de despesas usando um recibo anexado, além de criar e gerenciar relatórios de despesas. Além disso, os aprovadores podem usar o espaço de trabalho móvel **Gerenciamento de despesas** para exibir relatórios de despesas atribuídos a eles e aprovar ou rejeitar esses relatórios de despesas.


Esse espaço de trabalho móvel deve ser usado com o aplicativo móvel Dynamics 365 Unified Ops.


## <a name="overview"></a>Visão Geral

Muitas organizações exigem que uma cópia de um recibo seja anexada a um relatório de despesas relacionadas a viagens ou negócios que um funcionário envia para reembolso. O espaço de trabalho móvel **Gerenciamento de despesas** permite que os usuários criem rapidamente novas linhas de despesas no dispositivo móvel de sua escolha, usando uma foto anexada de um recibo. Como alternativa, os usuários podem tirar uma foto de um recibo e depois anexá-la a um relatório de despesas. Os funcionários também podem criar e gerenciar relatórios de despesas e, em seguida, enviá-los para aprovação e reembolso usando o dispositivo móvel.


Especificamente, o espaço de trabalho móvel **Gerenciamento de despesas** permite que os usuários executem estas tarefas:

- Tire uma foto de um recibo e carregue-o no Dynamics 365 Finance. Você poderá anexar essa foto a um relatório de despesas posteriormente.
- Carregue um arquivo como recibo capturado. Você poderá anexar esse arquivo a um relatório de despesas posteriormente.
- Crie uma nova linha de despesas usando um recibo anexado. Você pode adicionar o item de linha a um relatório de despesas posteriormente e enviá-lo para aprovação e reembolso.

Você também pode usar estes recursos:

- Crie um novo relatório de despesas.
- Anexe transações de cartão de crédito e outras despesas criadas anteriormente a um relatório de despesas.
- Crie novas despesas para um relatório de despesas.
- Anexe um recibo a qualquer despesa de um relatório de despesas, tirando uma foto do recibo ou enviando um arquivo como recibo capturado.
- Dependendo da política de despesas da empresa, adicione a lista de convidados a uma despesa.
- Dependendo da política de despesas da empresa, especifique as despesas.
- Envie um relatório de despesas para aprovação e reembolso.
- Aprove ou rejeite relatórios de despesas para os quais você seja um aprovador atribuído.

## <a name="prerequisites"></a>Pré-requisitos
Os pré-requisitos variam, com base na versão que foi implantada para sua organização.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Pré-requisitos se você usar Dynamics 365 Finance 
Se o Finance foi implantado para sua organização, o administrador do sistema deve publicar o espaço de trabalho móvel **Gerenciamento de despesas**. Para obter instruções, consulte [Publicar espaços de trabalho móveis](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Pré-requisitos se você usar a versão 1611 com atualização de plataforma 3 ou posterior
Se a versão 1611 com atualização da plataforma 3 ou posterior foi implantada para sua organização, o administrador do sistema deverá preencher os pré-requisitos a seguir. 

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
<td>Implemente o KB 4019015.</td>
<td>Administrador do sistema</td>
<td>KB 4019015 é uma atualização X++ ou hotfix de metadados que contém o espaço de trabalho móvel <strong>Gerenciamento de despesas</strong>. Para implementar o KB 4019015, o administrador do sistema deve seguir estas etapas.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Baixe o hotfix de metadados de Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Instale o hotfix de metadados</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Crie um pacote implantável</a> que contém os modelos <strong>ApplicationSuite</strong> e <strong>ExpenseMobile</strong> e, em seguida, carregue o pacote implantável no LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Aplique o pacote implantável</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publique o espaço de trabalho móvel <strong>Gerenciamento de despesas</strong>.</td>
<td>Administrador do sistema</td>
<td>Consulte <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicar um espaço de trabalho móvel</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Baixe e instale o aplicativo móvel Dynamics 365 for Operations
Baixe e instale o aplicativo móvel Dynamics 365 Unified Ops.

- [Para telefones Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Para iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Entre no aplicativo móvel
1. Inicie o aplicativo no dispositivo móvel.
2. Insira o URL do Dynamics 365.
4. Na primeira vez que você efetuar login, será solicitado seu nome de usuário e senha. Insira suas credenciais.
5. Depois de fazer login, os espaços de trabalho disponíveis para sua empresa são mostrados. Observe que se o administrador do sistema publicar uma nova área de trabalho posteriormente, você terá que atualizar a lista de áreas de trabalho móveis.


[![Deslizar para atualizar](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Capture um recibo usando o espaço de trabalho móvel Gerenciamento de despesas

1. No dispositivo móvel, abra o espaço de trabalho **Gerenciamento de despesas**.
2. Selecione **Capturar recibo**.
3. Selecione **Tirar foto** ou **Escolher imagem**.
4. Siga uma destas etapas:

    - Se você selecionou **Tirar foto**, Siga estas etapas:

        1. Você é levado para a câmera do dispositivo móvel para poder tirar uma foto do recibo. Quando terminar de tirar uma foto, selecione **OK** para aceitar a foto.
        2. Opcional: insira um nome para a foto e anotações.

    - Se você selecionou **Escolher imagem**, siga estas etapas:

        1. Selecione uma imagem na lista.
        2. Opcional: insira um nome para a imagem e anotações.

5. Escolha **Concluído**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Insira rapidamente despesas usando o espaço de trabalho móvel Gerenciamento de despesas
1. No dispositivo móvel, abra o espaço de trabalho **Gerenciamento de despesas**.
2. Selecione **Entrada rápida de despesas**.
3. Selecione a categoria da despesa. Você vê uma lista de categorias de despesa que são carregadas no aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Se a sua categoria não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por categoria de despesa ou alterne para pesquisar por tipo de despesa.
4. Insira a data da transação da despesa.
5. Opcional: insira o comerciante para a despesa.
6. Insira o valor da despesa.
7. Selecione a moeda da despesa. Você vê uma lista dos códigos de moeda que são carregadas no aplicativo para uso offline. Por padrão, 400 moedas são carregadas, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Se a sua moeda não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por moeda ou alterne para pesquisar por nome.
8. Selecione **Tirar foto** ou **Escolher imagem**.
9. Siga uma destas etapas:

    - Se você selecionar **Tirar foto**, será levado para a câmera do dispositivo móvel para poder tirar uma foto do recibo. Quando terminar de tirar uma foto, selecione **OK** para aceitar a foto.
    - Se você selecionou **Escolher imagem**, selecione uma imagem na lista.

10. Escolha **Concluído**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Aprove um relatório de despesas usando o espaço de trabalho móvel Gerenciamento de despesas (se você usar a atualização de julho de 2017)
1. No dispositivo móvel, abra o espaço de trabalho **Gerenciamento de despesas**.
2. **Aprovações de despesas** mostra o número de relatórios de despesas atribuídos a você para aprovação. O número é atualizado aproximadamente a cada 30 minutos. Selecione **Aprovações de despesas**.

    A lista de relatórios de despesas atribuídos a você para aprovação é mostrada.
    
3. Selecione um relatório de despesas para exibir os detalhes das despesas.
4. Selecione uma despesa para exibir os detalhes dela. As informações que são mostradas para uma despesa incluem detalhes de recibo, convidado e discriminação.
5. Na página **Relatório de despesas**, selecione para aprovar ou rejeitar o relatório de despesas.
6. Insira comentários para a ação de aprovação.
7. Escolha **Concluído**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Crie um novo relatório de despesas e envie-o para aprovação usando o espaço de trabalho móvel Gerenciamento de despesas (se você usar a atualização de julho de 2017)
1. No dispositivo móvel, abra o espaço de trabalho **Gerenciamento de despesas**.
2. Selecione **Entrada de despesas**.
3. Selecione **Novo relatório** ou selecione um relatório de despesas existente na lista.
4. Para novos relatórios de despesas, insira a finalidade e todas as informações adicionais disponíveis. Essas informações variam de acordo com forma como o gerenciamento de despesas está configurado para sua empresa.
5. Escolha **Concluído**.
6. Para adicionar despesas existentes, como transações de cartão de crédito, ao relatório de despesas, selecione **Anexar**.
7. Selecione uma ou mais despesas na lista.
8. Escolha **Concluído**.
9. Para adicionar uma nova despesa ao relatório de despesas, selecione **Nova despesa**.
10. Selecione a categoria da despesa. Você vê uma lista de categorias de despesa que são carregadas no aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Se a sua categoria não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por categoria de despesa ou alterne para pesquisar por tipo de despesa.
11. Opcional: insira o comerciante para a despesa.
12. Insira a data da transação da despesa.
13. Insira o valor da despesa.
14. Selecione a moeda da despesa. Você vê uma lista dos códigos de moeda que são carregadas no aplicativo para uso offline. Por padrão, 400 moedas são carregadas, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Se a sua moeda não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por moeda ou alterne para pesquisar por nome.
15. Escolha **Concluído**.
16. Para adicionar mais detalhes à despesa, selecione **Adicione mais detalhes**. Os campos disponíveis dependem da configuração do gerenciamento de despesas da sua empresa.
17. Se a política da empresa exigir um recibo da despesa, selecione **Recibos** e siga estas etapas:

    1. Selecione **Capturar recibo** ou **Anexar recibo**.
    2. Siga uma destas etapas:

        - Se você selecionou **Capturar recibo**, siga estas etapas:

            1. Selecione **Tirar foto** ou **Escolher imagem**.
            2. Siga uma destas etapas:

                - Se você selecionou **Tirar foto**, Siga estas etapas:

                    1. Você é levado para a câmera do dispositivo móvel para poder tirar uma foto do recibo. Quando terminar de tirar uma foto, selecione **OK** para aceitar a foto.
                    2. Opcional: insira um nome para a foto e anotações.

                - Se você selecionou **Escolher imagem**, siga estas etapas:

                    1. Selecione uma imagem na lista.
                    2. Opcional: insira um nome para a imagem e anotações.

            3.  Escolha **Concluído**.

        - Se você selecionou **Anexar recibo**, siga estas etapas:

            1.  Selecione uma ou mais imagens na lista.
            2.  Escolha **Concluído**.

    3. Selecione o botão **Voltar** para retornar aos detalhes de despesas.

18. Se a política da empresa exigir convidados da despesa, selecione **Convidados** e siga estas etapas:

    1. Selecione **Convidado**, **Convidados anteriores** ou **Colegas**.
    2. Siga uma destas etapas:

        - Se você selecionou **Convidado**, siga estas etapas:

            1. Insira o nome do convidado.
            2. Opcional: insira a organização e/o ou país do convidado.
            3. Opcional: insira o cargo do convidado.
            4. Escolha **Concluído**.

        - Se você selecionou **Convidados anteriores**, siga estas etapas:

            1. Selecione um ou mais convidados anteriores na lista. Você vê uma lista de convidados anteriores que adicionou a relatórios de despesas anteriores que são carregados em seu aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Se o convidado anterior não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por nome ou alterne para pesquisar por organização, país ou cargo.
            2. Escolha **Concluído**.

        - Se você selecionou **Colega**, siga estas etapas:

            1. Selecione um ou mais colegas na lista. Você vê uma lista de colegas que são carregados no aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Se seu colega não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por nome ou alterne para pesquisar por empresa ou cargo.
            2. Escolha **Concluído**.

    3. Selecione o botão **Voltar** para retornar aos detalhes de despesas.

19. Se a política da empresa exigir que a despesa seja discriminada, selecione **Discriminar** e siga estas etapas:

    1. Selecione a primeira data para discriminar.
    2. Selecione **Adicionar discriminação**.
    3. Selecione a subcategoria de discriminação da despesa. Você vê uma lista de subcategorias de despesa que são carregadas no aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Se a sua subcategoria não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise pelo nome da subcategoria de despesas.
    4. Insira o valor da transação para a discriminação.
    5. Edite a data da transação, se necessário.
    6. Escolha **Concluído**.
    7. Repita as etapas anteriores até terminar de adicionar todas as discriminações para a data selecionada.
    8. ara dias adicionais, você pode selecionar **Copiar para o dia seguinte** para copiar as discriminações para o dia seguinte. Outra alternativa é selecionar a data para discriminar e, em seguida, adicionar discriminações como fez para a primeira data.
    9. Após terminar de discriminar as despesas, selecione o botão **Voltar** para retornar aos detalhes de despesas.

20. Selecione o botão **Voltar** para retornar à página **Relatório de despesas**.
21. Repita as etapas anteriores até terminar de adicionar todas as despesas.
22. Selecione **Enviar**.
23. Insira comentários para o aprovador.
24. Escolha **Concluído**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]