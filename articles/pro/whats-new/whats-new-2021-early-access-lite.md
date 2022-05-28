---
title: O que há de novo no acesso antecipado do ciclo 2 de 2021 - Implantação lite do Project Operations
description: Este tópico fornece informações sobre os recursos disponíveis na versão de acesso antecipado do ciclo 2 de 2021 da implantação lite do Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7b5f3528e4b4e615b8e7f24bfd3702746fd584c9
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723662"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>O que há de novo no acesso antecipado do ciclo 2 de 2021 - Implantação lite do Project Operations

_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations no ambiente do Dataverse versão 4.23.0.4

A versão só será aplicada quando um ambiente tiver [optado pelo Acesso Antecipado](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

[Gerenciamento de subcontratos](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - esse recurso fornece melhor visibilidade e controle sobre todos os aspectos do trabalho em um projeto. A versão preliminar do gerenciamento de subcontratos inclui os seguintes recursos:

  - Um gerente de projeto pode criar um subcontrato com um fornecedor. Por padrão, as listas de preços anexadas ao registro do fornecedor são usadas para o subcontrato. A conta do fornecedor tem um tipo de relacionamento de **Fornecedor** ou **Provedor**.
  - Um gerente de projeto pode discriminar todas as compras como itens de linha no subcontrato. As linhas do subcontrato podem ser por tempo, despesas ou produtos. A classe de transação da linha de subcontrato determina para que serve a linha.
  - O gerente de conta do fornecedor e o gerente de projeto podem iterar no subcontrato. O preço pode ser ajustado nas listas de preços de compra que são anexadas ao subcontrato.
  - Durante o processo, se a linha de subcontrato for para tempo, o gerente de contas do fornecedor poderá associar contatos de fornecedor a cada linha de subcontrato. Essa associação fornece informações ao gerente de projeto que está trabalhando no subcontrato. Quando um contato de fornecedor é associado a uma linha de subcontrato, o sistema cria automaticamente um recurso reservável direto do contato, se um recurso reservável ainda não existir.
  - O método de cobrança em cada linha de subcontrato pode ser de preço fixo ou tempo e material. Para linhas do subcontrato de preço fixo, uma agenda de faturamento baseada em marcos é configurada.
