---
title: Novidades ou alterações na Versão de Atualização 26 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 26 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143544"
---
# <a name="project-service-automation-update-release-26-v3"></a>Versão de Atualização 26, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas do Project Service Automation Versão de Atualização 26, V3. Esta versão tem um número de compilação de V3.10.44.59 e está geralmente disponível por meio de uma atualização automática em dezembro de 2020.

## <a name="update-release-26"></a>Versão de Atualização 26

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

Os seguintes problemas foram corrigidos:

- Os usuários podem alterar a tarefa em uma entrada de hora que foi aprovada/enviada.
- Erro "Referência do Objeto não Definida" ao salvar a entrada de hora.
- A importação de entradas de horas de atribuições de recursos cria entradas de hora com os valores DateTime incorretos.
- Quando o Project Service Automation e o aplicativo Field Service estão instalados, o botão **Novo** é exibido duas vezes na barra de comandos para entradas de hora no aplicativo Field Service.
- As células **Permitir Unidade** e **Grupo de unidades** atualizam agora o trabalho na grade **Estimativas de Despesas**.
- O formulário **Atualizar Edição de Entrada de Hora** inclui **Linha do tempo**.
- A aprovação de tempo para entradas de hora que não são do projeto bloqueia o sistema ao pesquisar uma função de aprovador de projeto.

**Gerenciamento de Recursos**

Os seguintes problemas foram corrigidos:

- Validação adicionada no plug-in **PostProjectCreate** para verificar um requisito principal antes de criar um.
- O formulário de criação rápida de **Membro da Equipe do Projeto** lançará uma exceção de referência nula se campos forem removidos do formulário.
- A geração de requisitos para 12 horas em 1 ano falhará.
- Exceção de referência nula de mensagem de erro aprimorada durante a criação do requisito de recurso.

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- Validação aprimorada para abordar a exceção de referência nula gerada no plug-in **PreProjectUpdate**.
- Os projetos publicados pelo suplemento da área de trabalho do Microsoft Project excluem atribuições não atribuídas.
- Nova validação adicionada quando a referência de projeto de uma tarefa é inválida devido à exceção de referência nula no plug-in **PreValidateProjectTaskUpdate**.
- A grade Membro da Equipe não mostra atribuições distintas no registro do membro da equipe.
- Novas mensagens de validação e de erro adicionadas devido à exceção de referência nula no plug-in **PreProjectTaskDelete**.

**Sales**

Os seguintes problemas foram corrigidos:

- Ao selecionar uma linha baseada em projeto na cotação ou contrato, o botão **Sugestão** só deve estar visível ao selecionar uma linha baseada em produto associada a um produto existente.
- Divida privilégio **Create_Product** de privilégio **Create_ProjectContract**.
- Excluir uma linha de fatura causa falha de referência nula em **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.
