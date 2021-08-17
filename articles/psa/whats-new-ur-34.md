---
title: Novidades ou alterações na Versão de Atualização 34 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 34 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 1c8ef43b953ad282a1f5fed6eeeb1e1a991e715100b66938be03b5b5f3da575e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009742"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novidades ou alterações na Versão de Atualização 34 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 34. Esta versão tem um número de compilação de V3.10.55.38 e geralmente fica disponível por meio de uma atualização automática em julho de 2021.

## <a name="update-release-34"></a>Versão de Atualização 34

### <a name="bug-fixes"></a>Correções de bug
Os seguintes problemas foram corrigidos.

**Geral**

- As atualizações controladas pelo editor não ativam o novo fluxo de trabalho de aprovação moderno.
- Os atributos **Status de Destino** e **Tipo de Ação** estão ausentes na página principal **Conjunto de Aprovações**.

**Tempo e Despesa**

- Não é possível aprovar uma solicitação de recuperação usando o fluxo de aprovação moderno.
- Copiar uma semana de entradas de hora não funciona quando as entradas não estão relacionadas ao usuário conectado.

**Planejamento do projeto**

- Os contornos de atribuição de recursos são corrompidos ao importar a partir do suplemento da área de trabalho do Microsoft Project.

**Gerenciamento de recursos**

- Quando você publica um projeto do suplemento de cliente da área de trabalho do Microsoft Project, a data de término dos requisitos existentes é alterada.
- A precisão decimal excede duas casas decimais na caixa de diálogo de confirmação de extensão de reservas.

**Vendas**

- Quando você adiciona uma linha baseada em produto com um produto existente a um contrato de projeto, uma exceção **chave não encontrada no dicionário** é exibida.
- Clientes potenciais não podem ser qualificados quando um tipo de ordem é mapeado de um cliente potencial para uma oportunidade.
