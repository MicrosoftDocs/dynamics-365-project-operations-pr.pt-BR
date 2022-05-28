---
title: Atualizar do Project Service Automation para o Project Operations
description: Este tópico fornece uma visão geral do processo de atualização do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 3f31173197a3055cdc51567261dd91925fc9f430
ms.sourcegitcommit: bec7382d1319d59645e8e79fdb20df58617c97c6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2022
ms.locfileid: "8626706"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Atualizar do Project Service Automation para o Project Operations

Estamos felizes em anunciar a primeira de três fases para atualização do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Project Operations. Este tópico fornece uma visão geral para os clientes que estão embarcando nessa empolgante jornada. Os tópicos futuros incluirão considerações do desenvolvedor e detalhes sobre aprimoramentos de recursos. Eles não apenas fornecerão orientações para ajudar você a se preparar para a atualização para o Project Operations, como também explicarão o que você pode esperar após a atualização.

O programa de entrega da atualização será dividido em três fases.

| Entrega da atualização | Fase 1 (janeiro de 2022) | Fase 2 (ciclo de abril de 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Nenhuma dependência da estrutura de detalhamento de trabalho (WBS) para projetos | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| A WBS dentro dos limites atualmente suportados do Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS fora dos limites atualmente compatível com o Project Operations, incluindo suporte para o Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Processo de atualização concluído 

Como parte do processo de atualização, adicionamos logs de atualização ao mapa do site, para que os administradores possam diagnosticar falhas com mais facilidade. Além da nova interface, novas regras de validação serão adicionadas para garantir a integridade dos dados após uma atualização. As validações a seguir serão adicionadas ao processo de atualização.

| Validações | Fase 1 (janeiro de 2022) | Fase 2 (ciclo de abril de 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| A WBS será validada em relação a violações comuns de integridade de dados (por exemplo, atribuições de recursos associadas à mesma tarefa pai, mas com projetos pai diferentes). | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS será validada em relação aos [limites conhecidos do Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS será validada em relação aos limites conhecidos do Project Desktop Client. | |  | :heavy_check_mark: |
| Recursos reserváveis e calendários de projetos serão avaliados em relação a exceções comuns de regras de calendário incompatíveis. | | :heavy_check_mark: | :heavy_check_mark: |

Na fase 2, os clientes que atualizarem para o Project Operations terão seus projetos existentes atualizados para uma experiência somente leitura para planejamento de projetos. Nessa experiência somente leitura, a WBS completa ficará visível na grade de rastreamento. Para editar a WBS, os gerentes de projeto podem selecionar **Converter** na página principal **Projetos**. Um processo em segundo plano atualizará o projeto para que ele dê suporte à nova experiência de agendamento de projeto do Project for the Web. Esta fase é apropriada para clientes que possuem projetos que se enquadram nos [limites conhecidos do Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Na fase 3, será adicionado suporte para o Project Desktop Client, para benefício dos clientes que desejam continuar editando seus projetos por meio desse aplicativo. Contudo, se os projetos existentes forem convertidos para a nova experiência do Project for the Web, o acesso ao suplemento será desabilitado para cada projeto convertido.

## <a name="prerequisites"></a>Pré-requisitos

Para ser elegível para a atualização da fase 1, o cliente deve atender aos seguintes critérios:

- O ambiente de destino não deve conter nenhum registro na entidade **msdyn_projecttask**.
- As licenças válidas do Project Operations devem ser atribuídas a todos os usuários ativos do cliente. 
- O cliente deve validar o processo de atualização em pelo menos um ambiente de não produção que tenha um conjunto de dados representativo alinhado aos dados de produção.
- O ambiente de destino deve ser atualizado para a Versão de atualização 41 do Project Service Automation (3.10.62.162) ou posterior.

Os pré-requisitos para a fase 2 e fase 3 serão atualizados à medida que as datas de disponibilidade geral se aproximarem.

## <a name="licensing"></a>Licenciamento

Se você tiver licenças ativas para o Project Service Automation, poderá instalar e usar o Project Operations, que inclui todos os recursos do Project Service Automation e muito mais. Dessa forma, você poderá testar os recursos do Project Operations enquanto continua a usar o Project Service Automation em produção. Depois que suas licenças do Project Service Automation expirarem, você terá que fazer a transição para o Project Operations. Ao planejar essa transição, você deve considerar o fato de que a licença do Project Operations não inclui uma licença do Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Teste e refatoração de personalizações

Como ponto de partida, importe todas as personalizações para um ambiente limpo do Project Operations (lite) para confirmar que a importação foi bem-sucedida e que as operações de negócios se comportam conforme o esperado.

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

    > [!NOTE]
    > Dependendo da quantidade de dados no ambiente, a atualização pode levar várias horas. A equipe principal que está gerenciando a atualização deve planejar adequadamente e executar a atualização fora do horário comercial. Em alguns casos, se o volume de dados for grande, a atualização deve ser executada durante o fim de semana. A decisão sobre o agendamento deve ser baseada nos resultados dos testes em ambientes inferiores.

3. Atualize soluções personalizadas quando apropriado. Nesse momento, implante todas as alterações feitas em suas personalizações na seção [Teste e refatoração de personalizações](#testing-and-refactoring-customizations) deste tópico.
4. Acesse **Configurações** \> **Soluções** e selecione desinstalar a solução **Componentes Preteridos do Project Operations**.

    Esta solução é uma solução temporária que mantém o modelo de dados existente e os componentes presentes durante a atualização. Ao remover esta solução, você remove todos os campos e componentes que não são mais usados. Dessa forma, você ajuda a simplificar a interface e facilita a integração e a extensão.
    
### <a name="validate-common-scenarios"></a>Validar cenários comuns

Ao validar suas personalizações específicas, recomendamos que você também revise os processos empresariais com suporte nos aplicativos. Esses processos empresariais incluem, mas não se limitam à criação de entidades de vendas, como cotações e contratos, e à criação de projetos que incluem WBSs e aprovação de dados reais.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Principais mudanças entre o Project Service Automation e o Project Operations

Esta seção fornece um resumo das principais alterações que você pode esperar entre o Project Service Automation e o Project Operations.

### <a name="project-planning"></a>Planejamento do projeto

Os recursos de planejamento de projeto no Project Operations não dependem mais de uma combinação de lógica do cliente e lógica do servidor. Em vez disso, o Project Operations usa o Project for the Web como seu mecanismo de agendamento. Essa mudança nos recursos de agendamento permite vários novos recursos, como exibições de quadro e Gantt, planejamento baseado em recursos, [itens da lista de tarefas](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) e modos de agendamento do projeto. Os novos recursos de agendamento também são compatíveis com um rico conjunto de novas [interfaces de programação de aplicativos (APIs)](../project-management/schedule-api-preview.md). Essas APIs destinam-se a ajudar a garantir que nenhuma operação programática para criar, atualizar ou excluir uma entidade na WBS corrompa os campos calculados no agendamento.

## <a name="billing-and-pricing"></a>Cobrança e preço

Como parte dos investimentos contínuos no Project Operations, vários novos recursos estão disponíveis em Cobrança e preço. Veja alguns exemplos:

- [Registro do uso de material em projetos e tarefas de projeto](../material/material-usage-log.md)
- [Gerenciamento de subcontratos](../pro/subcontracting/managing-subcontracts-overview.md)
- [Contratos baseados em adiantamentos e honorários](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status e validações de contrato que não devem ser não excedidos](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Cobrança baseada em tarefas

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Quais tipos de implantação são atualmente compatíveis com atualização?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implantação do Project Operations Lite                        | Compatível               |
| Gerenciamento e Contabilidade do Projeto do Dynamics 365 Finance | Implantação do Project Operations Lite                        | Não compatível atualmente |
| Gerenciamento e contabilidade do projeto do Finance              | Project Operations para cenários baseados em recursos/itens sem estoque     | Não compatível atualmente |
| Gerenciamento e contabilidade do projeto do Finance              | Project Operations para cenários de pedido baseado em estoque/produção | Não compatível atualmente |
| Project Service Automation 3.x                         | Project Operations para cenários baseados em recursos/itens sem estoque     | Não compatível atualmente |
| Project for the Web (ambiente dedicado)            | Implantação do Project Operations Lite                        | Não compatível atualmente |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Como posso instalar o Project Operations antes que as ferramentas de atualização estejam disponíveis?

Há duas opções para instalar o Project Operations antes que as ferramentas de atualização estejam disponíveis:

- Provisione um novo ambiente.
- Implante o Project Operations separadamente em qualquer organização de vendas em que o Project Service Automation não esteja presente.

> [!NOTE]
> Se o Project Service Automation estiver instalado em uma organização, mas não tiver sido usado, ele poderá ser desinstalado. Depois de remover completamente o Project Service Automation, o Project Operations pode ser instalado na mesma organização.
