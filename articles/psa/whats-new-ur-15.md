---
title: Novidades ou alterações na Versão de Atualização 15 do Project Service Automation V3
description: Este artigo inclui informações sobre novidades na atualização do Project Service Automation versão 15, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: b87cae2cd8913457c2931d1661a57509d1398d29
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915630"
---
# <a name="project-service-automation-update-release-15-v3"></a>Versão de Atualização 15, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o orgulho de anunciar a versão mais recente do aplicativo Dynamics 365 Project Service Automation (PSA). Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e vá para a página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista os recursos e as correções novos ou alterados na atualização do PSA versão 15, V3. Esta versão tem um número de compilação de V3.10.5.28 e está geralmente disponível por meio de uma atualização automática em janeiro de 2020.

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
