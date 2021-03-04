---
title: Novidades em fevereiro de 2021 – Project Operations para cenários baseados em recursos/sem estoque
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de fevereiro de 2021 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ba44ea471f7d72d1e816ec74de304d3fdcf1f68
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141285"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em fevereiro de 2021 – Project Operations para cenários baseados em recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations no ambiente do Dataverse 4.7.0.95
- Gerenciamento e contabilidade de projeto no ambiente do Dynamics 365 Finance versão 10.0.16 

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área do Recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| **Cobrança e preço** | 2053736 | Os detalhes da linha da fatura agora podem ser acessados em **Fatura** > **Informações relacionadas**. |
| **Cobrança e preço** | 2122613 | As ações **Ativar** e **Desativar** foram removidas das entidades de associação **Lista de Preços**. |
| **Cobrança e preço** | 2128606 | O problema no **ullReferenceException** no plug-in **GetEstimatesForProject** foi resolvido. |
| **Implantação e configuração** | 2139346 | O problema com a importação não gerenciada da solução **Dynamics365ProjectOperationsDualWrite** foi resolvido. |
| **Implantação e configuração** | 2140569 | A solução do projeto não deve estar instalada nos ambientes do Dataverse Teams. |
| **Implantação e configuração** | 2086991 | Localização de personalização restrita de recursos da web. |
| **Gerenciamento de Oportunidades** | 2136794 | Exibir a mensagem de erro correta se houver falha nos processos **Confirmar fatura** ou **Marcar fatura como paga**. |
| **Gerenciamento de Oportunidades** | 2139330 | Alterar o gerente de Projeto não deve redefinir a empresa proprietária de volta para o valor padrão. |
| **Gerenciamento de Oportunidades** | 2146376 | O valor do imposto corrigido em um dado real não passível de cobrança é criado na confirmação da fatura. |
| **Planejamento e acompanhamento de projeto** | 2099879 | A implantação do ambiente do Dataverse deve criar uma categoria de transação padrão com ID estático e não gerar um por ambiente aleatoriamente. |
| **Planejamento e acompanhamento de projeto** | 2128577 | Os privilégios de usuário do Project Service para atualizar a categoria de transação em uma atribuição de recurso foram corrigidos. |
| **Planejamento e acompanhamento de projeto** | 2164035 | Problemas corrigidos com a função **Copiar Projeto**. |
| **Entrada de hora** | 2129161 | Restrições mais rígidas são aplicadas para garantir que os usuários não possam alterar e atualizar uma entrada de tempo que foi enviada ou aprovada. |
| **Entrada de hora** | 2103572 | A aprovação de tempo para entradas de hora não relacionadas ao projeto não deve procurar a função de aprovador do projeto. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Visão geral de gerenciamento e contabilidade de projeto no Dynamics 365 Finance 

Para obter mais informações sobre Gerenciamento e contabilidade de projeto no Dynamics 365 Finance, consulte [Novidades em janeiro de 2021 – Project Operations para cenários baseados em recursos/sem estoque](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Atualizações regulatórias

Para obter informações sobre atualizações regulatórias do Finance and Operations, consulte [Atualizações regulatórias](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Outra forma de aprender sobre atualizações regulatórias é entrar no Lifecycle Services (LCS) e exibir as atualizações regulatórias planejadas usando a ferramenta de pesquisa de problemas. A pesquisa de problemas permite pesquisar por país, tipo de recurso e versão.