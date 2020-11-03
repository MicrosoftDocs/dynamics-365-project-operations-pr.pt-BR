---
title: Configurar definições de parâmetro adicionais
description: Como definir configurações de parâmetros adicionais no Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 24a4fe83471da916fb91cfe20e739279c08d8e5e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071428"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Definir configurações de parâmetros adicionais (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Depois que você configurar os itens nos tópicos anteriores, você precisará definir parâmetros de projeto adicionais para usar em seus projetos. Ao instalar o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], você criou uma definição de parâmetros para criar todos os registros necessários para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] funcionar. Agora é hora de voltar e configurar outros campos dessas configurações.  
  
 Você precisará ter configurado às seguintes configurações:  
  
-   Unidade organizacional  
  
-   Frequência da fatura  
  
-   Modelos de Horas de Trabalho  
  
-   Lista de preços  
 
Nessa etapa, você também indicará o tipo de alocação de recursos que quer:  
  
- **Central**. Somente gerentes de recursos podem atribuir recursos para projetos.  
  
- **Híbrido**. Os gerentes de recursos, gerentes de projetos e gerentes de contas podem alocar recursos a projetos.  
  
 
Para definir parâmetros de projeto:  
  
1. Vá para **Project Service > Parâmetros**.  
  
2. Clique na configuração de parâmetros que deseja configurar (a que você criou ao instalar o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) ou clique em **Novo** para criar um novo.  
  
3. Na área **Geral** , defina todas as opções dos parâmetros do projeto.  
  
4. Na área **Lista de preços** , clique em **+** para adicionar uma lista de preços, selecione uma lista de preços na lista suspensa **Lista de Preços do Parâmetro do Projeto** e clique em **Salvar**.  
  
5. Clique no botão **Salvar** no canto inferior direito da tela.  

> [!NOTE]
> O registro do parâmetro do projeto deve ser mantido para que o Project Service funcione corretamente. Esse registro não deve ser excluído.

### <a name="see-also"></a>Consulte também  
 [Configurar recursos](../psa/set-up-resources.md)
