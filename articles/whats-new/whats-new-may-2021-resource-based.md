---
title: Novidades em maio de 2021 – Project Operations para cenários baseados em recurso/sem estoque
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de maio de 2021 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cc5e8104702951fd787d02407d26671e46d44f0c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029975"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em maio de 2021 – Project Operations para cenários baseados em recurso/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este artigo se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations na versão 4.10.0.186 do ambiente do Dynamics 365 Dataverse
- Gerenciamento e contabilidade de projetos em ambientes de aplicativos de finanças e operações versão 10.0.18

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

- [Modos de agendamento](../project-management/scheduling-modes.md): os gerentes de projeto podem definir se um projeto deve ser gerenciado usando o modo de programação de duração fixa, trabalho fixo ou unidades fixas.
- [Configurar a milhagem usando níveis de taxa de milhagem](../expense/set-up-mileage.md): atualizar níveis de taxa de milhagem para relatórios de despesas de funcionários.

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

A lista a seguir mostra os mapas de gravação dupla que foram modificados ou adicionados na versão do Project Operations de maio de 2021.

| Mapa de entidade | Versão atualizada | Comentários |
| --- | --- | --- |
| Fonte de financiamento do projeto (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Sincronizando os termos de pagamento do cliente do contrato do projeto. |
| Proposta de fatura do projeto V2 (faturas) | 1.0.0.3 | Sincronizando os termos de pagamento da fatura proforma. |
| Entidade de exportação de linha de fatura de fornecedor do projeto de integração do Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Atualizações de qualidade |
| Projetos V2 (msdyn\_projects) | 1.0.0.2 | Atualizações de qualidade |

Sempre execute a versão mais recente do mapa no seu ambiente e habilite todos os mapas de tabela relacionados, à medida que atualizar a solução do Dataverse do Project Operations e a versão da solução dos aplicativos de finanças e operações. Certos recursos e funcionalidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível ver a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para usar, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você tiver algum problema para iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de Gravação Dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Cobrança e preço | 2227635 | Os valores nos campos padrão **Grupo de unidades** e **Unidade** do produto na grade **Estimativas de Materiais**. |
| Cobrança e preço | 2234127 | O campo **ID da Tarefa** agora se integra corretamente aos valores reais do projeto Dataverse quando uma fatura do fornecedor é lançada. |
| Cobrança e preço | 2235564 | Salvar a linha do diário garante que a moeda exibida na entrada da linha do diário corresponda à moeda padrão da linha após a gravação. |
| Cobrança e preço | 2246671 | Tornar uma transação não debitável durante o faturamento reverte o registro de vendas não faturadas original e cria um novo registro de vendas não faturado como não debitável. |
| Cobrança e preço | 2264042 | A correção de fatura válida não deve ser bloqueada se houver um detalhe de correção de fatura que não seja válido no ambiente. |
| Cobrança e preço | 2146367 | O mapeamento de dupla gravação do cabeçalho da fatura do projeto foi estendido para incluir os termos de pagamento. |
|   Gerenciamento de oportunidades | 2086888 | Não adicione funções e categorias desativadas antes de copiar uma cotação para funções e categorias cobráveis de uma cotação recém-copiada. |
|   Gerenciamento de oportunidades | 2234376 | Os campos somente leitura estão esmaecidos na grade **Estimativas de Materiais**. |
|   Gerenciamento de oportunidades | 2238337 | Uma cotação com base em um contato pode ser salva, mesmo se não estiver associada a uma lista de preços do projeto. |
|   Gerenciamento de oportunidades | 2239810 | Fechar uma cotação como perdida também fecha o projeto associado e cancela todas as reservas. |
| Planejamento e acompanhamento de projeto | 2099559 | Adicionadas validações adicionais para a integridade do sistema antes da grade **Tarefas de projeto** ser aberta. |
| Planejamento e acompanhamento de projeto | 2178987 | Corrigido um erro transitório que ocorre ao selecionar **Próximo Estágio** na página **Projeto**. |
| Gerenciamento de Recursos | 2224817 | A funcionalidade para estender os padrões de reservas para o status de reserva correto. |
| Entrada de hora | 2202476 | A página **Entrada de Hora** agora usa o controle da grade de reação e corrige problemas como o desalinhamento da grade. |
| Entrada de hora | 2223377 | A entrada de tempo está oculta da seção **Relacionado** na página **Recurso Reservável** para evitar confusão com a usabilidade. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gerenciamento e contabilidade de projetos no Dynamics 365 Finance

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gerenciamento e contabilidade de projeto | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations para cenários baseados em recursos: não é possível converter uma cotação ganha devido a um erro de integração. |
| Gerenciamento e contabilidade de projeto | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: um erro ocorre quando você tenta associar uma linha de contrato a uma ID de projeto devido à verificação de linhas de contrato e tipos de transação sobrepostos. |
| Gerenciamento e contabilidade de projeto | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | O **ProjCDSProjectContractEntity** define o endereço da fatura da fonte de financiamento de um cliente diferente. |
| Viagens e Despesas | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Pode ocorrer um erro de postagem relacionado à configuração de quilometragem. |
| Viagens e Despesas | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | A funcionalidade **Divisão para pessoal** não está funcionando para transações de despesas em moeda estrangeira. |
| Viagens e Despesas | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Os valores do menu suspenso de categoria de despesas estão mostrando categorias incorretas para delegados, independentemente de serem um recurso. |
| Viagens e Despesas | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Não é possível salvar um relatório de despesas intercompanhia devido a um erro de **Validação de Recurso/Categoria**. |
| Viagens e Despesas | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | O cálculo incorreto da taxa de quilometragem no lançamento do relatório de despesas dividiu as linhas. |
| Viagens e Despesas | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Não é possível lançar um relatório de despesas intercompanhia quando o imposto estiver incluído e o tipo de conta de compensação no método de pagamento for **Trabalhador**. |
| Viagens e Despesas | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | A entidade de dados **TrvRequisitionLine** e o índice exclusivo revertido estão associados. |
| Viagens e Despesas | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | O relatório de despesas suporta a criação e atualização da linha do documento de origem. |
| Viagens e Despesas | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Um diário-razão auxiliar incorreto será mostrado em um cenário intercompanhia, se o imposto for lançado na entidade legal de destino. |
| Viagens e Despesas | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: a estimativa de despesa não é excluída do Finance quando é excluída do Dataverse. |
| Viagens e Despesas | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Quando a categoria de despesa não é uma categoria de projeto, as dimensões financeiras selecionadas na página **Despesas** não são copiadas no relatório de despesas. |
