---
title: Faturamento de fornecedor - Conceito e criação
description: Este tópico descreve o conceito de faturas de fornecedor, cenários de uso e como criar faturas de fornecedor no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580534"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Faturamento de fornecedor - Conceito e criação

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

O faturamento de fornecedor no Microsoft Dynamics 365 Project Operations pode ser usado por fornecedores para registrar custos de entregas de serviços e/ou materiais em um projeto.

Quando serviços e/ou materiais são subcontratados para um fornecedor, um subcontrato representa o acordo contratual com esse fornecedor. À medida que o fornecedor entrega os serviços ou os materiais são recebidos e usados nas tarefas do projeto, os custos são registrados no projeto. Periodicamente, o fornecedor envia faturas que são verificadas e combinadas com os custos registrados no projeto. Após a conclusão do processo de verificação, a fatura do fornecedor é confirmada e liberada para pagamento.

## <a name="scenarios-for-use"></a>Cenários de uso

As faturas de fornecedor no Project Operations podem ser usadas para dar suporte a dois cenários distintos.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Os clientes usam as experiências completas de subcontratação

As experiências de fatura de fornecedor representam uma forma de verificar e combinar entradas de hora, uso de material e despesa que fazem referência a componentes subcontratados com linhas da fatura de fornecedor. Esse processo pode ser usado para verificar a precisão das linhas da fatura de fornecedor. Depois que o processo de verificação for concluído e a fatura do fornecedor for confirmada, o aplicativo reverterá os valores reais registrados pelos logs de horas, despesas e uso de materiais aprovados e criará novos dados reais de custo usando as linhas da fatura de fornecedor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Os clientes não usam as experiências de subcontratação completas, mas desejam ter uma visão unificada dos custos dos projetos no Project Operations

Se você está acompanhando o processo de subcontratação em um sistema de terceiros, pode registrar os custos desse sistema no Project Operations criando faturas de fornecedor que não fazem referência a subcontratos. Dessa forma, seus gerentes de projeto podem ter uma visão única e unificada de todos os custos de um determinado projeto.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Criação de faturas de fornecedor no Project Operations

As faturas de fornecedor podem ser criadas de duas maneiras:

- Na página da lista de faturas de fornecedor ou na página de detalhes de uma única fatura de fornecedor
- Na página da lista de subcontratos ou na página de detalhes de um único subcontrato

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Criação na página da lista de faturas de fornecedor ou na página de detalhes

1. Vá para **Compras** \> **Faturas de fornecedor**.
2. Na página da lista de faturas de fornecedor ou na página de detalhes de uma única fatura de fornecedor, selecione **Novo** para criar uma nova fatura de fornecedor.

As faturas de fornecedor criadas dessa maneira também podem fazer referência a um subcontrato.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Criação na página da lista de subcontratos ou na página de detalhes

1. Vá para **Compras** \> **Subcontratos**.
2. Selecione um ou mais subcontratos.
3. Na página da lista de subcontratos ou na página de detalhes de um único subcontrato, selecione **Criar fatura de fornecedor** para criar uma nova fatura de fornecedor.

É criada uma nova fatura de fornecedor com o status **Rascunho** para cada subcontrato selecionado.

As faturas de fornecedor criadas dessa forma sempre fazem referência ao subcontrato no cabeçalho da fatura de fornecedor. Cada linha no subcontrato com um Método de cobrança por hora e material fará com que uma linha seja criada na fatura de fornecedor. Cada linha no subcontrato com um Método de cobrança de preço fixo fará com que uma linha seja criada na fatura de fornecedor para cara etapa da linha de subcontrato com o status **Pronto para faturamento**.

Os campos a seguir e os registros relacionados serão copiados do subcontrato para o cabeçalho da fatura de fornecedor:

- Fornecedor.
- As listas de preços relacionadas serão copiadas para a fatura de fornecedor como listas de preços.
- Moeda.
- Unidade contratante.
- Termos de pagamento.

Para linhas de subcontrato de tempo e material, os campos a seguir e os registros relacionados serão copiados da linha de subcontrato para a linha da fatura de fornecedor:

- Referências de subcontrato e linha de subcontrato
- Classe da transação
- Função
- Categoria da transação
- Campos Produto
- Project
- Tarefa
- Recurso reservável

Para linhas de subcontrato de preço fixo, os campos a seguir serão copiados da linha de subcontrato e da etapa da linha de subcontrato para a linha da fatura de fornecedor:

- Referências de subcontrato e linha de subcontrato.
- Classe da transação. Por padrão, o valor será **Etapa**.
- O nome e o valor da etapa serão copiados da etapa da linha de subcontrato relacionada.
- O usuário poderá selecionar um projeto e uma tarefa na linha da fatura de fornecedor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
