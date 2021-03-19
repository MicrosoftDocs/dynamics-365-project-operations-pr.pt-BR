---
title: Solucionar problemas de trabalho na grade de Tarefas
description: Este tópico fornece informações de solução de problemas necessárias ao trabalhar na grade de Tarefas.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286549"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Solucionar problemas de trabalho na grade de Tarefas 

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Este tópico descreve como corrigir problemas que você pode encontrar ao trabalhar com gerenciamento de custos.

## <a name="enable-cookies"></a>Ativar cookies

O Project Operations exige que os cookies de terceiros sejam habilitados para processar a estrutura de detalhamento de trabalho. Quando os cookies de terceiros não estão habilitados, em vez de ver as tarefas, você verá uma página em branco ao selecionar a guia **Tarefas** na página **Projeto**.

![Guia em branco quando os cookies de terceiros não estão habilitados](media/blankschedule.png)


### <a name="workaround"></a>Solução alternativa
Para os navegadores Microsoft Edge ou Google Chrome, os procedimentos a seguir descrevem como atualizar a configuração do seu navegador para habilitar cookies de terceiros.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Abra o navegador Microsoft Edge.
2. No canto superior direito, selecione as **reticências** (...) e, em seguida, **Configurações**.
3. Em **Cookies e permissões de site**, selecione **Cookies e dados do site**.
4. Desative **Bloquear cookies de terceiros**.

#### <a name="google-chrome"></a>Google Chrome

1. Abra o navegador Chrome.
2. No canto superior direito, selecione os três pontos verticais e depois selecione **Configurações**.
3. Em **Privacidade e segurança**, selecione **Cookies e outros dados do site**.
4. Selecione **Permitir todos os cookies**.

> [!IMPORTANT]
> Se você bloquear cookies de terceiros, todos os cookies e dados de sites de outros sites serão bloqueados, mesmo se o site for permitido em sua lista de exceções.

## <a name="pex-endpoint"></a>Ponto de Extremidade PEX

O Project Operations exige que um parâmetro do projeto faça referência ao Ponto de Extremidade PEX. Esse ponto de extremidade é necessário para se comunicar com o serviço usado para processar a estrutura de detalhamento de trabalho. Se o parâmetro não estiver habilitado, você receberá o erro "O parâmetro do projeto não é válido". 

### <a name="workaround"></a>Solução alternativa
 ![Campo Ponto de Extremidade PEX no parâmetro do projeto](media/projectparameter.png)

1. Adicione o campo **Ponto de Extremidade PEX** à página **Parâmetros do projeto**.
2. Atualize o campo com o seguinte valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Remova o campo da página **Parâmetros do projeto**.

## <a name="privileges-for-project-for-the-web"></a>Privilégios para projeto para a Web

O Project Operations conta com um serviço de agendamento externo. O serviço requer que um usuário tenha várias funções atribuídas para ler e gravar em entidades relacionadas à estrutura de detalhamento de trabalho. Essas entidades incluem tarefas de projeto, atribuições de recursos e dependências de tarefas. Se um usuário não puder renderizar a estrutura de detalhamento de trabalho quando for para a guia **Tarefas**, provavelmente é porque o projeto para o Project Operations não foi habilitado. Um usuário pode receber um erro de direito de acesso ou um erro relacionado a uma negação de acesso.


## <a name="workaround"></a>Solução alternativa

1. Vá para **Configurações > Segurança > Usuários > Usuários do Aplicativo**.  

   ![Leitor de aplicativo](media/applicationuser.jpg)
   
2. Clique duas vezes no nome de inscrição para verificar o seguinte:

 - O usuário tem acesso ao projeto: Essa verificação normalmente é feita garantindo que o usuário tenha o direito de acesso **Gerente de projeto**.
 - O usuário do aplicativo Microsoft Project existe e está configurado corretamente.
 
3. Se este usuário não existir, você poderá criar um novo registro de usuário. Selecionar **Novos usuários**. Altere o formulário de inscrição para **Usuário do aplicativo** e, em seguida, adicione o **ID do aplicativo**.

   ![Detalhes do usuário de inscrição](media/applicationuserdetails.jpg)

4. Verifique se o usuário recebeu a licença correta e se o serviço está habilitado nos detalhes dos planos de serviço da licença.
5. Verifique se o usuário consegue abrir project.microsoft.com.
6. Verifique por meio dos parâmetros do projeto se o sistema está apontando para o ponto de extremidade correto do projeto.
7. Verifique se o usuário de inscrição do projeto foi criado.
8. Aplique os seguintes direitos de acesso ao usuário:

  - Usuário do Dataverse
  - Sistema do Project Operations
  - Sistema do projeto

## <a name="error-when-updating-the-work-breakdown-structure"></a>Erro ao atualizar a estrutura de detalhamento de trabalho

Quando uma ou mais atualizações são feitas na estrutura de detalhamento de trabalho, as alterações eventualmente falham e não são salvas. Ocorre um erro na grade de agendamento, observando que "Não foi possível salvar as alterações recentes feitas por você."

### <a name="workaround"></a>Solução alternativa

1. Verifique se o usuário recebeu a licença correta e se o serviço está habilitado nos detalhes dos planos de serviço da licença.
2. Verifique se o usuário consegue abrir project.microsoft.com.
3. Verifique se o sistema está apontando para o ponto de extremidade correto do projeto,.
4. Verifique se o usuário de inscrição do projeto foi criado.
5. Aplique os seguintes direitos de acesso ao usuário:
  
  - Usuário ou usuário base do Dataverse
  - Sistema do Project Operations
  - Sistema do projeto
  - Sistema de gravação dupla do Project Operations (Esta função é necessária se você estiver implantando o cenário baseado em recursos/sem estoque do Project Operations.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]