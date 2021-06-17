---
title: Confirmar um contrato de projeto
description: Este tópico fornece informações sobre como confirmar um contrato no Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003662"
---
# <a name="confirm-a-project-contract"></a>Confirmar um contrato de projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Um contrato de projeto no Dynamics 365 Project Operations pode estar ativado com um motivo **Confirmado** ou fechado com um motivo **Perdido**. Quando você confirma um contrato de projeto, o status é atualizado de **Rascunho** para **Ativo** e a razão do status é **Confirmado**. Um contrato ativo ou fechado não pode ser editado ou reaberto. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Impacto financeiro da confirmação de um contrato de projeto

Após a confirmação de um contrato de projeto, o aplicativo recalculará os custos estornando os custos reais mais antigos e recriando os novos custos reais. Os novos custos reais são então processados com base no método de cobrança da linha de contrato de projeto associada. Se os valores reais de custo fizerem referência a uma linha de contrato por Tempo e Material, o aplicativo recriará automaticamente os valores reais de vendas não cobradas correspondentes. Se os custos reais fizerem referência a uma linha de contrato de Preço Fixo, o aplicativo interromperá o reprocessamento dos custos reais.

Limites que não devem ser excedidos, configuração de encargos e preços e custos sobre os reais são avaliados e atualizados como parte do processo de confirmações.

## <a name="close-a-project-contract-as-lost"></a>Fechar um contrato de projeto como perdido

Quando você fecha um contrato de projeto como perdido, o status do contrato é atualizado para **Fechado** e a razão do status é **Perdido**. O contrato do projeto torna-se somente leitura. Um diálogo de confirmação é fornecido antes que as alterações sejam concluídas porque você não pode reabrir um contrato de projeto fechado.

Se o contrato de projeto fechado como perdido fizer referência a um projeto em suas linhas, esse projeto também será marcado como fechado. Todas as reservas de recursos desse dia em diante serão canceladas. Quaisquer vendas não cobradas reais no contrato de projeto que ainda não estejam em uma fatura serão estornadas.

> [!NOTE]
> No Dynamics 365 Project Operations, fechar um contrato de projeto como perdido não afetará o status da oportunidade associada. A oportunidade permanecerá aberta e deverá ser fechada manualmente.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]