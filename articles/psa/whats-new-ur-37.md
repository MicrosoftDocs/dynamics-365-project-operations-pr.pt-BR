---
title: Novidades ou alterações na Versão de Atualização 37 do Project Service Automation V3
description: Este tópico lista os recursos e as correções disponíveis na Versão de Atualização 37 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727591"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novidades ou alterações na Versão de Atualização 37 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas do Project Service Automation Versão de Atualização 37, V3. Esta versão tem um número de build V3.10.58.120 e está geralmente disponível por meio de uma atualização automática em novembro de 2021.

## <a name="update-release-37"></a>Versão de Atualização 37

### <a name="bug-fixes"></a>Correções de bugs

Os seguintes problemas foram corrigidos.

**Tempo e Despesa**
- Os usuários não podem excluir uma entrada de tempo ao limparem a célula.
- A exibição **Minha aprovação com falha** contém apenas aprovações de projetos com um status **Enviado**.

**Gerenciamento de projetos**
- Os usuários recebem um erro de exceção de referência nula ao abrir um projeto no suplemento da área de trabalho da Microsoft se o nome da posição do membro da equipe do Projeto estiver vazio.
- Não há botão **Salvar** na página **Tarefa do Projeto** e, portanto, os usuários não poderão salvar alterações nos registros de tarefas.
- Os usuários não podem excluir um projeto com uma tarefa associada a uma cotação com um status **Ganho**.

**Vendas**
- O moeda **Moeda** na página **Projeto** é atualizada para corresponder à moeda do modelo aplicado.
- O custo é calculado incorretamente em tarefas com várias moedas.
