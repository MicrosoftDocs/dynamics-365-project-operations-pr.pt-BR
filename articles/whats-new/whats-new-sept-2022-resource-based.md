---
title: Novidades de setembro de 2022 – Project Operations para cenários baseados em recursos/não estocados
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de setembro de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634791"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de setembro de 2022 – Project Operations para cenários baseados em recursos/não estocados

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.46.0.60
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.29

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

| Área do recurso | Nome do recurso | Mais informações |
| --- | --- | --- |
| Gerenciamento de Oportunidades | **Revisão e Ativação de Cotações**<br>O Project Operations traz o suporte total do processo de vendas. As cotações do projeto podem ser ativadas para representar um estado em que a cotação é somente leitura e está sendo revisada. As cotações ativadas podem ser revisadas para criar novas cotações que tenham um número de revisão incrementado. As cotações ativadas de projeto ou revisões de cotação podem ser fechadas como Ganha ou Perdida. | [Ativar e revisar uma cotação de projeto](/dynamics365/project-operations/sales/activation-and-revision) |
| Cobrança e preço | **Padrão de preço agnóstico de fuso horário**<br>O Project Operations introduziu o conceito de uma data agnóstica de fuso horário em todos os dados reais do projeto. Um novo campo, **Data da transação**, agora está disponível em linhas do diário e reais e será usado para armazenar a data em que a transação ocorreu, mas sem converter essa data no Tempo Universal Coordenado. Essa data será usada para processos posteriores, como padronização de preço e criação de fatura. | <p>[Determinar as taxas de custo para estimativas baseadas em projeto e dados reais](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Determinar preços de vendas para estimativas e dados reais baseados em projetos](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Cobrança e preço | **Substituições de preço de data efetiva no Project Operations**<br>Substituições de preço com data de efetivação fornecem uma maneira de substituir ou alterar preços específicos na lista de preços. | [Substituições de preço com data de efetivação](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subcontratação | **Subcontratação e reconciliação de faturas de fornecedores**<br>Esse recurso permite que os clientes criem subcontratos para comprar tempo de recursos, categorias de despesas e materiais usados para o trabalho do projeto. Ele também permite que os clientes registrem, em aplicativos de finanças e operações, faturas de fornecedores que estarão disponíveis para gerentes de projeto no Dataverse para verificação. | <p>[Gerenciamento de subcontratos](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Criar faturas do fornecedor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Tempo e Despesa | **Aprovador Global**<br>Esse recurso permite o fornecedor independente de software (ISV) e a aprovação centralizada, independentemente do status do projeto ou do membro da equipe no projeto. | [Segurança e aprovações](/dynamics365/project-operations/approvals/approvals-security) |
| Gerenciamento de despesas | **Capacidade de lançar o passivo de despesas na moeda do fornecedor**<br>Esse recurso permite que os relatórios de despesas sejam lançados na moeda do fornecedor para o método de pagamento à vista. | [Capacidade de lançar o passivo de despesas na moeda do fornecedor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Aquisição de Projetos | **Pagamentos de fornecedor pagar quando pago**<br>Esse recurso permite que o recurso Pagar quando pago (PWP) seja usado com ambientes sem estoque do Project Operations. Permite que os pagamentos do fornecedor sejam bloqueados/retidos, com base nos prazos de retenção, até que o pagamento seja recebido do cliente. | [Pagamentos de fornecedor pagar quando pago](/dynamics365/project-operations/procurement/pay-when-paid) |
| Aquisição de Projetos | **Requisições de compra do Project**<br>Esse recurso permite que os usuários criem ordens de compra relacionadas ao projeto em entidades legais nas quais a integração do Project Operations no Dynamics 365 Customer Engagement está habilitada. As ordens de compra do projeto podem ser usadas para registrar a aquisição de material não estocado em relação ao projeto por pessoa do departamento de aquisições. As ordens de compra do projeto não serão sincronizadas com Dataverse. No entanto, você pode usar uma entidade virtual para exibir as linhas da ordem de compra do projeto no Dataverse para obter informações do gerente de projeto. O custo da fatura do fornecedor relacionado ao projeto é integrado à entidade Reais do projeto no Dataverse. O custo do projeto é registrado no livro auxiliar usando o diário de integração do Project Operations. | |
|Planejamento e acompanhamento de projeto|**Use APIs de agendamento do Project para realizar operações com entidades de Agendamento** </br> </br>A API de edição de contorno de atribuição de recursos permite que os desenvolvedores especifiquem programaticamente o esforço de um responsável pela tarefa em qualquer intervalo de data compatível para um planejamento de esforço em fases mais granular.|[Use APIs de agendamento do Project para realizar operações com entidades de Agendamento](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

A tabela a seguir mostra os mapas de gravação dupla que foram modificados ou adicionados na versão de setembro de 2022 do Project Operations.

| Mapa de entidade | Versão atualizada | Comentários |
| -------------- | ------------------- | ------------|
| Valores reais da integração do Project Operations (msdyn_actuals) | 1.0.0.15 | Este mapa oferece suporte ao processamento de reais de subcontratação com o Project Operations para cenários baseados em recursos. |
| Entidade de exportação de fatura de fornecedor do projeto de integração do Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Este mapa oferece suporte ao processamento de reais de subcontratação com o Project Operations para cenários baseados em recursos. |
| Entidade de exportação de linha de fatura de fornecedor do projeto de integração do Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Este mapa oferece suporte ao processamento de reais de subcontratação com o Project Operations para cenários baseados em recursos. |

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, à medida você atualizar a solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Cobrança e preço | 2754422 | As estimativas de materiais e despesas não fluem para o Finance quando os projetos são copiados no Dataverse. |
| Tempo e Despesa | 2787409 | Um aprovador inválido pode aprovar uma entrada de horas que não seja do projeto. |
| Gerenciamento de Oportunidades | 2788907 | Mensagem de erro atualizada na validação de exclusividade para linhas de pedido que incluem sinalizadores. |
| Tempo e Despesa | 2842253 | Tratamento de exceção nula para aprovação de tempo. |
| Cobrança e preço | 2844181 | A falha ao obter o ID de correlação bloqueia a criação da fatura. |
| Cobrança e preço | 2876628 | QLD, CLD - A resolução da lista de preços estimada deve usar campos de intervalo de datas herdados da lista de preços. |
| Subcontratação | 2893222 | Se nenhuma função for especificada para uma linha de subcontrato, deve ser possível selecionar essa linha em um membro da equipe para qualquer função. |

### <a name="project-management-and-accounting-in-finance"></a>Gerenciamento e contabilidade de projeto no Finance

Para obter informações sobre as correções de bug incluídas nesta atualização, entre no Microsoft Dynamics Lifecycle Services e consulte o [artigo da Base de Dados de Conhecimento](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Recursos ativados por padrão na futura versão

A tabela a seguir lista os recursos ativados por padrão na versão 10.0.30. A maioria dos recursos ativados automaticamente pode ser desativada no [Gerenciamento de recursos](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). No futuro, alguns recursos que foram ativados automaticamente poderão ser removidos do Gerenciamento de recursos e se tornarem obrigatórios. Essa mudança garante que os clientes estejam usando a funcionalidade atual, para que os aprimoramentos possam ser baseados na funcionalidade atual à medida que forem adicionados. Os recursos nunca serão ativados automaticamente em menos de um ano, a menos que sejam considerados essenciais.

| Nome do recurso | Habilitar data | Recurso adicionado | Estado do recurso | Módulo |
| --- | --- | --- |--- |--- |
| Ative a operação assíncrona quando o usuário precisar alternar entre as operações de sincronização e assíncrona | 21 de outubro de 2022 | 9 de abril de 2021 | Ativado por padrão | Gerenciamento de despesas |
| Avaliação da política de despesas para recebimentos necessários | 21 de outubro de 2022 | 20 de dezembro de 2021 | Ativado por padrão | Gerenciamento de despesas |
| Exibição de lista de relatórios de despesas criados por funcionários delegando | 21 de outubro de 2022 | 19 de fevereiro de 2020 | Ativado por padrão | Gerenciamento de despesas |
| Cálculo de totais de milhagem por ano fiscal | 21 de outubro de 2022 | 10 de maio de 2022 | Ativado por padrão | Gerenciamento de despesas |
