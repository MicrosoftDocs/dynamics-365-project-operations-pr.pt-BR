---
title: Novidades ou alterações na Versão de Atualização 30 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 30 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 07ca20425d05d1d638d9b2b8c3425562e39dd6627916794d1ad8441f00658459
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986972"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Novidades ou alterações na Versão de Atualização 30 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution.md).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 30. Esta versão apresenta o número de build V3.10.51.61 e geralmente está disponível por meio de uma atualização automática de abril de 2021.

## <a name="update-release-30"></a>Versão de Atualização 30

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

Os seguintes problemas foram corrigidos:

- Ocorrerá um erro quando você criar e salvar uma entrada de tempo na página **Criação Rápida** se o campo **Função** for removido.
- O filtro de entrada de tempo aplica o operador de filtro errado.
- As planilhas de horas copiadas não são exibidas automaticamente quando você seleciona **Copiar Semana** no controle de entrada de tempo.

**Gerenciamento de Recursos**

Os seguintes problemas foram corrigidos:

- Quando você estende uma reserva, o status de reserva atribuído à reserva definitiva fica incorreto. A extensão de uma reserva respeita o status de reserva definido como **Confirmado** nos metadados de configuração de reserva.
- Quando um status de reserva válido não é especificado, a mensagem de erro não é localizada corretamente.

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- Os projetos não podem ser criados em uma moeda e incluem tarefas relacionadas em outra moeda.

**Vendas**

Os seguintes problemas foram corrigidos:

- Quando uma lista de preços é copiada, os preços não são atualizados.
- Fechar uma cotação como ganha falha quando o detalhe de custo tem um valor de origem.
- Na entidade **Tarefa do Projeto**, o **Custo Estimado** foi renomeado como **Custo Planejado (Base)**.
- Uma exceção de referência nula é gerada quando faturas são criadas ou excluídas.
