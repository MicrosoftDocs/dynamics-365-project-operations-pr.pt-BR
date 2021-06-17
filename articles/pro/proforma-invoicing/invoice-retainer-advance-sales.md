---
title: Faturar um honorário ou adiantamento
description: Este tópico fornece informações sobre como faturar um honorário ou adiantamento no Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 238b55e906fb66415cf46d3abc8827d85c174dd7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003977"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Faturar um honorário ou adiantamento

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Dynamics 365 Project Operations oferece suporte a contratos baseados em adiantamentos e honorários únicos. Em um contrato de projeto, você pode registrar uma agenda de honorários ou um adiantamento único. No entanto, o registro em nível de contrato do projeto não disponibiliza imediatamente um honorário ou adiantamento para uso. Para usar um honorário ou adiantamento em uma fatura que realmente cobre do cliente, o honorário ou adiantamento deve ser faturado primeiro.

Conclua as etapas a seguir para faturar um honorário ou um adiantamento.

1. Selecione **Vendas** > **Cobrança** > **Honorários e Adiantamentos**. 
2. Na página **Adiantamentos e Honorários**, use o filtro para selecionar o honorário ou adiantamento específico para faturamento e marque-o como **Pronto para Faturamento**.
3. Crie uma fatura manualmente a partir da lista **Contrato do Projeto** ou página de detalhes. O honorário ou adiantamento é mostrado na fatura de rascunho na seção **Adiantamentos e Honorários** na página **Fatura**.
4. Confirme a fatura. Isso disponibilizará o honorário ou adiantamento para uso. Você pode verificar a fatura na página de listagem **Honorários e Adiantamentos**. Para um Adiantamento ou Honorário faturado, o valor disponível é mostrado na grade.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Criar um honorário ou adiantamento na grade de fatura

Você pode criar um honorário ou um adiantamento diretamente em uma fatura.

1. Em uma fatura de rascunho, na subgrade **Adiantamentos e Honorários**, selecione **Novo** para criar um novo honorário ou adiantamento. 
2. Na página **Criação Rápida**, adicione as informações necessárias e selecione **Salvar**. O honorário ou adiantamento é criado no contrato do projeto relacionado à fatura. O honorário ou adiantamento é marcado automaticamente como **Pronto para Faturamento** e, depois, adicionado à subgrade **Adiantamentos e Honorários** na página **Fatura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Reconciliar um honorário ou adiantamento faturado

Depois que um honorário ou adiantamento é faturado, eles podem ser usados ou reconciliados em uma fatura com hora, despesas, etapas ou outros encargos baseados no projeto. O cliente verá o valor da fatura reduzido pelo valor de honorário ou adiantamento usado nesta fatura.

Em cada fatura gerada para um contrato de projeto que faturou honorários ou adiantamentos, o Project Operation aplica automaticamente o honorário ou adiantamento à fatura.

Isso pode ser visto na grade **Honorários e Adiantamentos Aplicados** na página **Fatura**. A tabela a seguir fornece informações sobre os campos na grade **Honorários e Adiantamentos Aplicados** da página **Fatura do Projeto**.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Descrição | Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto** |Este campo somente leitura fornece uma descrição do honorário ou adiantamento usado nesta fatura. Este valor não pode ser alterado na fatura. Este valor pode ser atualizado na subgrade na página **Contrato de Projeto**. | Este campo pode ser exibido para o cliente na fatura impressa para indicar qual honorário ou adiantamento é aplicado na fatura. |
| Data da Entrega | Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**  | Este campo somente leitura fornece a data da fatura do honorário ou adiantamento usado nesta fatura. Este valor não pode ser alterado na fatura. Este valor pode ser atualizado na subgrade na página **Contrato de Projeto**. | Este campo pode ser exibido para o cliente na fatura impressa para indicar a data em que o honorário ou adiantamento foi faturado pela primeira vez para o cliente. |
| Valor | Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**  | Este campo somente leitura fornece o valor do honorário ou adiantamento usado nesta fatura. Este valor não pode ser alterado na fatura. Este valor pode ser atualizado na subgrade na página **Contrato de Projeto**. | Este campo pode ser exibido para o cliente na fatura impressa para indicar o valor original do honorário ou adiantamento que foi pago pelo cliente. |
| Valor Usado | Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**  | Este campo somente leitura fornece o valor calculado que resume quanto do honorário ou adiantamento foi usado. | Este campo pode ser exibido para o cliente na fatura impressa para indicar o valor deste honorário ou adiantamento que já foi usado. |
| Valor Ampliado | Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**  | Este campo editável fornece o valor do honorário ou adiantamento que está sendo usado nesta fatura do projeto. Este valor não pode ser superior ao que está disponível no adiantamento. O sistema calcula automaticamente isso como a diferença entre os campos **Valor** e **Quantidade Usada** na grade. Você pode diminuir esse valor para usar menos do que o disponível, mas não pode aumentar o valor para usar mais do que está disponível. | Este campo pode ser exibido para o cliente na fatura impressa para indicar o valor deste honorário ou adiantamento que está sendo usado na fatura. |
| Valor do Saldo dos Honorários. | Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**  | Este campo somente leitura fornece o valor de quanto restará do honorário ou adiantamento após a confirmação da fatura. | Este campo pode ser exibido para o cliente na fatura impressa para indicar o valor que restará deste honorário ou adiantamento após a confirmação ou o pagamento da fatura. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]