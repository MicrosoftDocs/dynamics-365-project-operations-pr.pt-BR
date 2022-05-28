---
title: Importar e manter transações de cartão de crédito
description: Este tópico explica como importar e manter transações de cartão de crédito relacionadas a despesas. Essas transações podem ser configuradas para que sejam importadas automaticamente em uma programação recorrente ou podem ser importadas manualmente conforme necessário.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: bd7ca997e18bf3c11fa188b603c899cc470df035
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683754"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importar e manter transações de cartão de crédito

As transações de cartão de crédito relacionadas a despesas podem ser configuradas para serem importadas automaticamente em um cronograma recorrente. Como alternativa, elas podem ser importadas manualmente conforme necessário. As transações de cartão de crédito são importadas por meio da entidade de dados Transações de cartão de crédito.

Para obter mais informações sobre entidades de dados, consulte [Entidades de dados](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importar transações de cartão de crédito

1. Na página **Transações de cartão de crédito**, selecione **Importar transações**. Se você estiver abrindo o gerenciamento de dados pela primeira vez, o sistema deverá atualizar a lista de entidades de dados para que seja possível continuar.
2. No campo **Nome**, insira uma descrição exclusiva do trabalho de importação.
3. No campo **Formato de dados de origem**, selecione o formato do arquivo que contém as transações de cartão de crédito a serem importadas.
4. Selecione **Carregar** e, em seguida, localize e selecione o arquivo a ser importado.
5. Depois que o arquivo for carregado, valide o mapeamento do arquivo de transações de cartão de crédito e as colunas da entidade de dados Transações de cartão de crédito selecionando o link **Exibir mapa** no bloco. Se houver erros de mapeamento ou se você precisar alterá-lo, faça as alterações na guia **Visualização de mapeamento** ou na guia **Detalhes de mapeamento**.
6. Para automatizar as transações de cartão de crédito, selecione **Criar trabalho de dados recorrente**. Você pode configurar a recorrência que define a frequência com que as transações de cartão de crédito devem ser importadas. Ao concluir, selecione **OK**.
7. Para importar o arquivo selecionado agora, selecione **Importar**.
8. Se ocorrerem erros durante a importação, você pode visualizar o log de execução ou os dados de preparo para ver os erros que devem ser corrigidos para ajudar a garantir uma importação bem-sucedida.

> [!NOTE]
> Se você precisar importar mais de um formato de arquivo, deverá criar trabalhos de importação separados para cada tipo de formato.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Reatribuir as transações de cartão de crédito de funcionários despedidos

Quando um registro de funcionário é encerrado, a conta do Active Directory Domain Services (AD DS) desse funcionário é desabilitada. No entanto, pode haver transações de cartão de crédito ativas que ainda devem ser contabilizadas como despesas e reembolsadas. Na página **Transações de cartão de crédito**, você pode reatribuir um funcionário em qualquer transação de cartão de crédito na qual o funcionário associado tenha sido despedido.

Selecione uma ou mais transações de cartão de crédito e, em seguida, selecione **Reatribuir transações**. Você pode selecionar outro funcionário ao qual atribuir as transações de cartão de crédito. Depois que as transações de cartão de crédito forem reatribuídas, elas poderão ser selecionadas para um relatório de despesas e pagas por meio do processo normal de reembolso de relatórios de despesas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]