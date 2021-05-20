---
title: Novidades ou alterações na Versão de Atualização 15 do Project Service Automation V3
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado na Versão da Atualização 15 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: fe1e2b2046faeee4e4c71484a976d70e8722e090
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949305"
---
# <a name="project-service-automation-update-release-15-v3"></a>Versão de Atualização 15, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o orgulho de anunciar a versão mais recente do aplicativo Dynamics 365 Project Service Automation (PSA). Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e vá para a página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 15. Esta versão tem um número de compilação de V3.10.5.28 e está geralmente disponível por meio de uma atualização automática em janeiro de 2020.

## <a name="update-release-15"></a>Versão de Atualização 15 

### <a name="enhancements"></a>Aprimoramentos

- Gerenciamento de projetos

### <a name="bug-fixes"></a>Correções de bugs

- Tempo e Despesa

  - Corrigido: Tratamento de erro de carregamento de complementos na exibição de reconciliação.
  - Corrigido: Hub de Recursos do Projeto: Renomear **Valor** para evitar ambiguidade.
  - Corrigido: Ajustar a exibição **Copiar Colunas de Entrada de Hora** para incluir o tipo.
  - Corrigido: Editar a duração da entrada de hora na exibição em grade usando números decimais resulta em erro desconhecido para alguns números.

- Gerenciamento de projetos

  - Corrigido: O menu suspenso para **Usar na Exibição de Rastreamento** agora expande com base na largura das opções.
  - Corrigido: Ao gerenciar projetos no fuso horário +13, os cálculos das tarefas podem exibir resultados imprecisos.
  - Corrigido: **Horário de Término do Membro da Equipe** foi corrigido ao usar um calendário de 24 horas.
  - Corrigido: **BPF** reativado no formulário principal **msdyn_project**.
  - Corrigido: O cálculo das atribuições não ignoram mais um dia.
  - Corrigido: Um novo banner de notificações foi adicionado ao formulário do projeto quando o fuso horário difere entre usuário e projeto.

- Sales

  - Corrigido: A pesquisa de categoria de estimativa de despesas pode ser usada para filtrar duplicatas.
  - Corrigido: O código em **PluginDomain.ExecuteInTryCatchBlock(..)** não oculta mais a origem da exceção.
  - Corrigido: Não é mais exibida uma mensagem de erro em **Pesquisa de projeto** no formulário **Linha da cotação** quando há mais de 1000 projetos.
  - Corrigido: A grade **Estimativas** para estimativas de mão-de-obra e de despesas agora exibe o símbolo correto da moeda.
  - Corrigido: Depois que uma organização atualiza o PSA da Versão de Atualização 14 para a Versão de Atualização 15, a guia **Agendar** não aparece mais em branco no formulário **Projeto**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]