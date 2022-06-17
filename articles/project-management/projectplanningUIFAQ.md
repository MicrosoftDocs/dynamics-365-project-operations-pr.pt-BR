---
title: Solucionar problemas de trabalho na grade de Tarefas
description: Este artigo apresenta informações sobre a solução de problemas necessárias ao trabalhar na grade de tarefas
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911030"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Solucionar problemas de trabalho na grade de Tarefas 


_**Aplicável a:** Project Operations para cenários baseados em recursos/sem estoque, Implantação leve – para realizar o faturamento, Project for the Web_

A grade de Tarefas utilizada pelo Dynamics 365 Project Operations é um iframe hospedado no Microsoft Dataverse. Como resultado desse uso, requisitos específicos devem ser atendidos para garantir que a autenticação e a autorização estejam funcionando corretamente. Este artigo descreve os problemas comuns que podem impactar a capacidade de renderizar a grade ou gerenciar tarefas na estrutura de detalhamento de trabalho (WBS).

Problemas comuns incluem:

- A guia **Tarefa** na grade de Tarefas está vazia.
- Ao abrir o projeto, ele não carrega, e a interface do usuário (IU) fica travada no botão giratório.
- Administração de privilégios do **Project for the Web**.
- As alterações não são salvas quando você cria, atualiza ou exclui uma tarefa.

## <a name="issue-the-task-tab-is-empty"></a>Problema: a guia Tarefa está vazia

### <a name="mitigation-1-enable-cookies"></a>Mitigação 1: habilitar cookies

O Project Operations exige que os cookies de terceiros sejam ativados para renderizar a estrutura de detalhamento do projeto. Quando os cookies de terceiros não estão habilitados, em vez de ver as tarefas, você verá uma página em branco ao selecionar a guia **Tarefas** na página **Projeto**.

Para os navegadores Microsoft Edge ou Google Chrome, os procedimentos a seguir descrevem como atualizar a configuração do seu navegador para habilitar cookies de terceiros.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Abra o navegador Microsoft Edge.
2. No canto superior direito, selecione as **reticências** (...) e, em seguida, **Configurações**.
3. Em **Cookies e permissões de site**, selecione **Cookies e dados do site**.
4. Desative **Bloquear cookies de terceiros**.
5. Atualize seu navegador. 

#### <a name="google-chrome"></a>Google Chrome

1. Abra o navegador Chrome.
2. No canto superior direito, selecione os três pontos verticais e depois selecione **Configurações**.
3. Em **Privacidade e segurança**, selecione **Cookies e outros dados do site**.
4. Selecione **Permitir todos os cookies**.
5. Atualize seu navegador. 

> [!NOTE]
> Se você bloquear cookies de terceiros, todos os cookies e dados de sites de outros sites serão bloqueados, mesmo se o site for permitido em sua lista de exceções.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Mitigação 2: verificar se o ponto de extremidade PEX foi configurado corretamente

O Project Operations exige que um parâmetro do projeto faça referência ao Ponto de Extremidade PEX. Esse ponto de extremidade é necessário para estabelecer comunicação com o serviço usado para renderizar a estrutura de detalhamento de trabalho. Se o parâmetro não estiver habilitado, você receberá o erro "O parâmetro do projeto não é válido". Para atualizar o ponto de extremidade PEX, conclua estas etapas.

1. Adicione o campo **Ponto de Extremidade PEX** à página **Parâmetros do projeto**.
2. Identifique o tipo de produto que você está usando. Esse valor é usado quando o Ponto de Extremidade PEX é definido. Após a recuperação, o tipo de produto já está definido no Ponto de Extremidade PEX. Mantenha esse valor.
3. Atualize o campo com o seguinte valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. A tabela a seguir fornece o parâmetro de tipo que deve ser usado com base no tipo de produto.

      | **Tipo de produto**                     | **Tipo de parâmetro** |
      |--------------------------------------|--------------------|
      | Project for the Web na organização padrão   | type=0             |
      | Project for the Web na organização chamada CDS | type=1             |
      | Project Operations                   | type=2             |

4. Remova o campo da página **Parâmetros do projeto**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Mitigação 3: entrar em project.microsoft.com
No navegador Microsoft Edge, abra uma nova guia, vá para project.microsoft.com e entre com a mesma função de usuário que você está usando para acessar o Project Operations.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problema: o projeto não carrega e a IU está travada no botão giratório

Para fins de autenticação, os pop-ups devem ser ativados para que a grade de Tarefas seja carregada. Se os pop-ups não estiverem ativados, a tela ficará travada no botão giratório de carregamento. O gráfico a seguir mostra o URL com um rótulo pop-up bloqueado na barra de endereços, o que faz o botão giratório travar ao tentar carregar a página. 

   ![Botão giratório e bloco pop-up travados.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Mitigação 1: habilitar pop-ups

Quando seu projeto está travado no botão giratório, é possível que os pop-ups não estejam ativados.

#### <a name="microsoft-edge"></a>Microsoft Edge

Existem duas maneiras de habilitar pop-ups no navegador Edge.

1. No navegador Edge, selecione a notificação no canto superior direito do navegador.
2. Selecione **Sempre permitir pop-ups e redirecionamentos de** um ambiente específico do Dataverse.
 
     ![Os pop-ups bloquearam a janela.](media/enablepopups.png)

Como alternativa, você pode concluir estas etapas.

1. Abra o navegador Microsoft Edge.
2. No canto superior direito, selecione as **reticências** (...) e selecione **Configurações** > **Permissões do site** > **Pop-ups e redirecionamentos**.
3. Desative a opção **Pop-ups e redirecionamentos** para bloquear pop-ups ou ative para permitir pop-ups no dispositivo.
4. Depois de habilitar pop-ups, atualize seu navegador. 

#### <a name="google-chrome"></a>Google Chrome
1. Abra o navegador Chrome.
2. Navegue até uma página onde os pop-ups estão bloqueados.
3. Na barra de endereços, selecione **Pop-up bloqueado**.
4. Selecione o link do pop-up que deseja ver.
5. Depois de habilitar pop-ups, atualize seu navegador. 

> [!NOTE]
> Para ver sempre os pop-ups do site, selecione **Sempre permitir pop-ups e redirecionamentos de [site]** e selecione **OK**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problema 3: administração de privilégios do Project for the Web

O Project Operations conta com um serviço de agendamento externo. O serviço requer que um usuário tenha várias funções atribuídas que lhe permita ler e escrever para entidades relacionadas à WBS. Essas entidades incluem tarefas de projeto, atribuições de recursos e dependências de tarefas. Se um usuário não puder renderizar a WBS ao navegar para a guia **Tarefas**, poderá ser porque a opção **Projeto** não foi ativada para o **Project Operations**. Um usuário pode receber um erro de direito de acesso ou um erro relacionado a uma negação de acesso.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Mitigação 1: valide o usuário do aplicativo e o direito de acesso de usuário final

1. Acesse **Configurações** > **Segurança** > **Usuários** > **Usuários do Aplicativo**.  

   ![Leitor de aplicativo.](media/applicationuser.jpg)
   
2. Clique duas vezes no registro do usuário do aplicativo para verificar:

     - O usuário tem acesso ao projeto: Você pode fazer isso verificando se o usuário tem o direito de acesso de **Gerente de projeto**.
     - O usuário do aplicativo Microsoft Project existe e está configurado corretamente.
 
3. Se este usuário não existir, crie um novo registro de usuário. 
4. Selecione **Novos usuários**, mude o formulário de inscrição para **Usuário do aplicativo** e adicione o **ID do aplicativo**.

   ![Detalhes do usuário de inscrição.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problema 4: as alterações não são salvas quando você cria, atualiza ou exclui uma tarefa

Quando você faz uma ou mais atualizações na WBS, as alterações apresentam erros e não são salvas. Ocorre um erro na grade de programação com a mensagem: "Não foi possível salvar suas alterações recentes".

### <a name="mitigation-1-validate-the-license-assignment"></a>Mitigação 1: validar a atribuição da licença

1. Verifique se o usuário recebeu a licença correta e se o serviço está habilitado nos detalhes dos planos de serviço da licença.  
2. Verifique se o usuário consegue abrir **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Mitigação 2: configuração de validação do usuário do aplicativo do Project
1. Verifique se o usuário do aplicativo Project foi criado.
2. Aplique os seguintes direitos de acesso ao usuário:
  
  - Usuário ou usuário base do Dataverse
  - Sistema do Project Operations
  - Sistema do Projeto
  - Sistema de Gravação Dupla do Project Operations. Essa função é necessária para o cenário de implantação baseados em recursos/sem estoque do Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
