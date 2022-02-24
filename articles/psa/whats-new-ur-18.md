---
title: Novidades ou alterações na Versão de Atualização 18 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 18 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147189"
---
# <a name="project-service-automation-update-release-18-v3"></a>Versão de Atualização 18, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e a página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 18. Esta versão apresenta o número de build V3.10.8.12 e geralmente está disponível por meio de uma atualização automática de abril de 2020.

## <a name="update-release-18"></a>Versão de Atualização 18

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

- Corrigido: os fluxos **Recuperar**, **Solicitar** e **Cancelar Aprovação** lançam exceções com mensagens de erro pouco claras.
- Corrigido: quando **Cancelar Aprovação** falha em uma despesa, um erro de exceção relevante não é lançado.
- Corrigido: a grade de Entrada de Horário trata incorretamente os dias não úteis na Austrália após a troca do horário de verão (DST) em outubro.
- Corrigido: a lógica padrão incorreta impede o envio de despesas.
- Corrigido: quando ocorre falha na aprovação de entrada de horário, a aprovação permanece em estado **Pendente**.
- Corrigido: erros de SQL em aprovações em massa (deadlock/tempo limite).
- Corrigido: problemas significativos de desempenho na experiência do usuário causados pela atualização de membros da equipe ao aprovar entradas de horário.

**Gerenciamento de projetos**

- Corrigido: notificação de fuso horário movida da exibição **Reconciliação** para o formulário principal **Projeto**.
- Corrigido: o modelo de calendário não está sendo padronizado corretamente quando um novo formulário de projeto é aberto.
- Corrigido: para navegadores baseados em cromo, os usuários não conseguem selecionar facilmente as tarefas anteriores a serem excluídas.
- Corrigido: criar ou copiar **Projeto do Modelo Vazio** busca atribuições não relacionadas.
- Corrigido: em casos de externos específicos, a criação de uma nova atribuição a partir da grade de tarefas resulta na criação de registros duplicados.
- Corrigido: no modo manual, os usuários não conseguem atualizar as datas de início da tarefa para serem posteriores à data atual salva.

**Gerenciamento de Recursos**

- Corrigido: a linha do subtotal da exibição **Reconciliação** calcula incorretamente a variação das reservas após estender as reservas.
- Corrigido: a exibição **Reconciliação** mostra incorretamente as atribuições de recurso quando o recurso que pode ser reservado tem um calendário que não corresponde ao calendário do projeto.

**Sales**

- Corrigido: quando as entradas de horário são aprovadas novamente (**Aprovar > Cancelar >** aprovar novamente), uma duplicata real não cobrável é criada.
