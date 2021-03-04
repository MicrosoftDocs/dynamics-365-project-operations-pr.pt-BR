---
title: Novidades ou alterações na Versão de Atualização 27 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 27 do Project Service Automation V3.
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146649"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Novidades ou alterações na Versão de Atualização 27 do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 27. Esta versão tem um número de compilação de V3.10.45.98 e está geralmente disponível por meio de uma atualização automática em janeiro de 2021.

## <a name="update-release-27"></a>Versão de Atualização 27

### <a name="bug-fixes"></a>Correções de bug

**Geral**

Os seguintes problemas foram corrigidos:

- Os logs gerados por plug-ins no Project Service Automation não foram configurados para exclusão automática.
- A atualização automática falha porque a solução do Project Service Automation contém um NavBarArea e um elemento de título nulo herdado.

**Tempo e Despesa**

Os seguintes problemas foram corrigidos:

- A grade **Entrada de tempo** exibe dados incorretos para o comportamento de data **Independente de Fuso Horário**.
- A grade **Entrada de tempo** exibe dados incorretos para o comportamento de data **Independente de Fuso Horário**.
- A pesquisa de tarefas não se limita ao projeto selecionado na página **Editar entrada de tempo**.
- A aprovação de tempo para entradas de hora que não são do projeto é bloqueada porque o sistema está procurando um aprovador de projeto.
- As entradas corretas em Dados reais exibe uma mensagem de erro incorreta.
- Quando uma tarefa contém um valor nulo para o custo real e os totais do projeto são atualizados, ocorre o seguinte erro: "Chave fornecida não presente no dicionário".
- Em casos específicos, os filtros **Agrupar por** na guia **Estimativa de projeto** não exibe estimativas de despesas.
- O intervalo **Horário de verão** não está correto para entradas de tempo.

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- Melhorias de cache, o que melhora o desempenho relacionado ao carregamento da página **Projeto**.
- Regra de negócios obsoleta que impede que as tarefas do projeto sejam concluídas.
- Os contornos do suplemento do Microsoft Project não estão respeitando o calendário do suplemento, resultando em requisitos de recursos incorretos.
- A criação de projetos com base em modelos define incorretamente as datas de atribuição e impede a capacidade de gerar requisitos de recursos.
- O usuário não pode acessar as opções **Categoria**, **Descrição** e **Status** usando o teclado.
- Os valores reais de vendas do projeto não incluem os valores de vendas de materiais e taxas.
- A agregação de vendas reais e custo real acontece incorretamente com diferentes taxas de câmbio.
- A descrição no **Modelo de horário de trabalho padrão** é enganosa.
- Recuar uma tarefa não remove a **Categoria** na interface do usuário até que seja atualizada.
- Falta de validação para garantir que não seja permitido mover um projeto além de sua data de término.

**Sales**

Os seguintes problemas foram corrigidos:

- Uma exceção de referência nula é gerada em uma linha de cotação do projeto porque **Importar da estimativa do projeto** é visível quando um projeto não foi selecionado.
- O erro "Referência de objeto não definida para uma instância de um objeto" ocorre ao fechar uma cotação como **Vencida**.
- O status de ajuste não é definido durante uma reversão real ao desvincular um projeto de uma linha de contrato.
- Quando o Dynamics 365 Field Service e Project Service Automation estão instalados, as opções **Preços de bloqueio** e **Use o preço atual** não são exibidas ao mesmo tempo na página **Fatura**.
- Para o idioma japonês, há tradução inconsistente com outras páginas baseadas no calendário.
- **Ativar** e **Desativar** foram removidos de entidades **Associação de lista de preços** no Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]