---
title: Novidades em abril de 2021 - implantação lite do Project Operations
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de abril de 2021 de implantação lite do Project Operations.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 868d6daf8ac3ad9ef4245cef3c74a735137d3903
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994077"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Novidades em abril de 2021 - implantação lite do Project Operations

_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations no ambiente do Dataverse versão 4.9.0.221 

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

- Materiais sem estoque para projetos. Os principais recursos incluem:
  - Estimativa e determinação de preços de materiais não estocados durante o ciclo de vendas de um projeto. Para obter mais informações, consulte [Configurar taxas de custo e de vendas para produtos do catálogo – lite](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Acompanhamento do uso de materiais não estocados durante a entrega do projeto. Para obter mais informações, consulte [Registre o uso de material em projetos e tarefas de projeto](../../material/material-usage-log.md).
  - O faturamento usou custos de materiais não estocados. Para obter mais informações, consulte [Gerenciar a lista de pendências de cobrança - lite](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Novas APIs no Dynamics 365 Dataverse permitem operações de criação, atualização e exclusão com **Entidades de agendamento**. Para obter mais informações, consulte [Use APIs de programação para realizar operações com entidades de programação](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Atualizações de qualidade

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Cobrança e preço | 2224568 | Adicionada lógica para habilitar personalizações que envolvem a chamada do plug-in de confirmação de fatura. |
| Cobrança e preço | 2101098 | Melhorou a lógica de campos padrão para fatura pro forma: **Endereço para Cobrança**, **Nome para Cobrança** e **Condições de Pagamento** agora é o padrão do registro de cliente do contrato de projeto correspondente. |
| Cobrança e preço | 2021413 | Atualizados os campos **Custo Real** e **Vendas** na entidade **Tarefa** para incluir valores de vendas de despesas faturadas e não faturadas em tarefas. |
| Cobrança e preço | 2182110 | Ao copiar um contrato de projeto, a ID da linha do contrato é regenerada no contrato do projeto de destino para garantir que seja exclusiva. |
| Gerenciamento de Oportunidades | 2186741 | Adicionadas validações para garantir que o campo **Origem** e **Tipo de Transação** não possam ser atualizados em detalhes da linha de cotação existente. |
| Gerenciamento de Oportunidades | 2191353 | As etapas não devem ser criadas em uma linha de contrato de tempo e material. |
| Gerenciamento de Oportunidades | 2216956 | Problemas corrigidos com **Atualizar Preços**. |
| Planejamento e acompanhamento | 2182979 | A função de cópia do projeto foi aprimorada para garantir que as linhas de estimativa de despesas sejam copiadas do projeto original. |
| Planejamento e acompanhamento | 2184144 | A função de cópia do projeto foi aprimorada para garantir que o nome da posição do recurso seja copiado do projeto original. |
| Planejamento e acompanhamento | 2184799 | Cópia do projeto: controle mais rígido para garantir que a data de início estimada não possa ser alterada durante o andamento da cópia. |
| Planejamento e acompanhamento | 2185134 | Cópia do projeto: a data de início estimada do projeto de destino é definida como a data de hoje. |
| Planejamento e acompanhamento | 2196373 | Cópia do projeto: verifique se os registros do gerente de projeto e do membro da equipe não estão duplicados na equipe do projeto. |
| Planejamento e acompanhamento | 2211833 | Cópia do projeto: as atribuições de recursos são copiadas da tarefa do projeto de origem no projeto de destino. |
| Planejamento e acompanhamento | 2186541 | Problemas corrigidos na grade **Estimativas** ao agrupar por recurso. |
| Planejamento e acompanhamento | 2166906 | A categoria de transação de uma tarefa deve ser copiada na entidade **Atribuição de Recursos**. |
| Gerenciamento de Recursos | 2125362 | Corrigidos problemas com a criação de um membro da equipe genérico usando um método de alocação baseado em horas. |
| Tempo e Despesa | 2113603 | Corrigido o problema relacionado à personalização com a remoção de atributos da página **Entrada de Tempo**. O sistema agora verifica se o atributo existe na página antes de acessá-los usando um script. |
| Tempo e Despesa | 2204377 | As planilhas de horas copiadas devem aparecer automaticamente quando você seleciona **Copiar Semana** durante a entrada de tempo. |
| Tempo e Despesa | 2209059 | O campo **Status** pode ser editado para entradas de tempo do Dynamics 365 Field Service. |
