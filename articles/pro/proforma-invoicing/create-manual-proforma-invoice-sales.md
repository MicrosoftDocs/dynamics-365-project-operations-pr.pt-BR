---
title: Criar uma fatura pro forma manual - lite
description: Este tópico fornece informações sobre como criar uma fatura pro forma manual no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764489"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Criar uma fatura pro forma manual - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

No Dynamics 365 Project Operations, é possível criar faturas pró-forma manualmente conforme necessário. Você pode criar manualmente uma fatura pro forma da página de listagem **Contratos de Projeto** ou da página de detalhes **Contrato de Projeto**.

##  <a name="project-contracts-list-page"></a>Página de listagem Contratos de Projeto

Na página de listagem **Contratos de Projeto**, selecione um ou mais contratos de projeto e crie faturas para todos os registros selecionados.

O sistema verifica qual dos contratos de projeto selecionados tem uma lista de pendências **Pronto para Faturar** anterior à data de hoje. Desses contratos, o sistema cria rascunhos de faturas pro forma. Se um contrato de projeto tiver vários clientes, poderá haver uma fatura criada por cliente e várias faturas por contrato de projeto.

Todas as faturas de projeto criadas estão disponíveis na página **Fatura**, na seção **Cobrança** da área **Vendas**.

## <a name="project-contract-details-page"></a>Página de detalhes Contrato de Projeto

Também é possível criar uma fatura pro forma na página de detalhes **Contrato de Projeto**. O sistema verifica o contrato de projeto que tem uma lista de pendências em **Pronto para Faturar** anterior à data de hoje. A partir desses contratos, o sistema cria rascunhos de faturas pro forma com base no número de clientes em cada linha do contrato.

Quando há uma única fatura pro forma criada, a página **Fatura** é aberta. Se várias faturas forem criadas para esse contrato de projeto, a página de lista de **Faturas** será aberta para mostrar todas as faturas criadas.
