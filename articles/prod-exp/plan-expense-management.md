---
title: Configurar gerenciamento de despesas
description: Este artigo descreve as considerações e as decisões que precisam ser tomadas durante o processo de planejamento antes de configurar o Gerenciamento de despesas no Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eca4362b0ff5d37b131e1d96e311aa48ac20397618314936944ba66e458dbdc2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007447"
---
# <a name="configure-expense-management"></a>Configurar gerenciamento de despesas

Este tópico descreve as considerações e as decisões que precisam ser tomadas durante o processo de planejamento antes de configurar o Gerenciamento de despesas. No Gerenciamento de despesas é possível armazenar informações sobre formas de pagamento, requisições de viagem, relatórios de despesas, políticas, entre outros.

Como muitas decisões tomadas ao planejar a configuração do Gerenciamento de despesas são baseadas na hierarquia e na estrutura financeira da organização, você deve consultar os documentos de planejamento dessas áreas.

## <a name="intercompany-expenses"></a>Despesas intercompanhia

Ao habilitar as despesas intercompanhia, você permite que as entidades legais e os funcionários incorram em despesas em nome de outra entidade legal e recebam o pagamento da entidade legal empregadora em sua organização. Por exemplo, se um funcionário na entidade legal A conclui um projeto para a entidade legal B e o projeto incorre em despesas relacionadas a viagens. Se as despesas intercompanhia estiverem habilitadas, o funcionário poderá arquivar um relatório de despesas que lançará a despesa para a entidade legal B, e a despesa deverá ser paga pela entidade legal A. Se a sua organização não tiver várias entidades legais, não será necessário habilitar as despesas intercompanhia.

**Decisão:** Deseja habilitar despesas intercompanhia?

## <a name="financial-management"></a>Gerenciamento financeiro

O Gerenciamento de despesas é totalmente integrado ao gerenciamento financeiro da organização. Muitas de suas configurações do Gerenciamento de despesas serão baseadas nas decisões tomadas em relação às finanças da sua organização. As seguintes seções descrevem as diversas áreas que requerem planejamento e decisões, com base nas decisões financeiras da organização e orientações de sua equipe de liderança.

### <a name="per-diems"></a>Diárias

É necessário definir as diárias de funcionários fornecidas pela sua organização. Como as diárias são geralmente usadas para cobrir despesas como refeições, hospedagens e outras despesas incidentais, é possível criar regras para as diárias oferecidas pela organização. as taxas de diária podem ser baseadas na época do ano, no local da viagem ou em ambos. Ao definir uma regra de diária, você pode especificar que uma porcentagem da taxa da diária será retida se um trabalhador receber refeições ou serviços gratuitos. Você também pode definir camadas de taxas de diária para estabelecer o número mínimo e máximo de horas que a taxa da diária pode ser aplicada à viagem de um trabalhador.

**Decisões:**

- Regras padrão de diária para o primeiro e o último dia:

    - Qual é o número mínimo de horas que um funcionário pode declarar em um dia e ainda receber uma diária?
    - Há redução no valor oferecido para refeições no primeiro e no último dia? Se houver uma redução, qual será a porcentagem?
    - Há redução no valor oferecido para hospedagem no primeiro e no último dia? Se houver uma redução, qual será a porcentagem?
    - Há redução no valor oferecido para outras despesas incorridas no primeiro e no último dia? Se houver uma redução, qual será a porcentagem?

- Regras padrão de diária:

    - Existe uma redução percentual na diária por refeição se, por exemplo, a refeição for gratuita? Se houver uma redução, qual será a porcentagem para cada refeição?
    - A redução da refeição é calculada por dia, por viagem ou pelo número de refeições por dia?
    - Os valores de diárias devem ser arredondados da maneira regular ou para cima?
    - As diárias são calculadas em um período de 24 horas ou em um dia do calendário?

- Regras de diária baseadas no local:

    - As taxas de diárias variam de acordo com o local? Quais locais estão incluídos?
    - Se as taxas de diárias variam de acordo com o local, para cada local, qual porcentagem é fornecida para os seguintes tipos de despesas:

        - Refeições
        - Hotel
        - Outras despesas

### <a name="expense-management-journals-and-accounts"></a>Diários e contas de Gerenciamento de despesas

O Gerenciamento de despesas requer o uso de vários diários e contas. É necessário decidir, por exemplo, se a mesma conta é usada para adiantamentos de dinheiro e contestações de cartão de crédito.

**Decisões:**

- Em qual diário-razão os relatórios de despesas aprovados são lançados?
- Qual conta é usada para adiantamentos de dinheiro?
- Os adiantamentos de dinheiro devem ser lançados imediatamente?

### <a name="payment-methods"></a>Formas de pagamento

Ao permitir que os funcionários incorram em despesas em nome de sua empresa, é necessário definir as formas de pagamento que os funcionários podem usar. Por exemplo, você pode permitir que os funcionários usem dinheiro ou um cartão de crédito corporativo. Você também pode permitir que os funcionários usem cartões de crédito pessoais e depois reembolsá-los. É necessário tomar as seguintes decisões para cada forma de pagamento permitida.

**Decisões:**

- Quais formas de pagamento são permitidas?
- Quem é o responsável pelas despesas incorridas na forma de pagamento?
- Há um tipo de contrapartida? Caso haja um tipo de contrapartida, qual será?
- Caso haja um tipo de contrapartida, qual será a conta?
- Se a forma de pagamento for um cartão de crédito, ela deverá ser usada somente com transações importadas?

### <a name="expense-categories-and-shared-categories"></a>Categorias de despesas e categorias compartilhadas

Quando os funcionários criam um relatório de despesas, cada despesa que eles registram deve ser associada a uma categoria de despesas. As categorias de despesas são derivadas de categorias compartilhadas que podem ser compartilhadas entre as entidades legais em sua organização. Essas categorias podem ser compartilhadas no Gerenciamento e contabilidade de projeto, dependendo da forma como a organização está definida. Com base na definição da sua organização e orientação da equipe de implementação, determine se as categorias que são usadas no Gerenciamento de despesas serão usadas apenas no Gerenciamento de despesas ou se deverão ser compartilhadas entre o Gerenciamento e contabilidade de projeto e o Gerenciamento de despesas. Observe que essas categorias podem ser compartilhadas entre Projeto e Despesa ou Projeto e Produção, mas não entre Despesa e Produção. É necessário tomar as seguintes decisões para cada categoria de despesas.

**Decisões:**

- Qual é a categoria da despesa? Os exemplos incluem categorias para voos, hotel ou milhagem.
- A categoria de despesas também pode ser usada no Gerenciamento e contabilidade de projeto?
- Qual é o tipo de despesa?
- Qual é a forma de pagamento padrão para a categoria de despesas?
- As despesas na categoria de despesas devem ser discriminadas?
- Qual é a conta principal padrão para a categoria de despesas?
- Qual é o grupo de impostos do item padrão para a categoria de despesas?
- São permitidas formas de pagamento adicionais para a categoria de despesas? Se forem permitidas formas de pagamento adicionais, quais serão elas?
- Existem subcategorias nesta categoria de despesas? Se houver subcategorias, você também precisará tomar as seguintes decisões:

    - Alguma das subcategorias foi excluída da recuperação de impostos?
    - Qual é o grupo de impostos do item das subcategorias?

Se a categoria de despesa também for usada no Gerenciamento e contabilidade de projeto, responda às perguntas restantes. Caso contrário, vá para a próxima seção.

- Quais contas de custo serão usadas para as despesas a seguir?

    - Custo
    - Alocação de folha de pagamento
    - WIP – Valor de custo
    - Custo – Item
    - WIP – Valor de custo – Item
    - Perda acumulada
    - WIP – Perda acumulada

- Quais contas de receita serão usadas para os itens a seguir?

    - Receita faturada
    - Receita acumulada - Valor de venda
    - WIP – Valor de venda
    - Receita acumulada – Produção
    - WIP – Produção
    - Receita acumulada – Lucro
    - WIP – Lucro
    - Receita acumulada – Subscrição
    - WIP – Subscrição

### <a name="taxes"></a>Impostos

Para impostos relacionados às despesas, é necessário determinar o que está incluído ou habilitado nos relatórios de despesas.

**Decisões:**

- O imposto sobre vendas está incluído nos valores das despesas?
- A restituição de imposto deve ser habilitada nas despesas?

    > [!NOTE]
    > Quando estiver planejando a contabilidade, se decidiu aplicar regras de imposto sobre vendas e sobre o uso dos EUA, não será possível habilitar a restituição de imposto nas despesas. (Para aplicar regras de imposto sobre vendas e sobre o uso dos EUA, defina a opção **Aplicar regras tributação do imposto sobre vendas** como **Sim**.)

## <a name="policies"></a>Políticas

Ao criar políticas de relatório de despesas, você pode ajudar a organização a economizar tempo e dinheiro quando os funcionários incorrerem em despesas em nome da empresa. As políticas ajudam a garantir que os funcionários permaneçam dentro do orçamento, forneçam todas as informações necessárias e usem o dinheiro somente quando precisarem. É necessário tomar as seguintes decisões para cada política de relatório de despesas e cada política de aprovação de relatório de despesas criada.

**Decisões:**

- Qual é o nome da política?
- Para que serve a política de despesas?
- Se você decidiu habilitar as despesas intercompanhia, a quais empresas em sua organização essa política se aplica?
- Quando a política entrará em vigor?
- Quando a política expirará?
- Qual é a regra da política?
- Qual é o resultado da regra da política?


[!INCLUDE[footer-include](../includes/footer-banner.md)]