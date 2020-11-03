---
title: Concessões do projeto
description: Este tópico explica como criar ou modificar uma concessão.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071609"
---
# <a name="project-grants"></a>Concessões do projeto

[!include [banner](../includes/banner.md)]

Uma concessão é um presente em dinheiro para um propósito ou projeto específico. Em geral, há restrições sobre como uma concessão pode ser gasta. No gerenciamento e contabilidade de projeto, você pode inserir e rastrear concessões e definir seus relacionamentos com projetos e contratos de projeto. Por exemplo, você pode realizar as seguintes tarefas:

- Associe concessões a projetos e fontes de financiamento por meio de links para as páginas **Projeto** e **Detalhes do contrato do projeto**.
- Insira e rastreie as alterações em uma concessão à medida que ela passa de um status para outro.
- Insira e rastreie os custos, os valores solicitados e os valores concedidos.
- Crie concessões principais e associe subconcessões a elas.

Você pode criar uma concessão inserindo todos os detalhes em um novo registro ou pode copiar os detalhes de uma concessão existente e atualizá-los.

## <a name="create-a-new-grant"></a>Criar uma concessão

1. Vá para **Gerenciamento e contabilidade de projeto** \> **Concessões** \> **Concessões**.
2. Selecione **Novo** \> **Concessão**.
3. Na página de detalhes da concessão, na FastTab **Geral** , no campo **ID da concessão** , insira um identificador alfanumérico para a concessão.
4. No campo **Nome da concessão** , insira um nome para a concessão.
5. No campo **Descrição** , adicione detalhes sobre a nova concessão.

    A maioria dos outros campos da página são opcionais e você pode inserir o mínimo ou o máximo de informações que desejar.

    A lista a seguir descreve as informações especificadas em cada FastTab da página de detalhes da concessão:

    - **Geral** – Insira o nome da concessão, o status, a descrição, a finalidade e o valor.
    - **Informações de contato** – Insira detalhes sobre os membros da equipe, o departamento que gerencia a concessão e o cliente da concessão ou a fonte da organização da concessão. Você também pode indicar se a sua organização é uma entidade de passagem que recebe a concessão e a transmite a outro destinatário. Selecione **Adicionar** para adicionar informações de contato, como números de telefone e endereços de email da organização que fornece a concessão.
    - **Datas e prazos** – Insira as datas relacionadas à concessão e ao pedido de concessão. Os exemplos incluem a data de vencimento do pedido, a data de envio e a data em que a concessão é aprovada ou rejeitada.
    - **Projetos associados e contratos de projeto** – Você pode inserir informações na FastTab apenas se o campo **Status da concessão** na FastTab **Geral** estiver definido como **Ativo** ou **Premiado**. Selecione uma das seguintes opções para concluir a tarefa relacionada:

        - **Adicionar fonte de financiamento** – Adicione uma nova fonte de financiamento para a concessão. Você pode inserir todos os detalhes agora ou usar as informações padrão e atualizá-las posteriormente.
        - **Adicionar contrato do projeto** – Adicione ou atualize as informações do contrato do projeto.
        - **Adicionar projeto** – Adicione ou atualize os detalhes do projeto.

    - **Configuração** – Insira os detalhes sobre fundos correspondentes, se esta informação for necessária. Muitas organizações que concedem concessões exigem que os beneficiários gastem uma quantia específica de seu próprio dinheiro ou recursos, para igualar o valor concedido na concessão. No campo **Projeto local ou ID de acompanhamento** , você pode inserir um identificador diferente do identificador do projeto.

        > [!NOTE]
        > Se parte da concessão for concedida a uma organização diferente, defina a opção **Subconcedente** como **Sim**. Para concessões fornecidas nos Estados Unidos, você pode especificar se uma concessão será fornecida sob mandato estadual ou federal.

    - **Detalhes do rebaixamento** – Adicione ou atualize informações sobre a frequência com que os fundos da concessão podem ser sacados, cobrados ou gastos.

## <a name="create-a-new-grant-from-a-copy"></a>Criar uma concessão a partir de uma cópia

1. Vá para **Gerenciamento e contabilidade de projeto** \> **Concessões** \> **Concessões**.
2. Selecione **Novo** \> **Copiar a partir da concessão**.
3. Insira um identificador alfanumérico e um nome para a nova concessão e selecione **OK**.
4. Na página de detalhes da concessão, revise os detalhes da concessão copiada e faça as alterações necessárias. A maioria dos campos da página é opcional.

## <a name="view-or-modify-grant-details"></a>Ver ou modificar os detalhes da concessão

1. Vá para **Gerenciamento e contabilidade de projeto** \> **Concessões** \> **Concessões**.
2. Selecione a concessão a ser modificada.
3. No Painel de Ações, na guia **Concessão** , no grupo **Manter** , selecione **Editar**.
4. Revise os detalhes da concessão e faça as alterações necessárias.
