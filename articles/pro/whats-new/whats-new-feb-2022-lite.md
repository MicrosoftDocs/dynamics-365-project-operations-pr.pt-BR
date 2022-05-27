---
title: Novidades em fevereiro de 2022 – implantação lite do Project Operations
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de fevereiro de 2022 da implantação lite do Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: af66a5f61adf4f016f3fa547bbdfc75d06b2711b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574554"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Novidades em fevereiro de 2022 – implantação lite do Project Operations

_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_

Este tópico se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.28.0.120

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

A partir desta versão, você pode adicionar até 300 membros da equipe a um único projeto. Anteriormente, o limite no número de membros da equipe era de 150. Para obter mais informações, consulte [Limites do projeto](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Atualizações de qualidade

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Cobrança e preço | 2497369 | A correção de materiais deve seguir o valor de data nos parâmetros **Correção**. |
| Cobrança e preço | 2498697 | Aprimorada a configuração de segurança para **Recuperação de entrada de hora**. |
| Cobrança e preço | 2517455 | A ação **Atualizar transações de linha de fatura** não deve ter permissão para ser acionada várias vezes simultaneamente para a mesma fatura. |
| Cobrança e preço | 2517465 | A ação **Desativar detalhes de linha de fatura** está bloqueada porque não tem suporte. |
| Cobrança e preço | 2556660 | Corrigidas as verificações de efetividade de data que são feitas na lista de preços anexada ao registro de parâmetros de um projeto. |
| Gerenciamento de oportunidades | 2369202 | Corrigida a lógica de negócios que verifica se as listas de preços com datas de efetividade sobrepostas podem ser anexadas ao mesmo contrato de projeto. |
| Gerenciamento de oportunidades | 2385965 | Corrigido o comportamento na guia **Clientes** da página **Contrato do projeto** ao selecionar **Salvar e fechar**. |
