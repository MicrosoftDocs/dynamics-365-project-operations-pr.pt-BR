---
title: Configurar e usar pagamentos de fornecedor pagar-quando-pago
description: Este tópico explica como criar termos de pagar-quando-pago (PWP) para que você possa liberar pagamentos parciais do fornecedor, com base nos pagamentos do cliente.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: f2469c8396eb4867b435f70b046aa421552d0fa1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288568"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Configurar e usar pagamentos de fornecedor pagar-quando-pago

[!include [banner](../includes/banner.md)]

Ao aprovar um fornecedor para trabalhar como subcontratado, talvez você queira reter o pagamento ao fornecedor até que o cliente pague pelo projeto. Para oferecer suporte a esse cenário, você pode configurar os termos de pagar-quando-pago (PWP) ao configurar a ordem de compra (OC) com o fornecedor.

Por exemplo, quando um cliente paga um valor em uma fatura de projeto, você pode liberar parte ou todo o valor da fatura do fornecedor. Basta configurar os termos de PWP que especificam que o fornecedor receberá o pagamento depois que você receber uma porcentagem do pagamento relacionado do cliente. Se você receber o pagamento parcial de um cliente, poderá liberar manualmente algumas das faturas de fornecedores relacionadas para pagamento.

O exemplo a seguir descreve o processo quando os termos de PWP são usados.

## <a name="example"></a>Exemplo

Sua organização concorda em fornecer a um cliente 100 computadores com software instalado, por um preço de 150,00 dólares americanos (USD) por computador. Depois, você contrata um fornecedor para fornecer os computadores que possuem o software instalado. De acordo com o contrato, o cliente deve aprovar a qualidade dos computadores antes de pagar sua organização. A política da sua organização consiste em reter o pagamento aos fornecedores até que o cliente pague a você. Portanto, você configura o projeto para que tenha uma porcentagem de PWP de 100%.

O fornecedor envia para você os 100 computadores que possuem o software instalado, juntamente com uma fatura de 10.000,00 USD. Como os termos de PWP são configurados para o seu projeto, você não paga o fornecedor no recebimento dos computadores. Em vez disso, você envia os computadores ao cliente, juntamente com uma fatura de 15.000,00. O cliente inspeciona os computadores e aprova o valor total da fatura do projeto.

Depois de receber o pagamento integral do cliente, você paga ao fornecedor 10.000,00, o valor total da fatura do fornecedor.

## <a name="set-up-pwp-terms-for-a-project"></a>Configurar os termos de PWP para um projeto

Ao configurar os termos de PWP para um projeto, você deve especificar, como uma porcentagem, o valor mínimo que um cliente deve pagar a você pelo projeto antes que você pague ao fornecedor. O valor limite é calculado automaticamente nas faturas do cliente para o projeto. Siga estas etapas para configurar a porcentagem limite para os termos de PWP.

1. Acesse **Gerenciamento e contabilidade de projeto** \> **Projetos** \> **Todos os projetos**.
2. Encontre e abra o projeto para o qual deseja configurar os termos de PWP.
3. Na FastTab **Contratos de fornecedores**, selecione **Adicionar linha**.
3. No campo **Código de conta**, selecione uma das seguintes opções:

    - **Tabela** – Os termos de PWP se aplicam a um único fornecedor.
    - **Grupo** – Os termos de PWP se aplicam a todos os fornecedores em um grupo de fornecedores.
    - **Todos** – Os termos de PWP se aplicam a todos os fornecedores.

4. Se você selecionou **Tabela** ou **Grupo** na etapa anterior, no campo **Fornecedor/Grupo de fornecedores**, selecione o fornecedor ou grupo de fornecedores ao qual os termos de PWP se aplicam. Se você selecionou **Todos** na etapa anterior, o campo **Fornecedor/Grupo de fornecedores** não pode ser editado.
5. Se os termos de retenção do fornecedor forem configurados para o fornecedor no projeto, no campo **Termos de retenção do fornecedor**, selecione a ID da regra para os termos de retenção.
6. No campo **Porcentagem limite de PWP**, insira a porcentagem limite para o projeto. A porcentagem que você insere para o projeto define o valor mínimo que o cliente deve pagar a você antes de você pagar ao fornecedor.

## <a name="create-a-po-that-has-pwp-terms"></a>Criar uma ordem de compra que tenha termos de PWP

Quando você lança uma fatura de um fornecedor, se o fornecedor estiver sujeito aos termos de PWP, esses termos serão exibidos nas linhas da ordem. Para criar uma ordem de compra com termos de PWP, siga estas etapas:

1. Acesse **Aquisição e fornecimento** \> **Ordens de compra** \> **Todas as ordens de compra**.
2. No Painel de Ação, selecione **Novo**. Em seguida, na caixa de diálogo **Criar uma ordem de compra**, insira as informações necessárias e selecione **OK**.

    Como alternativa, abra uma de OC existente na página de lista **Todas as ordens de compra**.

4. Na página **Ordem de compra**, na FastTab **Linhas de ordem de compra**, analise os detalhes da linha de OC do fornecedor. A opção **Pagar quando pago** é selecionada automaticamente, e o valor no campo **Porcentagem limite de PWP** é copiado automaticamente do campo **Porcentagem limite de PWP** na página **Projetos**.
6. Se você não quiser aplicar os termos de PWP ao fornecedor para uma linha de OC, desmarque a opção **Pagar quando pago**. Nesse caso, o campo **Porcentagem limite de PWP** para a linha de OC será redefinido para 0 (zero).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Atualizar o pagamento do cliente e pagar ao fornecedor

Quando um fornecedor conclui seu trabalho em um projeto e envia uma fatura para você, será preciso analisar o status do projeto e as faturas do cliente para determinar se os termos de PWP foram atendidos para o projeto. Se os termos de PWP para o fornecedor foram atendidos, você pode determinar quais linhas da fatura do fornecedor pagar, com base nos pagamentos do cliente para o projeto. Se você decidir pagar ao fornecedor mesmo que os termos de PWP não tenham sido atendidos, você pode substituir os termos de PWP na página **Fatura do fornecedor com pagar quando pago**.

1. Acesse **Gerenciamento e contabilidade de projeto** \> **Consultas e relatórios** \> **Consultas de retenção** \> **Fatura do fornecedor com pagar quando pago**.
2. Na página **Faturas do fornecedor com pagar quando pago**, no campo de pesquisa, insira valores para encontrar a fatura de fornecedor que deseja analisar e selecione **Pesquisar**.
3. Na FastTab **Linhas de fatura de fornecedor**, selecione as linhas que você deseja alterar.
4. Se as condições **Pagar quando pago** forem atendidas para a linha da fatura, selecione **Liberar pagamento do fornecedor**. A opção **Pagar quando pago** é desmarcada e o valor do campo **Pronto para pagamento** é alterado para **Sim**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]