---
title: Configurar retenção de fornecedor
description: Este tópico explica como configurar retenções de fornecedor.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594562"
---
# <a name="set-up-vendor-retention"></a>Configurar retenção de fornecedor

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico fornece informações sobre como configurar retenções de fornecedor.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Configure uma conta de retenção de fornecedor em Contabilidade

1. No Dynamics 365 Finance, acesse **Contabilidade** > **Preparação da publicação** > **Contas para transações automáticas**.
2. Adicionar uma nova linha.
3. No campo **Tipo de publicação**, selecione **Retenção de fornecedor**.
4. Selecione a conta principal para a publicação de retenção do fornecedor.

## <a name="create-vendor-retention-terms"></a>Crie as condições de retenção do fornecedor

Use a página **Condições de retenção do fornecedor** para definir e manter as condições de retenção de pagamentos aos fornecedores. Insira a porcentagem do pagamento ao fornecedor para retenção e a porcentagem dos valores retidos anteriormente para liberação. Os valores são retidos automaticamente nas faturas do fornecedor até que o contrato atinja o estado de conclusão especificado. Depois que as condições de retenção de um fornecedor são definidas, você poderá aplicá-las a todos os projetos em que o fornecedor trabalhar.

1. No Finance, acesse **Gerenciamento e contabilidade do projeto** > **Configuração** > **Retenção** > **Condições de retenção de pagamento ao fornecedor**.
2. Selecione **Novo** para adicionar um novo termo de retenção de fornecedor. O valor exibido no campo **ID da regra** da nova condição é inserido automaticamente. 
3. No campo **Descrição**, insira um nome descritivo para uma nova condição.
4. Na guia **Condições**, selecione **Adicionar linha** para inserir uma condição de retenção do fornecedor.
5. No campo **Porcentagem de unidades entregues**, insira uma porcentagem de conclusão da regra. Os valores serão retidos automaticamente nas faturas do fornecedor até que o estágio de projeto da conclusão seja igual à porcentagem inserida. Por exemplo, se você inserir 50,00, os valores serão retidos até que o projeto esteja 50% concluído.
6. No campo **Porcentagem a reter**, insira uma porcentagem de um valor da fatura do fornecedor a ser retido. Por exemplo, se você inserir 10,00 nesse campo, 10% do valor em faturas de fornecedor serão retidos até que o projeto atinja a porcentagem de conclusão definida no campo **Porcentagem de unidades entregues**.
7. No campo **Porcentagem a liberar**, insira uma porcentagem dos valores retidos anteriormente a ser liberado quando o projeto atingir o nível de conclusão selecionado.

> [!NOTE]
> Se houver mais de uma etapa para diferentes níveis de conclusão de projeto, insira uma linha separada de condição de retenção do fornecedor para cada regra de retenção. Cada linha pode especificar uma porcentagem de retenção diferente e uma porcentagem de liberação diferente para cada nível designado de conclusão do projeto.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Defina um contrato do fornecedor do projeto

Defina as condições de retenção do fornecedor aplicáveis ao projeto. Os termos de retenção do fornecedor também são exibidos nas ordens de compra que você cria para o fornecedor.

1. No Finance, acesse **Gerenciamento e contabilidade de projeto** > **Projetos** > **Todos os projetos**. 
2. Selecione um projeto e, no Painel de Ação, selecione **Grupo de projetos** > **Contratos de fornecedores**.
3. Na página **Contratos de fornecedores**, adicione uma nova linha.
4. No campo **Código de conta**, selecione uma das seguintes opções:
   - **Tabela**: os termos de retenção de fornecedor se aplicam a um único fornecedor.
   - **Grupo**: os termos de retenção de fornecedor se aplicam a todos os fornecedores em um grupo de fornecedores.
   - **Todos**: os termos de retenção de fornecedor se aplicam a todos os fornecedores.
5. No campo **Fornecedor/Grupo de fornecedores**, selecione o fornecedor ou grupo de fornecedores ao qual os termos de retenção do fornecedor se aplicam. Se você tiver selecionado **Todos** na etapa anterior, esse campo não estará disponível.
6. No campo **Condições de retenção do fornecedor**, selecione o ID da regra para as condições de retenção aplicáveis a esse fornecedor.

