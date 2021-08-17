---
title: Novidades em abril de 2021 – Project Operations para cenários baseados em recurso/sem estoque
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de abril de 2021 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dbce86e88f8315ac4a4957c1128b5619d5328bdbbe27793e161f8f2691899481
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008122"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em abril de 2021 – Project Operations para cenários baseados em recurso/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations no ambiente do Dataverse versão 4.9.0.221
- Gerenciamento e contabilidade de projeto no ambiente do Dynamics 365 Finance versão 10.0.17

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

- Materiais sem estoque para projetos. Os principais recursos incluem:
  - Estimativa e determinação de preços de materiais não estocados durante o ciclo de vendas de um projeto. Para obter mais informações, consulte [Configurar taxas de custo e de vendas para produtos do catálogo – lite](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Acompanhamento do uso de materiais não estocados durante a entrega do projeto. Para obter mais informações, consulte [Registre o uso de material em projetos e tarefas de projeto](../material/material-usage-log.md).
  - O faturamento usou custos de materiais não estocados. Para obter mais informações, consulte [Gerenciar lista de pendências de cobrança](../proforma-invoicing/manage-billing-backlog.md).
  - Para obter informações sobre como configurar esse recurso, consulte [Configurar materiais sem estoque e faturas de fornecedores pendentes](../procurement/configure-materials-nonstocked.md)
- Cobrança baseada em tarefas: Adicionada a capacidade de associar tarefas do projeto às linhas do contrato do projeto, sujeitando-as ao mesmo método de cobrança, frequência de fatura e clientes que os da linha do contrato. Essa associação garante faturamento, contabilidade, estimativa de receita e reconhecimento precisos para trabalhar de acordo com essa configuração nas tarefas do projeto.
- Novas APIs no Dynamics 365 Dataverse permitem operações de criação, atualização e exclusão com **Entidades de agendamento**. Para obter mais informações, consulte [Use APIs de programação para realizar operações com entidades de programação](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

A lista a seguir mostra os mapas de gravação dupla que foram modificados ou adicionados na versão do Project Operations de abril de 2021.

| **Mapa de entidade** | **Versão atualizada** | **Comentários** |
| --- | --- | --- |
| Valores reais da integração do Project Operations (msdyn\_actuals) | 1.0.0.14 | Mapa modificado para sincronizar os valores reais do projeto de materiais. |
| Entidade de integração do Project Operations para estimativas de despesas (msdyn\_estimateslines) | 1.0.0.2 | Adicionada a sincronização de linha de contrato do projeto para aplicativos do Finance and Operations para o suporte ao faturamento baseado em tarefas. |
| Entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments) | 1.0.0.5 | Adicionada a sincronização de linha de contrato do projeto para aplicativos do Finance and Operations para o suporte ao faturamento baseado em tarefas. |
| Tabela de integração do Project Operations para estimativas de material (msdyn\_estimateslines) | 1.0.0.0 | Novo mapa de tabela para sincronizar estimativas de material do Dataverse com os aplicativos do Finance and Operations. |
| Entidade de exportação de fatura de fornecedor do projeto de integração do Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Novo mapa de tabela para sincronizar cabeçalhos de faturas de fornecedor dos aplicativos do Finance and Operations com o Dataverse. |
| Entidade de exportação de linha de fatura de fornecedor do projeto de integração do Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Novo mapa de tabela para sincronizar linhas de faturas de fornecedor dos aplicativos do Finance and Operations com o Dataverse. |

Você deve sempre executar a versão mais recente do mapa em seu ambiente e habilitar todos os mapas de tabela relacionados conforme atualiza sua solução do Dataverse do Project Operations e a versão da solução Finance and Operations. Certos recursos e funcionalidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível ver a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Você pode ativar uma nova versão do mapa selecionando **Versões do mapa de tabela**, selecionando a versão mais recente e salvando a versão selecionada. Se você personalizou um mapa de tabela pronto para usar, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você tiver algum problema para iniciar o mapa, siga as instruções na [Problema de colunas de tabela ausentes nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations no Dynamics 365 Dataverse

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Cobrança e preço | 2124532 | O botão **Fatura Correta** é exibido em uma fatura pro forma quando o valor de retenção ou o valor de retenção aplicado está presente na fatura original. O botão é exibido apenas para ambientes com Finance versão 10.0.19 ou superior. |
| Cobrança e preço | 2224568 | Adicionada lógica para habilitar personalizações que envolvem a chamada do plug-in de confirmação de fatura. |
| Cobrança e preço | 2101098 | Melhorou a lógica de campos padrão para fatura pro forma: **Endereço para Cobrança**, **Nome para Cobrança** e **Condições de Pagamento** agora é o padrão do registro de cliente do contrato de projeto correspondente. |
| Cobrança e preço | 2021413 | Atualizados os campos **Custo Real** e **Vendas** na entidade **Tarefa** para incluir valores de vendas de despesas faturadas e não faturadas em tarefas. |
| Cobrança e preço | 2182110 | Ao copiar um contrato de projeto, a ID da linha do contrato é regenerada no contrato do projeto de destino para garantir que seja exclusiva. |
| Gerenciamento de Oportunidades | 2186741 | Adicionadas validações para garantir que o campo **Origem** e **Tipo de Transação** não possam ser atualizados em detalhes da linha de cotação existente. |
| Gerenciamento de Oportunidades | 2191353 | As etapas não devem ser criadas em uma linha de contrato de tempo e material. |
| Gerenciamento de Oportunidades | 2216956 | Problemas corrigidos com **Atualizar preços**. |
| Planejamento e acompanhamento | 2182979 | A função de cópia do projeto foi aprimorada para garantir que as linhas de estimativa de despesas sejam copiadas do projeto original. |
| Planejamento e acompanhamento | 2184144 | A função de cópia do projeto foi aprimorada para garantir que o nome da posição do recurso seja copiado do projeto original. |
| Planejamento e acompanhamento | 2184799 | Cópia do projeto: controle mais rígido para garantir que a data de início estimada não possa ser alterada durante o andamento da cópia. |
| Planejamento e acompanhamento | 2185134 | Cópia do projeto: a data de início estimada do projeto de destino é definida como a data de hoje. |
| Planejamento e acompanhamento | 2196373 | Cópia do projeto: verifique se os registros do gerente de projeto e do membro da equipe não estão duplicados na equipe do projeto. |
| Planejamento e acompanhamento | 2211833 | Cópia do projeto: as atribuições de recursos são copiadas da tarefa do projeto de origem no projeto de destino. |
| Planejamento e acompanhamento | 2186541 | Problemas corrigidos na grade **Estimativas** ao agrupar por recurso. |
| Planejamento e acompanhamento | 2166906 | A categoria de transação de uma tarefa deve ser copiada na entidade **Atribuição de Recursos**. |
| Gerenciamento de Recursos | 2125362 | Corrigidos problemas com a criação de um membro da equipe genérico usando um método de alocação baseado em horas. |
| Tempo e Despesa | 2113603 | Corrigido o problema relacionado à personalização com a remoção de atributos da página **Entrada de Tempo**. O sistema agora verifica se o atributo existe na página antes de acessá-los usando um script. |
| Tempo e Despesa | 2204377 | As planilhas de horas copiadas devem aparecer automaticamente quando você seleciona **Copiar Semana** durante a entrada de tempo. |
| Tempo e Despesa | 2209059 | O campo **Status** pode ser editado para entradas de tempo do Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Visão geral de gerenciamento e contabilidade de projeto no Dynamics 365 Finance

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Gerenciamento e contabilidade de projeto | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | A eliminação da estimativa reversa não está funcionando na seção **Periódico**.  |
| Gerenciamento e contabilidade de projeto | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | O recurso **Ajuste contábil** cria um problema com contas contábeis que têm **Não permitir entrada manual** selecionado. |
| Gerenciamento e contabilidade de projeto | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Adicionada lógica de negócios para processar faturas de correção, incluindo valor de retenção ou valor de retenção aplicado. |
| Gerenciamento e contabilidade de projeto | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | O lançamento do WIP - valor de venda no faturamento de projeto intercompanhia escolhe uma conta inesperada. |
| Gerenciamento e contabilidade de projeto | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Ao trabalhar com honorários em Project Operations, alterar o projeto padrão em um contrato após o faturamento dos pré-pagamentos causará problemas com as deduções recebidas. |
| Gerenciamento e contabilidade de projeto | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Em Project Operations, remover um projeto de um contrato deve redefinir o projeto padrão do contrato, se necessário. |
| Gerenciamento e contabilidade de projeto | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Em Project Operations, as linhas de despesas erradas aparecem na lista **Adicionar linha** na fatura intercompanhia. |
| Gerenciamento e contabilidade de projeto | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Em Project Operations, a página **Contrato de Compra** não está visível nas entidades legais do Finance que estão integradas ao Project Operations. |
| Gerenciamento e contabilidade de projeto | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Devido a um erro de integração do Dataverse, você não pode converter uma cotação em ganha no Project Operations. |
| Gerenciamento e contabilidade de projeto | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** pode definir o endereço da fatura da fonte de financiamento de um cliente diferente.  |
| Gerenciamento e contabilidade de projeto | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Em Project Operations, nenhuma dimensão é selecionada quando você cria uma fatura de postagem para uma transação. |
| Viagem e despesa | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | O saldo do adiantamento em dinheiro não será atualizado para um relatório de despesas se for aprovado e lançado linha por linha. |
| Viagens e Despesas | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Os impostos para relatórios detalhados de despesas intercompanhia não são calculados corretamente. |
| Viagens e Despesas | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Campos adicionais relacionados a projetos são exibidos na página **Relatórios de despesas intercompanhia**. |
| Viagens e Despesas | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Uma mensagem de erro incorreta ocorre nos recibos do cabeçalho dos relatórios de despesas. |
| Viagens e Despesas | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Um relatório de despesas será lançado incorretamente em um cenário intercompanhia se o imposto for lançado na entidade legal de destino. |
| Viagens e Despesas | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | As datas de envio dos relatórios não são impressas em relatórios de despesas aprovados. |
| Viagens e Despesas | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Os campos **Data de Aprovação** e **Data Rejeitada** não são preenchidos depois que uma despesa é aprovada. |
| Viagens e Despesas | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Uma requisição de viagem criada para um trabalhador pode ser usada para o relatório de despesas de outro trabalhador. |
| Viagens e Despesas | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | As categorias de despesas são bloqueadas ao adicionar uma nova linha de despesas. |
| Viagens e Despesas | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | A especificação de itens de linhas de um relatório de despesas já divididas resulta em um lançamento incompleto do comprovante de Contas a Pagar\Razão e quebra o Explorador de Fonte de Contabilidade porque **TRVEXPTRANS.SOURCEDOCUMENTLINE** está duplicado. |
| Viagens e Despesas | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | A política de requisição de viagem não está funcionando conforme o esperado. |
| Viagens e Despesas | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | O nome da conta do fornecedor não está sendo exibido nas transações de projeto publicadas para relatórios de despesas. |
| Viagens e Despesas | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Em Project Operations, você não pode aprovar tempo com uma tarefa para um projeto intercompanhia. |
| Viagens e Despesas | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | A categoria de devolução de adiantamento em dinheiro não está atualizando saldos de adiantamento em dinheiro quando lançados. |
| Viagens e Despesas | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | O preço de venda é calculado incorretamente em relatórios de despesas que foram criados em uma moeda estrangeira usando transações de cartão de crédito importadas e estão associados a um projeto. |
| Viagens e Despesas | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Revertida a entidade de dados **TrvRequisitionLine** e o índice exclusivo associado. |
| Viagens e Despesas | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Adicionada instrumentação à geração **SOURCEDOCUMENTLINE**. |
| Viagens e Despesas | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | O diário-razão auxiliar errado será mostrado em um cenário intercompanhia se o imposto for lançado na entidade legal de destino. |
| Viagens e Despesas | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Em Project Operations, as estimativas de despesas não são excluídas do Finance quando são excluídas do Dataverse. |
| Viagens e Despesas | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Quando uma categoria de despesa não é uma categoria de projeto, as dimensões financeiras selecionadas na página **Despesa** não são copiadas no relatório de despesas. |
