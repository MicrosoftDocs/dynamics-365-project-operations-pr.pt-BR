---
title: Erro de incompatibilidade de moeda
description: Este artigo fornece informações de solução de problemas sobre um erro de incompatibilidade de moeda que ocorre quando você salva tipos de registro específicos.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914710"
---
# <a name="currency-mismatch-error"></a>Erro de incompatibilidade de moeda 

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Ao salvar um projeto, contrato, cotação ou recurso reservável, você pode receber o erro **A moeda da empresa proprietária não corresponde à moeda da unidade de contratação. Escolha uma empresa proprietária ou unidade de contratação para continuar**. Isso ocorre porque há uma incompatibilidade de moeda entre a moeda da unidade de contratação para o registro e a moeda da empresa proprietária.


## <a name="resolution"></a>Resolução

Para contornar esse problema, faça o seguinte:
- Verifique a moeda da unidade de contratação para esse registro. Você pode ver a moeda abrindo o registro da unidade organizacional e verificando o valor na guia **Geral** no campo **Moeda**.
- Verifique a moeda da empresa proprietária. Você pode ver a moeda acessando **Relacionado** > **Razões** no registro da empresa. Clique duas vezes no registro contábil associado à empresa e verifique o valor na guia **Geral** no campo **Moeda contábil**.

Se a moeda definida na unidade de contratação e o registro contábil não corresponderem, ajuste a configuração ou selecione valores diferentes ao salvar o registro. O sistema exige que esses registros correspondam para garantir fluxos corretos de faturamento intercompanhia. Para obter mais informações sobre as configurações intercompanhia, consulte [Criar transações intercompanhia](../../project-accounting/create-intercompany-transactions.md).

Se o registro da empresa não tiver registro contábil associado, isso indica que há uma configuração ausente ao configurar o ambiente. A configuração deve ser corrigida pelo administrador do sistema. O administrador do sistema deve acessar **Configurações de gravação dupla**, interromper e reiniciar o **Mapa de gravação dupla de livros razão** com a sincronização inicial desse mapa e seus pré-requisitos. Para mais informações, consulte [Versões de mapa de gravação dupla do Project Operations](../../environment/resource-dual-write-maps.md).
