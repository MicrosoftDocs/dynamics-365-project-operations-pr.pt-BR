---
title: Recuperação de IVA
description: Este tópico explica como recuperar reembolsos em transações de imposto sobre valor agregado (IVA).
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49397592ea002b9da872ac1aa455719b6ca2292e
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960188"
---
# <a name="vat-recovery"></a>Recuperação de IVA 

Para receber reembolsos em transações qualificadas de imposto sobre valor agregado (IVA), uma empresa ou organização deve identificar, coletar, verificar e enviar informações precisas. Esse processo inclui várias tarefas e, dependendo do tamanho da sua empresa, pode incluir vários funcionários ou funções.

Para recuperar o IVA usando o gerenciamento de despesas, os seguintes pré-requisitos devem ser preenchidos:

- Os códigos de imposto devem ser criados para países/regiões alocadas para categorias de despesas.
- Um grupo de impostos deve ser criado para cada código de imposto.
- Um código de impostos de item deve ser criado para cada grupo de impostos.

Após a conclusão dos pré-requisitos, os funcionários seguem as etapas a seguir para solicitar o reembolso das transações de IVA.

1. Em um relatório de despesas, insira as informações fiscais sobre transações de cartão de crédito para identificar reembolsos de IVA qualificados.
2. Verifique se todas as informações fiscais estão completas e lance o relatório de despesas.
3. Processe as despesas que são qualificadas para a restituição de IVA internacional.
4. Envie os dados de restituição de IVA ao fornecedor terceirizado para fazer as declarações de restituição internacional.
5. Processe as despesas para a restituição de IVA interno.

As seções a seguir fornecem exemplos que mostram como os funcionários da Contoso concluem cada etapa.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Em um relatório de despesas, insira as informações fiscais sobre transações de cartão de crédito para identificar reembolsos de IVA qualificados

Gabrielle, uma representante de vendas da Contoso que mora nos EUA, voltou recentemente de uma viagem de vendas ao Reino Unido. Durante a viagem, ela teve algumas despesas pessoais com cartão de crédito para as refeições. Agora, Gabrielle deve criar um relatório de despesas para reconciliar as despesas.

Ao inserir as informações no relatório de despesas, ela seleciona **Reino Unido** no campo **País/região** na página **Editar relatório de despesas**. A lista de grupos de impostos é filtrada para mostrar somente os grupos que se aplicam ao Reino Unido. Gabrielle seleciona o grupo de impostos **Reino Unido 001** e seleciona o grupo de impostos **Refeições** do item. Ela adiciona uma nova transação para hospedagem. Como há somente um grupo de impostos e um grupo de impostos de itens para hospedagem no Reino Unido, essas informações são preenchidas automaticamente no relatório de despesas dela.

De acordo com a política da Contoso, todas as despesas devem ter um recibo correspondente. Portanto, quando Gabrielle salva o relatório de despesas, ela recebe uma mensagem informando que é necessário anexar um recibo para cada transação listada no relatório de despesas. Ela verifica se anexou uma imagem digital de cada recibo de transação ao relatório de despesas e envia o relatório para aprovação. Ela então envia os recibos físicos para a equipe de processamento de back office. Essa equipe enviará os dados de restituição de IVA ao fornecedor terceirizado que faz as declarações de restituição de IVA internacional para a Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Verifique se todas as informações fiscais estão completas e lance o relatório de despesas

Ana, a coordenadora de Contas a pagar da Contoso, deve inserir todas as informações fiscais que estiverem faltando em um relatório de despesas antes que o relatório possa ser postado. Ela abre a página **Detalhes do relatório de despesas** e vê o relatório de despesas aprovado de Gabrielle. Ana abre o relatório de despesas para ver os detalhes das transações. Ela vê que Gabrielle não inseriu o grupo de impostos de um item em uma das transações. Como essas informações não foram fornecidas, Ana não pode postar o relatório de despesas. Portanto, Ana verifica a página **Configurações fiscais** em Gerenciamento de despesas e encontra o grupo de impostos do item apropriado para o país/região e o tipo de transação. Ana agora pode lançar o relatório de despesas na contabilidade.

Ao lançar o relatório de despesas, um item de trabalho de IVA recuperável é criado. Este item de trabalho é atribuído a um membro da equipe de processamento de back office. Ana recebe uma mensagem que confirma que a postagem teve êxito. A mensagem também lista o número de transações de IVA que foram identificadas para restituição.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Processar as despesas que estão qualificadas para a restituição de IVA internacional

Alberto, um membro da equipe de processamento de back office da Contoso, é responsável por confirmar se todas as informações necessárias para a restituição do IVA estão incluídas nos relatórios de despesas. Ele abre a página **Restituição de imposto de despesa** e seleciona o relatório de despesas que Gabrielle enviou. Alberto verifica se todos os recibos necessários foram anexados e se o grupo de impostos correto e os códigos de imposto do item foram inseridos.

Quando Alberto recebe os recibos físicos de Gabrielle, ele verifica os recibos físicos em relação aos recibos digitais e altera o status do relatório de despesas para **Pronto para recuperação**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Envie os dados de restituição de IVA ao fornecedor terceirizado para fazer as declarações de restituição internacional

Quando Alberto estiver pronto para enviar os dados do relatório de despesas ao fornecedor terceirizado que fará as declarações de restituição do IVA, ele abrirá a página **Restituição de imposto de despesa**. Ele filtra a página para que somente os relatórios de despesas marcados como **Pronto para recuperação** sejam exibidos. Alberto seleciona **Arquivo** &gt; **Exportar para Excel**. As informações de IVA dos relatórios de despesas são exportadas para uma planilha do Microsoft Excel. Ele envia essa planilha para o fornecedor terceirizado e inclui uma mensagem informando que os recibos físicos foram enviados por courier.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Processar as despesas para a restituição de IVA interno

Alberto deve verificar se as transações do relatório de despesas estão qualificadas para a restituição de IVA e se os recibos digitais foram anexados aos relatórios. Para começar a processar as despesas qualificadas para a restituição interna, Alberto abre a página **Restituição de imposto de despesa** e seleciona o relatório de despesas que requer verificação. Ele verifica se os recibos estão em nome da empresa e não no do funcionário. Para a recuperação do IVA, os recibos devem estar em nome da empresa. Alberto então confirma se o grupo de impostos sobre vendas correto e os códigos de imposto sobre vendas do item foram aplicados.

Ao receber os recibos físicos, Alberto altera o status do relatório de despesas para **Pronto para recuperação**. Ele poderá, então, fazer a declaração junto à autoridade fiscal apropriada. Nesse caso, a autoridade fiscal apropriada nos EUA é o Serviço da Receita Federal (Internal Revenue Service — IRS).
