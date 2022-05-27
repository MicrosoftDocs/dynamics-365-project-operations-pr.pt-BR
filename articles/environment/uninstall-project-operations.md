---
title: Desinstale o Dynamics 365 Project Operations
description: Este tópico fornece informações sobre como desinstalar o Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e2600c770477ad32cebb66f33a8ca31502a6da3d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575842"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Desinstale o Dynamics 365 Project Operations 

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Para desinstalar o Dynamics 365 Project Operations, você deverá ter a função de Administrador.

1. Vá para **Configurações** > **Soluções**.

    ![Página Configurações.](./media/uninstall-proj-ops-solutions.png)
  
2. Remova as soluções na ordem exata em que estão listadas na tabela a seguir. 

    | Etapa | Solução   nome                                    | Nota                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 0 | msdyn_ProjectServiceUpgrade_managed.cab            | Se não for encontrada, ignore esta solução.                                                            |
    | 2 | ProjectOperations_Anchor                           | Se não for encontrada, ignore esta solução.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Se não for encontrada, ignore esta solução.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Se não for encontrada, ignore esta solução.                                                            |
    | 5 | ProjectService                                     | Sem observações adicionais.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Sem observações adicionais.                                                                         |
    | 7 | ProjectServiceCore                                 | Sem observações adicionais.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Se não for encontrada, ignore esta solução.                                                            |
    | 9 | FieldServiceCommon                                 | Necessário para gravação dupla com o Dynamics 365 Finance ou o Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Necessário para gravação dupla com o Dynamics 365 Finance ou o Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Necessário para Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Necessário para Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Necessário para Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Necessário para Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Necessário para Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Necessário para Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Necessário para Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Se não for encontrada, ignore esta solução.                                                            |
    | 19 | Dynamics365Notes                                   | Se não for encontrada, ignore esta solução.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Se não for encontrada, ignore esta solução.                                                            |
    | 21 | DualWriteCore                                      | Se não for encontrada, ignore esta solução.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Se não for encontrada, ignore esta solução.                                                            |
    | 23 | Dynamics365AssetManagement                         | Se não for encontrada, ignore esta solução.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Se não for encontrada, ignore esta solução.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Se não for encontrada, ignore esta solução.                                                            |
    | 26 | HCMCommon                                          | Se não for encontrada, ignore esta solução.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Se não for encontrada, ignore esta solução.                                                            |
    | 28 | Entidade                                              | Se não for encontrada, ignore esta solução.                                                            |
    | 29 | Dynamics365Company                                 | Se não for encontrada, ignore esta solução.                                                            |
    | 30 | CurrencyExchangeRates                              | Se não for encontrada, ignore esta solução.                                                            |
    | 31 | AssetCommon                                        | Se não for encontrada, ignore esta solução.                                                            |
