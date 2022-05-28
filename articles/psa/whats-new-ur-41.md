---
title: Novidades ou alterações na Versão de Atualização 41 do Project Service Automation V3
description: Este tópico lista os recursos e as correções disponíveis na Versão de Atualização 41 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580902"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novidades ou alterações na Versão de Atualização 41 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas do Project Service Automation Versão de Atualização 41, V3. Esta versão tem um número de compilação da V3.10.62.162 e está geralmente disponível por meio de uma atualização automática em março de 2022.

## <a name="update-release-41"></a>Versão de Atualização 41

### <a name="bug-fixes"></a>Correções de bug

Os seguintes problemas foram corrigidos.

**Gerenciamento de projetos**
- Quando você tenta criar um projeto a partir de um modelo baseado em um projeto criado a partir do suplemento da área de trabalho, o seguinte erro é exibido: "Validação do campo Trabalho Planejado da Atribuição de Recurso: a Data de Término de Cada Fração de Tempo de Atribuição de Recurso não deve ser anterior à Data de Início".

**Tempo e Despesa**
- Quando você tenta excluir uma entrada de hora, a seguinte mensagem de erro é exibida: "Ocorreu um erro inesperado do código ISV".

**Vendas**
- Ao criar uma fatura para uma etapa de preço fixo, os campos **Descrição** e **Descrição Externa** não são preenchidos. 
