---
title: Novidades ou alterações na Versão de Atualização 31 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 31 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 70a8bd381c27c9a3dd3b33c582e5616fad280e95
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586744"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Novidades ou alterações na Versão de Atualização 31 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 31. Esta versão apresenta o número de compilação V3.10.52.77 e está disponível para o público em geral por meio de uma atualização automática de maio de 2021.

## <a name="update-release-31"></a>Versão de Atualização 31

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

Os seguintes problemas foram corrigidos:

- Os botões de comando de controle de entrada de hora na página **Recurso Reservável** eram confusos.
- Uma exceção de referência nula foi gerada em **Project.SetTrackingFields** ao aprovar uma entrada de hora.

**Gerenciamento de Recursos**

Os seguintes problemas foram corrigidos:

- **Criar Membro da Equipe** não exibe corretamente a configuração de metadados de configuração de reserva para **Status Comprometido de Reserva Padrão**.
- Ao atualizar de PSA 1.X para 3.X, há falha no processo de atualização em **UpgradeResourceRequirements**.


**Vendas**

Os seguintes problemas foram corrigidos:

- A receita real converte os valores para a moeda do projeto na grade de rastreamento.
- O padrão da moeda não fica claro durante a criação de linhas do diário, linhas de cotação e linhas de contrato em cenários em que a moeda base de uma organização é diferente da moeda do projeto.
- A consulta **Validação do diário de correção pendente** não filtra por projeto.
- As vendas restantes são calculadas incorretamente em um projeto.
- Há falha nas cotações baseadas em um contato quando são criadas sem uma lista de preços.
- Nenhum controle giratório de processamento é exibido ao selecionar **Confirmar fatura**.
- Nenhum controle giratório de processamento é exibido ao selecionar **Criar fatura**.
- Fechar uma cotação como perdida não cancela as reservas.







