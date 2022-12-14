---
title: Gerenciar oportunidades de projeto
description: Este artigo fornece informações sobre como trabalhar com oportunidades relacionadas a projetos.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 56eba38476dd5b49f0043eee5d411d51f9bf56b8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825262"
---
# <a name="manage-project-opportunities"></a>Gerenciar oportunidades de projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As empresas baseadas em projetos normalmente têm operações de entrega espalhadas por vários países e regiões geográficas. O custo da execução e entrega do projeto pode variar com base na região geográfica ou divisão que gerencia a entrega. Por sua vez, isso pode impactar as margens de lucro do negócio. A entrega de serviços baseados em projetos costuma envolver grandes quantidades de tempo de recursos humanos, despesas consideráveis com viagens, custos de material e outras despesas.

As oportunidades baseadas em projeto no Dynamics 365 Project Operations são projetadas com extensões para o Dynamics 365 Sales. O artigo fornece detalhes sobre os diferentes campos e a lógica de negócios incluídos na funcionalidade adicional necessária para que as empresas baseadas em projeto gerenciem as oportunidades baseadas em projeto.

## <a name="view-all-project-based-opportunities"></a>Exibir todas as oportunidades baseadas em projetos

Uma lista de todas as oportunidades baseadas em projetos pode ser vista na página de listagem **Oportunidade**. 

1. Vá para **Vendas** > **Oportunidades**.
2. Use o **Seletor de exibição** para selecionar outras exibições filtradas das oportunidades. Você pode criar suas próprias exibições com critérios de filtro personalizados para configurar essas exibições e opções de navegação.

Oportunidades de projeto podem ser criadas ou excluídas desta página de lista ou da página de detalhes.

## <a name="business-process-flow-for-project-based-deals"></a>Fluxo de processo empresarial para negócios baseados em projetos

Os seguintes fluxos de processo empresariais são compatíveis com negócios baseados em projetos no Project Operations:

- Processo empresarial Cliente Potencial até a Oportunidade
- Processo de vendas de oportunidade

### <a name="lead-to-opportunity-business-process"></a>Processo empresarial Cliente Potencial até a oportunidade 
O processo empresarial cliente potencial até a oportunidade oferece suporte aos seguintes estágios:

| Estágio | Entidade mapeada | Funcionalidade |
| --- | --- | --- |
| Qualificar | Lead | Qualificar o cliente potencial para criar uma conta, contato e/ou oportunidade. |
| Desenvolver | Oportunidade | Desenvolver a oportunidade para adicionar mais informações sobre o trabalho envolvido, os principais participantes e a concorrência. |
| Propor | Oportunidade | Desenvolver a proposta e obter aprovação da equipe de revisão interna. |
| Fechar | Oportunidade | Vencer a oportunidade para fechar o negócio. |

### <a name="opportunity-sales-process"></a>Processo de vendas de oportunidade
O processo de vendas da oportunidade no Project Operations é uma extensão do fluxo de negócios do processo de vendas da oportunidade na aplicação Sales. Este processo de negócios foi predefinido para dar suporte aos seguintes estágios em uma oportunidade baseada em projeto.

| Estágio | Entidade mapeada | Funcionalidade |
| --- | --- | --- |
| Qualificar | Oportunidade | Qualificar o cliente potencial para criar uma conta, contato e/ou oportunidade. |
| Propor | Cotação | Desenvolver a proposta usando cotações do projeto e obter aprovação da equipe de revisão interna. |
| Contrato | Contrato do Projeto | Ganhe a cotação para criar o contrato e iniciar a execução e entrega do projeto. |
| Fechar | Contrato do Projeto | Termine o trabalho com êxito e feche o contrato do projeto. |

> [!NOTE]
> Se o seu negócio baseado em projeto começou com um cliente potencial, o processo empresarial Cliente Potencial para Oportunidade terá precedência.
>
> Se o seu negócio baseado em projeto começou com uma Oportunidade, o processo Vendas de oportunidade terá precedência.

Você pode editar o fluxo do processo empresarial do produto ou criar seus próprios fluxos do processo empresarial para rastrear o processo de vendas conforme necessário. Para obter mais informações sobre o fluxo do processo empresarial, consulte [Visão geral de fluxos do processo empresarial](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
