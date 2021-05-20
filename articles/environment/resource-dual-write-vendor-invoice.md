---
title: Integração de faturas de fornecedores
description: Este tópico fornece informações sobre a integração de faturas de fornecedores no Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955702"
---
# <a name="vendor-invoice-integration"></a>Integração de faturas de fornecedores

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Compras relacionadas ao projeto no Dynamics 365 Project Operations podem ser gravadas acessando **Contas a pagar** > **Faturas** > **Faturas de fornecedor pendentes** e usando um documento de fatura de fornecedor pendente. Para obter mais informações, consulte [Comprar materiais não estocados usando uma fatura de fornecedor pendente](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Antes de usar a funcionalidade descrita neste tópico, revise e aplique as configurações necessárias. Para obter mais informações, consulte [Habilitar materiais não estocados e faturas de fornecedores pendentes](../procurement/configure-materials-nonstocked.md).

No Project Operations, as faturas de fornecedor relativas ao projeto são postadas usando regras especiais de postagem:

- Os custos relacionados ao projeto (incluindo impostos não recuperáveis) não são postados logo na conta de custos do projeto no razão geral. Em vez disso, o custo é postado na **Conta de integração de compras**. Esta conta está configurada na guia **Gerenciamento e contabilidade de projetos** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto** na guia **Project Operations no Dynamics 365 Customer Engagement**.
- A gravação dupla sincroniza detalhes da fatura do fornecedor para o Microsoft Dataverse usando os seguintes mapas de tabela:

     - **Entidade de exportação de fatura de fornecedor de projeto de integração do Project Operations (msdyn_projectvendorinvoices)**: este mapa de tabela sincroniza as informações do cabeçalho da fatura do fornecedor. Apenas faturas de fornecedores com pelo menos uma linha contendo uma ID de projeto são sincronizadas para o Dataverse.
     - **Entidade de exportação de linha de fatura de fornecedor de projeto de integração do Project Operations (msdyn_projectvendorinvoicelines)**: este mapa de tabela sincroniza as informações de linha da fatura do fornecedor. Apenas as linhas contendo uma ID de projeto são sincronizadas para o Dataverse.

     > [!NOTE]
     > Detalhes da fatura do fornecedor no Dataverse não são editáveis.

Razão auxiliar de imposto, razão auxiliar de fornecedor e outras postagens financeiras são registradas conforme aplicável no Dynamics 365 Finance quando a fatura do fornecedor é postada.

![Integração de faturas de fornecedores](media/DW7VendorInvoice.png)

Quando os registros são gravados em uma entidade **Fatura de fornecedor** no Dataverse, é iniciado um processo automatizado de aprovação dos registros. Se necessário, o status do processo de aprovação automatizado pode ser revisado no Dataverse acessando **Configurações avançadas** > **Sistema** > **Trabalhos do sistema**. Após a aprovação ser concluída, o sistema cria registros da classe de transações de material na entidade **Dados Reais**.

Os dados reais relativos a material são processados usando o mapa da tabela de gravação dupla **Dados reais de integração do Project Operations (msdyn_actuals)**. Para obter mais informações, consulte [Estimativas e dados reais de projeto](resource-dual-write-estimates-actuals.md).

O processo periódico, **Importar de preparo** cria linhas de diário de integração do Project Operations relacionadas a faturas de fornecedor. O padrão da conta de compensação é a conta de integração de compras. Quando o diário de integração é postado, o saldo da conta é limpo para a transação de fatura de fornecedor e o valor da linha é movido para a conta de custo do projeto. Transações do razão auxiliar do projeto também são criadas para fins de faturamento derivado e reconhecimento de receita.
