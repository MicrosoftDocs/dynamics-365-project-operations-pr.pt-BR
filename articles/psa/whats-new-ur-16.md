---
title: Novidades ou alterações na Versão de Atualização 16 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 16 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 2c93d34b61001b7755d426539ac384641a7bc9da
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121564"
---
# <a name="project-service-automation-update-release-16-v3"></a>Versão de Atualização 16, do Project Service Automation V3

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.  Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e a página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, Atualizar uma Solução Preferencial](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 16. Esta versão tem um número de compilação de V3.10.6.34 e está geralmente disponível por meio de uma atualização automática em janeiro de 2020.


## <a name="update-release-16"></a>Versão de Atualização 16

### <a name="bug-fixes"></a>Correções de bugs

-   Tempo e Despesa

    -   Corrigido: Os usuários que tentarem enviar entradas de hora e despesas excluídas para aprovações receberão mensagens de erro relevantes.

-   Gerenciamento de projetos

    -   Corrigido: As unidades de recursos definidas para membros da equipe em modelos são respeitadas e os modelos são aplicados a um novo projeto.

    -   Corrigido: Melhoria no tratamento da reatribuição de propriedade do registro.

    -   Corrigido: Os projetos que estão no processo de serem copiados não poderão ser copiados até que todas as operações de cópia sejam concluídas.

-   Gerenciamento de Recursos

    -   Fixo: Estender reservas agora aceita curtas durações corretamente e não mais cria zero horas para reservas prolongadas.

    -   Corrigido: A exibição da reconciliação agora é renderizada quando o fuso horário do projeto for +5:30 GMT e o horário do usuário for diferente.

-   Sales

    -   Corrigido: Quando um projeto mapeado para uma linha de contrato for removida e um novo projeto for mapeado, os registros do novo projeto não estavam sendo reavaliados com base nas regras de faturamento e preço definidas na linha de contrato. Isso foi corrigido nessa versão. Os preços e os registros atuais do projeto mapeado recentemente serão revertidos e recriados corretamente com base nas regras de faturamento e cobrança da linha de contrato. Os registros atuais de um projeto não mapeado também serão reavaliados e recriados como consequência.

    -   Corrigido: Uma validação adicional foi incluída a um campo **Valor** da linha de estimativa para garantir que os valores nulos não sejam persistentes.

    -   Corrigido: Quando dados reais tiverem sido atualizados em um projeto, um botão de atualização foi adicionado ao formulário principal do projeto para permitir que os usuários sincronizem novamente os dados reais.

    -   Corrigido: Quando os usuários atualizarem do 2.X para 3.X, os projetos com valor NULL para o nome do projeto serão permitidos.

