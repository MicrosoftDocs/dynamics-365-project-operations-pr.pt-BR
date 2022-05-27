---
title: Impacto dos dados reais em um compromisso de preço fixo
description: Este tópico fornece informações sobre o impacto na tabela Dados reais em vários eventos durante o ciclo de vida de um compromisso de preço fixo no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579214"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Impacto dos dados reais em um compromisso de preço fixo

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

A tabela a seguir lista os dados reais de diferentes tipos de transação criados em vários eventos em um compromisso de preço fixo.

| Evento | Custo real | Valores reais de vendas não cobrados | Dados reais de vendas cobradas | Exemplo |
|---|---|---|---|---|
| As horas são criadas. | Não aplicável | Não aplicável | Não aplicável | <p>Bob Kozack, da unidade organizacional da Fabrikam US que tem uma taxa de custo de 100 dólares americanos (USD 100) por hora, está trabalhando em um projeto chamado "Instalação de braço na Adatum". Este projeto está mapeado para um método de cobrança de preço fixo na linha de contrato. Este é um exemplo de entrada de hora de Bob Kozak:</p><p>Bob Kozack - 8 horas</p> |
| As horas são enviadas. | Não aplicável | Não aplicável | Não aplicável | Uma linha do diário de custo é criada para a entrada de hora. A taxa de custo padrão é inserida na entrada de diário. |
| A entrada de hora é recuperada antes de ser aprovada. | Não aplicável | Não aplicável | Não aplicável | |
| As horas são aprovadas. | Os dados reais de custo são criados. | Não aplicável | Não aplicável | <p>Os novos dados reais que são criados:</p><ul><li>**Dados reais de custo:** Bob Kozack, 8 h, USD 800</li></ul> |
| A aprovação de horas é cancelada. | <p>O status de ajuste dos dados de custo real originais é atualizado para **Ajustado**.</p><p>Dados reais de custo de reversão são criados com o status de ajuste **Não Ajustável**.</p> | Não aplicável | Não aplicável | <p>Os dados reais existentes que são atualizados:</p><ul><li>**Custo real:** Bob Kozack, 8 h, USD 800, *Ajustado*</li></ul><p>Novos dados reais que são criados para reverter o impacto financeiro anterior:</p><ul><li>**Dados reais de custo:** Bob Kozack, (8 h), (USD 800), *Não Ajustável*</li></ul> |
| A entrada de hora é recuperada depois de ser aprovada. | <p>O status de ajuste dos dados de custo real originais é atualizado para **Ajustado**.</p><p>Dados reais de custo de reversão são criados com o status de ajuste **Não Ajustável**.</p> | Não aplicável | Não aplicável | <p>Os dados reais existentes que são atualizados:</p><ul><li>**Custo real:** Bob Kozack, 8 h, USD 800, *Ajustado*</li></ul><p>Novos dados reais que são criados para reverter o impacto financeiro anterior:</p><ul><li>**Dados reais de custo:** Bob Kozack, (8 h), (USD 800), *Não Ajustável*</li></ul> |
| O contrato é confirmado. | <p>O status de ajuste dos antigos dados reais de custo foi atualizado para **Ajustado**.</p><p>Dados reais de custo de reversão são criados com o status de ajuste **Não Ajustável**.</p><p>Novos dados reais de custo são criados depois que as regras contratuais são reavaliadas.</p> | Não aplicável | Não aplicável | <p>Os dados reais existentes que são atualizados:</p><ul><li>**Custo real:** Bob Kozack, 8 h, USD 800, *Ajustado*</li></ul><p>Novos dados reais que são criados para reverter o impacto financeiro anterior:</p><ul><li>**Dados reais de custo:** Bob Kozack, (8 h), (USD 800), *Não Ajustável*</li></ul><p>Novos dados reais que são criados relacionados ao impacto financeiro reavaliado:</p><ul><li>**Dados reais de custo:** Bob Kozack, 8 h, USD 800</li></ul> |
| Uma fatura é criada. | Não aplicável | Não aplicável | Não aplicável | |
| A fatura é confirmada com uma etapa. | Não aplicável | Não aplicável | Novos dados reais de vendas cobradas com base em etapa são criados. | <p>Dados reais existentes que permanecem inalterados:</p><ul><li>**Dados reais de custo:** Bob Kozack, 8 h, USD 800</li></ul><p>Novos dados reais que são criados para registrar os valores de vendas cobradas:</p><ul><li>**Dados reais de vendas cobradas:** Etapa, USD 5.000</li></ul> |
| A fatura é corrigida para creditar a etapa. | Não aplicável | Não aplicável | Os dados reais de vendas cobradas com reversão são criados. | <p>Dados reais existentes que permanecem inalterados:</p><ul><li>**Dados reais de custo:** Bob Kozack, 8 h, USD 800</li></ul><p>Os dados reais existentes que são atualizados:</p><ul><li>**Dados reais de vendas cobradas:** Etapa, USD 5.000, *Ajustado*</li></ul><p>Novos dados reais que são criados para reverter os valores de vendas cobradas anteriores:</p><ul><li>**Dados reais de vendas cobradas:** Etapa, (USD 5.000), *Não Ajustável*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
