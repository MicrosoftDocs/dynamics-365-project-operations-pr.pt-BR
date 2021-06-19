---
title: Novidades em Maio de 2021 - Implantação lite do Project Operations
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de Maio de 2021 de implantação lite do Project Operations.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060419"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Novidades em Maio de 2021 - Implantação lite do Project Operations

_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

   - Project Operations no ambiente do Dataverse versão 4.10.0.186.

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

- [Modos de agendamento](../../project-management/scheduling-modes.md): os gerentes de projeto agora podem definir se um projeto deve ser gerenciado usando uma duração fixa, trabalho fixo ou modo de agendamento de unidades fixas.

## <a name="quality-updates"></a>Atualizações de qualidade

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Cobrança e preço | 2224568 | Adicionada lógica para habilitar personalizações que envolvem a chamada do plug-in de confirmação de fatura. |
| Cobrança e preço | 2101098 | Melhoria de lógica de campos padrão para fatura proforma. Esses campos incluem, **Endereço para cobrança**, **Nome para cobrança** e **Termos de pagamento**. Os campos agora são predefinidos do registro de cliente do contrato de projeto correspondente. |
| Cobrança e preço | 2021413 | Atualizados os campos **Custo real** e **Vendas** na entidade **Tarefa** para incluir valores de vendas de despesas faturadas e não faturadas em tarefas. |
| Cobrança e preço | 2182110 | Ao copiar um contrato de projeto, a ID da linha do contrato é regenerada no contrato do projeto de destino para garantir que seja exclusiva. |
| Gerenciamento de Oportunidades | 2186741 | Adicionadas validações para garantir que o campo **Origem** e tipo de transação não podem ser atualizados nos detalhes da linha da cotação existente. |
| Gerenciamento de Oportunidades | 2191353 | A criação do marco não deve ser permitida em uma linha de contrato de hora e material. |
| Gerenciamento de Oportunidades | 2216956 | Problemas corrigidos com **Atualizar preços**. |
| Planejamento e acompanhamento | 2182979 | A função de cópia do projeto foi aprimorada para garantir que as linhas de estimativa de despesas sejam copiadas do projeto original. |
| Planejamento e acompanhamento | 2184144 | A função de cópia do projeto foi aprimorada para garantir que o nome da posição do recurso seja copiado do projeto original. |
| Planejamento e acompanhamento | 2184799 | Controle mais rígido ao copiar um projeto para garantir que a data de início estimada não possa ser alterada enquanto a cópia estiver em andamento. |
| Planejamento e acompanhamento | 2185134 | Durante a cópia de um projeto, a data de início estimada do projeto de destino é definida como a data de hoje. |
| Planejamento e acompanhamento | 2196373 | Certifique-se de que os registros do gerente de projeto e dos membros da equipe não sejam duplicados na equipe do projeto ao copiar um projeto. |
| Planejamento e acompanhamento | 2211833 | As atribuições de recursos são copiadas da tarefa do projeto de origem no projeto de destino. |
| Planejamento e acompanhamento | 2186541 | Problemas corrigidos na grade **Estimativas** ao agrupar por **Recurso**. |
| Planejamento e acompanhamento | 2166906 | A categoria de transação de uma tarefa deve ser copiada na entidade **Atribuição de recursos**. |
| Gerenciamento de Recursos | 2125362 | Corrigidos problemas com a criação de um membro da equipe genérico usando um método de alocação baseado em horas. |
| Tempo e Despesa | 2113603 | Corrigido o problema relacionado à personalização com a remoção de atributos da página **Entrada de hora**. O sistema agora verifica se o atributo existe na página antes de acessar o atributo usando um script. |
| Tempo e Despesa | 2204377 | As planilhas de horas copiadas devem aparecer automaticamente quando você selecionar **Copiar Semana**. |
| Tempo e Despesa | 2209059 | O campo **Status** pode ser editado para entradas de hora do Dynamics 365 Field Service. |
