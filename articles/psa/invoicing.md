---
title: Faturando no Project Service Automation
description: Este tópico fornece informações sobre faturamento.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f8107a660f9993c7b6a32d69047a81fb7e0abef8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071492"
---
# <a name="invoicing-in-project-service-automation"></a>Faturando no Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O faturamento no Dynamics 365 Project Service Automation é útil porque fornece aos gerentes de projeto um segundo nível de aprovação antes da criação das faturas para os clientes. O primeiro nível de aprovação é concluído quando as entradas de tempo e despesa que os membros da equipe do projeto enviam são aprovadas.

O PSA não foi desenvolvido para gerar faturas voltadas para o cliente pelos seguintes motivos:

- Ele não contém informações de imposto.
- Ele não pode converter outras moedas na moeda de faturamento usando taxas de câmbio configuradas corretamente.
- Ele não pode formatar faturas corretamente para que possam ser impressas.

Porém, você pode usar um sistema financeiro ou contábil para criar faturas voltadas para o cliente que usa as informações das propostas de fatura que são geradas no PSA.

## <a name="creating-project-invoices-in-psa"></a>Criando faturas de projeto no PSA

As faturas do projeto podem ser criadas uma a uma ou em massa. Também é possível criá-las manualmente, ou elas podem ser configuradas para que sejam geradas em execuções automatizadas.

### <a name="manually-create-project-invoices-in-psa"></a>Criar manualmente faturas do projeto no PSA

Na página de lista **Contratos do Projeto** , é possível criar faturas do projeto separadamente para cada contrato de projeto ou criar faturas em massa para vários contratos de projeto.

Siga esta etapa a fim de criar uma fatura para um contrato de projeto específico.

- Na página de lista **Contratos de Projeto** , abra um contrato de projeto e selecione **Criar Fatura**.

    ![Criando faturas do projeto para um contrato de projeto específico](media/CreateProjectInvoicesOneByOne.png)

    Uma fatura é gerada para todas as transações do contrato de projeto selecionado que tem um status de **Pronto para Faturar**. Essas transações incluem tempo, despesas, etapas e linhas de contrato baseadas em produto.

Siga estas etapas para criar faturas em massa.

1. Na página de lista **Contratos de Projeto** , selecione um ou mais contratos de projeto para os quais você deve criar uma fatura e selecione **Criar Faturas do Projeto**.

    ![Criando faturas de projeto em massa](media/CreateProjectInvoicesBulk.png)

    Uma mensagem de aviso informa que pode haver um atraso antes da criação das faturas. O processo também é mostrado.

2. Selecione **OK** para fechar a caixa da mensagem.

    Uma fatura é gerada para todas as transações em uma linha de contrato com um status de **Pronto para Faturar**. Essas transações incluem tempo, despesas, etapas e linhas de contrato baseadas em produto.

3. Para exibir as faturas que são geradas, vá para **Vendas** \> **Cobrança** \> **Faturas**. Você verá uma fatura para cada contrato de projeto.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Configurar a criação automatizada das faturas do projeto no PSA

Siga estas etapas para configurar uma fatura automatizada no PSA.

1. Vá para **Project Service** \> **Configurações** \> **Trabalhos em lote**.
2. Crie um trabalho em lote e denomine-o **Criação de Faturas no PSA**. O nome do trabalho em lote deve incluir o termo "Criar Faturas".
3. No campo **Tipo de trabalho** , selecione **Nenhum**. Por padrão, as opções **Frequência Diária** e **Está Ativo** são definidas como **Sim**.
4. Selecione **Executar Fluxo de Trabalho**. Na caixa de diálogo **Pesquisar Registro** , você verá três fluxos de trabalho:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Selecione **ProcessRunCaller** e selecione **Adicionar**.
6. Na próxima caixa de diálogo, selecione **OK**. Um fluxo de trabalho **Suspender** é seguido por um fluxo de trabalho **Processar**.

    Também é possível selecionar **ProcessRunner** na etapa 5. Em seguida, quando você selecionar **OK** , um fluxo de trabalho **Processar** é seguido por um fluxo de trabalho **Suspender**.

Os fluxos de trabalho **ProcessRunCaller** e **ProcessRunner** criam faturas. **ProcessRunCaller** chama **ProcessRunner**. **ProcessRunner** é o fluxo de trabalho que de fato cria as faturas. Ele passa por todas as linhas de contrato para as quais as faturas devem ser criadas e cria faturas para essas linhas. A fim de determinar as linhas de contrato para as quais as faturas devem ser criadas, o trabalho examina as datas de execução de fatura das linhas de contrato. Se as linhas de contrato que pertencem a um contrato tiverem a mesma data de execução de fatura, as transações serão combinadas em uma fatura que tenha duas linhas de fatura. Se não houver transações para as quais criar faturas, o trabalho pulará a etapa de criação de fatura.

Quando **ProcessRunner** termina de ser executado, ele chama **ProcessRunCaller** , fornece a hora de término e é fechado. **ProcessRunCaller** então inicia um timer que é executado por 24 horas a partir da hora de término especificada. Ao fim do timer, **ProcessRunCaller** é fechado.

O trabalho do processo em lote para criação de faturas é um trabalho recorrente. Se esse processo em lote for executado muitas vezes, várias instâncias do trabalho serão criadas e causarão erros. Portanto, você deve iniciar o processo em lote apenas uma vez, assim como deve reiniciá-lo apenas se a execução for interrompida.

> [!NOTE]
> O faturamento em lote no Project Service Automation é executado somente para linhas de contrato do projeto que são configuradas por agendas de fatura. Uma linha de contrato com um método de cobrança de preço fixo deve ter marcos configurados. Uma linha de contrato do projeto com um método de cobrança de horas e de material precisará de uma configuração de agenda de faturas baseada em data. As informações sobre a configuração de frequências de faturamento no contexto de um projeto que é baseado em uma linha de cotação são fornecidas no tópico [Cotações e linhas de cotação](basic-quote-lines.md#invoice-schedule). O mesmo se aplica a um projeto baseado em linha de contrato.      
 
### <a name="edit-a-draft-psa-invoice"></a>Editar uma fatura de rascunho do PSA

Quando você cria um rascunho da fatura do projeto, todas as transações de vendas não cobradas que foram criadas quando as entradas de tempo e despesa foram aprovadas são reunidas na fatura. É possível fazer os seguintes ajustes enquanto a fatura estiver em um estágio de rascunho:

- Excluir ou editar detalhes da linha da fatura.
- Editar e ajustar a quantidade e o tipo de cobrança.
- Adicionar diretamente tempo, despesa e tarifas como transações na fatura. Você pode usar esse recurso se a linha da fatura for mapeada para uma linha de contrato que permite essas classes de transação.

Selecione **Confirmar** para confirmar uma fatura. A ação Confirmar é uma ação unidirecional. Quando você seleciona **Confirmar** , o sistema torna a fatura somente leitura e cria dados reais de vendas cobradas de cada detalhe de linha de fatura para cada linha de fatura. Se os detalhes da linha da fatura fizerem referência a dados reais de vendas não cobradas, o sistema também reverterá os dados reais de vendas não cobradas. (Todos os detalhes da linha da fatura que foram criados de uma entrada de tempo ou despesa farão referência a dados reais de vendas não cobradas.) Os sistemas de integração de contabilidade podem usar essa reversão para reverter o WIP (trabalho em andamento) do projeto para fins de contabilidade.

### <a name="correct-a-confirmed-psa-invoice"></a>Corrigir uma fatura confirmada do PSA

As faturas confirmadas do PSA podem ser editadas (corrigidas). Quando você corrige uma fatura confirmada, um novo rascunho de fatura corretiva é criado. Como a suposição é de que você quer reverter todas as transações e quantidades da fatura original, essa fatura corretiva inclui todas as transações da fatura original, e todas as quantidades nela serão 0 (zero).

Se não houver transação para corrigir, você poderá removê-las do rascunho de fatura corretiva. Se quiser reverter ou retornar apenas uma quantidade parcial, você poderá editar o campo **Quantidade** nos detalhes da linha. Se você abrir os detalhes da linha da fatura, será possível ver a quantidade da fatura original. É possível editar a quantidade da fatura atual para que seja menor ou maior que a quantidade da fatura original.

Quando você confirma uma fatura corretiva, os dados reais de vendas cobradas originais são revertidos e novos dados reais de vendas cobradas são criados. Se a quantidade foi reduzida, a diferença também fará com que novos dados reais de vendas não cobradas sejam criados. Por exemplo, se as vendas cobradas originais eram por oito horas e os detalhes da linha da fatura corretiva tiverem uma quantidade reduzida de seis horas, o PSA reverterá a linha de vendas cobradas original e criará dois novos dados reais:

- Dados reais de vendas cobradas por seis horas.
- Dados reais de vendas não cobradas pelas duas horas restantes. Essa transação pode ser cobrada posteriormente ou marcada como não passível de cobrança, dependendo das negociações com o cliente.
