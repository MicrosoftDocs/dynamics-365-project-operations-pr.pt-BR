---
title: Aplicativo móvel de despesas
description: Esse tópico fornece informações sobre o espaço de trabalho móvel Gerenciamento de despesas.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5ab5959fa5c9c5463826a9a792112a93e469de5f
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818169"
---
# <a name="mobile-expense-app"></a>Aplicativo móvel de despesas

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Esse tópico fornece informações sobre o espaço de trabalho móvel **Gerenciamento de despesas**. Este espaço de trabalho permite que os usuários capturem e carreguem um recibo para que possam anexá-lo a um relatório de despesas posteriormente. Os usuários também podem criar rapidamente uma linha de despesas usando um recibo anexado, além de criar e gerenciar relatórios de despesas. Além disso, os aprovadores podem usar o espaço de trabalho móvel **Gerenciamento de despesas** para exibir relatórios de despesas atribuídos a eles e aprovar ou rejeitar esses relatórios de despesas.

Esse espaço de trabalho móvel deve ser usado com o aplicativo móvel Dynamics 365 Unified Ops.

Muitas organizações exigem que uma cópia de um recibo seja anexada a um relatório de despesas relacionadas a viagens ou negócios que um funcionário envia para reembolso. O espaço de trabalho móvel **Gerenciamento de despesas** permite que os usuários criem rapidamente novas linhas de despesas no dispositivo móvel de sua escolha, usando uma foto anexada de um recibo. Como alternativa, os usuários podem tirar uma foto de um recibo e depois anexá-la a um relatório de despesas. Os funcionários também podem criar e gerenciar relatórios de despesas e, em seguida, enviá-los para aprovação e reembolso usando o dispositivo móvel.

Especificamente, o espaço de trabalho móvel **Gerenciamento de despesas** permite que os usuários executem estas tarefas:

- Tire uma foto de um recibo. Carregue a foto do recibo e anexe-a posteriormente a um relatório de despesas.
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

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Pré-requisitos se você usar Dynamics 365 Finance

Se o Finance foi implantado para sua organização, o administrador do sistema deve publicar o espaço de trabalho móvel **Gerenciamento de despesas**. 

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Baixe e instale o aplicativo móvel Dynamics 365 Unified Ops
Baixe e instale o aplicativo móvel Dynamics 365 Unified Ops.

- [Para telefones Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Para iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Entre no aplicativo móvel
1. Inicie o aplicativo no dispositivo móvel.
2. Insira o URL do Dynamics 365.
4. Na primeira vez que você efetuar login, será solicitado seu nome de usuário e senha. Insira suas credenciais.
5. Depois de fazer login, os espaços de trabalho disponíveis para sua empresa são mostrados. Se o administrador do sistema publicar um novo espaço de trabalho posteriormente, você precisará atualizar a lista de espaços de trabalho móveis.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Capture um recibo usando o espaço de trabalho móvel Gerenciamento de despesas

1. No dispositivo móvel, abra o espaço de trabalho **Gerenciamento de despesas**.
2. Selecione **Capturar recibo**.
3. Selecione **Tirar foto** ou **Escolher imagem**.
4. Siga uma destas etapas:

    - Se você selecionou **Tirar foto**, Siga estas etapas:

        1. Você é levado para a câmera do dispositivo móvel para poder tirar uma foto do recibo. 
        2. Quando terminar de tirar uma foto, selecione **OK** para aceitar a foto.
        3. Opcional: insira um nome para a foto e anotações.

    - Se você selecionou **Escolher imagem**, siga estas etapas:

        1. Selecione uma imagem na lista.
        2. Opcional: insira um nome para a imagem e anotações.

5. Escolha **Concluído**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Insira rapidamente despesas usando o espaço de trabalho móvel Gerenciamento de despesas

1. No dispositivo móvel, abra o espaço de trabalho **Gerenciamento de despesas**.
2. Selecione **Entrada rápida de despesas**.
3. Selecione a categoria de despesa. Você vê uma lista de categorias de despesa que são carregadas no aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a sua categoria não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por categoria de despesa ou alterne para pesquisar por tipo de despesa.
4. Insira a data da transação da despesa.
5. Opcional: insira o comerciante para a despesa.
6. Insira o valor da despesa.
7. Selecione a moeda da despesa. Você vê uma lista dos códigos de moeda que são carregadas no aplicativo para uso offline. Por padrão, 400 moedas são carregadas, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a sua moeda não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por moeda ou alterne para pesquisar por nome.
8. Selecione **Tirar foto** ou **Escolher imagem**.
9. Siga uma destas etapas:

    - Se você selecionar **Tirar foto**, será levado para a câmera do dispositivo móvel para poder tirar uma foto do recibo. Quando terminar de tirar uma foto, selecione **OK** para aceitar a foto.
    - Se você selecionou **Escolher imagem**, selecione uma imagem na lista.

10. Escolha **Concluído**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Aprovar um relatório de despesas usando o espaço de trabalho móvel Gerenciamento de despesas

1. No dispositivo móvel, abra o espaço de trabalho **Gerenciamento de despesas**.
2. **Aprovações de despesas** mostra o número de relatórios de despesas atribuídos a você para aprovação. O número é atualizado aproximadamente a cada 30 minutos. Selecione **Aprovações de despesas**.

    A lista de relatórios de despesas atribuídos a você para aprovação é mostrada.

3. Selecione um relatório de despesas para exibir os detalhes das despesas.
4. Selecione uma despesa para exibir os detalhes dela. As informações que são mostradas para uma despesa incluem detalhes de recibo, convidado e discriminação.
5. Na página **Relatório de despesas**, selecione para aprovar ou rejeitar o relatório de despesas.
6. Insira comentários para a ação de aprovação.
7. Escolha **Concluído**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Crie um novo relatório de despesas e o envie para aprovação usando o espaço de trabalho móvel Gerenciamento de despesas

1. No dispositivo móvel, abra o espaço de trabalho **Gerenciamento de despesas**.
2. Selecione **Entrada de despesas**.
3. Selecione **Novo relatório** ou selecione um relatório de despesas existente na lista.
4. Para novos relatórios de despesas, insira a finalidade e todas as informações adicionais disponíveis. Essas informações variam de acordo com forma como o gerenciamento de despesas está configurado para sua empresa.
5. Escolha **Concluído**.
6. Para adicionar despesas existentes, como transações de cartão de crédito, ao relatório de despesas, selecione **Anexar**.
7. Selecione uma ou mais despesas na lista.
8. Escolha **Concluído**.
9. Para adicionar uma nova despesa ao relatório de despesas, selecione **Nova despesa**.
10. Selecione a categoria da despesa. Você vê uma lista de categorias de despesa que são carregadas no aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a sua categoria não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por categoria de despesa ou alterne para pesquisar por tipo de despesa.
11. Opcional: insira o comerciante para a despesa.
12. Insira a data da transação da despesa.
13. Insira o valor da despesa.
14. Selecione a moeda da despesa. Você vê uma lista dos códigos de moeda que são carregadas no aplicativo para uso offline. Por padrão, 400 moedas são carregadas, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a sua moeda não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por moeda ou alterne para pesquisar por nome.
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

            3. Escolha **Concluído**.

        - Se você selecionou **Anexar recibo**, siga estas etapas:

            1. Selecione uma ou mais imagens na lista.
            2. Escolha **Concluído**.

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

            1. Selecione um ou mais convidados anteriores na lista. Você vê uma lista de convidados anteriores que adicionou a relatórios de despesas anteriores que são carregados em seu aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se o convidado anterior não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por nome ou alterne para pesquisar por organização, país ou cargo.
            2. Escolha **Concluído**.

        - Se você selecionou **Colega**, siga estas etapas:

            1. Selecione um ou mais colegas na lista. Você vê uma lista de colegas que são carregados no aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se seu colega não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise por nome ou alterne para pesquisar por empresa ou cargo.
            2. Escolha **Concluído**.

    3. Selecione o botão **Voltar** para retornar aos detalhes de despesas.

19. Se a política da empresa exigir que a despesa seja discriminada, selecione **Discriminar** e siga estas etapas:

    1. Selecione a primeira data para discriminar.
    2. Selecione **Adicionar discriminação**.
    3. Selecione a subcategoria de discriminação da despesa. Você vê uma lista de subcategorias de despesa que são carregadas no aplicativo para uso offline. Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número. Para obter mais informações, os desenvolvedores devem consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a sua subcategoria não estiver na lista, selecione **Pesquisar** para fazer uma pesquisa online. Pesquise pelo nome da subcategoria de despesas.
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
24. Selecione **Concluído**.

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Por que o aplicativo móvel de despesas não entra no método de pagamento por padrão?

As organizações podem personalizar a configuração do **método de pagamento padrão** para cada categoria de despesa ao criá-la. Além disso, ao configurar métodos de pagamento, você pode definir o campo **Método de pagamento padrão** como **Importar apenas**.

Quando **Importar apenas** estiver habilitado para um método de pagamento, o método de pagamento não será inserido por padrão. Ele fiará em branco em categorias de despesas em que este método de pagamento esteja configurado. Esse comportamento é consistente na experiência da Web e na experiência móvel.
    
Quando **Importar apenas** não estiver habilitado para um método de pagamento, o valor definido será inserido por padrão para as categorias de despesas em que esse método de pagamento esteja configurado. No entanto, há um problema conhecido em que o valor padrão não é inserido no aplicativo móvel de despesas. Para contornar esse problema, selecione manualmente um método de pagamento antes de salvar o relatório de despesas. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Por que não posso adicionar ou editar dimensões financeiras no aplicativo móvel de despesas?

A entrada de dimensões e distribuições não é compatível. Para contornar essa limitação, você pode definir esses campos por padrão no aplicativo móvel, configurando as dimensões financeiras padrão por projeto ou funcionário.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Por que às vezes vejo um erro de sincronização no aplicativo móvel de despesas?

Se as linhas de despesas não atenderem aos requisitos da política e o usuário enviar o relatório de despesas sem tratar do aviso da política, os dados móveis não serão sincronizados com o servidor e ocorrerá uma falha de sincronização. Todos os relatórios de despesas enviados após a ocorrência de uma falha de sincronização permanecerão em um estado de falha e causarão mais falhas de sincronização. A única forma de corrigir essa situação é excluir manualmente as notificações de sincronização. Esse problema foi solucionado, interrompendo o envio de relatórios de despesas quando os avisos de política não foram resolvidos; assim, evita-se os erros de sincronização.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Por que a validação do projeto e da categoria não é refletida corretamente no aplicativo móvel de despesas?

Não há suporte a essa validação no momento. No entanto, o suporte pode ser adicionado no futuro. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Quais tipos de documentos são compatíveis com o aplicativo móvel de despesas?

O aplicativo móvel de despesas oferece suporte apenas a imagens. Atualmente, ele não oferece suporte a PDFs ou outros documentos.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
