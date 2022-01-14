---
title: Novidades ou alterações na Versão de Atualização 38 do Project Service Automation V3
description: Este tópico lista os recursos e as correções disponíveis na Versão de Atualização 38 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901479"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novidades ou alterações na Versão de Atualização 38 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas do Project Service Automation Versão de Atualização 38, V3. Esta versão tem um número de compilação de V3.10.59.117 e está geralmente disponível por meio de uma atualização automática em dezembro de 2021.

## <a name="update-release-38"></a>Versão de Atualização 38

### <a name="bug-fixes"></a>Correções de bug

Os seguintes problemas foram corrigidos.

**Tempo e Despesa**

- Uma exceção ocorre quando o comprimento dos logs do conjunto de aprovação excede 100.000 registros.
- Os usuários não podem acessar a grade **Entrada de Hora** na página principal **Entrada de Hora**.
- A caixa de diálogo **Importação de Entrada de Hora** não mostra nenhum texto quando nenhum item está qualificado para importação.
- Os usuários podem criar conjuntos de aprovação onde o campo **Status de Destino** é definido como **Desconhecido**.

**Gerenciamento de projetos**

- Os contornos não são mostrados corretamente nas atribuições de recursos para UTC (+09:30) e UTC (+10:00) quando o horário de verão é iniciado.
- O campo **Coluna adicional** para estruturas de detalhamento de trabalho está oculto em algumas localidades.
- O seletor de datas para o controle de calendário na grade **Tarefa do Projeto** não está localizado corretamente para chinês.

**Vendas**

- Os valores de **Desempenho do Contrato** e **Custo real do projeto** não correspondem quando recursos reserváveis que têm unidades de contratação e moedas diferentes enviam entradas de tempo.
- Um fluxo de trabalho personalizado para confirmar faturas automaticamente falha quando as faturas são importadas como uma solução gerenciada. A seguinte mensagem é mostrada: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Status da fatura inválida."
- Quando **Raiz** é selecionado como a opção de sumarização e o projeto tem estimativas de uma combinação de classes de transações (por exemplo, uma combinação de estimativas de tempo, despesas e materiais), o sistema resume as classes de transação como um único linha de taxa.
- Em cenários em que uma linha de despesa é adicionada antes de uma linha de contrato ser associada a um projeto, o preço correto não é inserido como valor padrão no campo **Atualizar Preços**.
- Valores de vendas negativos não são permitidos nas entidades **Projeto** e **Tarefa**.
