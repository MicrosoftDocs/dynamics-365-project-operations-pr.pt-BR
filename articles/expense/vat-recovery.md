---
title: Restituição de IVA no gerenciamento de despesas
description: Este tópico explica como receber reembolsos em transações qualificadas de imposto sobre valor agregado (IVA).
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a840c808a76c96dd5f9dfb863c230801718c203c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001682"
---
# <a name="vat-recovery-in-expense-management"></a>Restituição de IVA no gerenciamento de despesas

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Para receber reembolsos em transações qualificadas de imposto sobre valor agregado (IVA), uma empresa ou organização deve identificar, coletar, verificar e enviar informações precisas. Esse processo inclui várias tarefas e, dependendo do tamanho da sua empresa, pode incluir vários funcionários ou funções.

Para recuperar o IVA no módulo **Gerenciamento de despesas**, os seguintes pré-requisitos devem ser preenchidos:

- Os códigos de imposto devem ser criados para países/regiões alocadas para categorias de despesas.
- Um grupo de impostos deve ser criado para cada código de imposto.
- Um código de impostos de item deve ser criado para cada grupo de impostos.

Após o preenchimento dos pré-requisitos, as etapas a seguir devem ser concluídas para solicitar reembolsos de transações de IVA.

1. Em um relatório de despesas, insira as informações fiscais sobre transações de cartão de crédito para identificar reembolsos de IVA qualificados.
2. Verifique se todas as informações fiscais estão completas e lance o relatório de despesas.
3. Processe as despesas que são qualificadas para a restituição de IVA internacional.
4. Envie os dados de restituição de IVA ao fornecedor terceirizado para fazer as declarações de restituição internacional.
5. Processe as despesas para a restituição de IVA interno.

As seções a seguir fornecem exemplos que mostram como funcionários da Contoso concluem cada etapa.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Inserir as informações fiscais sobre transações de cartão de crédito para identificar reembolsos de IVA qualificados

Nancy, uma representante de vendas da Contoso baseado nos Estados Unidos, voltou recentemente de uma viagem de vendas ao Reino Unido. Durante a viagem, Gabrielle teve algumas despesas pessoais com cartão de crédito para as refeições. Agora, Gabrielle deve criar um relatório de despesas para reconciliar as despesas.

Ao inserir as informações no relatório de despesas, ela seleciona **Reino Unido** no campo **País/região** na página **Editar relatório de despesas**. A lista de grupos de impostos é filtrada para mostrar somente os grupos que se aplicam ao Reino Unido. Gabrielle seleciona o grupo de impostos **Reino Unido 001** e seleciona o grupo de impostos **Refeições** do item. Em seguida, ela adiciona uma nova transação para hospedagem. Como há somente um grupo de impostos e um grupo de impostos de itens para hospedagem no Reino Unido, essas informações são preenchidas automaticamente no relatório de despesas dela.

Por política da Contoso, todas as despesas devem ter um recibo correspondente. Portanto, quando Gabrielle salva o relatório de despesas, ela recebe uma mensagem informando que é necessário anexar um recibo para cada transação listada no relatório de despesas. Ela verifica se anexou uma imagem digital de cada recibo de transação ao relatório de despesas e envia o relatório para aprovação. Ela então envia os recibos físicos para a equipe de processamento de back office. Essa equipe enviará os dados de recuperação de IVA ao fornecedor terceirizado que registra as devoluções de recuperação de IVA internacional da Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Verificar as informações fiscais e postar um relatório de despesas

Antes de abril, o coordenador de Contas a pagar para a Contoso, pode publicar um relatório de despesas, ela deve inserir todas as informações fiscais que estiverem faltando nele. Ela abre a página **Detalhes do relatório de despesas** e vê o relatório de despesas aprovado de Gabrielle. Ana abre o relatório de despesas para ver os detalhes das transações. Ela vê que Gabrielle não inseriu o grupo de impostos de um item em uma das transações. Como essas informações não foram fornecidas, Ana não pode postar o relatório de despesas. Portanto, ela ela na página **Configurações fiscais** em Gerenciamento de despesas e encontra o grupo de impostos do item apropriado para o país/região e o tipo de transação. Ana agora pode lançar o relatório de despesas na contabilidade.

Ao lançar o relatório de despesas, um item de trabalho de IVA recuperável é criado. Este item de trabalho é atribuído a um membro da equipe de processamento de back office. Ana recebe uma mensagem que confirma que a postagem teve êxito. A mensagem também lista o número de transações de IVA que foram identificadas para restituição.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Processar as despesas que estão qualificadas para a restituição de IVA internacional

Arnie, um membro da equipe de processamento de back-office da Contoso, é responsável por verificar se todas as informações necessárias para a recuperação do IVA estão incluídas nos relatórios de despesas. Ele abre a página **Restituição de imposto de despesa** e seleciona o relatório de despesas que Gabrielle enviou. Alberto verifica se todos os recibos necessários foram anexados e se o grupo de impostos correto e os códigos de imposto do item foram inseridos.

Quando Alberto recebe os recibos físicos de Gabrielle, ele os verifica em relação aos recibos digitais e altera o status do relatório de despesas para **Pronto para recuperação**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Enviar dados de restituição de IVA ao fornecedor terceirizado

Quando Alberto estiver pronto para enviar os dados do relatório de despesas ao fornecedor terceirizado que fará as declarações de restituição do IVA, ele abrirá a página **Restituição de imposto de despesa**. Ele filtra a página para que somente os relatórios de despesas marcados como **Pronto para recuperação** sejam exibidos. Alberto seleciona **Arquivo** &gt; **Exportar para Excel**. As informações de IVA dos relatórios de despesas são exportadas para uma planilha do Microsoft Excel. Ele envia essa planilha para o fornecedor terceirizado e inclui uma mensagem informando que os recibos físicos foram enviados por courier.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Processar as despesas para a restituição de IVA interno

Alberto deve verificar se as transações do relatório de despesas estão qualificadas para a restituição de IVA e se os recibos digitais foram anexados aos relatórios. Para começar a processar as despesas qualificadas para a restituição interna, Alberto abre a página **Restituição de imposto de despesa** e seleciona o relatório de despesas que requer verificação. Ele verifica se os recibos estão em nome da empresa e não no do funcionário. (Para a restituição de IVA, os recibos devem estar no nome da empresa.) Alberto verifica se o grupo de impostos correto e os códigos de imposto do item foram inseridos.

Ao receber os recibos físicos, Alberto altera o status do relatório de despesas para **Pronto para recuperação**. Ele poderá, então, fazer a declaração junto à autoridade fiscal apropriada. Nesse caso, a autoridade fiscal apropriada nos Estados Unidos é o Serviço da Receita Federal (Internal Revenue Service — IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]