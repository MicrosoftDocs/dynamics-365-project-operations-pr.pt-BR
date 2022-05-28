---
title: Novidades de setembro de 2021 – Project Operations para cenários baseados em recursos/não estocados
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de setembro de 2021 do Project Operations para cenários baseados em recursos/não estocados.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 06f23630ef0205394f376e5bb93a29ae8a9eab15
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582880"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de setembro de 2021 – Project Operations para cenários baseados em recursos/não estocados

*Aplicável A: Project Operations para cenários baseados em recursos/sem estoque*

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

   - Project Operations na versão 4.14.0.99 do ambiente do Microsoft Dataverse.
   - Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

Não há atualizações para mapas de gravação dupla do Project Operations nesta versão. Para obter uma lista atual e versões dos mapas de gravação dupla do Project Operations, consulte [Versões de mapa de gravação dupla do Project Operations](../environment/resource-dual-write-maps.md).

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, conforme você atualiza sua solução do Project Operations Dataverse e a versão da solução do Finance. Certos recursos e funcionalidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Você pode ver a versão ativa do mapa na página **Gravação dupla** na coluna **Versão**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para usar, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Horas e despesas | 1811407 | Ajustado o direito de acesso de Aprovador de Projeto para aprovações de entradas de despesas. |
| Horas e despesas | 1811438 | Ajustado o direito de acesso de Aprovador de Projeto para o cancelamento de aprovações de entradas de tempo. |
| Horas e despesas | 2370126 | Atualizados os ícones **Tarefa do Projeto** e **Função** na entidade **Entrada de Tempo**. |
| Horas e despesas | 2379879 | Corrigido a função **Copiar Semana** na entrada de tempo ao usar o Dynamics 365 para telefone. |
| Cobrança e preço | 2371906 | O valor total da fatura proforma não deve ser ajustável no Project Operations para implantações baseadas em recursos. |
| Cobrança e preço | 2385802 | Corrigido o erro que ocorre com horas reais negativas quando os totais do projeto são atualizados. |
| Cobrança e preço | 2389675 | Aprimorado o comportamento de confirmação de fatura proforma. A entidade de trabalhos de longa execução deve levar em consideração a atividade necessária para gravar os resultados de confirmação para a contabilidade. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gerenciamento e contabilidade de projetos no Dynamics 365 Finance

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Viagens e despesas | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Os valores em transações de fornecedores e os impostos lançados de uma despesa criada a partir de uma transação de cartão de crédito estão incorretos. |
| Viagens e despesas | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | As linhas de liquidação incorretas são criadas quando o diário de pagamento é gerado. |
| Viagens e despesas | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Os valores em transações de impostos lançados de uma despesa criada a partir de uma transação de cartão de crédito estão incorretos. |
| Viagens e despesas | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Excluir uma linha de despesas pode levar muito tempo. |
| Contabilidade de projeto | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Depois de aplicar o 4619395 da base de dados de conhecimento, não há suporte à alteração da sequência numérica para **Contínua** e quando você lança uma estimativa, ocorre o seguinte erro: "O sistema não oferece suporte à configuração 'contínua' da sequência numérica Proj_X." |
| Contabilidade de projeto | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Pode haver falha no lançamento de uma fatura de fornecedor com a seguinte mensagem de erro, "As transações no comprovante não têm saldo de acordo com 17/5/2021. (moeda contábil: 0,00 – moeda de relatório: 0,01)." |
