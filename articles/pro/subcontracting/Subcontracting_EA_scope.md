---
title: Subcontratação na versão do acesso antecipado de outubro de 2021
description: Este tópico fornece uma visão geral dos recursos de subcontrato no Project Operations que fazem parte da versão de acesso antecipado de outubro de 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383681"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Subcontratação na versão do acesso antecipado de outubro de 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este tópico fornece uma visão geral dos recursos de subcontrato no Dynamics 365 Project Operations que fazem parte da versão de acesso antecipado de outubro de 2021. Este conjunto de recursos não está pronto para ambientes de produção ou ao vivo e, portanto, esses recursos permanecerão na versão de acesso antecipado até que o conjunto completo de recursos seja lançado. É altamente recomendável que você não use o recurso de subcontratação definido para cenários de produção ao vivo até que o banner de versão preliminar seja removido. 

A lista a seguir fornece um esboço do que está disponível atualmente na versão de acesso antecipado de outubro de 2021:

1. O gerente de projeto cria um subcontrato com um fornecedor. Por padrão, as listas de preços anexadas ao registro do fornecedor são usadas para o subcontrato. A conta do fornecedor tem um tipo de relacionamento de **Fornecedor** ou **Provedor**.

2. O gerente de projeto pode discriminar todas as compras como itens de linha no subcontrato. As linhas do subcontrato podem ser por tempo, despesas ou produtos. A classe de transação da linha de subcontrato determina para que serve a linha.

3. O gerente de conta do fornecedor e o gerente de projeto podem iterar no subcontrato. O preço pode ser ajustado nas listas de preços de compra que são anexadas ao subcontrato.

4. Nesse ponto ou posteriormente no processo, se a linha de subcontrato for para tempo, o gerente de conta do fornecedor associa os contatos de fornecedor a cada linha de subcontrato. Essa associação fornece informações ao gerente de projeto que está trabalhando no subcontrato. Quando um contato de fornecedor é associado a uma linha de subcontrato, o sistema cria automaticamente um recurso reservável direto do contato, se um recurso reservável ainda não existir.

5. O método de faturamento em cada linha do subcontrato pode ser **Preço fixo** ou **Tempo e Material**. Para linhas do subcontrato de preço fixo, uma agenda de faturamento baseada em marcos é configurada.

As etapas restantes no fluxo do processo empresarial para subcontratação que estão descritas na Visão geral não estão disponíveis no momento. Quando novas funcionalidades forem adicionadas, este tópico será atualizado. 

A ilustração a seguir representa a versão de Acesso Antecipado de Subcontratação em contraste com o processo empresarial de ponta a ponta.

![Fluxo do processo de subcontratação](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Versão de acesso antecipado às linhas de subcontrato com base na quantidade e no trabalho
Na versão de Acesso Antecipado de outubro de 2021, apenas as linhas de subcontrato com base na quantidade têm suporte. Isso significa que uma linha de subcontrato pode ser usada para comprar tempo, despesas ou materiais de um fornecedor, mas não todo um corpo de trabalho. Isso também significa que a quantidade que está sendo comprada (unidades de tempo, despesas ou quantidade de materiais) em uma linha de subcontrato pode ser usada em qualquer projeto no sistema.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
