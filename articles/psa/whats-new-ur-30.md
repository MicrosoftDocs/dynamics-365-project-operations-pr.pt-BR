---
title: Novidades ou alterações na Versão de Atualização 30 do Project Service Automation V3
description: Este artigo lista os recursos e as correções disponíveis na atualização do Project Service Automation versão 30, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ad00b126a13e18a5de47df335aea06b9690efa13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925060"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Novidades ou alterações na Versão de Atualização 30 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista os recursos e as correções novos ou alterados na atualização do Project Service Automation versão 30, V3. Esta versão apresenta o número de build V3.10.51.61 e geralmente está disponível por meio de uma atualização automática de abril de 2021.

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
