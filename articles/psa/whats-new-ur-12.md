---
title: Novidades ou alterações na Versão de Atualização 12 do Project Service Automation V3
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado na Versão da Atualização 12 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143814"
---
# <a name="project-service-automation-update-release-12-v3"></a>Versão de Atualização 12, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o orgulho de anunciar a versão mais recente do aplicativo Dynamics 365 Project Service Automation (PSA). Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e vá para a página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 12. Esta versão tem um número de compilação da V3.10.2.34 e está geralmente disponível por meio de uma atualização automática em outubro de 2019.

## <a name="update-release-12"></a>Versão de Atualização 12

### <a name="bug-fixes"></a>Correções de bugs

- Tempo e Despesa

    - Corrigido: As mensagens de erro de entrada de hora foram atualizadas com um contexto mais relevante.
    - Corrigido: A grade de entrada de hora e a agenda exibem corretamente a barra de rolagem quando necessário.
    - Corrigido: As despesas e as entradas de tempo enviadas podem ser aprovadas.
    - Corrigido: A mensagem da caixa de diálogo de confirmação do cancelamento da aprovação foi corrigida para refletir o status da aprovação quando alterado de **Aprovada** para **Enviada**.
    - Corrigido: Os campos **Preço**, **Unidade** e **Quantidade** são bloqueados no registro de Despesas após a aprovação.

- Gerenciamento de projetos

    - Corrigido: A ação **Novo** no formulário principal de **Membro da equipe** foi removida.
    - Corrigido: As atribuições de recursos foram atualizadas para considerar erros de arredondamento imprecisos, que resultam em uma alteração na data de término da tarefa.
    - Corrigido: Na grade da tarefa, erros relevantes do lado do servidor serão exibidos para o usuário.
    - Corrigido: O nome do membro da equipe agora é processado no seletor de pessoas da tarefa, e não no nome da posição.

- Gerenciamento de Recursos

    - Corrigido: Os detalhes dos requisitos de recursos para projetos criados a partir de um modelo agora usam o calendário do projeto.
    - Corrigido: As habilidades e competências agora são padronizadas a partir dos dados mestre da função para o requisito do recurso criado para essa função.

- Sales

    - Corrigido: IDs de objeto duplicados encontrados no formulário do **Contrato principal**.
    - Corrigido: A lógica foi atualizada para tornar a guia **Análise de cotação** visível para exibir a configuração de metadados da guia.
    - Corrigido: Data contábil no registro real agora é gerada com base na data da entrada de hora/despesa e não da data da aprovação.


[!INCLUDE[footer-include](../includes/footer-banner.md)]