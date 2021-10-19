---
title: Novidades ou alterações na Versão de Atualização 36 do Project Service Automation V3
description: Este tópico lista os recursos e as correções disponíveis na Versão de Atualização 36 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606719"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Novidades ou alterações na Versão de Atualização 36 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas do Project Service Automation Versão de Atualização 36, V3. Esta versão tem um número de compilação da V3.10.57.152 e está geralmente disponível por meio de uma atualização automática em outubro de 2021.

## <a name="update-release-36"></a>Versão de Atualização 36

### <a name="bug-fixes"></a>Correções de bugs

Os seguintes problemas foram corrigidos.

**Geral**
- O nome do campo **Modelo de Horário de Trabalho Padrão** é traduzido incorretamente na página **Parâmetros do Projeto**.
- Os plug-ins assíncronos não lidam corretamente com as exceções relacionadas ao **SharedVariableService**.

**Tempo e Despesa**
- Quando as linhas do diário estão ausentes ou o usuário não tem os privilégios corretos para ler as linhas do diário, ocorre um erro incorreto quando as aprovações do projeto são canceladas.
- Os usuários não podem cancelar uma aprovação quando uma entrada de despesas ou horas tem mais de uma aprovação de projeto associada.
- **Ausência** e **Férias** são traduzidos incorretamente para o idioma chinês em uma pesquisa na página de criação rápida **Entrada de Hora**.

**Gerenciamento de recursos**
- O usuário não pode pesquisar recursos no **Assistente de Agendamento** quando o modo de visualização é definido como **Dia**, **Semana** ou **Mês**.
- Recursos genéricos podem ter permissão incorreta para terem nomes de posição vazios. 
- Fechar um contrato como perdido não cancela reservas futuras.

**Vendas**
- Quando um ambiente tem um grande volume de produtos, o desempenho é prejudicado na grade **Estimativa de Materiais**.
- Ao criar um projeto a partir de um modelo, a moeda do projeto não é padronizada para a unidade contratante do respectivo Gerente de Projeto.
- Os valores reais nem sempre correspondem ao que é refletido no projeto devido, ou os valores tornam-se negativos em cenários de recall específicos.
- Ocorre um erro ao associar um projeto criado a partir de um modelo de projeto a uma linha de contrato.
- Os usuários podem excluir uma linha de contrato com as etapas **Pronto para faturamento** e **Fatura Criada**. Isso não deveria ser permitido.
- Quando as estimativas são importadas de um projeto, os encargos dos detalhes da linha da cotação são configurados incorretamente quando o faturamento baseado em tarefa está habilitado para a linha da cotação.
- Quando você adiciona uma etapa de faturamento de preço fixo, ela não é refletida na subgrade de etapas marco até que a página seja atualizada.
- Uma exceção de referência nula é gerada quando você cria um contrato de projeto com um nome de cotação que seja nulo.
- Tarefas de modo manual em que a moeda do projeto é diferente da moeda do recurso resultam em estimativas de preço incorretas.
- Os usuários não conseguem fazer recall de uma transação que foi corrigida com êxito por uma fatura corretiva.
- As categorias de transações desativadas aparecem na grade **Estimativas de despesas**.



