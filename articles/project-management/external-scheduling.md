---
title: Agendamento externo
description: Este artigo fornece informações sobre agendamento externo.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736954"
---
# <a name="external-scheduling"></a>Agendamento externo

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O modo de agendamento externo permite que você crie, atualize e exclua nativamente entidades relacionadas a estruturas de detalhamento de trabalho (WBSs), mas sem os limites atuais impostos pelo Microsoft Project for the Web. Ele também fornece validação limitada. Esse modo deve ser usado apenas pelos seguintes clientes:

- Clientes que possuem as ferramentas necessárias para definir uma WBS fora da lógica de agendamento fornecida pelo Project Operations
- Clientes que precisam gerenciar hierarquia de agendamento, dependências ou duração de tarefas

> [!IMPORTANT]
> Os dados que não forem inseridos corretamente nas entidades relacionadas à WBS talvez não sejam renderizados na grade de reconciliação de recurso, grade de estimativas, grade de acompanhamento ou grade de atribuição de recurso.

## <a name="configuration"></a>Configuration

Por padrão, esse recurso está ativado. No entanto, na página principal do projeto pronta para uso, o campo relacionado não é visível por padrão. Para habilitar o campo, no Maker Portal, abra a página principal da entidade do projeto, selecione o campo **Mecanismo de Agendamento** e, em seguida, altere o campo para **Visível por Padrão**. Se você não usar a página principal do projeto pronta para uso, edite sua página existente e adicione o campo **Mecanismo de Agendamento** a ela.

## <a name="settings"></a>Configurações

Para usar o modo de agendamento externo, você deve primeiro criar um novo projeto e selecionar o mecanismo de agendamento **Programado externamente** na lista suspensa na página principal do projeto. Depois que esse modo for configurado para um projeto, ele não poderá ser alterado.

## <a name="viewing-the-wbs"></a>Exibindo a WBS

Se um projeto for agendado externamente, o acesso ao Project for the Web será restrito àquele projeto. Para exibir a WBS, você deve acessar a grade de rastreamento, onde é mostrada a WBS completa.

## <a name="creating-and-editing-the-wbs"></a>Criando e editando a WBS

Se o agendamento externo estiver habilitado para um projeto, você deverá definir os dados para todas as entidades relacionadas à WBS, incluindo tarefas, membros da equipe, atribuições de recurso e dependências.

A ilustração a seguir mostra o modelo de dados para planejamento de projeto.

![Modelo de dados de planejamento de projeto](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Limitações funcionais

As operações a seguir não são permitidas em projetos agendados externamente.

### <a name="project-planning"></a>Planejamento do projeto

- **Copiar projeto** – Essa operação não tem suporte em projetos agendados externamente.
- **Mover projeto** – Alterações na data de início de um projeto não moverão o início de tarefas ou atribuições de recurso na WBS.
- **Atualizando o Gerente de Projetos** – As alterações no gerente de projeto na página principal do projeto não criarão automaticamente um novo membro de equipe do projeto até que o projeto seja convertido.
- **Atualizando o modelo de horário de trabalho do projeto** – As alterações no modelo de horário de trabalho do projeto não recalcularão o cronograma do projeto.
- **Contornos de atribuição de recurso** – A criação de atribuições de recurso não atualizará automaticamente o campo **mdyn\_ PlannedWork**. Esse campo é usado para armazenar contornos para o esforço de atribuição de recurso. Se mostrar o esforço em fases de tempo na grade de atribuição de recurso ou na grade de reconciliação de recurso, você deverá definir contornos de atribuição de recurso válidos. Esses contornos devem ser formatados corretamente para disparar o cálculo de contornos de custo e contornos de preço de venda. Recomendamos que você crie um projeto de teste agendado pelo Project for the Web e revise os dados associados para confirmar os requisitos e a formatação.

### <a name="resource-management"></a>Gerenciamento de recursos

- **Cumprimento de recurso genérico** – O Cumprimento de recurso genérico não tem suporte para projetos agendados externamente. As tentativas de atender aos requisitos abertos ativos criarão novos membros de equipe de projeto, mas não excluirá o membro genérico de equipe nem substituirá o membro genérico de equipe em quaisquer atribuições de recursos existentes.
- **Excluir membro de equipe** – A exclusão de um membro de equipe não excluirá automaticamente as atribuições de recurso.

### <a name="quoting-and-contracting"></a>Cotação e contratação

- **Importando detalhes da Linha de Cotação e da Linha de Contrato** – Quando os detalhes da linha de cotação ou contrato são importados de um projeto, o aplicativo terá sido testado para oferecer suporte a um máximo de apenas 500 tarefas na WBA, com base em um limite de 20 atribuições por tarefa.

### <a name="actuals-and-invoicing"></a>Dados reais e faturamento

- Embora não haja alterações nas validações existentes entre a WBS e as transações financeiras, é importante que você esteja em conformidade com o modelo de dados pronto para uso, para garantir que todas as transações de recebimento de dados sejam executadas conforme o esperado.
