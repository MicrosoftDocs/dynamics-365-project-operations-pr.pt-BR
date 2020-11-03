---
title: Criando uma fatura pro forma manual
description: Este tópico fornece informações sobre como criar uma fatura pro forma manual no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4071657"
---
# <a name="creating-a-manual-proforma-invoice"></a>Criando uma fatura pro forma manual

_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_

No Dynamics 365 Project Operations, as faturas pro forma podem ser criadas manualmente conforme necessário. Você pode criar manualmente uma fatura pro forma da página de listagem **Contratos de Projeto** ou da página de detalhes **Contrato de Projeto**.

##  <a name="project-contracts-list-page"></a>Página de listagem Contratos de Projeto

Na página de listagem **Contratos de Projeto** , selecione um ou mais contratos de projeto e crie faturas para todos os registros selecionados.

O sistema verifica qual dos contratos de projeto selecionados tem uma lista de pendências **Pronto para Faturar** anterior à data de hoje. Desses contratos, o sistema cria rascunhos de faturas pro forma. Se um contrato de projeto tiver vários clientes, poderá haver uma fatura criada por cliente e várias faturas por contrato de projeto.

Todas as faturas de projeto criadas estão disponíveis na página **Fatura** , na seção **Cobrança** da área **Vendas**.

## <a name="project-contract-details-page"></a>Página de detalhes Contrato de Projeto

Uma fatura pro forma também pode ser criada da página **Contrato de Projeto** , que cria a fatura para aquele contrato de projeto específico. O sistema verifica que o contrato de projeto tem uma lista de pendências **Pronto para Faturar** anterior à data de hoje. A partir desses contratos, o sistema cria rascunhos de faturas pro forma com base no número de clientes em cada linha do contrato.

Quando há uma única fatura pro forma criada, a página **Fatura** é aberta. Se houver várias faturas criadas para esse contrato de projeto, então a página de listagem **Faturas** é aberta para mostrar todas as faturas criadas.
