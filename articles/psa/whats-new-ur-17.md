---
title: Novidades ou alterações na Versão de Atualização 17 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 17 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 70749646f5b67db3cf868a6d9a83c14dc490793a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585077"
---
# <a name="project-service-automation-update-release-17-v3"></a>Versão de Atualização 17, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.  Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e a página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 17. Esta versão tem um número de compilação V3.10.6.34 e está geralmente disponível por meio de uma atualização automática desde março de 2020.


## <a name="update-release-17"></a>Versão de Atualização 17

### <a name="bug-fixes"></a>Correções de bugs

**Geral**

- Corrigido: Atualizar Project Service Automation para aplicar as licenças do Membro da Equipe (o Hub do Recurso do Projeto incluirá metadados do plano do Serviço do Membro da Equipe 3.x)
 
**Hora e Despesa**

- Fixo: Não é possível alterar uma estimativa de despesa de um valor diferente de zero para zero (0). A alteração é ignorada.

**Gerenciamento de projetos**

- Corrigido: Uma verificação de valores nulos foi adicionada ao nome da posição de um membro da equipe.
- Corrigido: O campo **msdyn_userresourceid** na entidade **msdyn_resourceassignment** foi descontinuado.
- Corrigido: A atualização do 2.X para 3.X agora trata contornos de esforço vazios em atribuições de tarefas.

**Sales**

- Corrigido: **Invoice.PreValidateInvoiceUpdate** agora trata o cenário de reatribuir os proprietários dos registros corretamente.
- Corrigido: Quando a classe de transação for **Hora**, **UnitGroup** agora é editável para todas as entidades, incluindo **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** e **ContractLineDetails**. No entanto, **Unidade** não é editável apenas para **JournalLine** e **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
