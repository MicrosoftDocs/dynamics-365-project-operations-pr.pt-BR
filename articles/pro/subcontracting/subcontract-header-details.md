---
title: Detalhes do cabeçalho para subcontratos
description: Este tópico explica a funcionalidade fornecida no cabeçalho do subcontrato no Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fade0ff876486ad60ffd9ad618be7864c1b28185
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598152"
---
# <a name="header-details-for-subcontracts"></a>Detalhes do cabeçalho para subcontratos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este tópico explica a funcionalidade fornecida no cabeçalho do subcontrato no Dynamics 365 Project Operations.

Como um Gerente de Projeto planeja e executa projetos, ele pode empregar subcontratados e adquirir produtos e serviços de fornecedores. Quando um Gerente de Projeto precisa comprar produtos ou serviços, ele pode criar um subcontrato no Project Operations.

Para criar um subcontrato, conclua as etapas a seguir.

1. No painel de navegação, selecione **Subcontratos** e, na página **Subcontrato**, selecione **Novo**.
2. Insira as informações necessárias e selecione **Salvar**.

    A tabela a seguir fornece informações sobre os campos na página **Cabeçalho de subcontrato**.

    | Campo | Descrição |Impacto funcional |
    |---|------|---| 
    | Name | O nome do subcontrato. | Em todas as listas suspensas de subcontrato, o nome do subcontrato é listado na primeira coluna para ajudar você a identificar o subcontrato. | 
    | Descrição | Uma breve descrição dos serviços e produtos que estão sendo adquiridos no subcontrato. | Nenhum(a) |
    | Fornecedor | O nome da empresa da qual os produtos e serviços estão sendo adquiridos. Esse registro da conta tem um tipo de relacionamento **Fornecedor** ou **Fornecedor**. | Com base no fornecedor selecionado, os valores padrão são inseridos automaticamente para os seguintes campos:<br/> **• Moeda** </br> **• Listas de Preços** </br> **• Condições de Pagamento**</br> **• Endereço de Pagamento**</br> **• Endereço para Cobrança**</br> **• Nome para Cobrança** </br>**• Gerente de Contas do Fornecedor**|
    | Data do Subcontrato | A data em que o subcontrato é criado. | A data do subcontrato é usada para selecionar a lista de preços de compra correta nas listas de preços anexadas ao fornecedor relacionado ou nos parâmetros do projeto. |
    | Razão do status | O status do subcontrato. | O status determina onde o subcontrato está no processo empresarial e se ele pode ser editado. <br/>Os valores incluem:<br>• **Rascunho**: o subcontrato pode ser editado. Você só pode editar subcontratos com o status **Rascunho**.<br/>• **Confirmado**: a negociação com o fornecedor foi concluída e o subcontrato foi aprovado para entrega. <br/>• **Fechado**: a entrega do subcontrato foi concluída.<br/>• **Cancelado**: o subcontrato foi cancelado e nenhuma entrega está planejada.  | 
    | Currency | A moeda em que os produtos e serviços são adquiridos. O valor padrão é inserido automaticamente a partir da conta do fornecedor, mas pode ser alterado. | A moeda do subcontrato é usada para selecionar a lista de preços de compra nas listas de preços anexadas ao fornecedor relacionado ou nos parâmetros do projeto. Listas de preços em outra moeda não podem ser associadas ao subcontrato. O custo de horas, despesas e materiais que os recursos do fornecedor entregam a partir deste subcontrato é registrado nessa moeda no projeto. Depois que o registro do subcontrato é salvo, a moeda do subcontrato não pode ser alterada.|
    | Unidade de Contratação | A divisão da empresa que está celebrando um contrato de compra ou um subcontrato com o fornecedor. | Nenhum(a) |
    | Condições de pagamento | As condições de pagamento das faturas do fornecedor emitidas neste subcontrato. O valor padrão é inserido automaticamente a partir do registro da conta do fornecedor. | As condições de pagamento do subcontrato são copiadas para todas as faturas do fornecedor relacionadas a este subcontrato. As condições de pagamento podem ser atualizadas se o subcontrato tiver o status **Rascunho**. | 
    | Endereço de Pagamento | O endereço do fornecedor para o qual os pagamentos devem ser enviados. O valor padrão é inserido automaticamente a partir do registro da conta do fornecedor. | O endereço de pagamento do subcontrato é copiado como o endereço de pagamento para todas as faturas do fornecedor criadas para este subcontrato. O endereço de pagamento pode ser atualizado se o subcontrato tiver o status **Rascunho**.|
    | Nome para Cobrança | O nome da pessoa ou divisão da empresa do fornecedor que enviará a fatura. O valor padrão é inserido automaticamente a partir do registro da conta do fornecedor. | O valor **Nome para Cobrança** do subcontrato é copiado para todas as faturas do fornecedor relacionadas a este subcontrato. Este campo pode ser atualizado se o subcontrato tiver o status **Rascunho**.|
    | Endereço Para Cobrança | O endereço usado nas faturas do fornecedor. O valor padrão é inserido automaticamente a partir do registro da conta do fornecedor. | Este é o endereço "fatura de" nas faturas do fornecedor criadas para este subcontrato. |
    | Subtotal | Se um subcontrato não tiver linhas, insira o subtotal da ordem antes dos impostos. Se o subcontrato tiver linhas, esse campo será somente leitura. O valor mostrado é o subtotal de todas as linhas do subcontrato. | Nenhum(a) |
    | Total de Impostos | Se um subcontrato não tiver linhas, insira o total de impostos neste subcontrato. Se o subcontrato tiver linhas, esse campo será somente leitura. O valor mostrado é a soma do valor dos impostos de todas as linhas do subcontrato. | Nenhum(a) |
    | Valor Total | Esse campo calculado mostra o valor total da linha de subcontrato após a inclusão dos impostos. | Nenhum(a) |
    | Data Confirmada | A data em que o subcontrato foi confirmado. | Nenhum(a) |
    | Solicitado por | Por padrão, este campo é definido com o nome do usuário que cria o subcontrato. No entanto, o criador do subcontrato pode alterar o valor para indicar a pessoa em nome da qual o subcontrato está sendo criado. | Nenhum(a) |
    | Gerente de Contas do Fornecedor | O nome do contato principal da conta do fornecedor. O valor padrão é inserido automaticamente a partir do registro da conta do fornecedor. Você pode selecionar outro contato como gerente de contas do fornecedor do subcontrato. | Você pode configurar alertas de email para notificar o contato quando forem feitas alterações no subcontrato como resultado das negociações de preço. |
