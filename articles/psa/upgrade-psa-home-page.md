---
title: Home page de atualização
description: Este artigo mostra onde encontrar informações importantes sobre os recursos novos e alterados no Dynamics 365 Project Service Automation e o processo de atualização para a versão mais recente.
ms.prod: ''
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5dcf41af31a60b952ce82c08e3c082490d59d4f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926624"
---
# <a name="upgrade-home-page"></a>Home page de atualização

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Upgrade do PSA versão 2.x ou 1.x para a versão 3.x

### <a name="new-instances"></a>Novas instâncias

Desde 17 de maio de 2019, quando o Project Service Automation é selecionado durante o provisionamento de uma nova instância, a versão 3.x é instalada por padrão.

### <a name="existing-instances"></a>Instâncias existentes

Anteriormente, os clientes que possuem uma instância do PSA versão 2.xe precisavam atualizar para a versão 3.x, que é a versão do PSA baseado em UCI (Interface Unificada do Cliente), deviam entrar em Suporte da Microsoft com o suporte e fornecer os detalhes da instância, para que o suporte possa ativar a instância para atualização para a versão 3.x. A partir de 1º de março de 2020, os clientes que possuem uma instância do PSA versão 2.xe precisam atualizar para a versão 3.x, poderão atualizar suas instâncias diretamente do portal de administração sem precisar entrar em contato com o Suporte da Microsoft.  

> [!NOTE]
> O PSA versão 3.x inclui alterações significativas. Ele foi baseado na estrutura de Interface Unificada para ajudar a fornecer uma melhor experiência do usuário. O aplicativo recriado oferece uma interface do usuário consistente e uniforme e segue princípios de design responsivos para uma exibição ideal em qualquer tamanho de tela ou dispositivo. Houve outras alterações em todo o aplicativo. Algumas das áreas que foram alteradas incluem preços, reservas e designação de recursos, tempo, despesas e aprovações.

Antes de iniciar o processo de atualização, recomendamos que você conclua as seguintes tarefas:

- Verifique se o Dynamics 365 Field Service e o Project Service Automation estão instalados na instância identificada. Se as duas soluções estiverem instaladas, planeje atualizar as duas antes de retomar o uso regular da instância.
- Analise cuidadosamente os artigos a seguir. A conscientização e o reconhecimento das alterações entre as versões ajudarão você no processo de atualização. Estes artigos fornecem informações sobre as principais alterações no PSA, junto com considerações e recomendações para planejar a atualização para a versão 3.x.

    - [Novidades ou alterações no Project Service Automation versão 3](whats-new-changed-v3.md)
    - [Considerações sobre atualização - Project Service Automation versão 2.x ou 1.x para a versão 3](upgrade-v3.md)

- Atualize sua instância de área restrita para avaliar as alterações em sua implementação antes de atualizar sua instância de produção.

Depois de analisar os artigos mencionados antes e estar pronto para atualizar para o PSA versão 3.x ou a versão baseada em UCI, envie uma solicitação ao suporte da Microsoft para disponibilizar a atualização no Centro de Administração. Em sua solicitação, forneça os detalhes da sua instância.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Versões mais antigas do PSA (PSA versão 2.x) em uma instância recém-criada

Desde 17 de maio de 2019, todas as novas instâncias têm o UCI como cliente padrão. Para alinhamento com essa alteração, o PSA versão 3.xe e o Field Service versão 8.x serão provisionados por padrão, porque essas versões foram projetadas para funcionar com o cliente de UCI.

A partir de 1º de março de 2020, os clientes do Dynamics PSA não poderão mais criar um novo ambiente com versões anteriores do PSA, por exemplo, PSA versão 2.x ou inferior. Todos os novos ambientes serão para obter apenas a versão 3.x do PSA.

> [!NOTE]
> Para obter a melhor experiência ao usar versões mais antigas dos aplicativos Field Service e PSA, acesse a página **Configurações do sistema** e, no campo **Usar apenas a nova Interface Unificada (recomendado)**, selecione **Não**, já que essas versões não foram projetadas para serem carregadas corretamente na UCI. Depois de desativar a UCI, você pode abrir e executar essas versões do Field Service e PSA usando o cliente da Web antigo. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
