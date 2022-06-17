---
title: O que há de novo em junho de 2022 - Implantação lite do Project Operations
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de junho de 2022 da implantação lite do Microsoft Dynamics 365 Project Operations.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959381"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>O que há de novo em junho de 2022 - Implantação lite do Project Operations

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.43.0.77

## <a name="quality-updates"></a>Atualizações de qualidade

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Subcontratação | 2708885 | Corrigida a mensagem de erro que aparece quando um usuário cria um registro de cabeçalho de reserva de recurso reservável em que nenhum recurso reservável é preenchido. |
| Planejamento e rastreamento de projeto | 2629441 | Corrigida a lógica de acionamento do fluxo de trabalho para ajudar a evitar um loop infinito quando as tarefas do projeto são atualizadas. |
| Horas e despesas | 2641209 | As importações de entradas de horas de atribuições/reservas devem reter uma referência de recurso reservável. |
| Planejamento e rastreamento de projeto | 2651148 | O cabeçalho do documento do projeto deve ser protegido.|
| Planejamento e rastreamento de projeto | 2653145 | Adicionadas validações para garantir que um registro de projeto não possa ser criado com caracteres inválidos em seu nome. |
| Horas e despesas | 2654710 | Corrigida a filtragem na página **Aprovações**. |
| Cobrança e preço | 2667805 | Adicionadas validações para ajudar a evitar a criação de dados reais de vendas cobradas se não existirem dados reais de vendas não cobradas. |
| Cobrança e preço | 2668378 | Validações adicionadas para ajudar a impedir que uma dimensão de preço personalizada seja adicionada, a menos que um nome lógico e um nome de campo sejam preenchidos. |
| Horas e despesas | 2700428 | Aprimorou a lógica de aprovações para garantir que outros conjuntos de aprovações para o projeto possam ser processados mesmo se um dos conjuntos de aprovações estiver preso em trabalhos do sistema. |
