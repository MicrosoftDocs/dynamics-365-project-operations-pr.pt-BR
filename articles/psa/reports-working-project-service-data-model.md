---
title: Trabalhar com o modelo de dados do Project Service Automation
description: Este artigo fornece informações sobre como trabalhar com o modelo de dados.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 67932eea78048c09f5f836d1330f412466622c6a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926670"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Trabalhar com o modelo de dados do Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


O Dynamics 365 Project Service Automation estende outras entidades de aplicativos e introduz suas próprias entidades no modelo de dados do Common Data Service. Este artigo descreve algumas das entidades encontradas em cenários típicos de criação de relatórios no PSA.

## <a name="reporting-on-opportunities"></a>Relatar oportunidades

O Project Service Automation estende a entidade **Oportunidade** do Dynamics 365 Sales adicionando campos que possibilitam cenários baseados em projetos. Esses campos são identificados por um nome de esquema prefixado com **msdyn\_**. Um novo campo que é importante para relatar oportunidades do PSA é **Tipo de Ordem**. Um valor de **Baseado em Trabalho** neste campo indica que a oportunidade é do PSA. Outros campos que foram adicionados à entidade incluem **Organização Contratante**, que captura a organização que está mantendo a oportunidade, e **Gerente de Contas**, que captura o nome do gerente de contas responsável pela oportunidade.

A entidade **Linha de Oportunidade** também inclui campos relacionados ao Project Service. **Método de Cobrança** indica se a linha de oportunidade deve ser cobrada com base em tempo e material ou preço fixo, e **Projeto** captura o nome do projeto que está sustentando a oportunidade. Outros campos que podem ser relatados capturam custos e valores de orçamentos de clientes para o item de linha.

## <a name="reporting-on-quotes"></a>Relatar cotações

O PSA estende a entidade **Cotação** do Sales adicionando campos relacionados a projetos. **Tipo de Ordem** distingue cotações do PSA de cotações de outra procedência. Um valor de **Baseado em Trabalho** neste campo indica que a cotação é do PSA. Outros campos que podem ser relevantes para relatar cotações do PSA incluem campos de valor, como **Custos Passíveis de Cobrança**, **Custos Não Passíveis de Cobrança**, **Margem Bruta**, **Estimativas** e **Orçamento**. Outros campos úteis indicam se a cotação é rentável, se será concluída no prazo e se atende às expectativas de orçamento do cliente.

O PSA também estende a entidade **Linha de Cotação** do Sales. Um campo que o PSA adiciona é **Método de Cobrança**, que indica como a linha de cotação será cobrada (tempo e material ou preço fixo). Outros campos que foram adicionados à entidade capturam o projeto relacionado que está sustentando a linha de cotação, o faturamento, o custo e o orçamento.

Além disso, o PSA adiciona novas entidades relacionadas à cotação ao modelo de dados do Dynamics 365. Veja alguns exemplos:

- **Detalhes da Linha de Cotação** – Esta entidade contém os detalhes das estimativas de projeto da linha de cotação. Ela tem dois registros para cada linha de cotação. Um registro armazena o custo e os detalhes do custo da linha de cotação, o outro armazena o valor de vendas e os detalhes de vendas da linha de cotação.
- **Agenda de Faturas da Linha de Cotação** – Esta entidade contém a agenda de cobrança da linha de cotação. Essa agenda é gerada com base na frequência de faturamento que é atribuída à linha de cotação.
- **Etapa da Linha de Cotação** – Esta entidade contém as etapas de cobrança para linhas de cotação com preço fixo.
- **Detalhamento de Análise da Linha de Cotação** – Esta entidade contém detalhes financeiros da linha de cotação. Esses detalhes podem ser úteis para relatar vendas cotadas e valores de custo estimados por várias dimensões.

Outras entidades que o PSA adiciona a cotações são **Lista de Preços do Projeto da Linha de Cotação**, **Categoria de Recurso da Linha de Cotação** e **Categoria de Transação da Linha de Cotação**.

![Diagrama mostrando cotação, linha de cotação e relacionamentos do projeto.](media/PS-Reporting-image2.png "Diagrama mostrando cotação, linha de cotação e relacionamentos do projeto")

## <a name="reporting-on-project-contracts"></a>Relatar contratos de projetos

O PSA estende a entidade **Ordem** do Sales que é usada quando contratos de projetos são registrados. Ele adiciona um novo campo importante, **Tipo de Ordem**, que identifica o contrato como um contrato de projeto do PSA em vez de uma ordem de venda. Um valor de **Baseado em Trabalho** neste campo indica que a ordem é um contrato de projeto do PSA. Outros novos campos adicionados à entidade **Ordem** capturam detalhes sobre custos, status do contrato do PSA e a organização proprietária do contrato.

O PSA também estende a entidade **Linha de Ordem de Venda**. Entre os campos que ele adiciona estão campos que capturam o método de cobrança (tempo e material ou preço fixo), valores de orçamentos de clientes e o projeto subjacente.

Além disso, o PSA adiciona novas entidades que foram criadas para contratos de projetos. Veja alguns exemplos:

- **Detalhes da Linha de Contrato do Projeto** – Esta entidade contém os detalhes no nível da linha que são acumulados para o valor da linha de contrato. Eles podem ser tão minuciosos quanto os itens de linha que são gerados com base em uma agenda de projeto no nível da tarefa.
- **Agenda de Faturas da Linha de Contrato** – Esta entidade contém a agenda de cobrança que é gerada com base na frequência de faturas atribuída à linha de contrato.
- **Etapas do Contrato** – Esta entidade contém as etapas de cobrança para linhas de contrato que possuem um prazo de cobrança com preço fixo.

Outras entidades que o PSA adiciona a contratos são **Lista de Preços de Projeto da Linha de Contrato do Projeto**, **Categoria de Recurso da Linha de Contrato do Projeto** e **Categoria de Transação da Linha de Contrato do Projeto**.

![Diagrama mostrando ordem, linha da ordem e relacionamentos do projeto.](media/PS-Reporting-image3.png "Diagrama mostrando ordem, linha da ordem e relacionamentos do projeto")

## <a name="reporting-on-projects"></a>Relatar projetos

A entidade **Projetos** e suas entidades relacionadas são exclusivas ao PSA. **Projeto** é a entidade de nível superior que é usada para capturar o lado do trabalho e do custo das operações. Veja aqui uma lista das entidades relacionadas:

- **Membro da equipe do projeto** – Esta entidade contém detalhes sobre os recursos reserváveis atribuídos ao projeto. Esses recursos podem ser recursos reserváveis genéricos ou recursos reserváveis nomeados que são fornecidos pelo gerente do projeto ou gerados com base na agenda do projeto.
- **Tarefa do Projeto** – Esta entidade contém as tarefas que compõem o plano ou a agenda do projeto.
- **Atribuição de Recurso** – Esta entidade contém a atribuição de tarefas para o recurso reservável.
- **Requisito de Recurso** – Esta entidade contém os requisitos para quaisquer membros genéricos da equipe de recurso.
- **Estimativa** e **Linha de estimativa** – Estas entidades têm um relacionamento cabeçalho/linha e contêm estimativas de despesas para o projeto. As estimativas de tarefas são armazenadas na entidade **Estimativa de Recursos**.

![Diagrama mostrando requisito de recurso e relacionamentos do projeto.](media/PS-Reporting-image4.png "Diagrama mostrando requisito de recurso e relacionamentos do projeto")

## <a name="reporting-on-resources"></a>Relatar recursos

Os recursos de projeto usam as entidades de **Recurso Reservável** do Universal Resource Scheduling (URS) compartilhados com outros aplicativos, como o Microsoft Dynamics 365 Field Service. Veja uma lista das entidades que talvez você precise usar ao relatar recursos de projeto:

- **Recurso Reservável** – Esta entidade representa o usuário, contato, recurso genérico, conta, grupo ou equipamento que é usado na equipe do projeto.
- **Características de Recursos Reserváveis** – Esta entidade inclui as habilidades, certificações ou formação acadêmica do recurso. As características podem ter valores de classificação que são definidos pelo modelo de classificação.
- **Categoria de Recurso Reservável** – Esta entidade representa a função do recurso reservável.
- **Reservas de Recursos Reserváveis** – Esta entidade representa o tempo reservado em projetos para o recurso. Cada reserva tem uma entidade de cabeçalho e entidades de linha, e cada linha tem um status que representa o status da reserva.

![Diagrama mostrando relacionamentos de características de recursos reserváveis.](media/PS-Reporting-image5.png "Diagrama mostrando relacionamentos de características de recursos reserváveis")

## <a name="reporting-on-actual-transactions"></a>Relatar transações reais

Quando você aprova uma folha de ponto ou despesa, ou fatura um contrato no PSA, a transação comercial é capturada na entidade **Real**. Essa entidade pode servir de base para quase todos os relatórios relacionados a finanças no PSA. A entidade **Real** captura o custo e as transações de vendas do evento comercial. Ela também captura muitos atributos relevantes.

Ao trabalhar com a entidade **Real**, é importante compreender quais transações são registradas na entidade e quando elas são registradas. Este é o fluxo típico de trabalho com entradas de hora (o fluxo para entradas de despesa é semelhante):

1. Quando a entrada de hora é salva, nenhum registro é criado na entidade **Real**.
2. Quando a entrada de hora é enviada, nenhum registro é criado na entidade **Real**.
3. Quando a entrada de hora é aprovada, um registro é criado na entidade **Real** e um segundo registro também pode ser criado. O primeiro registro armazena o custo da entrada de hora. O segundo registro armazena o valor das vendas não cobradas da entrada de hora. O segundo registro depende da existência de um cliente, uma cotação ou uma linha de contrato atribuída ao projeto.

    | Data do documento | Tipo de transação | Classe da transação | Cliente         | Contrato   | Recurso     | Função do recurso | Tipo de cobrança | Quantidade | Preço unitário | Quantidade |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 3/2/18        | Custo             | Time              | Alpine Ski House | CRM da Alpine | Vitória Cavalcante | Gerente de projetos   | Passível de cobrança   | 8.0      | 50.00      | 400.00 |
    | 3/2/18        | Vendas não cobradas   | Time              | Alpine Ski House | CRM da Alpine | Vitória Cavalcante | Gerente de projetos   | Passível de cobrança   | 8.0      | 100.00     | 800.00 |

    Esses dois registros são separados, mas relacionados. Eles não são débitos nem créditos.

4. Se um contrato estiver associado ao projeto, quando a entrada de hora for faturada, mais dois registros serão criados na entidade **Real**. Primeiro, é criado um valor negativo para o registro de vendas não cobradas. Esse registro essencialmente reverte a venda não cobrada. Depois, é criada uma transação para a venda cobrada. Novamente, esses registros são separados, mas relacionados, não são débitos nem créditos.

    | Data do documento | Tipo de transação | Classe da transação | Cliente         | Contrato   | Recurso     | Função do recurso | Tipo de cobrança | Quantidade | Preço unitário | Quantidade   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 4/2/18        | Vendas não cobradas   | Time              | Alpine Ski House | CRM da Alpine | Vitória Cavalcante | Gerente de projetos   | Passível de cobrança   | - 8.0    | 100.00     | - 800.00 |
    | 4/2/18        | Vendas cobradas     | Time              | Alpine Ski House | CRM da Alpine | Vitória Cavalcante | Gerente de projetos   | Passível de cobrança   | 8.0      | 100.00     | 800.00   |

A entidade **Origem da Transação** registra a origem do registro **Real**, e a entidade **Conexão da Transação** registra os registros relacionados do registro **Real**. Além disso, o registro **Real** contém referências a projeto, contrato de projeto (ordem), recurso reservável e cliente.

![Diagrama mostrando a conexão da transação, a origem e os relacionamentos reais.](media/PS-Reporting-image6.png "Diagrama mostrando a conexão da transação, a origem e os relacionamentos reais")


[!INCLUDE[footer-include](../includes/footer-banner.md)]
