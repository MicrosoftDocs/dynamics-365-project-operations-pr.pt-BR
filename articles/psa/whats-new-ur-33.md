---
title: Novidades ou alterações na Versão de Atualização 33 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 33 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: a72202905fc0464577bb126aa5890a8f952dc3a8aff505416e535b42b53df7db
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006502"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novidades ou alterações na Versão de Atualização 33 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 33. Esta versão tem um número de compilação de V3.10.54.98 e geralmente fica disponível por meio de uma atualização automática em julho de 2021.

## <a name="update-release-33"></a>Versão de Atualização 33

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

Os seguintes problemas foram corrigidos:

- Dois campos bloqueados, **msdyn_description** e **msdyn_externaldescription** são editáveis após o envio.
- Uma mensagem de erro será exibida se uma despesa não relacionada a um projeto for criada.
- Quando uma entrada de tempo é criada, a função do recurso assume como padrão uma função inativa.
- As linhas do diário associadas a uma despesa recuperada e excluída não são excluídas.
- No **Formulário de Criação Rápida de entrada de horas**, atualize a exibição **Lista de Tarefas do Projeto** para alterar a data exibida por padrão para a data de início da tarefa.
- Quando você cria uma entrada de tempo a partir da guia **Relacionado** do recurso reservável, a entrada de hora é criada incorretamente para o usuário conectado em vez do recurso reservável pai.
- Novos campos são adicionados à caixa de diálogo **Aprovação em massa de MDD**.

**Planejamento do projeto**

Os seguintes problemas foram corrigidos:
- Desempenho lento na criação de projetos quando os modelos de horas de trabalho do projeto são aplicados a calendários complexos.
- Quando a data de início é maior que a data de término, um erro é exibido no modelo de projeto de cópia devido às diferenças no componente de tempo de cada campo.

**Gerenciamento de recursos**

Os seguintes problemas foram corrigidos:
- Um parâmetro incorreto é usado na consulta de utilização de recursos e o XML leva a resultados de filtro incorretos na grade **Utilização de Recursos**.
- A confirmação **Estender Reservas** exibe a data de término incorreta para as reservas.

**Vendas**

Os seguintes problemas foram corrigidos:
- Uma mensagem de erro ocorre se um preço de categoria for criado com valores ausentes.
- Uma mensagem de erro ocorre se um marco de linha de contrato for criado sem uma linha de ordem.
