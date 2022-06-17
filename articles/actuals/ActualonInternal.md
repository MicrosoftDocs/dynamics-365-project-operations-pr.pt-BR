---
title: Impacto dos dados reais de um projeto interno
description: Este artigo fornece informações sobre o impacto na tabela Dados reais em vários eventos de um projeto interno no Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921334"
---
# <a name="actuals-impact-for-an-internal-project"></a>Impacto dos dados reais de um projeto interno

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

A tabela a seguir lista os dados reais de diferentes tipos de transação criados em vários eventos em um compromisso de projeto interno.

| Evento | Custo real | Exemplo |
|---|---|---|
| As horas são criadas. | Não aplicável | <p>Bob Kozack, da unidade organizacional da Fabrikam US que tem uma taxa de custo de 100 dólares americanos (USD 100) por hora, está trabalhando em um projeto chamado "Instalação de braço na Adatum". Este projeto está mapeado para um método de cobrança de preço fixo na linha de contrato. Este é um exemplo de entrada de hora de Bob Kozak:</p><p>Bob Kozack - 8 horas</p> |
| As horas são enviadas. | Não aplicável | Uma linha do diário de custo é criada para a entrada de hora. A taxa de custo padrão é inserida na entrada de diário. |
| A entrada de hora é recuperada antes de ser aprovada. | Não aplicável | |
| As horas são aprovadas. | Os dados reais de custo são criados. | <p>Os novos dados reais que são criados:</p><ul><li>**Dados reais de custo:** Bob Kozack, 8 h, USD 800</li></ul> |
| A aprovação de horas é cancelada. | <p>O status de ajuste dos dados de custo real originais é atualizado para **Ajustado**.</p><p>Dados reais de custo de reversão são criados com o status de ajuste **Não Ajustável**.</p> | <p>Os dados reais existentes que são atualizados:</p><ul><li>**Custo real:** Bob Kozack, 8 h, USD 800, *Ajustado*</li></ul><p>Novos dados reais que são criados para reverter o impacto financeiro anterior:</p><ul><li>**Dados reais de custo:** Bob Kozack, (8 h), (USD 800), *Não Ajustável*</li></ul> |
| A entrada de hora é recuperada depois de ser aprovada. | <p>O status de ajuste dos dados de custo real originais é atualizado para **Ajustado**.</p><p>Dados reais de custo de reversão são criados com o status de ajuste **Não Ajustável**.</p> | <p>Os dados reais existentes que são atualizados:</p><ul><li>**Custo real:** Bob Kozack, 8 h, USD 800, *Ajustado*</li></ul><p>Novos dados reais que são criados para reverter o impacto financeiro anterior:</p><ul><li>**Dados reais de custo:** Bob Kozack, (8 h), (USD 800), *Não Ajustável*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
