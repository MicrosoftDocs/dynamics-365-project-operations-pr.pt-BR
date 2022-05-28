---
title: Configurar a criação automática de fatura
description: Este tópico fornece informações sobre como configurar o sistema para gerar faturas automaticamente.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 43b75ea823a62acaab708a1ef2fa2467904fdd00
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583387"
---
# <a name="configure-automatic-invoice-creation"></a>Configurar a criação automática de fatura

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_


Conclua as etapas a seguir para configurar uma fatura automatizada executada no Dynamics 365 Project Operations.

1. Vá para **Configurações** > **Trabalhos em lote**.
2. Crie um trabalho em lote e denomine-o **Faturas de criação do Project Operations**. O nome do trabalho em lote deve incluir as palavras "criar faturas".
3. No campo **Tipo de Trabalho**, selecione **Nenhum**. Por padrão, as opções **Frequência Diária** e **Está Ativo** são definidas como **Sim**.
4. Selecione **Executar Fluxo de Trabalho**. Na caixa de diálogo **Pesquisar Registro**, você verá três fluxos de trabalho:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Selecione **ProcessRunCaller** e selecione **Adicionar**.
6. Na próxima caixa de diálogo, selecione **OK**. Um fluxo de trabalho **Suspender** é seguido por um fluxo de trabalho **Processar**.

  > [!NOTE]
  > Também é possível selecionar **ProcessRunner** na etapa 5. Em seguida, quando você selecionar **OK**, um fluxo de trabalho **Processar** é seguido por um fluxo de trabalho **Suspender**.

Os fluxos de trabalho **ProcessRunCaller** e **ProcessRunner** criam faturas. **ProcessRunCaller** chama **ProcessRunner**. **ProcessRunner** é o fluxo de trabalho que de fato cria as faturas. Ele passa por todas as linhas de contrato para as quais as faturas devem ser criadas e cria faturas para essas linhas. A fim de determinar as linhas de contrato para as quais as faturas devem ser criadas, o trabalho examina as datas de execução de fatura das linhas de contrato. Se as linhas de contrato que pertencem a um contrato tiverem a mesma data de execução de fatura, as transações serão combinadas em uma fatura que tenha duas linhas de fatura. Se não houver transações para as quais criar faturas, o trabalho pulará a etapa de criação de fatura.

Quando **ProcessRunner** termina de ser executado, ele chama **ProcessRunCaller**, fornece a hora de término e é fechado. **ProcessRunCaller** então inicia um timer que é executado por 24 horas a partir da hora de término especificada. Ao fim do timer, **ProcessRunCaller** é fechado.

O trabalho do processo em lote para criação de faturas é um trabalho recorrente. Se esse processo em lote for executado muitas vezes, várias instâncias do trabalho serão criadas e causarão erros. Portanto, você deve iniciar o processo em lote apenas uma vez, assim como deve reiniciá-lo apenas se a execução for interrompida.

> [!NOTE]
> O faturamento em lote só é executado para linhas de contrato de projeto configuradas por agendas de faturas. Uma linha de contrato com um método de cobrança de preço fixo deve ter marcos configurados. Uma linha de contrato do projeto com um método de cobrança de horas e de material precisará de uma configuração de agenda de faturas baseada em data. O mesmo se aplica a um projeto baseado em linha de contrato.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]