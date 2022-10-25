---
title: Atualizar do Project Service Automation para o Project Operations
description: Este artigo fornece uma visão geral do processo de atualização do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9686961"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Atualizar do Project Service Automation para o Project Operations

Estamos felizes em anunciar a segunda de três fases para atualização do Microsoft Dynamics 365 Project Service Automation para o Microsoft Dynamics 365 Project Operations. Este artigo fornece uma visão geral para clientes que estão embarcando nessa empolgante jornada. 

O programa de entrega da atualização será dividido em três fases.

| Entrega da atualização | Fase 1 (janeiro de 2022) | Fase 2 (novembro de 2022) | Fase 3 (ciclo de abril de 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nenhuma dependência da estrutura de detalhamento de trabalho (WBS) para projetos | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Uma WBS dentro dos limites atualmente compatíveis com o Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| Uma WBS fora dos limites atualmente compatíveis com o Project Operations, incluindo suporte para o Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Processo de atualização concluído 

Como parte do processo de atualização, adicionamos logs de atualização ao mapa do site para permitir que os administradores possam diagnosticar falhas com mais facilidade. Além da nova interface, novas regras de validação serão adicionadas para garantir a integridade dos dados após uma atualização. As validações a seguir serão adicionadas ao processo de atualização.

| Validações | Fase 1 (janeiro de 2022) | Fase 2 (novembro de 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| A WBS será validada em relação a violações comuns de integridade de dados (por exemplo, atribuições de recursos associadas à mesma tarefa pai, mas com projetos pai diferentes). | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS será validada em relação aos [limites conhecidos do Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS será validada em relação aos limites conhecidos do Project Desktop Client. | |  | :heavy_check_mark: |
| Recursos reserváveis e calendários de projetos serão avaliados em relação a exceções comuns de regras de calendário incompatíveis. | | :heavy_check_mark: | :heavy_check_mark: |

Na fase 2, os clientes que atualizarem para o Project Operations terão seus projetos existentes atualizados para uma experiência somente leitura para planejamento de projetos. Nessa experiência somente leitura, a WBS completa ficará visível na grade de rastreamento. Para editar a WBS, os gerentes de projeto podem selecionar [**Converter**](/PSA-Upgrade-Project-Conversion.md) na página principal do projeto. Em seguida, um processo em segundo plano atualizará o projeto para que ele dê suporte à nova experiência de agendamento de projeto do Project for the Web. Esta fase é apropriada para clientes que possuem projetos que se enquadram nos [limites conhecidos do Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Na fase 3, será adicionado suporte para o Project Desktop Client, para benefício dos clientes que desejam continuar editando seus projetos por meio desse aplicativo. Contudo, se os projetos existentes forem convertidos para a nova experiência do Project for the Web, o acesso ao suplemento será desabilitado para cada projeto convertido.

## <a name="prerequisites"></a>Pré-requisitos

Para ser elegível para a atualização da Fase 1, você deverá atender aos seguintes critérios:

- O ambiente de destino não deve conter nenhum registro na entidade **msdyn_projecttask**.
- As licenças válidas do Project Operations devem ser atribuídas a todos os usuários ativos. 
- Você deve validar o processo de atualização em pelo menos um ambiente de não produção que contenha um conjunto de dados representativo alinhado ao seu ambiente de produção.
- O ambiente de destino deve ser atualizado para a Versão de Atualização 37 do Project Service Automation (V3.10.58.120) ou posterior.

Para ser elegível para a atualização da Fase 2, você deverá atender aos seguintes critérios:

- As licenças válidas do Project Operations devem ser atribuídas a todos os usuários ativos. 
- Você deve validar o processo de atualização em pelo menos um ambiente de não produção que contenha um conjunto de dados representativo alinhado ao seu ambiente de produção.
- O ambiente de destino deve ser atualizado para a Versão de Atualização 37 do Project Service Automation (V3.10.58.120) ou posterior.
- Os ambientes com tarefas (msdyn_projecttask) só terão suporte se o número total de tarefas por projeto for 500 ou menos.

Os pré-requisitos para a Fase 3 serão atualizados à medida que a data de disponibilidade geral se aproximar.

## <a name="licensing"></a>Licenciamento

Se você tiver licenças ativas para o Project Service Automation, poderá instalar e usar o Project Operations, que inclui todos os recursos do Project Service Automation e muito mais. Em seguida, você poderá testar as funcionalidades do Project Operations em um ambiente separado enquanto continua a usar o Project Service Automation em produção. Depois que suas licenças do Project Service Automation expirarem, você terá que fazer a transição para o Project Operations. Ao planejar essa transição, você deve considerar o fato de que a licença do Project Operations não inclui uma licença do Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Teste e refatoração de personalizações

Como ponto de partida, importe todas as personalizações para um ambiente limpo do Project Operations (Lite) para confirmar que a importação foi bem-sucedida e que as operações de negócios se comportam conforme o esperado.

Aqui estão algumas coisas a serem observadas:

- A importação pode falhar devido a dependências ausentes. Em outras palavras, as personalizações fazem referência a campos ou outros componentes que foram removidos no Project Operations. Nesse caso, remova essas dependências do ambiente de desenvolvimento.
- Se suas soluções gerenciadas e não gerenciadas incluem componentes que não são personalizados, remova esses componentes da solução. Por exemplo, ao personalizar a entidade **Projeto**, adicione apenas o cabeçalho da entidade à solução. Não adicione todos os campos. Se você adicionou todos os subcomponentes anteriormente, talvez seja necessário criar manualmente uma solução e adicionar componentes relevantes a ela.
- Formulários e visualizações podem não aparecer como esperado. Em algumas circunstâncias, se você personalizou qualquer um dos formulários ou exibições prontos para uso, as personalizações podem impedir que novas atualizações no Project Operations entrem em vigor. Para identificar esses problemas, recomendamos que você faça uma revisão lado a lado de uma instalação limpa do Project Operations e uma instalação do Project Operations que inclua suas personalizações. Compare os formulários mais usados em sua empresa para confirmar se sua versão do formulário ainda faz sentido e não está faltando algo na versão limpa do formulário. Faça o mesmo tipo de revisão lado a lado para todas as exibições que você personalizou.
- A lógica de negócios pode falhar no tempo de execução. Como as referências a campos em seus plug-ins não são validadas no momento da importação, a lógica de negócios pode falhar em razão de referências a campos que não existem mais e você pode receber uma mensagem de erro semelhante ao exemplo a seguir: "A entidade 'Project' não contém atributo com Nome = 'msdyn_plannedhours' e NameMapping = 'Logical'." Nesse caso, modifique suas personalizações para que usem os novos campos. Se você usar classes de proxy geradas automaticamente e referências de tipo forte em sua lógica de plug-in, considere regenerar esses proxies a partir de uma instalação limpa. Dessa forma, você pode identificar facilmente todos os locais onde seus plug-ins dependem de campos obsoletos.

Depois de atualizar suas personalizações para importar o Project Operations de forma limpa, vá para as próximas etapas.

## <a name="end-to-end-testing-in-development-environments"></a>Testes de ponta a ponta em ambientes de desenvolvimento

### <a name="initiate-upgrade"></a>Iniciar a atualização 

1. No centro de administração da Power Platform, localize e selecione seu ambiente. Em seguida, nos aplicativos, localize e selecione **Dynamics 365 Project Operations**.
2. Selecione **Instalar** para iniciar a atualização. O centro de administração da Power Platform apresentará essa instalação como uma nova instalação. Contudo, a presença de uma versão anterior do Project Service Automation será detectada e a instalação existente será atualizada.

    Após a conclusão da atualização, o ambiente deve mostrar que o Project Operations está instalado e que o Project Service Automation não está instalado.

    Dependendo da quantidade de dados no ambiente, a atualização pode levar várias horas. A equipe principal que está gerenciando a atualização deve planejar adequadamente e executar a atualização fora do horário comercial. Em alguns casos, se o volume de dados for grande, a atualização deve ser executada durante o fim de semana. A decisão sobre o agendamento deve ser baseada nos resultados dos testes em ambientes inferiores.

3. Atualize soluções personalizadas quando apropriado. Nesse momento, implante todas as alterações feitas em suas personalizações na seção [Teste e refatoração de personalizações](#testing-and-refactoring-customizations) deste artigo.
4. Acesse **Configurações** \> **Soluções** e selecione desinstalar a solução **Componentes Preteridos do Project Operations**.

    Esta solução é uma solução temporária que mantém o modelo de dados existente e os componentes presentes durante a atualização. Ao remover esta solução, você remove todos os campos e componentes que não são mais usados. Dessa forma, você ajuda a simplificar a interface e facilita a integração e a extensão.
    
### <a name="upgrade-to-project-operations-lite"></a>Atualização para o Project Operations Lite

As etapas a seguir descrevem o processo de atualização e o registro em log de erros associado:

1. **Verificação da Versão PSA:** para instalar o Project Operations, você deve ter a versão V3.10.58.120 ou superior.
1. **Pré-validação:** quando um administrador inicia uma atualização, o sistema executa uma operação de pré-validação em cada entidade que é essencial para a solução Project Operations. Esta etapa verifica se todas as referências de entidades são válidas e garante que os dados relacionados à WBS estejam dentro dos limites publicados do Project for the Web.
1. **Atualização de metadados:** após a pré-validação bem-sucedida, o sistema inicia as alterações no esquema e cria uma solução de componentes obsoletos. Você poderá remover essa solução obsoleta depois de concluir toda a refatoração necessária de personalizações. Esta etapa é a parte mais longa do processo de atualização e pode levar até quatro horas para ser concluída.
1. **Atualização de dados:** depois que todas as alterações de esquema necessárias forem concluídas na etapa de atualização de metadados, seus dados serão migrados para o novo esquema e todos os padrões e recálculos necessários serão feitos.
1. **Atualização do mecanismo da agenda de projeto:** após a atualização de dados bem-sucedida, a guia **Agenda** na página principal será renomeada para **Tarefas**. Quando um usuário selecionar essa guia após a atualização, ele será direcionado para navegar até a grade de rastreamento para exibir uma versão somente leitura da WBS. Para editar a WBS, ele deverá iniciar o [processo de conversão](/PSA-Upgrade-Project-Conversion.md) da agenda. Todos os projetos sem uma WBS pré-existente podem usar a nova experiência de agendamento diretamente, sem conversão.
 
### <a name="validate-common-scenarios"></a>Validar cenários comuns

Ao validar suas personalizações específicas, recomendamos que você também revise os processos empresariais com suporte nos aplicativos. Esses processos empresariais incluem, mas não se limitam à criação de entidades de vendas, como cotações e contratos, e à criação de projetos que incluem WBSs e aprovação de dados reais.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Principais mudanças entre o Project Service Automation e o Project Operations

Esta seção fornece um resumo das principais alterações que você pode esperar entre o Project Service Automation e o Project Operations.

### <a name="project-planning"></a>Planejamento do projeto

Os recursos de planejamento de projeto no Project Operations não dependem mais de uma combinação de lógica do cliente e lógica do servidor. Em vez disso, o Project Operations usa o Project for the Web como seu mecanismo de agendamento. Essa mudança nos recursos de agendamento permite vários novos recursos, como exibições de quadro e Gantt, planejamento baseado em recursos, [itens da lista de tarefas](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) e modos de agendamento do projeto. Os novos recursos de agendamento também são compatíveis com um rico conjunto de novas [interfaces de programação de aplicativos (APIs)](../project-management/schedule-api-preview.md). Essas APIs destinam-se a ajudar a garantir que nenhuma operação programática para criar, atualizar ou excluir uma entidade na WBS corrompa os campos calculados no agendamento.

### <a name="billing-and-pricing"></a>Cobrança e preço

Como parte dos investimentos contínuos no Project Operations, vários novos recursos estão disponíveis em Cobrança e preço. Veja alguns exemplos:

- [Registro do uso de material em projetos e tarefas de projeto](../material/material-usage-log.md)
- [Gerenciamento de subcontratos](../pro/subcontracting/managing-subcontracts-overview.md)
- [Contratos baseados em adiantamentos e honorários](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status e validações de contrato que não devem ser não excedidos](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Cobrança baseada em tarefas

### <a name="resource-management"></a>Gerenciamento de recursos

O Project Operations fornece suporte opcional para o painel do URS (Universal Resource Scheduling) e o assistente de agendamento. Essa nova experiência se tornará obrigatória no ciclo de abril de 2023.

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Quais tipos de implantação são atualmente compatíveis com atualização?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implantação do Project Operations Lite                        | Compatível               |
| Gerenciamento e Contabilidade do Projeto do Dynamics 365 Finance | Implantação do Project Operations Lite                        | Não compatível atualmente |
| Gerenciamento e contabilidade do projeto do Finance              | Project Operations para cenários baseados em recursos/itens sem estoque     | Não compatível atualmente |
| Project Service Automation 3.x                         | Project Operations para cenários baseados em recursos/itens sem estoque     | Não compatível atualmente |
| Project for the Web (ambiente dedicado)            | Implantação do Project Operations Lite                        | Não compatível atualmente |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Como posso instalar o Project Operations antes que as ferramentas de atualização estejam disponíveis?

Há duas opções para instalar o Project Operations antes que as ferramentas de atualização estejam disponíveis:

- Provisione um novo ambiente.
- Implante o Project Operations separadamente em qualquer organização de vendas em que o Project Service Automation não esteja presente.

Se o Project Service Automation estiver instalado em uma organização, mas não tiver sido usado, ele poderá ser desinstalado. Depois de remover completamente o Project Service Automation, o Project Operations pode ser instalado na mesma organização.
