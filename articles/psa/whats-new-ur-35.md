---
title: Novidades ou alterações na Versão de Atualização 35 do Project Service Automation V3
description: Este artigo lista os recursos e as correções disponíveis na atualização do Microsoft Dynamics 365 Project Service Automation versão 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912824"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Novidades ou alterações na Versão de Atualização 35 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista os recursos e as correções novos ou alterados na atualização do Project Service Automation versão 35, V3. Esta versão tem um número de compilação de V3.10.56.110 e geralmente fica disponível por meio de uma atualização automática em setembro de 2021.

## <a name="update-release-35"></a>Versão de Atualização 35

### <a name="bug-fixes"></a>Correções de bug

Os seguintes problemas foram corrigidos.

**Tempo e Despesa**

- O aprovador do projeto recebe um erro de privilégio de leitura ao aprovar entradas de despesas com uma função **Aprovador de Projeto**.
- O aprovador do projeto recebe um erro de privilégio de gravação em **msdyn_projectapproval** quando cancela uma entrada de tempo aprovada com uma função **Aprovador de Projeto**.
- Quando você seleciona **Copiar semana** em uma entrada de tempo no módulo do aplicativo Dynamics 365 para telefones - Hub de Recursos do Projeto, ocorre o seguinte erro: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- A política **Tentar novamente** aprova de forma automática entradas que foram rejeitadas anteriormente.
- A subgrade **Conjuntos de Aprovações** mostra ações não aplicáveis da faixa de opções.
- Há ícones ausentes para **Tarefa do Projeto** e **Função do Recurso** na entidade **Entrada de Tempo**.
- Quando você importa atribuições de recursos, as entradas de tempo importadas não têm a duração correta para atribuições que foram criadas por meio de tarefas de modo manual.
- **Excluir** está ausente da página **Pesquisa Avançada para registros de Entrada de Tempo**.
- **Salvar** está ausente da página **Informação de entrada de tempo**. Este problema impede que as alterações sejam salvas quando a página é fechada.

**Planejamento do projeto**

- As grades **Atribuição de Recursos** e **Reconciliação de Recursos** não classificam os atributos agrupados em ordem alfabética.
- As tarefas não poderão ser criadas se o comportamento da data estiver personalizado para **Somente Data**.

**Gerenciamento de recursos**

- Se o Dynamics 365 Field Service e Project Service Automation estiverem instalados, os problemas de sobreposição ocorrerão quando **Exibição Associada de Requisito de Recurso** estiver associado a uma página principal.
- Clicar duas vezes em **Salvar** na caixa de diálogo **Criação Rápida de Membro de Equipe** impedirá que o requisito de recurso seja criado.

**Vendas**

- Uma exceção será gerada se você excluir uma tarefa associada a uma cotação com um status **Ganho**.
