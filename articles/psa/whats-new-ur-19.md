---
title: Novidades ou alterações na Versão de Atualização 19 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 19 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280699"
---
# <a name="project-service-automation-update-release-19-v3"></a>Versão de Atualização 19, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 19. Esta versão apresenta o número de compilação V3.10.30.41 e está disponível para o público em geral por meio de uma atualização automática de maio de 2020.

## <a name="update-release-19"></a>Versão de Atualização 19

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

Os seguintes problemas foram corrigidos: 

- Erros derivados de importações de entrada de horas não são apresentados corretamente.
- A Grade de entrada de horas não oferece suporte ao comportamento de campo **Somente Data**.
- Os Recursos do Projeto não conseguem criar uma despesa com um projeto.

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos: 

-  A tarefa neto causa uma estimativa de esforço incorreta durante o cálculo de conclusão (EAT).

**Sales**

Os seguintes problemas foram corrigidos: 

- A ação **Recalcular** não funciona com os detalhes da linha do contrato de despesa ou com os detalhes da linha de cotação.
- **Atualizar Preços** está ausente para estimativas de despesas.
-  Os clientes não podem selecionar razões do status do contrato personalizadas na página **Contrato do Projeto**.
- Os clientes sofrem uma degradação no desempenho ao criar uma lista de preços personalizada a partir de uma cotação.
- Os clientes sofrem inconsistências com **unidades** padrão nas páginas **Detalhes da linha de cotação** e **Detalhes da linha do contrato**.
- Adicionar itens de categoria de transação não passível de cobrança a uma linha de contrato passível de cobrança não respeitará o tipo de cobrança **Não Passível de Cobrança** da categoria de transação.
- Os clientes não podem usar as funções e a categoria recém-adicionadas em contratos criados anteriormente.
- Os clientes sofrem uma degradação no desempenho Recuperação desnecessária em PreValidateProjectTeamMemberUpdate.cs
- Funções configuradas como não passíveis de cobrança na lista **Categorias de Recursos** devem ser adicionadas à guia **Funções Passíveis de Cobrança** como **Não Passível de Cobrança** na linha do contrato de um projeto.
- Os clientes podem sofrer uma degradação no desempenho ao criar um projeto porque **GetBookableResourceIdFromUser** recupera todas as colunas de recursos reserváveis em vez de apenas o ID principal.
- Entidade **TransactionType** ausente do plug-in de atualização de pré-validação para impedir que os usuários insiram **Unidades** e **UnitGroups** que não são válidos para os tipos de transação.
- A etapa **Retirar** não funciona para a importação de entrada de horas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]