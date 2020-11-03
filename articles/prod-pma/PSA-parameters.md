---
title: Parâmetros de integração do Project Service Automation
description: Este tópico explica como configurar como os dados padrão são inseridos quando você integra Microsoft Dynamics 365 for Project Service Automation ao Microsoft Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 1a0cee090e0ecb306aa3bda62c79a57dfade93c0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071568"
---
# <a name="project-service-automation-integration-parameters"></a>Parâmetros de integração do Project Service Automation

[!include[banner](../includes/banner.md)]

Na página **Parâmetros de integração do Project Service Automation** , você pode configurar como os dados padrão são inseridos ao integrar o Dynamics 365 Project Service Automation ao Dynamics 365 Finance. Para que os projetos sejam sincronizados com êxito do Project Service Automation para Finance, você deve configurar os campos a seguir.

Para abrir a página **Parâmetros de integração do Project Service Automation** , vá para parâmetros de integração **Gestão e contabilidade de projetos** \> **Configuração** \> **Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - A integração de tarefas de projeto, as categorias de transação de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.
> - A integração dos valores reais está disponível na versão 8.0.1 ou posterior.


| Tab                    | Campo                | Descrição |
|------------------------|----------------------|-------------|
| Geral                | Tipo de projeto padrão | Selecione o tipo de projeto padrão. Quando os projetos são sincronizados a partir do Project Service Automation, este valor é usado se você não forneceu um valor padrão no modelo de integração. Durante a sincronização, o campo **Tipo de projeto** de novos projetos é definido com este valor. No entanto, o valor pode ser atualizado quando as linhas do contrato do projeto são sincronizadas no Project Service Automation. |
|                        | Categoria de tempo        | Selecione a categoria de tempo padrão. Este valor é usado quando as estimativas de horas são sincronizadas a partir do Project Service Automation. Quando as estimativas de horas e horas reais são sincronizadas a partir do Project Service Automation, o campo **Categoria** de novas previsões de horas do projeto em Finanças é definido com este valor. |
|                        | Categoria de taxa         | Selecione a categoria de taxa padrão. Este valor é usado quando as taxas atuais são sincronizadas a partir do Project Service Automation. Quando as taxas reais são sincronizadas a partir do Project Service Automation, o campo **Categoria** de novas transações de taxa em Finanças é definido com este valor. |
| Padrões do grupo do projeto | Tipo de projeto         | Clique em **Novo** para adicionar uma linha onde você pode selecionar o tipo de projeto para definir o grupo de projetos padrão. Um tipo de projeto específico pode ser selecionado apenas uma vez na configuração. |
|                        | Grupo de Projeto        | Selecione o grupo de projetos padrão para o tipo de projeto selecionado. Quando novos projetos são sincronizados a partir do Project Service Automation, o campo **Grupo de Projeto** é definido com o valor padrão para o tipo de projeto se você não forneceu um valor padrão no modelo de integração. |
| Padrões de tipo de cobrança  | Tipo de cobrança         | Clique em **Novo** para adicionar uma linha onde você pode selecionar o tipo de cobrança para definir a propriedade de linha padrão. Um tipo de cobrança específico pode ser selecionado apenas uma vez na configuração. |
|                        | Propriedade de linha        | Selecione a propriedade de linhas padrão para o tipo de cobrança selecionado. Quando novas estimativas de horas, novas estimativas de despesas ou novos valores reais são sincronizados a partir do Project Service Automation, o campo **Propriedade de linha** é definido com o valor padrão para o tipo de cobrança. |
| Bloqueio de funcionalidade  | Não aplicável       | Selecione a funcionalidade a ser desabilitada em Finanças para projetos e contratos originados do Project Service Automation. Por exemplo, você pode desativar a capacidade de editar contratos e projetos, criar estruturas analíticas de trabalho e inserir planilhas de horas em Finanças. Os campos relacionados à contabilidade continuarão habilitados, mesmo que não sejam disponibilizados pela configuração do parâmetro. Por padrão, todas as funcionalidades estão habilitadas. |
