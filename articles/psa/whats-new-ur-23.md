---
title: Novidades ou alterações na Versão de Atualização 23 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 23 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: adf893a0627ae59f2132bb46686110dafda01d3d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006452"
---
# <a name="project-service-automation-update-release-23-v3"></a>Versão de Atualização 23, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 23. Esta versão tem um número de build V 3.10.34.30 e foi disponibilizada para o público em geral por meio de uma atualização automática em agosto de 2020.

## <a name="update-release-23"></a>Versão de Atualização 23

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

Os seguintes problemas foram corrigidos:
- Lide com um caso de borda em **Exclusão de Membro da Equipe de Projeto** para fornecer uma exceção significativa.
- A importação de atribuição resulta em uma tela de remoção em branco.

**Gerenciamento de Recursos**

Os seguintes problemas foram corrigidos:

- O **Cartão de recursos da grade de utilização de recursos** mostra dados incorretos quando a escala de tempo é superior a cinco dias.
- Quando os clientes criam um recurso reservável, o plug-in falha de forma intermitente ao adicionar automaticamente o recurso a um grupo do Microsoft Office 365.
- A exibição **Reconciliação** mostra os contornos manuais incorretamente na exibição **Semana** ou **Mês**.

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- Um número excessivo de entidades **RetrieveMultiple para usersettings** estão causando degradação do desempenho para aprovações de projetos e outras operações.
- A pesquisa de recursos de grade **Planejamento de Tarefas** limita-se a mostrar apenas até cinco membros da equipe de projeto. 
- A pesquisa de recursos de grade **Planejamento de Tarefas** não filtra recursos inativos.
- O modo manual não está funcionando como esperado na estrutura de detalhamento de trabalho do planejamento de projeto.
- A grade **Planejamento de Tarefas** mostra **Categorias de Transações Inativas**.
- A grade **Atribuição de Recursos** é arredondada incorretamente quando uma tarefa tem várias atribuições.
- Os valores de arredondamento são diferentes entre o custo planejado e o custo real para uma única tarefa.

**Sales**

Os seguintes problemas foram corrigidos:

- Dar um clique duplo em **Obter Todas as Categorias de Transação** cria várias linhas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]