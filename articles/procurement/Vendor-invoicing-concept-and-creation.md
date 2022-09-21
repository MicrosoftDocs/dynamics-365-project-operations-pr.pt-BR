---
title: Criar faturas do fornecedor
description: Este artigo descreve o conceito de faturas de fornecedor e explica como criá-las no Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475404"
---
# <a name="create-vendor-invoices"></a>Criar faturas do fornecedor

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Para usar a funcionalidade descrita neste artigo, você deve habilitar o recurso **Habilitar o processamento de dados reais de subcontrato com o Project Operations para cenários baseados em recursos** no espaço de trabalho **Gerenciamento de recursos**.

O faturamento de fornecedor no Microsoft Dynamics 365 Project Operations pode ser usado por fornecedores para registrar custos de entregas de serviços e/ou materiais em um projeto que é concluído por fornecedores.

Quando serviços e/ou materiais são subcontratados para um fornecedor, um subcontrato representa o acordo contratual com esse fornecedor. À medida que o fornecedor entrega os serviços ou os materiais são recebidos e usados nas tarefas do projeto, os custos são registrados no projeto. O fornecedor envia faturas periodicamente. Essas faturas são verificadas e comparadas com os custos registrados no projeto. Após a conclusão do processo de verificação, a fatura do fornecedor é confirmada e liberada para pagamento.

## <a name="scenarios-for-use"></a>Cenários de uso

As faturas de fornecedor no Project Operations podem ser usadas para dar suporte a dois cenários distintos:

- Os clientes usam as experiências completas de subcontratação.
- Os clientes não usam as experiências de subcontratação completas, mas desejam ter uma visão unificada dos custos dos projetos no Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Os clientes usam as experiências completas de subcontratação

As experiências de fatura de fornecedor representam uma forma de verificar e combinar entradas de hora, uso de material e despesa que fazem referência a componentes subcontratados com linhas da fatura de fornecedor. Esse processo pode ser usado para verificar a precisão das linhas da fatura de fornecedor. Depois que o processo de verificação for concluído e a fatura do fornecedor for confirmada, o sistema reverterá os valores reais registrados pelos logs de uso de horas, despesas e materiais aprovados e criará novos dados reais de custo usando as linhas da fatura do fornecedor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Os clientes não usam as experiências de subcontratação completas, mas desejam ter uma visão unificada dos custos dos projetos no Project Operations

Se você está acompanhando o processo de subcontratação em um sistema de terceiros, pode registrar os custos desse sistema no Project Operations criando faturas de fornecedor que não fazem referência a subcontratos. Dessa forma, seus gerentes de projeto podem ter uma visão única e unificada de todos os custos de um determinado projeto.

## <a name="create-vendor-invoices-in-project-operations"></a>Criar faturas de fornecedor no Project Operations

As faturas do fornecedor são criadas no Dynamics 365 Finance, usando o módulo **Contas a pagar**. Você não pode criar faturas de fornecedor diretamente no Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Configurar a verificação de fatura do fornecedor

Se a fatura do fornecedor for destinada a um subcontrato no Dataverse, você deverá habilitar o parâmetro **A verificação manual por PM é necessária**. A configuração da opção determina se a fatura do fornecedor deve ser confirmada automaticamente no Dataverse ou se requer confirmação manual. O cabeçalho de cada fatura de fornecedor de projeto inclui uma opção com o mesmo nome. Por padrão, a opção no cabeçalho de todas as faturas de fornecedores do projeto é definida com o valor definido aqui. Contudo, você pode atualizar o valor conforme necessário no cabeçalho de faturas de fornecedores individuais.

Se a opção for definida como **Sim**, a fatura do fornecedor criada no Finance e sincronizada com o Dataverse terá o status **Rascunho**. A fatura deve ser validada e verificada pelo gerente de projeto e confirmada antes de ser processada e lançada no projeto específico e nas contas contábeis no Finance.

Se a opção for definida como **Não**, a fatura do fornecedor será confirmada automaticamente. Nenhuma outra ação é necessária.

Para configurar a verificação de fatura do fornecedor, siga estas etapas.

1. No Finance, vá para **Gerenciamento e contabilidade de projeto** \> **Configuração** \> **Parâmetros de gerenciamento e contabilidade de projeto**.
1. Na guia **Financeiro**, defina a opção **A verificação manual por PM é necessária** como **Sim** se a política da empresa exigir a verificação de faturas de fornecedores subcontratados. Se a verificação pelo gerente de projeto não for necessária no Dataverse, deixe a opção definida como **Não**. Por padrão, a configuração será usada na página **Fatura de fornecedor pendente**.

> [!NOTE]
> As faturas do fornecedor criadas para subcontratos no Dataverse podem ser processadas corretamente somente se a opção **A verificação manual por PM é necessária** estiver definida como **Sim**. Os dados reais de tempo, material e despesas que os subcontratados criam podem ser comparados manualmente com as linhas da fatura do fornecedor pelo gerente de projeto somente se esta opção estiver definida como **Sim**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Configurar uma conta de integração de compras para faturas de fornecedores

Quando uma fatura de fornecedor é lançada no Finance para o Project Operations – ambiente integrado (sem estoque), as finanças são lançadas na conta de integração de compras. O sistema gera os dados reais no Dataverse para a fatura lançada. Esses dados reais são lançados no Finance usando o diário de integração do projeto. O lançamento do diário de integração do projeto lança o custo real e reverte a conta de integração de compras.

Para configurar uma conta de integração de compras para faturas de fornecedor, siga estas etapas.

1. No Finance, vá para **Gerenciamento e contabilidade de projeto** \> **Configuração** \> **Parâmetros de gerenciamento e contabilidade de projeto**.
1. Na guia **Project Operations no Dynamics 365 Customer Engagement**, selecione **Materiais** \> **Conta de integração de compras**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Criar e lançar faturas de fornecedores subcontratados

Quando um funcionário de contas a pagar recebe uma fatura do subcontratado, uma nova fatura é criada no Finance.

1. No Finance, vá para **Contas a pagar** \> **Faturas** \> **Faturas de fornecedor pendentes**.
1. No **Painel de Ações**, selecione **Novo** para criar uma fatura de fornecedor.
1. No cabeçalho da fatura, no campo **Conta de fatura**, selecione **Subcontratado**.
1. Selecione a data da fatura.
1. Na guia **Cabeçalho**, defina a opção **A verificação manual por PM é necessária** como **Sim**. A configuração padrão dessa opção vem da página **Parâmetros de gerenciamento e contabilidade de projeto**. Contudo, ela pode ser alterada no nível da fatura do fornecedor.
1. Na guia rápida **Linha da fatura**, selecione **Adicionar linha** para criar uma linha de fatura do fornecedor.
1. Selecione a categoria de compras que foi criada para as linhas de subcontrato e insira o preço unitário, a unidade de medida e a quantidade.
1. Na seção de linhas da fatura do fornecedor, na guia **Projeto**, selecione o projeto com o qual o subcontratado compartilha a fatura do subcontrato.
1. Selecione a categoria do projeto. Pode ser de qualquer tipo de **Item**, **Despesa**, **Materiais** ou **Horas**.
1. Selecione a função somente se a categoria de projeto selecionada for do tipo **Hora**.
1. Selecione **Lançar** para lançar a fatura do fornecedor.

Como alternativa, você pode criar uma fatura de fornecedor acessando **Contas a pagar** \> **Faturas** \> **Abrir faturas de fornecedor** e selecionando **Novo**.

Quando a fatura do fornecedor é lançada, ela fica disponível no Dataverse para verificação e processamento do gerente de projeto.

## <a name="vendor-invoice-processing-in-dataverse"></a>Processamento de fatura de fornecedor no Dataverse

Na fatura do fornecedor criada no Dataverse, alguns valores de campo vêm da fatura do fornecedor registrada no Finance. Outros valores são valores padrão que vêm do subcontrato.

Os campos a seguir e os registros relacionados serão copiados do subcontrato para o cabeçalho da fatura de fornecedor:

- Currency
- Unidade de contratação
- Condições de pagamento

Nas linhas da fatura do fornecedor, o Project Operations usa os seguintes valores de campo para inserir o subcontrato padrão e a referência de linha de subcontrato:

- Classe da transação
- Função
- Categoria da transação
- Campos Produto
- Project
- Tarefa

> [!NOTE]
> As linhas de subcontrato de preço fixo não são compatíveis com o Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
