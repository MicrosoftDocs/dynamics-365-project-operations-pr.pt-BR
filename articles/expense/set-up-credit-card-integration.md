---
title: Configurar integração do cartão de crédito
description: Este tópico explica como trabalhar com transações de cartão de crédito relacionadas a despesas.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 49c8f2369a8be41fbc04c74bdb6b565b4f4b7b79
ms.sourcegitcommit: 9f26cf8bb640af1eb9f7f0872805965d7ffcb9d3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/19/2021
ms.locfileid: "7826242"
---
# <a name="set-up-credit-card-integration"></a>Configurar integração do cartão de crédito

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As transações de cartão de crédito relacionadas a despesas podem ser configuradas para serem importadas automaticamente em um cronograma recorrente. Como alternativa, elas podem ser importadas manualmente conforme necessário. As transações de cartão de crédito são importadas por meio da entidade de dados transações de cartão de crédito.

## <a name="import-credit-card-transactions"></a>Importar transações de cartão de crédito

Para importar transações de cartão de crédito, siga estas etapas:

1. Na página **Transações de cartão de crédito**, selecione **Importar transações**. Se estiver abrindo o gerenciamento de dados pela primeira vez, o sistema deverá atualizar a lista de entidades de dados para que você possa continuar.
2. No campo **Nome**, insira uma descrição exclusiva para o trabalho de importação.
3. No campo **Formato de dados de origem**, selecione o formato do arquivo que contém as transações de cartão de crédito a serem importadas.
4. Selecione **Carregar** e, em seguida, localize e selecione o arquivo a ser importado.
5. Depois que o arquivo for carregado, valide o mapeamento do arquivo de transações de cartão de crédito e as colunas da entidade de dados transações de cartão de crédito selecionando o link **Exibir mapa** no bloco. Se houver erros de mapeamento ou se você precisar alterá-lo, faça as alterações na guia **Visualização de mapeamento** ou na guia **Detalhes de mapeamento**.
6. Para automatizar as transações de cartão de crédito, selecione **Criar trabalho de dados recorrente**. Você pode configurar a recorrência que define a frequência com que as transações de cartão de crédito devem ser importadas. Ao terminar, selecione **OK**.
7. Para importar o arquivo selecionado agora, selecione **Importar**.
8. Se ocorrerem erros durante a importação, você poderá visualizar o log de execução ou os dados de preparo para ver os erros que devem ser corrigidos para ajudar a garantir uma importação bem-sucedida.

> [!NOTE]
> Se você precisar importar mais de um formato de arquivo, deverá criar trabalhos de importação separados para cada tipo de formato.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Reatribuir as transações de cartão de crédito de funcionários despedidos

Quando um registro de funcionário é encerrado, a conta do Active Directory Domain Services (AD DS) desse funcionário é desabilitada. No entanto, pode haver transações de cartão de crédito ativas que ainda devem ser contabilizadas como despesas e reembolsadas. Na página **Transações de cartão de crédito**, você pode reatribuir o funcionário a qualquer transação de cartão de crédito em que o funcionário associado foi encerrado.

Selecione uma ou mais transações de cartão de crédito e, em seguida, selecione **Reatribuir transações**. Você pode selecionar outro funcionário ao qual atribuir as transações de cartão de crédito. Depois que as transações de cartão de crédito forem reatribuídas, elas poderão ser selecionadas para um relatório de despesas e pagas por meio do processo normal de reembolso de relatórios de despesas.

## <a name="delete-credit-card-transactions"></a>Excluir transações de cartão de crédito 

Às vezes, depois que as transações de cartão de crédito são importadas, talvez seja preciso excluir certas transações. Isso pode ocorrer porque as transações são duplicadas ou porque os dados não são precisos. Os administradores podem usar o recurso **"Excluir transações de cartão de crédito"** para selecionar e excluir transações de cartão de crédito que **não são anexadas** a um relatório de despesas. 

1. Acesse **Tarefas periódicas** > **Excluir transações de cartão de crédito**.
2. Selecione **Filtro** e forneça informações para identificar os registros a serem incluídos.
3. Selecione **OK** para excluir os registros. 

## <a name="storing-credit-card-numbers"></a>Armazenar números de cartão de crédito

Três opções estão disponíveis para armazenar números de cartão de crédito. Os números de cartão de crédito são armazenados na página **Parâmetros de gerenciamento de despesas**.

- **Impedir a entrada do número do cartão**: os números de cartão de crédito não são armazenados.
- **Números de cartão de hash (armazena os quatro últimos dígitos)**: os últimos quatro dígitos dos números do cartão de crédito são armazenados em um formato criptografado.
- **Números de cartão da loja**: os números de cartão de crédito são armazenados em um formato não criptografado. Esta opção não está em conformidade com o padrão de segurança de dados (DSS) do Setor de Cartões de Pagamento (PCI). Portanto, para manter sua organização em conformidade com as regulamentações PCI DSS, os administradores da organização devem optar por não armazenar números de cartão de crédito ou armazenar números de cartão hash.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
