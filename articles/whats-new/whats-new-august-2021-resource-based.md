---
title: Novidades em agosto de 2021 – Project Operations para cenários baseados em recursos/sem estoque
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de agosto de 2021 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cd5a7e74fc90c6138cd672ff6109b59a8d2ae916
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323447"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em agosto de 2021 – Project Operations para cenários baseados em recursos/sem estoque

*Aplicável A: Project Operations para cenários baseados em recursos/sem estoque*

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

   - Project Operations na versão 4.13.0.152 do ambiente do Microsoft Dataverse.
   - Gerenciamento e contabilidade de projeto no ambiente do Dynamics 365 Finance versão 10.0.20.

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

- **Conjuntos de aprovações**: a aprovação define tempo do grupo, despesa ou solicitações de aprovação de uso de material em subconjuntos menores de operações. Esse agrupamento permite que as aprovações sejam processadas por projeto, em uma ordem específica, e permite novas tentativas e sequenciamento. O agrupamento das solicitações de aprovação aumenta a confiabilidade e a capacidade de rastreamento do processamento de aprovações para grandes volumes de aprovações. Para obter mais informações, veja [Conjuntos de aprovações](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

Não há atualizações para mapas de Gravação Dupla do Project Operations nesta versão. 

Para obter uma lista atual e versões dos mapas de gravação dupla do Project Operations, consulte [Versões de mapa de gravação dupla do Project Operations](../environment/resource-dual-write-maps.md).

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, conforme você atualiza sua solução do Project Operations Dataverse e a versão da solução do Finance. Certos recursos e funcionalidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Você pode ver a versão ativa do mapa na página **Gravação dupla** na coluna **Versão**. Ative uma nova versão do mapa selecionando **Versões do mapa da tabela**, selecionando a versão mais recente e salvando a versão selecionada. Se você personalizou um mapa de tabela pronto para usar, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) no guia de solução de problemas de Gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Cobrança e preço | 2295625 | O nome do marco deve ser copiado da agenda da fatura para o detalhe da linha da fatura. |
| Cobrança e preço | 2316323 | O desconto não deve ser editável em uma fatura pró-forma no Project Operations para cenários baseados em recursos. |
| Gerenciamento de oportunidades | 2338619 | As regras de negócios **Oportunidade** e **Cotação** devem ser chamadas apenas nas páginas. |
| Gerenciamento de recursos | 2316523 | O uso de **Enviar Solicitação** de um requisito de recurso com uma função anexada não deve exibir um erro. |
| Gerenciamento de recursos | 2326885 | A criação de um requisito de recurso por meio de um projeto não deve exibir um erro. |
| Horas e despesas | 2335584 | Fluxos de tarefas obsoletas na entrada de tempo. |
| Horas e despesas | 2336884 | O botão de entrada de tempo **Copiar Semana** deve funcionar para mais do que apenas o usuário atual. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Visão geral de gerenciamento e contabilidade de projeto no Dynamics 365 Finance

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Viagens e despesas | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Transações incorretas de fornecedores e transações de impostos sobre vendas são lançadas quando uma despesa é criada de uma transação de cartão de crédito. |
| Viagens e despesas | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | A liquidação errada são linhas criadas quando o diário de pagamento é gerado. |
| Viagens e despesas | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Transações incorretas de fornecedores e transações de impostos sobre vendas são lançadas quando uma despesa é criada de uma transação de cartão de crédito. |
| Viagens e despesas | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Excluir uma linha de despesas pode levar muito tempo. |
| Contabilidade de projeto | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | O sistema não dá suporte à configuração de sequenciamento numérico contínuo quando você lança uma estimativa depois de aplicar o KB 4619395. |
| Contabilidade de projeto | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | O lançamento da fatura do fornecedor pode falhar com a mensagem de erro "As transações no comprovante não têm saldo em 17/05/2021. (moeda contábil: 0,00 - moeda de relatório: 0,01)" |
