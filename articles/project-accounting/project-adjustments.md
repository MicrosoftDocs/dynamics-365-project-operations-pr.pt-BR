---
title: Ajustes de projeto
description: Este artigo fornece informações sobre ajustes de projeto.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788290"
---
# <a name="project-adjustments"></a>Ajustes de projeto

_**Aplicável a:** Project Operations para cenários baseados em estoque/produção_

## <a name="adjustments-overview"></a>Visão geral dos ajustes

Você pode configurar o Microsoft Dynamics 365 Project Operations para que os usuários possam fazer alterações nas transações lançadas. É possível ajustar as transações do projeto individualmente ou pode selecionar várias transações por vez em uma lista de todas as transações do projeto. Os ajustes do projeto são usados, por exemplo, para atualizar em massa o status faturável, recalcular o custo após uma alteração na configuração ou atualizar as fontes de financiamento.

Os usuários podem acessar a funcionalidade de ajustes de projeto de várias maneiras:

- Usando a página **Ajustar transações** que pode ser acessada em **Gerenciamento e contabilidade de projeto** \> **Configuração**.
- Usando o botão **Ajuste** na página **Transações de projeto lançadas** que pode ser acessada em **Gerenciamento e contabilidade de projeto** \> **Transações**.
- Usando o botão **Ajuste** na página **Transações de projeto lançadas** contexto de um projeto. Esta página pode ser acessada em **Gerenciamento e contabilidade de projeto** \> **Todos os projetos**.

Para permitir ajustes, você deve habilitar um ou mais status de transação em **Gerenciamento e contabilidade de projeto** \> **Gerenciamento de projetos e parâmetros de contabilidade** na guia **Geral** na seção **Permitir ajuste do status da transação**. Exemplos de status de transação incluem transações lançadas, transações faturadas ou transações eliminadas. Qualquer status de transação definido como **Não** terá transações nesse status que não aparecerão no processo de ajuste como selecionáveis para ajuste.

Uma opção de configuração denominada **Criar sempre transação de ajuste** está atualmente disponível em Gerenciamento de projetos e parâmetros de contabilidade. Você pode desativar esta opção para atualizar a transação original em vez de criar transações durante o ajuste em um subconjunto de cenários. Foi anunciado que esse parâmetro será descontinuado em 1º de março de 2023. Após 1º de março de 2023, o sistema sempre se comportará como se a opção estivesse habilitada.

## <a name="adjustments-process-flow"></a>Fluxo do processo de ajustes

As etapas a seguir mostram o fluxo típico para processar ajustes.

1. Abra a página **Ajustes de projeto**.
2. Selecione **Selecionar** para pesquisar transações que atendam aos critérios de ajuste esperados.
3. Na lista de transações, selecione todas as transações ou um subconjunto das transações para ajuste.
4. Selecione **Ajustar** e modifique os atributos na linha. Como alternativa, se os valores foram especificados manualmente durante a entrada da transação, você pode optar por inserir valores padrão do sistema.
5. A lista de transações é retornada e uma marca de seleção aparece na coluna **Ajuste pendente** para indicar onde as alterações foram feitas. Quaisquer ajustes com alterações pendentes são mostrados na metade inferior da página. Nessa parte da página, você pode fazer alterações detalhadas adicionais além do que foi mostrado na página anterior.
6. Selecione **Lançar** para lançar as transações de ajuste.

Dependendo da configuração, geralmente são criadas novas transações para o ajuste.

- O campo **Status da Fatura** da transação original é definido como **Ajustado**.
- Uma transação de reversão é criada para reverter a transação original e o campo **Status** é definido como **Ajustado**.
- Uma nova transação é criada com as alterações feitas durante o processo de ajuste.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Seleção de várias transações de projeto lançadas por vez para ajustes e notas de crédito

Um novo recurso que foi introduzido na versão 10.0.30 permite a seleção de várias transações para ajuste por vez na página **Transações de projeto lançadas**.

Antes de poder usar esse recurso, ele deverá estar habilitado no seu sistema. Os administradores podem usar o espaço de trabalho **Gerenciamento de recursos** para verificar o status do recurso e ativá-lo, se necessário. No espaço de trabalho **Gerenciamento de recursos**, procure e selecione **Seleção de várias transações de projeto lançadas para ajustes e notas de crédito** e selecione **Habilitar agora**.

Esse recurso permite a seguinte funcionalidade principal:

- Ele pode ser acessado a partir da página de transação lançada dentro de um projeto usando o botão existente **Ajuste**.
- Ele permite um controle de seleção de várias linhas na página **Transações de projeto lançadas**. É possível aplicar filtros à página da lista e selecionar seus registros antes de iniciar os ajustes.
- Ele desativa o botão **Ajuste** se qualquer transação única não puder ser ajustada ou se você selecionar uma combinação de notas de crédito e diários juntos em vez de individualmente.
- Por causa da adição do controle de seleção de várias linhas, o link **Custo comprometido** na faixa de opções não é mais desativado se várias linhas forem selecionadas.
- Ele adiciona a seguinte mensagem de aviso: "Você selecionou mais de (número selecionado) registros para ajuste. Continuar com esta ação pode levar algum tempo. Tem certeza de que deseja prosseguir com esta ação?"

Esse recurso também remove a etapa 2 do fluxo do processo descrito anteriormente neste artigo. Portanto, todas as transações selecionadas antes da abertura da página **Ajustar transações** serão incluídas na lista de transações para ajuste. Não é preciso usar o botão **Selecionar** para procurá-los.

> [!NOTE] 
> Mesmo que esse recurso esteja desabilitado, você ainda pode selecionar vários registros para ajuste. Contudo, apenas um registro *permanecerá selecionado*, e a caixa de diálogo **Selecionar transações** aparecerá imediatamente após você selecionar para abrir os ajustes.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Status de transações de ajuste que podem ser habilitados ou desabilitados para ajustes

Os seguintes status podem ser ativados ou desativados na guia **Geral** da página **Gerenciamento de projetos e parâmetros de contabilidade**:

- Postado
- Proposta de Fatura
- Faturado
- Estimado
- Eliminado
- Saldo inicial (hora)

## <a name="adjustment-parameters"></a>Parâmetros de ajuste

Esses parâmetros estão listados na página **Parâmetros de gerenciamento e contabilidade de projeto** na guia **Geral** no grupo **Ajuste** e modificarão o comportamento de como os ajustes são processados. 

| Nome do parâmetro | Description |
|----------------|-------------
| Criar sempre transação de ajuste | Se esse parâmetro estiver habilitado, o processo de ajuste sempre criará uma transação revertida e uma transação ajustada quando houver impacto financeiro ou de relatório. Se o parâmetro estiver desativado, o processo de ajuste atualizará a transação original em vez de criar um estorno e uma transação para um cenário como uma atualização do texto da transação. |
| Campo de atualização automática | Se esse parâmetro estiver habilitado, o sistema recalculará o preço de custo e o preço de venda. |
| Usar data de ajuste como novo projeto | Esse parâmetro é usado para mover transações para um período fiscal futuro antes do sistema oferecer suporte a essa função. Não recomendamos que você o use, pois ele altera a data comercial da transação e será descontinuado em uma versão futura. |
| Permitir atividades encerradas | Em geral, as transações não podem ser criadas para atividades encerradas. Se esse parâmetro estiver ativado, esse comportamento será substituído. Portanto, ajustes podem ser criados para atividades encerradas. |
