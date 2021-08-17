---
title: Padrões de dimensão financeira
description: Este tópico fornece informações sobre como configurar padrões de dimensão financeira.
author: sigitac
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8a7845b7f6b7256edad6efc7b20872078f8c5ab0b60477d2a42b5b9d61104bff
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005422"
---
# <a name="financial-dimension-defaults"></a>Padrões de dimensão financeira

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

O Dynamics 365 Project Operations usa a estrutura de [Dimensões financeiras](/dynamics365/finance/general-ledger/financial-dimensions) no Dynamics 365 Finance para fornecer insights adicionais sobre transações de contabilidade e do razão auxiliar do projeto.

As dimensões financeiras padrão podem ser definidas em um cliente, fonte de financiamento do projeto, etapa, linha de contrato do projeto ou projeto.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Defina as dimensões financeiras padrão para um cliente

Os padrões de dimensão do cliente são especificados em Finanças. Conclua as etapas a seguir para definir padrões de dimensão.

1. Vá para **Contas a receber** > **Clientes** > **Todos os clientes**.
2. Na página **Clientes**, na guia **Dimensões financeiras**, defina os valores de dimensão financeira para o cliente específico.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Defina as dimensões financeiras padrão para contratos de projeto

Os contratos de projeto são criados e mantidos no Common Data Service (CDS). Atributos de contabilidade para contratos de projeto são definidos no módulo **Gerenciamento e contabilidade de projetos** em Finanças.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Defina as dimensões financeiras para uma fonte de financiamento do projeto

1. Acesse **Gerenciamento e contabilidade de projetos** > **Projetos** > **Contratos do projeto**.
2. Selecione o registro que deseja atualizar e na guia **Contrato do projeto**, selecione **Mostrar contabilidade padrão**.
3. Expanda **Informações relacionadas** e selecione a guia **Fontes de financiamento**.
4. Defina os padrões de dimensão financeira. Observe que as dimensões financeiras são padronizadas a partir da conta do cliente.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Definir dimensões financeiras para uma linha de contrato do projeto

1. Acesse **Gerenciamento e contabilidade de projetos** > **Projetos** > **Contratos do projeto**.
2. Selecione o registro a ser atualizado e, na guia **Contrato do projeto**, selecione **Mostrar contabilidade padrão**.
3. Expanda **Informações relacionadas** e selecione a guia **Linhas do contrato**.
4. Defina os padrões de dimensão financeira. Os padrões de dimensão financeira são aplicáveis e podem ser usados apenas com linhas de contrato de preço fixo (etapa).

Esses padrões são usados em transações por conta de projetos relacionados e linhas de fatura.

## <a name="define-default-financial-dimensions-for-projects"></a>Defina as dimensões financeiras padrão para projetos

Projetos são criados e mantidos no CDS. Atributos de contabilidade para projetos são definidos no módulo **Gerenciamento e contabilidade de projetos** em Finanças.

1. Acesse **Gerenciamento e contabilidade de projeto** > **Projetos** > **Todos os projetos**.
2. Selecione o registro a ser atualizado e, na guia **Projeto**, selecione **Mostrar contabilidade padrão**.
3. Expanda **Informações relacionadas** e selecione a guia **Configuração**.
4. Defina os padrões de dimensão financeira. Observe que dimensões financeiras são padronizadas a partir da conta do cliente. Se o projeto estiver associado a uma linha de contrato com vários clientes de contrato de projeto, o cliente principal será usado para dimensões financeiras padrão.

As dimensões financeiras padrão do projeto são usadas para definir padrões de linha de diário para transações de hora, despesas e taxas no **Diário de Integração de Operações do Projeto** e nas linhas de fatura do projeto relacionado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]