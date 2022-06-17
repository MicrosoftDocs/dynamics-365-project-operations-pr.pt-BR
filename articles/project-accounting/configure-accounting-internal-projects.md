---
title: Configurar contabilidade para projetos internos
description: Este artigo fornece informações sobre como configurar práticas de contabilidade para projetos internos no Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919448"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurar contabilidade para projetos internos

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Os projetos internos permitem que as empresas rastreiem os custos relacionados às atividades que não estão sendo cobradas de um cliente. Exemplos de projetos internos incluem:

- Desenvolver um produto, como um aplicativo móvel, e monitorar o custo associado ao desenvolvimento.
- Gerenciamento do tempo e de despesas de pré-venda. Este projeto interno de pré-venda pode ser convertido posteriormente em um projeto faturável se a cotação for ganha.

Todos os projetos não associados a um contrato no Dynamics 365 Project Operations são tratados como internos. Os perfis de custo e de receita do projeto não são usados para determinar as regras de contabilidade para o projeto. O custo interno do projeto é sempre lançado usando os princípios de lucros e perdas. As contas contábeis para lançamentos são definidas na página **Configuração de lançamento do razão**.

- As transações de tempo são lançadas por meio de débito da conta **Custo** e crédito na conta **Alocação de folha de pagamento**.
- As transações de despesas são lançadas por meio de débito na conta **Custo** e crédito na conta **Contrapartida para despesas**.
- As transações são lançadas por meio de débito na conta **Custo** e de crédito na conta **Custo - Item**.

Depois que as transações forem lançadas no projeto, se o projeto estiver associado a um contrato de projeto, o sistema reverterá todas as transações acumuladas e criará novas transações faturáveis. As transações faturáveis seguem as regras de contabilidade definidas no respectivo perfil Custo e receita de projeto.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
