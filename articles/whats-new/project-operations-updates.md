---
title: Atualizações do Project Operations
description: Este tópico fornece informações sobre as versões liberadas do Dynamics 365 Project Operations.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d19148c868aa5be77db59e70fcf1fb8b7de6868c
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213431"
---
# <a name="project-operations-updates"></a>Atualizações do Project Operations

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - fatura de acordo com pro forma e Project Operations para cenários baseados em estoque/produção__

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Componentes do Project Operations

O Dynamics 365 Project Operations consiste em dois componentes:

- O Project Operations no ambiente do Dataverse abrange recursos da oportunidade para faturamento pro forma. O Dataverse é usado na implantação lite e na implantação de cenários de recursos/não estocados do Project Operations.
- Gerenciamento e contabilidade de projeto no ambiente do Dynamics 365 Finance abrange os recursos de gerenciamento de despesas, contabilidade de projetos e reconhecimento de receitas. O ambiente do aplicativo Finance and Operations é usado no Project Operations para cenários com base em recursos/sem estoque e Project Operations para cenários baseados em estoque/produção.

## <a name="project-operations-release-notes"></a>Notas de versão do Project Operations
- As notas de versão mais recentes do Project Operations para cenários baseados em [Recursos/sem estoque](whats-new-may-2021-resource-based.md).
- As notas de versão mais recentes do Project Operations para cenários de [Implantação Lite](../pro/whats-new/whats-new-may-2021-lite.md).
- As notas de versão mais recentes do Project Operations para cenários baseados em [Com estoque/produção](../prod-pma/whats-new/whats-new-apr-2021-stocked.md).

## <a name="project-operations-latest-version"></a>Versão mais recente do Project Operations

| Project Operations no ambiente do Dataverse | Gerenciamento e contabilidade de projeto nos ambientes dos aplicativos Finance and Operations | 
| --- | --- |
| 4.10.0.186 | 10.0.18 |

Para o cenário de recursos do Project Operations/sem estoque, recomendamos o uso do Dual Write Orchestration versão 2.2.2.60 ou superior.

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Lançamento de versões do Project Operations no ambiente do Dataverse

As atualizações para Project Operations no ambiente do Dataverse estão disponíveis mensalmente. 

| Estação | Região | Número da versão atual | Atualizações automáticas para implantação Lite | Atualizações automáticas para implantação de Recursos/sem estoque | Número da próxima versão | Próxima versão disponível ao público |
|-----------|-----------------------|-----------------|--------------|---------------------|---------------------|---------------------|
| Estação 1 |   &nbsp;              |    &nbsp;       | &nbsp;       |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Primeira Versão         |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 28 de maio de 2021           |
| Estação 2 |   &nbsp;              |    &nbsp;       | &nbsp;       |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | América do Sul         |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 28 de maio de 2021           |
|    &nbsp; | Canadá                |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 28 de maio de 2021           |
|   &nbsp;  | Índia                 |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 28 de maio de 2021           |
|   &nbsp;  | França                |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 28 de maio de 2021           |
|   &nbsp;  | Emirados Árabes Unidos  |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 28 de maio de 2021           |
|   &nbsp;  | África do Sul          |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 28 de maio de 2021           |
| Estação 3 |      &nbsp;           |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Japão                 |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 04 de junho de 2021          |
|   &nbsp;  | Pacífico Asiático          |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 04 de junho de 2021          |
|   &nbsp;  | Grã-Bretanha         |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 04 de junho de 2021          |
|   &nbsp;  | Oceania               |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 04 de junho de 2021          |
| Estação 4 |     &nbsp;            |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Europa                |  4.10.0.186     | Concluída     | Concluída            | TBD                 | 11 de junho de 2021          |
| Estação 5 |     &nbsp;            |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | América do Norte         |  4.10.0.186     | Concluída     | 11 de junho de 2021          | TBD                 | 18 de junho de 2021          |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Agenda da versão para Gerenciamento e contabilidade de projeto no ambiente dos aplicativos Finance and Operations

As atualizações para gerenciamento e contabilidade de projetos são lançadas oito vezes por ano.

|          Versão compatível          | Exibição da disponibilidade (PEAP) | Geralmente disponível (atualização automática) | Cronograma de atualização automática (via Configurações de Atualização de LCS) - data de início da produção |   Fim do serviço   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.18          |        5 de março de 2021        |           16 de abril de 2021          |                            30 de abril de 2021                            |    16 de julho de 2021   |
|          10.0.17          |       1 de fevereiro de 2021      |           19 de março de 2021          |                             2 de abril de 2021                            |    11 de junho de 2021   |

As datas planejadas da versão estão sujeitas a alterações. Para obter mais informações, consulte [Disponibilidade de atualização de serviço](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json).

|          Versão de Destino          | Exibição da disponibilidade (PEAP) | Geralmente disponível (atualização automática) | Cronograma de atualização automática (via Configurações de Atualização de LCS) - data de início da produção |   Fim do serviço   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.19          |        23 de abril de 2021       |            18 de junho de 2021           |                             2 de julho de 2021                             | 17 de setembro de 2021 |
|          10.0.20          |         28 de maio de 2021        |           16 de julho de 2021           |                             30 de julho de 2021                             |  22 de outubro de 2021  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
