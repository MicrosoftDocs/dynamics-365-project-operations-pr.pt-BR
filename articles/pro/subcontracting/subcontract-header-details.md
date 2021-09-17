---
title: Detalhes do cabeçalho para subcontratos
description: Este tópico explica a funcionalidade fornecida no cabeçalho do subcontrato no Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323627"
---
# <a name="header-details-for-subcontracts"></a>Detalhes do cabeçalho para subcontratos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este tópico explica a funcionalidade fornecida no cabeçalho do subcontrato no Dynamics 365 Project Operations.

Como um Gerente de Projeto planeja e executa projetos, ele pode empregar subcontratados e adquirir produtos e serviços de fornecedores. Quando um Gerente de Projeto precisa comprar produtos ou serviços, ele pode criar um subcontrato no Project Operations.

Para criar um subcontrato, conclua as etapas a seguir.

1. No painel de navegação, selecione **Subcontratos** e, na página **Subcontrato**, selecione **Novo**.
2. Insira as informações necessárias e selecione **Salvar**.

    A tabela a seguir fornece informações sobre os campos na página Cabeçalho de subcontrato.

    | **Campo** | **Descrição** |
    | --- | --- | 
    | Name | O nome do subcontrato. |
    | Descrição | Uma breve descrição dos serviços e produtos que estão sendo adquiridos no subcontrato. |
    | Fornecedor | O nome da empresa da qual os produtos e serviços estão sendo adquiridos. Esse registro da conta tem um tipo de relacionamento **Fornecedor** ou **Fornecedor**. |
    | Data do Subcontrato | A data em que o subcontrato é criado. |
    | Razão do status | O status do subcontrato. |
    | Currency | A moeda na qual os produtos e serviços são adquiridos. O valor nesse campo tem como padrão a conta do fornecedor, mas pode ser alterado. As listas de preços de projeto que são usadas para definir preços de produtos e serviços no subcontrato devem estar nessa moeda. As listas de preços em qualquer outra moeda não poderão ser associadas ao subcontrato. Os custos dos produtos e serviços incorridos neste subcontrato serão registrados no projeto nessa moeda. |
    | Unidade de Contratação | A divisão da empresa que está celebrando um contrato de compra ou um subcontrato com o fornecedor. |
    | Condições de pagamento | As condições de pagamento nas faturas do fornecedor emitidas nesse subcontrato. O valor nesse campo tem como padrão o registro de conta do fornecedor. |
    | Endereço de Pagamento | O endereço para onde o pagamento das faturas do fornecedor é enviado. O valor nesse campo tem como padrão o registro de conta do fornecedor. |
    | Nome para Cobrança | O nome da pessoa ou divisão da empresa do fornecedor que enviará a fatura. O valor nesse campo tem como padrão o registro da conta do fornecedor e será usado como o nome do contato principal nas faturas do fornecedor criadas para esse subcontrato. |
    | Endereço para Cobrança | O endereço usado em faturas deste fornecedor. O valor nesse campo tem como padrão o registro de conta do fornecedor. Esse endereço também é usado como o endereço da fatura em faturas do fornecedor criadas para esse subcontrato. |
    | Subtotal | Se um subcontrato não tiver linhas, insira um valor nesse campo que denote o subtotal do pedido antes dos impostos. Se o subcontrato tiver linhas, esse campo será somente leitura. O valor exibido é o valor do subtotal de todas as linhas do subcontrato. |
    | Total de Impostos | Se um subcontrato não tiver linhas, insira um valor nesse campo que denote os impostos nesse subcontrato. Se o subcontrato tiver linhas, esse campo será somente leitura. O valor exibido é a soma do valor do imposto de todas as linhas do subcontrato. |
    | Valor Total |  Esse campo calculado mostra o valor total da linha de subcontrato após a inclusão dos impostos.  |
    | Data Confirmada | A data em que o subcontrato foi confirmado.  |
    | Solicitado por | O valor nesse campo assume como padrão o nome do usuário que cria o subcontrato. Esse valor pode ser alterado pelo criador do subcontrato para indicar a pessoa em nome de quem está criando o subcontrato.  |
    | Gerente de Contas do Fornecedor | O nome do contato principal da conta do fornecedor. O valor nesse campo tem como padrão o registro de conta do fornecedor. O valor desse campo pode ser alterado pelo usuário para selecionar um contato diferente como o gerente da conta do fornecedor do subcontrato. Alertas de email e negociações de preços podem ser configurados e enviados por esse contato. |


