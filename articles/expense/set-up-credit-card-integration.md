---
title: Configurar integração de cartão de crédito
description: Este tópico explica como importar e manter transações de cartão de crédito relacionadas a despesas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276154"
---
# <a name="set-up-credit-card-integration"></a>Configurar integração de cartão de crédito

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As transações de cartão de crédito relacionadas a despesas podem ser configuradas para serem importadas automaticamente em um cronograma recorrente. Como alternativa, elas podem ser importadas manualmente conforme necessário. As transações de cartão de crédito são importadas por meio da entidade de dados Transações de cartão de crédito.

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