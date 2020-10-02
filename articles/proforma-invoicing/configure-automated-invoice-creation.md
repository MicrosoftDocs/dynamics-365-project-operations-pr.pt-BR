---
title: Configurar criação de fatura automatizada
description: Este tópico fornece informações sobre como configurar o sistema para gerar faturas automaticamente.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898112"
---
# <a name="configure-automated-invoice-creation"></a>Configurar criação de fatura automatizada

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

Conclua as etapas a seguir para configurar uma fatura automatizada executada no Project Operations.

1. Vá para **Configurações** \> **Trabalhos em lote**.
2. Crie um trabalho em lote e denomine-o **Faturas de criação do Project Operations**. O nome do trabalho em lote deve incluir o termo "criar faturas".
3. No campo **Tipo de trabalho**, selecione **Nenhum**. Por padrão, as opções **Frequência Diária** e **Está Ativo** são definidas como **Sim**.
4. Selecione **Executar Fluxo de Trabalho**. Na caixa de diálogo **Pesquisar Registro**, você verá três fluxos de trabalho:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Selecione **ProcessRunCaller** e selecione **Adicionar**.
6. Na próxima caixa de diálogo, selecione **OK**. Um fluxo de trabalho **Suspender** é seguido por um fluxo de trabalho **Processar**.

    Também é possível selecionar **ProcessRunner** na etapa 5. Em seguida, quando você selecionar **OK**, um fluxo de trabalho **Processar** é seguido por um fluxo de trabalho **Suspender**.

Os fluxos de trabalho **ProcessRunCaller** e **ProcessRunner** criam faturas. **ProcessRunCaller** chama **ProcessRunner**. **ProcessRunner** é o fluxo de trabalho que de fato cria as faturas. Ele passa por todas as linhas de contrato para as quais as faturas devem ser criadas e cria faturas para essas linhas. A fim de determinar as linhas de contrato para as quais as faturas devem ser criadas, o trabalho examina as datas de execução de fatura das linhas de contrato. Se as linhas de contrato que pertencem a um contrato tiverem a mesma data de execução de fatura, as transações serão combinadas em uma fatura que tenha duas linhas de fatura. Se não houver transações para as quais criar faturas, o trabalho pulará a etapa de criação de fatura.

Quando **ProcessRunner** termina de ser executado, ele chama **ProcessRunCaller**, fornece a hora de término e é fechado. **ProcessRunCaller** então inicia um timer que é executado por 24 horas a partir da hora de término especificada. Ao fim do timer, **ProcessRunCaller** é fechado.

O trabalho do processo em lote para criação de faturas é um trabalho recorrente. Se esse processo em lote for executado muitas vezes, várias instâncias do trabalho serão criadas e causarão erros. Portanto, você deve iniciar o processo em lote apenas uma vez, assim como deve reiniciá-lo apenas se a execução for interrompida.

> [!NOTE]
> O faturamento em lote só é executado para linhas de contrato de projeto configuradas por agendas de faturas. Uma linha de contrato com um método de cobrança de preço fixo deve ter marcos configurados. Uma linha de contrato do projeto com um método de cobrança de horas e de material precisará de uma configuração de agenda de faturas baseada em data. O mesmo se aplica a um projeto baseado em linha de contrato.     
