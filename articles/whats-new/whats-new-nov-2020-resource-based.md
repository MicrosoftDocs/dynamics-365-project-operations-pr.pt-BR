---
title: Novidades em novembro de 2020 – Project Operations para cenários baseados em recursos/sem estoque
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de novembro de 2020 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c7ec9360401bf214ae867769b0e48e545a6bad48
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367251"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em novembro de 2020 – Project Operations para cenários baseados em recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations no ambiente do CDS versão 4.4.0.70
- Gerenciamento e contabilidade de projeto no ambiente do Dynamics 365 Finance versão 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Atualizações do Project Operations para cenários baseados em recursos-sem estoque

### <a name="project-operations-on-cds"></a>Project Operations no CDS

| Área do recurso                 | Número de referência | Atualização de qualidade                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Gerenciamento de oportunidades       | 2036993          | A linha de estimativa e as linhas de contrato de atribuição de recursos são atualizadas nas cotações vencedoras quando o tipo de linha de cotação for **Todas as tarefas**.                                                 |
| Cobrança e preço          | 2070392          | Linhas de contrato do projeto na fatura aumentam sempre que **Atualizar transações de fatura** é selecionado.                                                                         |
| Planejamento do projeto             | 2043336          | Não foi possível excluir um registro de membro da equipe do projeto.                                                                                                                                  |
| Planejamento do projeto             | 2046013          | Comportamento inconsistente de colunas de tag de Estimativas durante a carga x ao alterar o tipo de fase de tempo.                                                                                   |
| Planejamento do projeto             | 2046647          | Os horários de início e término estão atrasados em uma hora quando os requisitos de recursos são gerados pelos membros da equipe do projeto.                                                                      |
| Planejamento do projeto             | 2053879          | (De acordo com o futuro lançamento do CDS) PublishUnassignedAssignments interrompe uma tentativa de salvar uma tarefa quando surge o erro, "O valor passado para ConditionOperator.In está vazio."                       |
| Planejamento do projeto             | 2055501          | Deixar **Data de Início do Projeto** em branco gera falha no agendamento.                                                                                                      |
| Planejamento do projeto             | 2066817          | Não é possível criar um recurso genérico usando o seletor de pessoas na guia **Tarefas**.                                                                                                   |
| Planejamento do projeto             | 2067034          | O botão **Exibir Detalhes** não está disponível na página **Detalhes da Tarefa**.                                                                                                       |
| Gerenciamento de recursos          | 2046667          | Os membros de equipe genéricos não são excluídos mesmo depois de todos os recursos terem sido preenchidos.                                                                                                    |
| Entrada rápida de tempo e despesa | 2047499          | O botão **Novo** na página de Entrada de Tempo abre a página **Nova Assinatura de E-mail**.                                                                                               |
| Entrada rápida de tempo e despesa | 2059859          | Um pop-up inesperado abre ao criar uma entrada de despesa.                                                                                                                         |
| Outra                        | 2044181          | (Desinstalando a ordem de compra) Ao tentar desinstalar as soluções principais do serviço do Projeto msdyn_ProjectServiceCore_Patch e msdyn, ocorre o erro "Registro indisponível".  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Visão geral de gerenciamento e contabilidade de projeto no Dynamics 365 Finance

| Área do recurso        | Número de referência | Atualização de qualidade                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reconhecimento de receita | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | A porcentagem concluída da estimativa do projeto está incorreta quando o contrato usa uma moeda estrangeira e a porcentagem do andamento do trabalho para concluir o método.                     |
| Reconhecimento de receita | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Não foi possível publicar estimativas com o método de conclusão **Custo real**.                                                                                                    |
| Reconhecimento de receita | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Falha na eliminação devido a um erro de desequilíbrio de voucher quando a moeda da empresa e a moeda da transação são diferentes.                                              |
| Gerenciamento de despesas  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Para usuários não administradores, os valores de pesquisa das colunas de linha de despesas, como **ID do projeto** e **Categoria de Despesa** não são exibidos corretamente na estrutura do conector de dados. |
| Gerenciamento de despesas  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | O padrão da propriedade de linha não está sendo exibido nas Categorias de despesas.                                                                                                         |
| Gerenciamento de despesas  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | A integração de despesas deve incluir a propriedade da linha do relatório de despesas.                                                                                             |
| Faturamento           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Não é possível publicar as propostas de fatura do projeto devido a uma mensagem de erro que informa que a combinação de FD não foi validada.                                                    |
| Faturamento           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Não é possível exibir as transações na página de detalhes da **fatura**.                                                                                                              |
| Faturamento           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | As linhas da proposta de fatura podem ser excluídas.                                                                                                                                  |
| Contabilidade de projeto  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Os itens do menu **Previsão** não estão visíveis na página de lista **Projetos**.                                                                                                   |
| Contabilidade de projeto  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Não é possível abrir **Demonstrativo de projeto**   > **Transações e previsão**.                                                                                                       |
| Contabilidade de projeto  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Ajustar contabilidade** não está habilitado para transações de projeto faturadas.                                                                                                  |
| Contabilidade de projeto  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Os detalhes contábeis não estão incluídos na tabela **ProjCDSActualsImport** quando o diário de **Integração** é lançado.                                                  |
| Contabilidade de projeto  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | A entrada da Previsão do projeto é duplicada ao remover e uma atribuição de recurso é adicionada novamente.                                                                            |
| Contabilidade de projeto  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Selecionar um link de ID do Projeto não abre a URL do link profundo do CDS.                                                                                                         |
| Contabilidade de projeto  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Não é possível atualizar a data de início em uma tarefa no CDS.                                                                                                                           |
| Contabilidade de projeto  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Ao ativar o recurso, Múltiplas linhas de contrato não é possível sem a integração do CDS.                                                                                   |

### <a name="regulatory-updates"></a>Atualizações regulatórias
Para obter informações sobre atualizações regulatórias do Finance and Operations, consulte [Atualizações regulatórias](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Você também pode entrar no LCS e exibir as atualizações regulatórias planejadas usando a Ferramenta de pesquisa de problemas. A pesquisa de problemas permite pesquisar por país, tipo de recurso e versão.
