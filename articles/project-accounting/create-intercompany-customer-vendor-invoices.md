---
title: Criar faturas intercompanhia de clientes e fornecedores
description: Este tópico fornece informações sobre como criar faturas intercompanhia de clientes e fornecedores.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9448cb29adb4206efaabe3f313a1f619cd32b9be
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591482"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Criar faturas intercompanhia de clientes e fornecedores

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Um contador do projeto em uma entidade legal que faz o empréstimo cria uma fatura de cliente intercompanhia para os custos do projeto que estão sendo transferidos para a entidade que toma o empréstimo. Depois que a fatura do cliente intercompanhia for aprovada e lançada, a entidade legal que faz o empréstimo envia a fatura intercompanhia para a entidade legal que toma o empréstimo.

O contador do projeto da entidade legal que faz o empréstimo pode configurar um processo em lotes para gerar faturas intercompanhia de forma recorrente. O contador do projeto especifica os critérios, como projetos específicos, para criar faturas intercompanhia em um lote.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Criar manualmente uma fatura de cliente intercompanhia para transações do projeto 

Use este procedimento para criar manualmente uma fatura de cliente intercompanhia para transações do projeto. Pesquise as horas que foram lançadas pelos trabalhadores em projetos nas entidades legais que tomam o empréstimo e as despesas incorridas pela entidade legal em nome das entidades legais que tomam o empréstimo. É possível pesquisar por nome da entidade legal, número do contrato do projeto, número do projeto, intervalo de datas ou qualquer combinação dessas opções. Nos resultados de pesquisa, selecione as transações a serem adicionadas a uma fatura intercompanhia. 

As etapas a seguir devem ser executadas na entidade legal mutuante. 

1. No Dynamics 365 Finance, acesse **Gerenciamento e contabilidade de projeto** > **Faturas de projeto** > **Faturas de cliente intercompanhia**. Na página de lista **Faturas de cliente intercompanhia**, no Painel de Ações, selecione **Novo**.
2. Na página **Criar fatura intercompanhia**, no campo **Entidade legal**, selecione uma entidade legal de empréstimo.
3. Opcional: insira um contrato de projeto e número de projeto específicos.
4. Limite a pesquisa selecionando um intervalo de datas. Insira datas específicas nos campos **Data de início** e **Data de término**. Somente as transações intercompanhia lançadas dentro desse intervalo de datas são exibidas nos resultados da pesquisa.
5. Defina **Parâmetro da linha do diário avançado do projeto** como **Sim** e selecione **Pesquisar**.
6. Nos resultados da pesquisa, selecione as transações a serem incluídas na proposta de fatura intercompanhia e selecione **OK**.
7. Na página **Fatura de cliente intercompanhia**, as transações de projeto intercompanhia selecionadas nos resultados da pesquisa são exibidas. Para modificar as transações antes de enviar a fatura para a entidade legal que toma o empréstimo, faça o seguinte:
  
    1. Na página **Fatura de cliente intercompanhia**, abra os detalhes da fatura e selecione **Adicionar linha**.
    2. Para remover uma linha, selecione-a e selecione **Remover**.
    3. Visualize comentários, motivos, dimensões financeiras e outras informações sobre uma linha selecionada nos detalhes da linha da fatura.
    
8. Para lançar a fatura de cliente intercompanhia, no Painel de Ações, selecione **Lançar**.

> [!NOTE]
> Se a organização exigir que as faturas intercompanhia sejam revisadas antes de serem lançadas, um administrador do sistema poderá configurar um fluxo de trabalho para faturas intercompanhia. Se um fluxo de trabalho não estiver configurado para faturas intercompanhia, você pode lançar a fatura intercompanhia.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Criar um trabalho em lotes para faturas intercompanhia

É possível criar várias faturas intercompanhia ao mesmo tempo para entidades legais que tomam o empréstimo. Usando a funcionalidade de pesquisa, é possível, por exemplo, pesquisar todas as transações lançadas por trabalhadores que tomaram o empréstimo e relacionadas aos projetos gerenciados por outras entidades legais. Em seguida, para cada entidade legal que toma o empréstimo, você pode criar uma fatura intercompanhia para as transações fornecidas nos resultados de pesquisa.

1. Vá para **Gerenciamento e contabilidade de projeto** > **Periódico** > **Faturas de projeto** > **Criar faturas de cliente intercompanhia**.
2. Na página **Criar faturas de cliente intercompanhia**, no campo **Empresa**, selecione uma entidade legal para faturar. Se você não selecionar uma empresa, todas as transações que atendem aos critérios de pesquisa são exibidas para todas as entidades legais que tomam o empréstimo.
3. Em **Criar uma fatura por**, selecione se deseja criar uma fatura para transações intercompanhia com base em um projeto ou em uma entidade legal que toma o empréstimo.
4. Opcional: para selecionar um projeto e um contrato de projeto específicos para criar faturas intercompanhia, clique em **Selecionar**. Na página **Consulta**, no campo **Critérios**, selecione o contrato do projeto, número do projeto, ou ambos, e selecione **OK**.
5. Na guia **Lote**, configure um processo em lotes para criar faturas intercompanhia com frequência. Para obter mais informações, consulte [Enviar um trabalho de processamento em lotes de um formulário](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Para lançar faturas intercompanhia, no Painel de Ações, selecione **Lançar**.

> [!NOTE]
> Se a organização exigir que as faturas intercompanhia sejam revisadas antes de serem lançadas, um administrador do sistema poderá configurar um fluxo de trabalho para faturas intercompanhia. Se um fluxo de trabalho não estiver configurado para faturas intercompanhia, você pode lançar faturas intercompanhia.

## <a name="post-the-intercompany-vendor-invoice"></a>Lançar a fatura de fornecedor intercompanhia

Um contador de projeto na entidade legal que toma o empréstimo pode revisar as faturas de fornecedores intercompanhia pendentes quando a fatura de cliente intercompanhia correspondente é lançada. No Finance, na entidade legal que toma o empréstimo, vá para **Contas a pagar** > **Faturas** > **Fatura de fornecedor pendente**. O número da fatura pendente corresponderá ao número da fatura do cliente intercompanhia. Verifique se a fatura está correta e lance a fatura. Lançar a fatura de fornecedor intercompanhia cria uma transação no diário-razão auxiliar e na contabilidade do projeto que reflete os custos de transação na entidade legal que toma o empréstimo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
