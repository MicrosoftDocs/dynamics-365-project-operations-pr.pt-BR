---
title: Novidades de setembro de 2022 – implantação do Project Operations lite
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de setembro de 2022 da implantação lite do Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634838"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Novidades de setembro de 2022 – implantação do Project Operations lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.46.0.60

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

| Área do recurso | Nome do recurso | Mais informações |
| --- | --- | --- |
| Gerenciamento de Oportunidades | **Revisão e Ativação de Cotações**<br>O Project Operations traz o suporte total do processo de vendas. As cotações do projeto podem ser ativadas para representar um estado em que a cotação é somente leitura e está sendo revisada. As cotações ativadas podem ser revisadas para criar novas cotações que tenham um número de revisão incrementado. As cotações ativadas de projeto ou revisões de cotação podem ser fechadas como Ganha ou Perdida. | [Ativar e revisar uma cotação de projeto](/dynamics365/project-operations/sales/activation-and-revision) |
| Cobrança e preço | **Padrão de preço agnóstico de fuso horário**<br>O Project Operations introduziu o conceito de uma data agnóstica de fuso horário em todos os dados reais do projeto. Um novo campo, **Data da transação**, agora está disponível em linhas do diário e reais e será usado para armazenar a data em que a transação ocorreu, mas sem converter essa data no Tempo Universal Coordenado. Essa data será usada para processos posteriores, como padronização de preço e criação de fatura. | <p>[Determinar as taxas de custo para estimativas baseadas em projeto e dados reais](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Determinar preços de vendas para estimativas e dados reais baseados em projetos](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Cobrança e preço | **Substituições de preço de data efetiva no Project Operations**<br>Substituições de preço com data de efetivação fornecem uma maneira de substituir ou alterar preços específicos na lista de preços. | [Substituições de preço com data de efetivação](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Tempo e Despesa | **Aprovador Global**<br>Esse recurso permite o fornecedor independente de software (ISV) e a aprovação centralizada, independentemente do status do projeto ou do membro da equipe no projeto. | [Segurança e aprovações](/dynamics365/project-operations/approvals/approvals-security) |
|Planejamento e acompanhamento de projeto|**Use APIs de agendamento do Project para realizar operações com entidades de Agendamento** </br> </br>A API de edição de contorno de atribuição de recursos permite que os desenvolvedores especifiquem programaticamente o esforço de um responsável pela tarefa em qualquer intervalo de data compatível para um planejamento de esforço em fases mais granular.|[Use APIs de agendamento do Project para realizar operações com entidades de Agendamento](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Atualizações de qualidade

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Cobrança e preço | 2754422 | As estimativas de materiais e despesas não fluem para o Dynamics 365 Finance quando os projetos são copiados no Dataverse. |
| Tempo e Despesa | 2787409 | Um aprovador inválido pode aprovar uma entrada de horas que não seja do projeto. |
| Gerenciamento de Oportunidades | 2788907 | Mensagem de erro atualizada na validação de exclusividade para linhas de pedido que incluem sinalizadores. |
| Tempo e Despesa | 2842253 | Tratamento de exceção nula para aprovação de tempo. |
| Cobrança e preço | 2844181 | A falha ao obter o ID de correlação bloqueia a criação da fatura. |
| Cobrança e preço | 2876628 | QLD, CLD - A resolução da lista de preços estimada deve usar campos de intervalo de datas herdados da lista de preços. |
| Subcontratação | 2893222 | Se nenhuma função for especificada para uma linha de subcontrato, deve ser possível selecionar essa linha em um membro da equipe para qualquer função. |
