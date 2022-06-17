---
title: Copiar um projeto
description: Este artigo fornece informações sobre como copiar projeto no Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925750"
---
# <a name="copy-a-project"></a>Copiar um projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Com o Dynamics 365 Project Operations, você pode criar projetos rapidamente selecionando **Copiar Projeto** no formulário **Projetos**. Para copiar um projeto, abra o projeto que deseja copiar e selecione **Copiar projeto**. A ação copiará o seguinte:

- Propriedades do projeto 
- Estrutura de detalhamento de trabalho
- Membros da equipe de projeto
- Estimativas do projeto
- Estimativas de despesas do projeto
- Estimativas de material do projeto
- Listas de verificação do projeto
- Buckets do projeto

## <a name="project-properties"></a>Propriedades do projeto

Quando o projeto é copiado, os valores nos campos a seguir são copiados.

| Campo | Materiais sem estoque no Project Operations | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| Customer | :heavy_check_mark: | :heavy_check_mark: | |
| Modelo de Calendário | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Currency | :heavy_check_mark: | :heavy_check_mark: | |
| Unidade de Contratação | :heavy_check_mark: | :heavy_check_mark: | |
| Empresa Proprietária | :heavy_check_mark: | | |
| Gerente de Projeto | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Status Geral do Projeto | :heavy_check_mark: | :heavy_check_mark: | |
| Comentários | :heavy_check_mark: | :heavy_check_mark: | |
| Estimativas | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Data de Início Estimada</p><p><strong>Observação:</strong> esse campo especifica a data em que o projeto foi criado a partir da cópia. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Data de Conclusão Estimada</p><p><strong>Observação:</strong> a data nesse campo é ajustada com base na data de início do novo projeto que foi criado a partir da cópia.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Esforço (Horas) | :heavy_check_mark: | :heavy_check_mark: | |
| Custo Estimado da Mão de Obra | :heavy_check_mark: | :heavy_check_mark: | |
| Custo Estimado da Despesa | :heavy_check_mark: | :heavy_check_mark: | |
| Custo Estimado dos Materiais | | :heavy_check_mark: | |

> [!NOTE]
> Copiar projeto é uma operação de execução prolongada. Os registros do projeto, seus atributos relevantes e muitas entidades relacionadas também são copiados. Devido à natureza de execução prolongada da operação, após o início da cópia, a página do projeto de destino é bloqueada para edição até que a operação de cópia seja concluída.

## <a name="work-breakdown-structure"></a>Estrutura de detalhamento de trabalho

Quando o projeto é copiado, toda a estrutura de detalhamento de trabalho carregada por recurso é copiada. Os recursos nomeados são substituídos por recursos genéricos. Se os recursos nomeados não tiverem o mesmo horário de trabalho que o recurso genérico, o agendamento será recalculado e as durações das tarefas poderão ser alteradas.

## <a name="project-team-members"></a>Membros da equipe de projeto

Quando uma equipe de projeto for copiada do projeto de origem, os recursos genéricos são copiados. As atribuições de recursos genéricos também são mantidas, pois estavam no projeto de origem. Os recursos nomeados serão convertidos em membros da equipe genéricos.

> [!NOTE]
> Os membros da equipe e as atribuições não são copiados no Project for the Web.

## <a name="estimates"></a>Estimativas

Quando o projeto é copiado, as linhas de estimativa de recursos, despesas e materiais são copiadas do projeto de origem. 

Para obter informações sobre como acessar programaticamente Copiar Projeto, consulte [Desenvolver modelos de projeto com Copiar Projeto](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Cotações e contratos

Cotações e contratos não são vinculados ao projeto de destino.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
