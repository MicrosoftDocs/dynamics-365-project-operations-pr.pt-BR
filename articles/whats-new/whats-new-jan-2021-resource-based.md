---
title: Novidades em janeiro de 2021 – Project Operations para cenários baseados em recursos/sem estoque
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de janeiro de 2021 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24a6f3b49b9c67b7c2d97461ab0f23a9a704dbc7
ms.sourcegitcommit: ef7d498bf80b0bcc1245dc42f30c410c31f891bb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/13/2021
ms.locfileid: "4958885"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em janeiro de 2021 – Project Operations para cenários baseados em recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_


Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations no ambiente do Dataverse versão 4.6.0.154
  - Gerenciamento e contabilidade de projeto no ambiente do Dynamics 365 Finance versão 10.0.16

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área do Recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| **Implantação e configuração** | 2106818 | A renomeação de recurso da web que estava causando problemas relacionados à personalização de páginas foi corrigida. |
| **Cobrança e preço** | 2091908 | A visibilidade das opções **Bloquear precificação** e **Usar Precificação Atual** na página **Fatura** quando o Project Operations é instalado com o Dynamics 365 Field Service foi corrigida. |
| **Cobrança e preço** | 2103058 | **Totais do Projeto** foi atualizado para lidar com valores nulos do custo real em uma tarefa. |
| **Cobrança e preço** | 2116100 | Mensagens de erro aprimoradas usadas com a funcionalidade **Entradas Corretas em Dados Reais**. |
| **Cobrança e preço** | 2116129 | Melhor visibilidade de estimativas de despesas na guia **Estimativas** na página **Projetos**. |
| **Cobrança e preço** | 2119112 | A agregação fixa de vendas reais e custo real ao usar taxas de câmbio diferentes foi corrigida. |
| **Cobrança e preço** | 2134705 | O erro "Não é possível ler a propriedade **getResourceString** de indefinido" ao abrir a página **Fatura** e instalar o Field Service foi corrigido. |
| **Gerenciamento de Oportunidades** | 2022195 | A grade de cobrança baseada em tarefas na página **Projeto** inclui um ícone indicando que há um contrato ou linha de cotação vinculada a essa tarefa. |
| **Gerenciamento de Oportunidades** | 2029135 | O erro do processo empresarial que ocorre quando um usuário tenta abrir uma linha da fatura em uma fatura confirmada que possui um valor de adiantamento faturado foi corrigido. |
| **Gerenciamento de Oportunidades** | 2040713 | O erro de script que ocorre ao criar uma fatura de um contrato e instalar o Field Service foi corrigido. |
| **Planejamento e acompanhamento de projeto** | 2090202 | As regras de negócios marcadas que não são mais usadas como **Preterida**. |
| **Tempo e Despesa** | 2091249 | Os controles foram reduzidos para que os usuários não possam alterar a tarefa em uma entrada de tempo enviada ou aprovada. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Visão geral de gerenciamento e contabilidade de projeto no Dynamics 365 Finance

| **Área do Recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| **Gerenciamento e contabilidade de projeto** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Valor de contrato incorreto na página **Por conta** para um projeto de preço fixo com várias fontes de financiamento. |
| **Gerenciamento e contabilidade de projeto** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | O espaço reservado **Invoiceproposal.PSAnfRefProjId** não está exibindo a ID do Projeto para o fluxo de trabalho **Examinar propostas de fatura de projeto**. |
| **Gerenciamento e contabilidade de projeto** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | A data de desconto à vista errada é usada ao lançar propostas de fatura do projeto. |
| **Gerenciamento e contabilidade de projeto** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Remover e ler a atribuições de recursos no Project Operations dobra as entradas de previsão do projeto no Finance. |
| **Gerenciamento e contabilidade de projeto** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | No Project Operations, não é possível criar estimativas de projeto no Dataverse sem ter uma linha de contrato no projeto. |
| **Gerenciamento e contabilidade de projeto** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | A dimensão financeira em uma transação de despesas do projeto não está sincronizada com o comprovante relacionado e a distribuição contábil do relatório de despesas quando os custos são lançados no Saldo. |
| **Gerenciamento e contabilidade de projeto** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | O filtro de **Status da fatura** em transações de projeto lançadas para projetos de preço fixo não funciona. |
| **Gerenciamento e contabilidade de projeto** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | A eliminação da estimativa reversa não está funcionando na seção **Periódico**. |
| **Gerenciamento e contabilidade de projeto** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | As linhas de proposta da fatura podem ser excluídas no Project Operations se estiverem integradas ao Dataverse. |
| **Gerenciamento e contabilidade de projeto** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Evitar habilitar o recurso de múltiplas linhas de contrato sem a integração do Dataverse. |
| **Gerenciamento e contabilidade de projeto** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Quando o faturamento por conta for igual a lucros e perdas, a receita faturada é listada como zero na página Estimativas. |
| **Gerenciamento e contabilidade de projeto** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | As correções de faturas não estão funcionando em ambientes integrados. |
| **Gerenciamento e contabilidade de projeto** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Ao lançar o WIP – valor de venda no faturamento de projeto intercompanhia, a conta errada é selecionada. |
| **Gerenciamento e contabilidade de projeto** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | No Project Operations, as dependências em tarefas de estimativa no Dataverse não podem ser atualizadas. |
| **Gerenciamento e contabilidade de projeto** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | A exclusão repetida de diários de integração do Project Operations no Finance leva à perda de dados. |
| **Gerenciamento e contabilidade de projeto** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | O seguinte erro ocorre ao lançar uma proposta de fatura do projeto "A transação não coincide com a moeda de relatório quando a fatura antecipada deduzida é adicionada novamente". |
| **Gerenciamento e contabilidade de projeto** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | A ID do projeto incorreto é incluída nas deduções depois que o contrato do projeto padrão é atualizado no Project Operations. |
| **Gerenciamento e contabilidade de projeto** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | A estimativa e o reconhecimento da receita não podem ser concluídos quando o Project Operations está habilitado. |
| **Gerenciamento e contabilidade de projeto** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | No Project Operations, remover um projeto de um contrato não redefine o projeto padrão no contrato. |
| **Gerenciamento e contabilidade de projeto** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | No Project Operations, em uma fatura intercompanhia, as linhas de despesas incorretas aparecem na lista **Adicionar linha**. |
| **Viagens e Despesas** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | As linhas de despesas não podem ser lançadas porque a configuração de hora está ausente na linha de contrato. |
| **Viagens e Despesas** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Quando a validação do projeto/da categoria é obrigatória, as categorias de despesas associadas ao projeto não estão visíveis no relatório de despesas. |
| **Viagens e Despesas** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | O saldo de adiantamento de dinheiro não é atualizado quando um relatório de despesas é lançado por linha. |
| **Viagens e Despesas** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | O trabalho **Atualizar informações de pagamento** falha após reverter liquidações em que uma fatura foi liquidada com duas ou mais transações de pagamento. |
| **Viagens e Despesas** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Há um problema com o cálculo de redução de refeição do último dia para a categoria de despesas diárias. |
| **Viagens e Despesas** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | O relatório do **Tipo de despesa por funcionário** não mostra despesas discriminadas se a primeira conexão do usuário foi no idioma es-MX. |
| **Viagens e Despesas** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | O pagamento de fornecedor para uma fatura de relatório de despesas está usando a conta resumo errada para o lançamento da liquidação. |
| **Viagens e Despesas** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Quando um relatório de despesa é lançado com **Permitir agrupamento de transações com base na conta de pagamento de compensação** e **Correção da Data Contábil no lançamento** ativados mostra que as datas contábeis não estão agrupadas na tabela **Distribuição contábil**, o que afeta os registros de impostos. |
| **Viagens e Despesas** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | O mapeamento da subcategoria de despesa é removido quando a caixa de seleção Usar em despesa é limpo e selecionado novamente. |
| **Viagens e Despesas** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Um relatório de despesas intercompanhia não poderá ser criado se a ID do projeto for adicionada no nível do cabeçalho. |
| **Viagens e Despesas** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Há um problema com pagamentos de despesas quando o valor da despesa é maior do que o valor do adiantamento em dinheiro. |
| **Viagens e Despesas** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | O campo **ID do projeto** em um relatório de despesas intercompanhia estarão vazias se a função do usuário for atribuída a uma organização específica. |
| **Viagens e Despesas** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | A categoria de despesas é bloqueada ao adicionar uma nova linha de despesas. |
| **Viagens e Despesas** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | A especificação de linhas do relatório de despesas que já estão divididas resulta em um comprovante de Contas a pagar/Contabilidade incompleto lançado. Devido à duplicação de **TRVEXPTRANS.SOURCEDOCUMENTLINE**, o Gerenciador de Fontes Contábeis também está corrompido. |
| **Viagens e Despesas** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | O índice adicionado na tabela **TRVREQUISITIONLINE** para a qual o cliente tem duplicatas, resulta em um erro durante a atualização. |
| **Viagens e Despesas** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | No Project Operations, o tempo com tarefas intercompanhia no Dataverse não pode ser criado ou aprovado. |

## <a name="regulatory-updates"></a>Atualizações regulatórias

Para obter informações sobre atualizações regulatórias do Finance and Operations, consulte [Atualizações regulatórias](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Você também pode entrar no LCS e exibir as atualizações regulatórias planejadas usando a Ferramenta de pesquisa de problemas. A pesquisa de problemas permite pesquisar por país, tipo de recurso e versão.
