---
title: Erro de incompatibilidade de moeda
description: Este tópico fornece informações de solução de problemas sobre um erro de incompatibilidade de moeda que ocorre quando você salva tipos de registro específicos.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589734"
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
