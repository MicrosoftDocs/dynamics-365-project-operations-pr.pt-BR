---
title: Copiar contratos baseados em projeto
description: Este artigo fornece informações sobre como copiar contratos de projeto no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410307"
---
# <a name="copy-project-based-contracts"></a>Copiar contratos baseados em projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Você pode criar facilmente novos contratos de projeto ao copiar os contratos existentes de uma das seguintes maneiras:

- Na página de listagem **Contratos de Projeto**, selecione um contrato de projeto e, em seguida, selecione **Copiar**.
- Na página **Contrato de Projeto**, selecione **Copiar**.

Em ambos os casos, aparecerá uma caixa de diálogo, na qual você pode definir os parâmetros do contrato copiado. A caixa de diálogo inclui os campos a seguir. Dependendo dos valores selecionados, o processo de cópia pode mudar.

| Campo | Description | Impacto a jusante |
| --- | --- | --- |
| Tópico | Insira o tópico do contrato de destino. Quando a caixa de diálogo é aberta, o sistema define o campo com o nome do contrato de origem, mas a palavra "cópia" é acrescentada. | Não há impacto posterior para este campo. |
| Customer | Uma referência à empresa do cliente ou registro de conta. Quando a caixa de diálogo é aberta, o sistema define o campo para a conta do contrato de origem. | Esse campo é o cliente principal no contrato. |
| Empresa Proprietária | A empresa responsável pela entrega dos projetos associados a este negócio. Quando a caixa de diálogo é aberta, o sistema define o campo para a empresa proprietária do contrato de origem. | A empresa proprietária é a entidade legal que executará o projeto após o fechamento do negócio. A moeda da empresa proprietária deve corresponder à moeda da unidade contratante. |
| Unidade de Contratação | A unidade organizacional responsável pela entrega dos projetos associados a este negócio. Quando a caixa de diálogo é aberta, o sistema define o campo para a unidade contratante do contrato de origem. | A unidade de contratação é a divisão da empresa que executará os projetos após o fechamento do negócio. Cada unidade contratante tem uma moeda. Essa moeda é usada para relatar os custos estimados e reais incorridos durante o projeto. |
| Currency | A moeda de transação do negócio. Quando a caixa de diálogo é aberta, o sistema define o campo para a moeda do contrato de origem. A moeda pode ser alterada. Nesse caso, o campo **Copiar Preços** sempre será definido como **Não**, pois as listas de preços no contrato de origem não serão mais relevantes. | Essa moeda é usada para listas de preços padrão, a fim de gerar estimativas financeiras no contrato e emitir uma fatura para o cliente quando o negócio for fechado. |
| Data de Entrega Solicitada | A data de entrega solicitada pelo cliente. | Essa data é usada como a data de término quando você cria datas de faturamento em uma frequência específica. |
| Copiar precificação | Um valor que indica se os preços no contrato deverão ser copiados do contrato de origem. | Se o campo estiver definido como **Sim**, as referências de lista de preços de projeto e produto serão copiadas do contrato de origem para o contrato de destino. Se estiver definido como **Não**, as listas de preços padrão serão usadas com base nas listas de preços mais recentes nos parâmetros da conta ou do projeto. |

Quando você seleciona **OK** na caixa de diálogo, o sistema cria uma cópia do contrato, com base nos valores dos parâmetros definidos. Em seguida, o novo contrato é aberto.

As informações a seguir **não** são copiadas do contrato de origem para o contrato de destino, pois são específicas de cada contrato:

- Agendamento de faturas
- Clientes de contrato e de linha de contrato
- Referência de projeto nas linhas de contrato baseadas em projeto
- Informações de orçamento do cliente

Linhas de contrato para projetos e produtos, estimativas em detalhes da linha de contrato e valores que não devem ser excedidos no nível de contrato são copiados. A entrada de preços padrão e taxas de custo depende da seleção no campo **Preço de cópia** na caixa de diálogo **Parâmetros de Cópia**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
