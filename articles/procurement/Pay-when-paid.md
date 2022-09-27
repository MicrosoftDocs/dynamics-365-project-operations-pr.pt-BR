---
title: Pagamentos de fornecedor pagar quando pago
description: Este tópico explica como usar o cenário PWP (pagar quando pago).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525327"
---
# <a name="pay-when-paid-vendor-payments"></a>Pagamentos de fornecedor pagar quando pago

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico explica como usar o cenário PWP (pagar quando pago).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Criar uma ordem de compra que tenha termos PWP

Quando você lança a fatura de um fornecedor, se o fornecedor estiver sujeito aos termos de PWP, esses termos serão exibidos nas linhas da OC (ordem de compra). Para criar uma ordem de compra com termos de PWP, siga estas etapas:

1. Siga uma ou destas etapas no Microsoft Dynamics 365 Finance:

    - Acesse **Aquisição e fornecimento** \> **Ordens de compra** \> **Todas as ordens de compra**. No Painel de Ação, selecione **Novo**. Na caixa de diálogo **Criar ordem de compra**, selecione o fornecedor para o qual os termos de PWP estão configurados no projeto, insira as outras informações necessárias e selecione **OK**.
    - Acesse **Gerenciamento e contabilidade de projeto** \> **Projetos** \> **Todos os projetos**. No Painel de Ações, na guia **Gerenciar**, selecione **Tarefa do item**. Selecione a ordem de compra. Selecione o fornecedor para o qual os termos do PWP estão configurados no projeto e, em seguida, selecione **OK**.

2. Na página **Ordem de compra**, na Guia Rápida **Linhas da ordem de compra**, selecione **Adicionar linha** para criar uma linha de ordem de compra.
3. Selecione o número do item ou a categoria de compras e insira os outros detalhes necessários. Revise os detalhes da linha da OC para o fornecedor.

    A opção **Pagar quando pago** é selecionada automaticamente, e o valor no campo **Porcentagem limite de PWP** é copiado automaticamente do campo **Porcentagem limite de PWP** na página **Projetos**.

4. Se você não quiser aplicar os termos de PWP ao fornecedor para uma linha de OC, desmarque a opção **Pagar quando pago**. Nesse caso, o campo **Porcentagem limite de PWP** para a linha da OC será redefinido como **0** (zero).
5. Na página **Ordem de compra**, no Painel de Ações, na guia **Compra**, selecione **Confirmar** para confirmar a ordem de compra.
6. No Painel de Ações, na guia **Fatura**, selecione **Fatura** para gerar a fatura para a ordem de compra.

## <a name="create-a-project-invoice-proposal"></a>Criar uma proposta de fatura do projeto

As propostas de fatura de projeto são usadas para criar faturas de projeto para o cliente. No cenário de PWP, os pagamentos do fornecedor dependem dos pagamentos do cliente de acordo com as configurações do PWP. No entanto, existem opções que permitem liberar os pagamentos sem os pagamentos do cliente, conforme necessário. Para criar uma fatura de projeto para o cliente, siga estas etapas:

1. Nos aplicativos de participação do cliente, acesse **Project** \> **Projetos** e selecione o projeto.
2. Na guia **Dados reais**, selecione a linha real que é gerada pela OC que tenha o tipo de transação **Vendas não faturadas**. Em seguida, selecione **Pronto para fatura**.
3. Acesse **Sales** \> **Vendas** \> **Contrato do projeto** e selecione o contrato do projeto.
4. No Painel de Ações, selecione **Fatura** para gerar a fatura de cliente.
5. No Finance, acesse **Gerenciamento e contabilidade de projetos** \> **Periódico** \> **Importar da tabela de preparação** e selecione **OK** para gerar o diário de integração do Project Operations.
6. Acesse **Gerenciamento de projetos e contabilidade** \> **Faturas do projeto** \> **Proposta de fatura do projeto** e selecione **Lançar** para lançar a proposta de fatura que foi gerada para o projeto.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Atualizar o pagamento do cliente e pagar ao fornecedor

Quando um fornecedor conclui seu trabalho em um projeto e envia uma fatura para você, será necessário analisar o status do projeto e as faturas do cliente para determinar se os termos de PWP foram atendidos para o projeto. Se os termos de PWP para o fornecedor foram atendidos, você pode determinar quais linhas da fatura do fornecedor pagar, com base nos pagamentos do cliente para o projeto. Se você decidir pagar ao fornecedor mesmo que os termos de PWP não tenham sido atendidos, você pode substituir os termos de PWP na página **Fatura do fornecedor com pagar quando pago**.

1. No Finance, acesse **Gerenciamento e contabilidade de projeto** \> **Projetos** \> **Todos os projetos** e selecione o projeto.
2. No Painel de Ações, selecione **Controlar** e, em seguida, selecione **Faturas de fornecedor** para mostrar todas as faturas de fornecedor que foram geradas para o projeto.
3. Na página **Faturas do fornecedor com pagar quando pago**, no campo de pesquisa, insira valores para encontrar a fatura de fornecedor que deseja analisar e selecione **Pesquisar**.
4. Selecione a opção **Pagar quando pago** para exibir somente as faturas de PWP.
5. Na Guia Rápida **Linhas de fatura de fornecedor**, selecione as linhas que deseja liberar para pagamento.
6. Selecione **Liberar pagamento do fornecedor**. A opção **Pagar quando pago** é desmarcada e o valor do campo **Pronto para pagamento** é alterado para **Sim**.
