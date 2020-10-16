---
title: Visão geral de despesa
description: Este tópico inclui informações sobre a funcionalidade Despesa no Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967352"
---
# <a name="expense-home-page"></a>Home page de despesas

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_


O Dynamics 365 Project Operations oferece suporte à capacidade de processar despesas. O processamento de despesas com ou sem projetos usando um fluxo de trabalho personalizável de políticas, categorias de transação e aprovações.

Em Project Operations, há dois modelos de implantação compatíveis com Despesa: 

- **Completa**: a implantação completa está disponível para **cenários baseados em recursos/sem estoque do Project Operations** ou **cenários baseados em ordem de produção do Project Operations**.
- **Básico**: a implantação básica está disponível para **cenários baseados em recursos/sem estoque do Project Operations** e **Implantação lite - gerenciar faturamento pro forma**.

## <a name="full"></a>Completo 
A implantação completa de Despesa fornece uma aplicação de política completa que inclui a capacidade de criar políticas, como:

  - Limites de categoria de despesa
  - Viagem
  - Diária
  - Importações de cartão de crédito
  - Reconhecimento ótico de caracteres do recibo

## <a name="basic"></a>Básico 
O cenário de implantação básica de Despesa permite apenas registrar as despesas básicas em um projeto. 

Para obter mais informações, consulte [Entrada de despesa (lite)](basic-expense.md)

## <a name="determine-your-expense-deployment"></a>Determinar a implantação de Despesa
Para determinar se você está executando a implantação de gerenciamento de Despesa básica, verifique se a URL do endereço termina com **.crm.dynamics.com**. 
