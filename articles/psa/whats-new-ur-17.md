---
title: Novidades ou alterações na Versão de Atualização 17 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 17 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: bb93208217972639f91b39b7b6705d9897373ef7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126784"
---
# <a name="project-service-automation-update-release-17-v3"></a>Versão de Atualização 17, do Project Service Automation V3

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.  Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e a página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

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


