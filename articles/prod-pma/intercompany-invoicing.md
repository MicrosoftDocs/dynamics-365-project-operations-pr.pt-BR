---
title: Faturamento intercompanhia
description: Este artigo fornece informações e exemplos sobre o faturamento intercompanhia de projetos.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76eba87e7cc78dcc14510a8fb53677d626bf204f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270754"
---
# <a name="intercompany-invoicing"></a>Faturamento intercompanhia

[!include [banner](../includes/banner.md)]

Este artigo fornece informações e exemplos sobre o faturamento intercompanhia de projetos.

Sua organização pode ter várias divisões, subsidiárias e outras entidades legais que transferem produtos e serviços de outros projetos entre si. A entidade legal que fornece o serviço ou produto é chamada de *entidade legal que faz o empréstimo*, e a entidade legal que recebe o serviço ou produto é chamada de *entidade legal que toma o empréstimo*. 

A ilustração a seguir mostra um cenário típico em que duas entidades legais, SI FR (a entidade legal que toma o empréstimo) e SI USA (a entidade legal que faz o empréstimo) compartilham recursos para entregar um projeto para o cliente A. Para esse cenário, SI FR é contratada para entregar o trabalho para o cliente A. 

[![Exemplo de faturamento intercompanhia](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

O objetivo é tornar o controle de custos, o reconhecimento de receita, os impostos e o preço de transferência para transações de projetos intercompanhia mais flexíveis e eficientes. Além disso, os seguintes recursos são fornecidos:

-   Criar faturas de cliente para um projeto em uma entidade legal que toma o empréstimo usando folhas de ponto, despesas e faturas de fornecedor intercompanhia em uma entidade legal que faz o empréstimo.
-   Oferecer suporte a cálculos de impostos e custos indiretos.
-   Adiar o reconhecimento da receita em uma entidade legal que faz o empréstimo e quando uma entidade legal que toma o empréstimo deve reconhecer o custo.
-   Acumular receita de trabalho em processo (WIP) na entidade legal que faz o empréstimo.
-   Definir preços de transferência que podem ser baseados em vários modelos de preços. Veja alguns exemplos:
    -   **Quantidade** — o valor que você insere no campo **Preços** é o custo real por quantidade ou unidade.
    -   **Valor de encargos** — o preço/custo por transação mais o valor de encargos que você insere no campo **Preços**.
    -   **Porcentagem dos encargos** — o preço de transferência é o preço/custo por transação multiplicado pela porcentagem dos encargos que você insere no campo **Preços**.
    -   **Porcentagem do preço de venda** — a porcentagem do preço de venda que é transferida para a entidade legal que faz o empréstimo.
    -   **Quantidade abaixo do preço de venda** — o valor que a entidade legal que toma o empréstimo retém dos preços de venda antes da transferência para a entidade legal que faz o empréstimo.
    -   **Taxa de contribuição** — o número que você insere no campo **Preços** é a taxa de contribuição, que é expressa como uma porcentagem do preço de venda.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Exemplo 1: Configurar parâmetros para o faturamento intercompanhia
Neste exemplo, USSI é uma entidade legal que faz o empréstimo e seus recursos estão relatando as horas para a entidade legal que toma o empréstimo, FRSI, que é proprietária do contrato com o cliente final. As horas e as despesas que os funcionários da USSI relatam podem ser incluídas na fatura do projeto que a FRSI gera. Além disso, há uma terceira fonte de transações que pode se originar da entidade legal que faz o empréstimo (USSI neste exemplo) quando ela fornece serviços de fornecedores compartilhados para subsidiárias (como FRSI) e então repassa esses custos para projetos nessas subsidiárias. Todos os documentos de fatura e cálculos de impostos correspondentes são concluídos pelo Finance. 

Para este exemplo, FRSI deve ser um cliente na entidade legal USSI e USSI deve ser um fornecedor na entidade legal FRSI. Você poderá então configurar um relacionamento intercompanhia entre as duas entidades legais. O procedimento a seguir mostra como configurar os parâmetros para que as entidades legais possam participar do faturamento intercompanhia.

1. Configure FRSI como um cliente na entidade legal USSI e configure USSI como um fornecedor na entidade legal FRSI. Existem três pontos de entrada para as etapas necessárias desta tarefa.

   | Etapa |                                                       Ponto de entrada                                                        |                                                                                                                                                                                               Descrição                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  T   | Em USSI, clique em <strong>Contas a receber</strong> &gt; <strong>Clientes</strong> &gt; <strong>Todos os clientes</strong>. |                                                                                                                                                                  Crie um registro de cliente para FRSI e selecione o grupo de clientes.                                                                                                                                                                  |
   |  N   |    Em FRSI, clique em <strong>Contas a pagar</strong> &gt; <strong>Fornecedores</strong> &gt; <strong>Todos os fornecedores</strong>.     |                                                                                                                                                                    Crie um registro de fornecedor para USSI e selecione o grupo de fornecedores.                                                                                                                                                                    |
   |  C   |                                  Em FRSI, abra o registro do fornecedor que você acabou de criar.                                  | No Painel de Ações, na guia <strong>Geral</strong>, no grupo <strong>Configuração</strong>, clique em <strong>Intercompanhia</strong>. Na página <strong>Intercompanhia</strong>, na guia <strong>Relação comercial</strong>, mude o controle deslizante <strong>Ativo</strong> para <strong>Sim</strong>. No campo <strong>Empresa do cliente</strong>, selecione o registro do cliente que você criou na etapa A. |


2. Clique em **Gerenciamento e contabilidade de projeto** &gt; **Configurar** &gt; **Parâmetros de gerenciamento e contabilidade de projeto** e clique na guia **Intercompanhia**. A maneira como você configura os parâmetros depende se você é a entidade legal que toma o empréstimo ou a entidade legal que faz o empréstimo.
   -   Se você for a entidade legal que toma o empréstimo, selecione a categoria de aquisição que deve ser usada para corresponder às faturas de fornecedor, que são geradas automaticamente.
   -   Se você for a entidade legal que faz o empréstimo, para cada entidade que toma o empréstimo, selecione uma categoria de projeto padrão para cada tipo de transação. As categorias de projeto são usadas para configuração de imposto quando a categoria faturada em transações intercompanhia existe somente na entidade legal que toma o empréstimo. Você pode optar por acumular receita para transações intercompanhia. Esse acúmulo é feito quando as transações são lançadas e, em seguida, revertidas quando a fatura intercompanhia é lançada.

3. Clique em **Gerenciamento e contabilidade de projeto** &gt; **Configurar** &gt; **Preços** &gt; **Preço de transferência**.
4. Selecione uma moeda, um tipo de transação e um modelo de preço de transferência. A moeda usada na fatura é a moeda configurada no registro do cliente para a entidade legal que toma o empréstimo na entidade legal que faz o empréstimo. A moeda é usada para fazer a correspondência das entradas na tabela de preços de transferência.
5. Clique em **Contabilidade** &gt; **Configuração de lançamento** &gt; **Contabilidade intercompanhia** e configure um relacionamento para USSI e FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Exemplo 2: Criar e lançar uma folha de ponto intercompanhia
USSI, a entidade legal que faz o empréstimo, deve criar e lançar a folha de ponto para um projeto da FRSI, a entidade legal que toma o empréstimo. Existem dois pontos de entrada para as etapas necessárias desta tarefa.

| Etapa | Ponto de entrada                                                                       | Descrição                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T    | **Gerenciamento e contabilidade de projeto** &gt; **Folhas de ponto** &gt; **Todas as folhas de ponto** | Crie uma folha de ponto. Na linha da folha de ponto, no campo **Entidade legal**, selecione **FRSI**. No campo **ID do Projeto**, selecione o projeto na FRSI. Insira as horas para cada dia da semana. |
| N    | Página **Folha de ponto**                                                                | Após a execução do fluxo de trabalho, lance a folha de ponto e anote o número do comprovante.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Exemplo 3: Criar e lançar uma fatura de fornecedor intercompanhia
USSI, a entidade legal que faz o empréstimo, deve criar e lançar a fatura de fornecedor intercompanhia para um projeto da FRSI, a entidade legal que toma o empréstimo. Essa fatura de fornecedor representa a mão de obra terceirizada e as despesas realizadas por fornecedores que são pagos pela USSI. Existem dois pontos de entrada para as etapas necessárias desta tarefa.

| Etapa | Ponto de entrada                                                                                      | Descrição                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T    | **Contas a pagar** &gt; **Faturas** &gt; **Faturas de fornecedor em aberto** &gt; **Nova fatura de fornecedor** | Crie uma fatura de fornecedor e insira os serviços que foram adquiridos em nome do projeto da FRSI.                                                                                                                                                                                  |
| N    | A página **Fatura de fornecedor**                                                                      | Insira linhas que representem os serviços terceirizados em nome da FRSI. Na FastTab **Detalhes da linha**, na guia **Projeto** para a linha da fatura, no campo **Empresa do projeto**, insira **FRSI**. Insira o projeto e as informações correspondentes. Em seguida, lance a fatura de fornecedor. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Exemplo 4: Criar e lançar a fatura intercompanhia
USSI, a entidade legal que faz o empréstimo, deve criar e lançar a fatura intercompanhia. Existem dois pontos de entrada para as etapas necessárias desta tarefa.

| Etapa | Ponto de entrada                                                                                             | Descrição                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| T    | **Gerenciamento e contabilidade de projeto** &gt; **Faturas de projeto** &gt; **Fatura de cliente intercompanhia**  | Clique em **Novo** para abrir a página **Criar fatura intercompanhia**.                                                                                  |
| N    | **Gerenciamento e contabilidade de projeto** &gt; **Faturas de projeto** &gt; **Faturas de cliente intercompanhia** | Na página **Criar fatura intercompanhia**, insira a entidade legal, especifique a transação que deve ser incluída e clique em **Pesquisar**. |
| C    | **Gerenciamento e contabilidade de projeto** &gt; **Faturas de projeto** &gt; **Faturas de cliente intercompanhia** | Selecione as transações a serem faturadas ou clique em **Selecionar tudo** para faturar todas as transações na lista e, em seguida, clique em **OK**.                  |
| D    | A página **Fatura intercompanhia**                                                                       | A proposta de fatura de cliente intercompanhia será exibida.                                                                                             |
| E    | A página **Fatura intercompanhia**                                                                       | Clique em **Lançar**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Exemplo 5: Lançar a fatura de fornecedor e faturar o cliente
Quando a entidade legal que faz o empréstimo, USSI, lança a fatura de cliente intercompanhia, uma fatura de fornecedor pendente correspondente é criada na entidade legal que toma o empréstimo, FRSI. Depois que essa fatura de fornecedor é lançada, a FRSI também fatura o cliente do projeto pelas horas inseridas pela USSI. Existem três pontos de entrada para as etapas necessárias desta tarefa.

| Etapa | Ponto de entrada                                                                                        | Descrição                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| T    | **Contas a pagar** &gt; **Faturas** &gt; **Faturas de fornecedores pendentes**                            | Revise a fatura para verificar se os valores da folha de ponto estão incluídos e, a seguir, lance a fatura de fornecedor.                  |
| N    | **Gerenciamento e contabilidade de projeto** &gt; **Faturas de projeto** &gt; **Propostas de fatura do projeto** | Crie uma nova fatura de projeto para o projeto e verifique se as transações de horas que foram lançadas são exibidas.            |
| C    | A página **Fatura de projeto**                                                                       | Selecione a fatura do projeto e clique em **Exibir detalhes** para revisar os valores de custo e de vendas. Em seguida, lance a fatura. |


Para obter mais informações, consulte [Configurar faturamento intercompanhia de projetos](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]