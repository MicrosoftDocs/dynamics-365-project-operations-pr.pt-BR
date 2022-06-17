---
title: Detalhes do cabeçalho para faturas de fornecedor
description: Este artigo explica a funcionalidade fornecida no cabeçalho da fatura de fornecedor no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929844"
---
# <a name="header-details-for-vendor-invoices"></a>Detalhes do cabeçalho para faturas de fornecedor

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este artigo explica a funcionalidade fornecida no cabeçalho da fatura de fornecedor no Microsoft Dynamics 365 Project Operations.

À medida que os gerentes de projeto planejam e executam projetos, eles podem empregar subcontratados e comprar produtos e serviços de fornecedores. Durante a execução de um projeto, são incorridos custos das categorias de serviços, materiais e despesas adquiridas em subcontratos com fornecedores. Os fornecedores faturam esses custos de projetos criando faturas de fornecedor.

A tabela a seguir apresenta informações sobre os campos nos cabeçalhos da fatura de fornecedor no Project Operations.

| Campo | Descrição | Impacto funcional |
| --- | --- | --- |
| Nome | O nome da fatura de fornecedor. | Em todas as listas suspensas de fatura de fornecedor, o nome da fatura de fornecedor é listado na primeira coluna para ajudar a identificar a fatura de fornecedor. Por padrão, quando uma fatura de fornecedor é criada a partir de um subcontrato, o campo **Nome** da fatura de fornecedor é definido como um valor que consiste no nome do subcontrato mais a data atual. |
| Descrição | Uma breve descrição dos serviços e produtos que estão sendo faturados na fatura de fornecedor. | Nenhum |
| Fornecedor | O nome da empresa que está faturando os produtos e serviços. Essa empresa deve ser um registro da conta que tem um tipo de relacionamento de **Fornecedor** ou **Provedor**. | <p>Dependendo do fornecedor selecionado, os valores padrão são inseridos automaticamente nos seguintes campos:</p><ul><li>Moeda</li><li>Listas de preços</li><li>Condições de pagamento</li><li>Endereço de pagamento</li></ul> |
| Subcontrato | Uma referência ao subcontrato para a fatura de fornecedor. | <p>Dependendo do subcontrato selecionado, os valores padrão são inseridos automaticamente nos seguintes campos:</p><ul><li>Moeda</li><li>Listas de preços</li><li>Condições de pagamento</li><li>Endereço de pagamento</li></ul><p>O subcontrato selecionado no cabeçalho da fatura de fornecedor é inserido por padrão nas linhas da fatura de fornecedor e não pode ser alterado.</p> |
| Data da fatura | A data dos dados reais de custo que serão criados quando a fatura de fornecedor for confirmada. | A data das fatura também é usada para selecionar a lista de preços de compra correta nas listas de preços anexadas ao fornecedor relacionado ou nos parâmetros do projeto. |
| Razão do status | O status da fatura de fornecedor. | <p>O status determina onde a fatura de fornecedor está no processo empresarial e se ela pode ser editada. Veja alguns dos valores disponíveis:</p><ul><li>**Rascunho** – É possível editar a fatura de fornecedor.</li><li>**Confirmado** – A fatura de fornecedor foi verificada e confirmada. Não é possível editar ou excluir as faturas de fornecedor com esse status.</li><li>**Em andamento** – A fatura de fornecedor está sendo revisada. É possível editar, mas não excluir as faturas de fornecedor com esse status.</li><li>**Cancelado** – A fatura de fornecedor foi cancelada. Não é possível editar ou excluir as faturas de fornecedor com esse status.</li></ul> |
| Moeda | A moeda em que o fornecedor está faturando os produtos e serviços na fatura de fornecedor. | Em uma fatura de fornecedor que faz referência a um subcontrato, a moeda do subcontrato é inserida por padrão como moeda da fatura de fornecedor. Em uma fatura de fornecedor que não faz referência a um subcontrato, o valor padrão é inserido a partir do registro da conta de fornecedor e pode ser alterado. Depois que uma fatura de fornecedor é salva, a moeda não pode mais ser editada. |
| Unidade de contratação | A divisão da empresa responsável por receber os serviços e/ou produtos do fornecedor. | Nenhum |
| Condições de pagamento | Os termos de pagamento das faturas de fornecedor emitidas. O valor padrão é inserido automaticamente a partir do registro da conta do fornecedor. | Os termos de pagamento de um subcontrato são copiados para todas as faturas de fornecedor relacionadas ao subcontrato. Os termos de pagamento poderão ser atualizados se a fatura de fornecedor tiver o status **Rascunho**. |
| Endereço de pagamento | O endereço do fornecedor para o qual os pagamentos devem ser enviados. O valor padrão é inserido automaticamente a partir do registro da conta do fornecedor. | O endereço de pagamento de um subcontrato é copiado como endereço de pagamento para todas as faturas de fornecedor criadas para esse subcontrato. O endereço de pagamento poderá ser atualizado se a fatura de fornecedor tiver o status **Rascunho**. |
| Subtotal | Se a fatura de fornecedor não tiver linhas, insira o subtotal da fatura antes dos impostos. Se a fatura de fornecedor tiver linhas, este campo será somente leitura. Nesse caso, o valor mostrado é o subtotal de todas as linhas da fatura de fornecedor. | Nenhum |
| Total de impostos | Se a fatura de fornecedor não tiver linhas, insira o total de impostos no subcontrato. Se a fatura de fornecedor tiver linhas, este campo será somente leitura. Nesse caso, o valor mostrado é a soma dos valores de impostos de todas as linhas da fatura de fornecedor. | Nenhum |
| Valor total | Este campo calculado mostra o valor total da fatura de fornecedor após a inclusão dos impostos. | Nenhum |

> [!NOTE]
> Não é possível alterar os seguintes campos em uma fatura de fornecedor depois que ela é salva: **Fornecedor**, **Subcontrato**, **Moeda**, **Unidade contratante** e **Termos de pagamento**. Se forem necessárias alterações nesses campos em uma fatura de fornecedor, você deverá excluir a fatura de fornecedor e criar uma nova fatura de fornecedor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
