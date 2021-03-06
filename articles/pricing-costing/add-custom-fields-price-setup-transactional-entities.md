---
title: Adicionar campos personalizados necessários a entidades transacionais e de configuração de preço
description: Este tópico fornece informações sobre como adicionar referências de campos personalizados obrigatórios a entidades e a formulários e exibições.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a27bfe881fdb6431941fa860d279e3e7b526f623
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898292"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Adicionar campos personalizados necessários a entidades transacionais e de configuração de preço

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

Este tópico pressupõe que você concluiu os procedimentos do tópico [Criar campos e entidades personalizados a serem usados como dimensões de preço](create-custom-fields-entities-pricing-dimensions.md). Se você não concluiu esses procedimentos, volte e conclua-os e retorne a este tópico. 

Neste tópico, os procedimentos mostrarão como adicionar as referências de campo personalizadas necessárias às entidades e aos elementos da interface do usuário, como formulários e exibições.

## <a name="add-custom-pricing-dimension-fields"></a>Adicionar campos personalizados de dimensão de preço 
Depois que campos e entidades personalizados tiverem sido criados, a próxima etapa será conscientizar entidades transacionais e de configuração de preço sobre todos os conjuntos de opções e entidades personalizadas criando campos de referência. De acordo com o que a lista de dimensões de preço incluir, dimensões de conjunto de opções ou dimensões de entidade, ou ambas, siga somente as etapas em **Dimensões de preço personalizadas baseadas em conjunto de opções** ou **Dimensões de preço personalizadas baseadas em entidade**, ou em ambas, respectivamente.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensões de preço personalizadas baseadas em conjunto de opções
Quando uma dimensão personalizada de preço for baseada no conjunto de opções, adicione-a como um campo às principais entidades. No procedimento a seguir, **Local de Trabalho do Recurso** e **Horas de Trabalho do Recurso** são usadas como as dimensões de preço baseadas em conjunto de opções. Primeiro elas devem ser adicionadas como campos às entidade de preço, **Preço da Função** e **Markup de Preço da Função**.

1. Em Operações do projeto, selecione **Configurações** > **Soluções** e clique duas vezes em **\<your organization name> dimensões de preço**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Preço da Função**.
3. Expanda a entidade **Preço da Função** e selecione **Campos**.
4. Selecione **Novo** para criar um novo campo chamado **Local de Trabalho do Recurso** e selecione **Conjunto de opções** como o tipo de campo. 
5. Selecione **Usar um Conjunto de opções existente**, o conjunto de opções **Local de Trabalho do Recurso** e **Salvar**.
6. Repita as etapas de 1 a 5 para adicionar esse campo à entidade **Markup de Preço da Função**. 
7. Repita as etapas de 1 a 5 para o conjunto de opções **Horas de Trabalho do Recurso**.

> [!IMPORTANT]
> Quando você adiciona um campo a mais de uma entidade, use o mesmo nome de campo em todas as entidades. 

Nas fases de vendas e estimativa de um projeto, as estimativas do esforço de trabalho que é exigido para concluir o trabalho **Local** e **No local**, em **Horas regulares** e **Horas extras** são usadas para estimar o valor da Cotação/do Projeto. Os campos **Local de Trabalho do Recurso** e **Horas de Trabalho do Recurso** serão adicionados às entidades de estimativa **Detalhes da Linha de Cotação**, **Detalhes da Linha de Contrato**, **Membro da Equipe de Projeto**, e **Linha de Estimativa**.

1. Em Operações do projeto, selecione **Configurações** > **Soluções** e clique duas vezes em **\<your organization name> dimensões de preço**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Detalhes da Linha de Cotação**.
3. Expanda a entidade **Detalhes da Linha de Cotação** e selecione **Campos**.
4. Selecione **Novo** para criar um novo campo chamado **Local de Trabalho do Recurso** e selecione o tipo de campo **Conjunto de opções**. 
5. Selecione **Usar um Conjunto de opções existente** e **Local de Trabalho do Recurso** e, depois, **Salvar**.
6. Repita as etapas de 1 a 5 para adicionar esse campo às entidades **Detalhes da Linha de Contrato do Projeto**, **Membro da Equipe do Projeto** e **Linha de Estimativa**.
7. Repita as etapas de 1 a 6 para o conjunto de opções **Horas de Trabalho do Recurso**. 

Para entrega e faturamento, o trabalho concluído precisa ser precificado precisamente para seleção de **Local** ou **No Local** e se foi concluído durante **Horas regulares** ou **Horas extras** nos Dados Reais do Projeto. Os campos **Local de Trabalho do Recurso** e **Horas de Trabalho do Recurso** devem ser adicionados às entidades **Entrada de Tempo**, **Dados Reais**, **Detalhes da Linha de Fatura** e **Linha do Diário**.

1. Selecione **Configurações** > **Soluções** e clique duas vezes em **\<your organization name> dimensões de preço**.
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Entrada de Temo**.
3. Expanda a entidade **Detalhes da Linha de Cotação** e selecione **Campos**.
4. Selecione **Novo** para criar um novo campo chamado **Local de Trabalho do Recurso** e selecione **Conjunto de opções** como o tipo de campo. 
5. Selecione **Usar um Conjunto de opções existente**, o conjunto de opções **Local de Trabalho do Recurso** e **Salvar**.
6. Repita as etapas de 1 a 5 para adicionar esse campo às entidades **Dados Reais**, **Detalhes da Linha de Fatura** e **Linha do Diário**.
7. Repita as etapas de 1 a 6 para o conjunto de opções **Horas de Trabalho do Recurso**. 

Isso conclui as alterações no esquema exigidas para dimensões personalizadas baseadas em conjunto de opções.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensões de preço personalizadas baseadas em entidade

Quando a dimensão de preço personalizada for uma entidade, você adicionará relacionamentos 1:N entre a entidade da dimensão e as principais entidades. Usando o exemplo do Cargo Padrão acima, é razoável esperar que cada funcionário receba um cargo padrão. Consequentemente, você precisará de um relacionamento 1:N do Cargo Padrão para Recurso Reservável, ou do relacionamento N:1 se tiver sido criado do Recurso Reservável para o Cargo Padrão.

1. Em Operações do projeto, selecione **Configurações** > **Soluções** e clique duas vezes em **\<your organization name> dimensões de preço**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Cargo Padrão**.
3. Expanda a entidade **Cargo Padrão** e selecione **Relacionamentos 1: N**.
4. Selecione **Novo** para criar um novo relacionamento 1:N chamado **Cargo Padrão para Recurso Reservável**. Insira as informações necessárias e selecione **Salvar**.

O Cargo Padrão também precisará ser adicionado às entidades Preço, **Preço da Função** e **Markup de Preço da Função**. Isso também pode ser feito usando relacionamentos 1:N entre as entidades **Cargo Padrão** e **Preço da Função** e as entidades **Cargo Padrão** e **Markup de Preço da Função**.

1. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Cargo Padrão**.
2. Expanda a entidade **Cargo Padrão** e selecione **Relacionamentos 1: N**.
3. Selecione **Novo** para criar um novo relacionamento 1:N chamado **Cargo Padrão para Preço da Função**. Insira as informações necessárias e selecione **Salvar**.
4. Repita as etapas de 1 a 4 para criar relacionamentos 1:N entre as entidades **Cargo Padrão** e **Markup de Preço da Função**.

Nas fases de vendas e estimativa do projeto, para chegar ao preço da Cotação/do Projeto, as estimativas do esforço de trabalho são necessárias para cada cargo padrão. Isso significa que são necessários relacionamentos 1:N do Cargo Padrão para cada uma dessas entidades de estimativa: 

- **Detalhe da Linha de Cotação**
- **Detalhe da Linha de Contrato do Projeto**
- **Membro da Equipe do Projeto**
- **Linha de Estimativa**

5. Repita as etapas de 1 a 5 para criar relacionamentos 1:N de **Cargo Padrão** para **Detalhes da Linha de Cotação**, **Detalhes da Linha de Contrato do Projeto**, **Membro da Equipe do Projeto** e **Linha de Estimativa**.

  Nas fases Entrega e Faturamento, o trabalho concluído por cada cargo padrão deve ser precisamente precificado nos Dados Reais do Projeto. Isso significa que há necessidades de relacionamentos 1:N de **Cargo Padrão** para as entidades **Entrada de Tempo**, **Dados Reais**, **Detalhes da Linha de Fatura** e **Linha do Diário**.

6. Repita as etapas de 1 a 6 para criar relacionamentos 1:N de **Cargo Padrão** para as entidades **Entrada de Tempo**, **Dados Reais**, **Detalhes da Linha de Fatura** e **Linha do Diário**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Configurar padronização do valor de Dimensão usando os recursos de mapeamento da plataforma
Para Entrada de Tempo, seria útil que o sistema padronizasse o cargo padrão na Entrada de Tempo do Recurso Reservável que está registrando a entrada de tempo. Use as etapas a seguir para adicionar mapeamentos de campo no relacionamento 1:N de **Recurso Reservável** para **Entrada de Tempo**.

1. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades > Cargo Padrão**.
2. Expanda a entidade **Cargo Padrão** e selecione **Relacionamentos 1: N**.
3. Clique duas vezes em **Recurso Reservável para Entrada de Tempo**. Na página **Relacionamento**, selecione **Usar Mapeamentos de Campo**. 
4. Selecione **Novo** para criar um novo mapeamento de campo entre o campo **Cargo Padrão** na entidade **Recurso Reservável** para o campo de referência **Cargo Padrão** na entidade **Entrada de Tempo**. 

Isso conclui as alterações no esquema exigidas para dimensões personalizadas baseadas em entidade.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Adicionar campos personalizados a formulários, exibições e regras de negócios

Depois de ter feito todas as alterações de esquema necessárias, a próxima etapa é tornar os campos visíveis na interface do usuário adicionando os campos aos formulários e exibições.

1. Abra o formulário ou a exibição. No painel de navegação à direita, selecione o campo e arraste-o para a tela de formulário. 
2. Se estiver editando uma exibição, use o painel de navegação à direita, selecione **Adicionar campos** e, na caixa de diálogo **Listagem de campo**, selecione os campos necessários e selecione **OK**.

A tabela a seguir fornece uma lista abrangente de formulários e exibições prontos para uso, por entidade, que precisarão ser atualizados com os novos campos. Se você tiver exibições ou formulários adicionais em suas personalizações nessas entidades, adicione os novos campos a eles também.

| Entity        | Formulários que precisam do novo campo   |Exibições que precisam do novo campo      |
| ------------------------------|---------------------------------|----------------------------------|
|  Preço da Função|• Informações |• Preços Ativos de Categorias de Recursos<br> • Exibição Associada de Preços de Categorias de Recursos|
|  Markup de Preço da Função|• Informações|• Markup de Preço da Função Ativo<br>• Exibição Associada do Markup de Preço da Função|
|  Detalhes da linha de cotação|• Informações do Projeto<br>• Criação Rápida do ProJeto|• Detalhes da Linha de Cotação Ativos<br>• Detalhes Combinados da Linha de Cotação<br>• Exibição Associada de Detalhes da Linha de Cotação|
|  Detalhe da Linha de Contrato do Projeto|• Informações do Projeto<br>• Criação Rápida do ProJeto|• Detalhes Combinados da Linha de Contrato<br>• Detalhes da Linha de Contrato Ativa<br>• Exibição Associada de Detalhes da Linha de Contrato|
|  Membro da Equipe do Projeto|• Informações<br>• Novo Formulário|• Membros Ativos da Equipe do Projeto<br>• Membros da Equipe do Projeto<br>• Exibição Associada de Membros da Equipe do Projeto|
|  Entrada de Horas|• Informações<br>• Criar Entrada de Hora|• Minhas Entradas de Hora por Data<br>• Minhas Entradas de Horas para Esta Semana<br>• Entradas de hora para aprovação|
|  Linha do Diário|• Informações<br>• Criação rápida:|• Linhas de diário ativas<br>• Exibição Associada de Linhas de Diário|
|  Detalhes da Linha da Fatura|• Informações<br>• Criação rápida:|• Detalhes de Linha de Fatura Ativos<br>• Transações de Fatura Passíveis de Cobrança<br>• Transações de Fatura Complementares<br>• Exibição Associada de Detalhes de Linha de Fatura<br>• Transações de Fatura Não Passíveis de Cobrança|
|  Real|• Informações<br>• Dados Reais Ativos|• Exibição Associada de Dados Reais|

Talvez os campos personalizados também tenham que ser adicionados às regras de negócios, dependendo do que você definiu. Um exemplo pronto para uso é para a regra de negócios **Capacidade de Edição da Entrada de Tempo baseada no status**. Essa regra define quais campos precisam ser bloqueados quando a Entrada de Tempo estiver em um status não editável, como **Aprovado**. Adicione campos a essa regra de negócios para que os campos sejam bloqueados para edição quando a Entrada de Tempo estiver em um status diferente de **Rascunho** ou **Devolvido**.
