---
title: Novidades ou alterações na Versão de Atualização 25 do Project Service Automation V3
description: Este artigo lista os recursos e as correções disponíveis na atualização do Project Service Automation versão 25, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2330c7dc5d2dfb148d5c7fb9a5ce643fded84dde
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922530"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Novidades ou alterações na Versão de Atualização 25 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista os recursos e as correções que são novos ou alterados para a atualização do Project Service Automation versão 25, V3. Esta versão tem um número de build V 3.10.43.76 e foi disponibilizada para o público em geral por meio de uma autoatualização em outubro de 2020.

## <a name="update-release-25"></a>Versão de Atualização 25

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

O seguinte problema foi corrigido:

- O gráfico de entrada de tempo mostrando dados adicionais baseados em um intervalo muito grande sendo recuperado.

**Gerenciamento de Recursos**

O seguinte problema foi corrigido:

- Código do package deployer adicionado para ignorar a importação de patch do Universal Resource Scheduling caso já exista um patch de versão superior.

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- Arredondamento corrigido e discrepâncias da taxa de câmbio resultando em custo planejado incorreto na grade de rastreamento do projeto.
- Compatível com a exibição de duas ou mais grades de reação no formulário do **Projeto**.
- Validação fornecida para abordar a capacidade de atribuir uma tarefa após a data de término do calendário, resultando na falha de atribuição de recursos.
- Melhoria no tratamento de erros para abordar a Exceção de Referência Nula gerada a partir do seguinte:

    - Plug-in **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** quando uma tarefa de projeto é criada sem um projeto associado
    - Plug-in **PreProjectTeamMemberCreate**
    - Plug-in **PostProjectTeamMemberDelete**
    - Plug-in **PreValidateProjectTaskDelete**

**Sales**

Os seguintes problemas foram corrigidos:

- Melhoria do tratamento de erros para abordar as Exceções de Referência Nula geradas de **Copiar Projeto: Gerenciamento de Estimativas do HelperResource**.
- **Não pronto para faturamento** em um **Registro Acumulado de Hora e Material** não limpa o status de cobrança.
- Correção dos botões **Preços** incorretamente rotulados na guia **Preço da Função** e **Itens de Catálogo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
