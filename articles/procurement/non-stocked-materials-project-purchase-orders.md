---
title: Peça materiais não estocados para um projeto usando ordens de compra do projeto
description: Este tópico explica como você pode pedir materiais não estocados para um projeto usando ordens de compra do projeto.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563008"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Peça materiais não estocados para um projeto usando ordens de compra do projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

O departamento de compras da sua organização pode usar [ordens de compra](/dynamics365/supply-chain/procurement/purchase-order-overview) para rastrear ordens de produtos e serviços. As ordens de compra de materiais não estocados podem ser atribuídas a um projeto. O faturamento dessas ordens de compra registra o custo no projeto.

## <a name="prerequisites"></a>Pré-requisitos
Conclua as etapas a seguir para habilitar a funcionalidade de ordens de compra do projeto.

1. No Dynamics 365 Finance, acesse o espaço de trabalho **Gerenciamento de Recursos**.
2. Na lista de recursos, encontre e selecione o recurso **Habilitar ordens de compra no Project Operations para cenários baseados em recursos/não estocados**.
3. Selecione **Habilitar**.
4. Configure materiais não estocados e faturas de fornecedores pendentes, conforme descrito em [Configurar materiais não estocados e faturas de fornecedores pendentes](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Crie uma ordem de compra do projeto a partir da lista de ordens de compra do projeto

1. No Finance, acesse **Gerenciamento e contabilidade de projeto** > **Projetos** > **Todos os Projetos** e selecione um projeto.
2. No Painel de Ações, na guia **Gerenciar**, no grupo **Novo**, selecione **Tarefa de item** > **Ordem de compra**.
3. Na página **Criar ordem de compra**, selecione o fornecedor ao qual deseja fazer a ordem de compra, insira outras informações conforme apropriado e selecione **OK**.
4. Na página **Ordem de compra**, na grade **Linhas da ordem de compra**, selecione **Adicionar linha**.
5. Insira um número de item, quantidade, unidade, preço unitário e outras informações conforme apropriado.

    > [!NOTE]
    > Somente itens e serviços não estocados podem ser usados com ordens de compra do projeto. Não há suporte a itens estocados e categorias de compras.

6. Continue a adicionar itens conforme necessário e confirme a ordem de compra.

    É possível registrar os recebimentos de produtos e serviços criando e lançando um recebimento de produto.

    > [!NOTE]
    > As receitas do produto não são registradas nos dados reais do projeto no Microsoft Dataverse e não afetam o livro auxiliar do projeto.

    Depois que um fornecedor envia a fatura para itens e serviços na ordem de compra, o departamento de compras pode gerar uma fatura para a ordem de compra acessando **Fatura** > **Gerar** > **Fatura** no Painel de Ações. Para obter mais informações sobre faturas de fornecedores pendentes, consulte [Comprar materiais não estocados usando uma fatura de fornecedor pendente](pending-vendor-invoices.md).
