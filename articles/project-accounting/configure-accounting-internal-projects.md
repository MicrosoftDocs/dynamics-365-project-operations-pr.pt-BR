---
title: Configurar contabilidade para projetos internos
description: Este tópico fornece informações sobre como configurar práticas de contabilidade para projetos internos no Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132364"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurar contabilidade para projetos internos

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Os projetos internos permitem que as empresas rastreiem os custos relacionados às atividades que não estão sendo cobradas de um cliente. Exemplos de projetos internos incluem:

- Desenvolver um produto, como um aplicativo móvel, e monitorar o custo associado ao desenvolvimento.
- Gerenciamento do tempo e de despesas de pré-venda. Este projeto interno de pré-venda pode ser convertido posteriormente em um projeto faturável se a cotação for ganha.

Qualquer projeto não associado a um contrato no Dynamics 365 Project Operations é tratado como interno. Os perfis de custo e de receita do projeto não são usados para determinar as regras de contabilidade para o projeto. O custo interno do projeto é sempre lançado usando os princípios de lucros e perdas. As contas contábeis para lançamentos são definidas na página **Configuração de lançamento do razão**.

- As transações de tempo são lançadas por meio de débito da conta **Custo** e crédito na conta **Alocação de folha de pagamento**.
- As transações de despesas são lançadas por meio de débito na conta **Custo** e crédito na conta **Contrapartida para despesas**.

Depois que as transações forem lançadas no projeto, se o projeto estiver associado a um contrato de projeto, o sistema reverterá todas as transações acumuladas e criará novas transações faturáveis. As transações faturáveis seguem as regras de contabilidade definidas no respectivo perfil Custo e receita de projeto.




[!INCLUDE[footer-include](../includes/footer-banner.md)]