---
title: Sincronizar capacidade do recurso
description: Este artigo fornece informações sobre como sincronizar a capacidade de um recurso em calendários e projetos.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b684833ffae83b7cedfc73ee96a8aa8ddd4ec57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920690"
---
# <a name="synchronize-resource-capacity"></a>Sincronizar capacidade do recurso

[!include [banner](../includes/banner.md)]

Os processos de sincronização de recursos ajudam a garantir que as informações do calendário e do calendário base se encaixem no agendamento de recursos do projeto. Se o calendário for alterado, os processos farão as atualizações necessárias no agendamento dos recursos do projeto. Os processos também ajudam a melhorar o desempenho, porque as informações dos recursos do calendário são sincronizadas com antecedência. Portanto, as atualizações nas informações de agendamento de recursos ocorrem mais rapidamente. Recomendamos que você agende os processos em lote, em vez de um de cada vez. Caso contrário, existe o risco de alguém se esquecer das datas inclusivas da última sincronização das informações. Se não forem usadas datas inclusivas, podem ocorrer lacunas durante a sincronização de datas.

![Sincronização de calendário.](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sincronizar acúmulos de capacidade dos recursos

O processo de sincronização foi projetado para sincronizar todas as informações do calendário de recursos. Essas informações incluem informações básicas do calendário sobre quaisquer alterações na tabela de capacidade do calendário de recursos do projeto. Se novos recursos forem adicionados ao projeto, a sincronização ajudará a garantir que as informações atualizadas do calendário estejam disponíveis. Essa sincronização pode ser feita a qualquer momento.

É recomendável usar atualização em lote. As opções estão disponíveis durante a sincronização das reservas de capacidade.

1. Selecione **Gerenciamento e contabilidade de projeto** &gt; **Periódico** &gt; **Sincronização de capacidade** &gt; **Sincronizar acúmulos de capacidade de recursos**.
2. Defina as opções na tabela a seguir.

    | Opção      | Descrição |
    |-------------|-------------|
    | Código de período | Opcionalmente, selecione o código de intervalo de datas do razão geral para definir as datas de início e de término do processo de sincronização para os acúmulos de capacidade de recursos. |
    | Data de Início  | Insira a data de início do processo de sincronização para os acúmulos de capacidade de recursos. |
    | Data de término    | Insira a data de término do processo de sincronização para os acúmulos de capacidade de recursos. |

[![Processo de sincronização.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]