---
title: Novidades ou alterações na Versão de Atualização 21 do Project Service Automation V3
description: Este artigo lista os recursos e as correções disponíveis na atualização do Project Service Automation versão 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7d7c098a4572aa4f5730ffdbdab77b2897cdfeff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918804"
---
# <a name="project-service-automation-update-release-21-v3"></a>Versão de Atualização 21, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista os recursos e as correções novos ou alterados na atualização do Project Service Automation versão 21, V3. Esta versão apresenta o número de compilação V 3.10.32.50 e está disponível para o público em geral por meio de uma atualização automática em junho de 2020.

## <a name="update-release-21"></a>Versão de Atualização 21

### <a name="bug-fixes"></a>Correções de bug

**Tempo e Despesa**

Os seguintes problemas foram corrigidos:

- Ao hospedar o **Controle de Grade de Entrada de Tempo** nos Painéis, a grade não usa a largura total do contêiner da grade do painel.
- Para fusos horários específicos, o controle de grade da **Entrada de Tempo** não exibe registros.
- As entradas de horas após 21 h aparecem no dia errado.
- Os usuários não conseguem enviar despesas se a categoria **Recibo de despesa obrigatório** não tiver um valor definido.

**Gerenciamento de Recursos**

Os seguintes problemas foram corrigidos:

- As reservas inativas são exibidas em **Reconciliação**.
- O preenchimento de recurso genérico não tinha validação para garantir a existência de um status de reserva válido.

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- As grades do formulário **Projeto** (**Atribuição de Recurso**, **Tarefa**, exibição de **Reconciliação**, **Estimativas de Despesas**) continuam editáveis mesmo se o projeto não estiver ativo.
- Os clientes duplicados não podem ser mesclados com os clientes vinculados a contratos de projetos confirmados.
- Quando um recurso sem um calendário válido é adicionado, o sistema não retorna uma mensagem de erro amigável.
- O botão **Adicionar Tarefa** na grade de tarefas é habilitado quando o projeto está vinculado ao **Suplemento do Microsoft Project**.
- O esforço aumenta de forma incontrolável quando uma tarefa com uma categoria é atribuída a um recurso com uma função para a qual há um preço de custo definido.

**Sales**

Os seguintes aprimoramentos foram realizados:

- **Frequência da fatura** e **Início da Cobrança** foram movidos para a guia **Agenda de Faturas**.

Os seguintes problemas foram corrigidos:

- O **Preço de Venda Total** é 0 (zero) para **Categoria**, embora **Função** tenha um preço de venda total diferente de zero.
- Os clientes não podem alterar o valor do campo **Status da Fatura** para **Pronto para faturamento** quando outro processo personalizado estiver atualizando um campo adicional.
- O botão **Atualizar Linhas da Fatura** pode criar várias linhas duplicadas se for selecionado repetidas vezes.
- O botão **Atualizar Preços** não funciona na subgrade **Preços da Função** no formulário de **Exibição Rápida**.
- A lógica **Resolução da Lista de Preços de Venda** trata incorretamente os fusos horários, resultando na seleção incorreta de listas de preços.
- O **Custo Total Real** de um projeto pode apresentar uma diferença fracionária após a aprovação de uma única entrada de tempo.
- A lógica **Resolução de Preço** não fornece uma mensagem de erro amigável se **Preço de Função Recuperado** não tiver valores nos campos **Unidade Principal** e **Preço na Unidade Principal**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
