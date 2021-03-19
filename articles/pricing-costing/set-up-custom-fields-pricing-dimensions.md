---
title: Configurar campos personalizados como dimensões de preço
description: Este tópico fornece informações sobre como configurar dimensões de precificação usando campos personalizados.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1468c3396a01c1bee1bc0f47eac1ee8b44eaa459
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274849"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Configurar campos personalizados como dimensões de preço

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Antes de começar, este tópico presume que você concluiu os procedimentos nos tópicos [Criar campos e entidades personalizados](create-custom-fields-entities-pricing-dimensions.md) e [Adicionar campos personalizados obrigatórios a entidades transacionais e de configuração de preço](add-custom-fields-price-setup-transactional-entities.md). Se você não concluiu esses procedimentos, volte e conclua-os e retorne a este tópico. 

Esse tópico fornece informações sobre a configuração de dimensões de preço personalizadas. Na página **Parâmetros**, a guia **Dimensões de Precificação Baseadas em Valor** mostra os registros nas entidades de dimensões de precificação. Por padrão, há duas linhas na grade desta guia:

- **msdyn_resourcecategory** (Função)
- **msdyn_OrganizationalUnit** (Unidade Organizacional)

> [!IMPORTANT]
> Não exclua essas linhas. No entanto, se não precisar delas, você pode torná-las não aplicáveis em um contexto específico ao definir **Aplicável ao custo**, **Aplicável às vendas** e **Aplicável à compra** como **Não**. Definir esses valores de atributo como **Não** tem o mesmo efeito de não ter o campo como dimensão de preço.

Para que um campo se torne uma dimensão de preço, ele deve:

- Criado como um campo nas entidades **Preço da função** e **Markup de preço da função**. Para obter mais informações sobre esse procedimento, consulte [Adicionar campos personalizados para configuração de preço e entidades transacionais](add-custom-fields-price-setup-transactional-entities.md).

- Criado como uma linha na tabela **Dimensão de preço**. Por exemplo, adicione as linhas de dimensão de preço conforme exibido no gráfico a seguir. 

![Linhas de dimensões de preço baseadas em valor](media/Amt-based-PD.png)

As Horas de Trabalho do Recurso (**msdyn_resourceworkhours**) foram adicionadas como uma dimensão baseada em markup e adicionadas à grade na guia **Dimensão de Precificação Baseada em Markup**.

![Linhas de dimensões de preço baseadas em markup](media/Markup-based-PD.png)


> [!IMPORTANT]
> Todas as alterações nos dados de dimensões de precificação nessa tabela, existentes ou novas, são propagadas para a lógica de negócios de precificação somente após a atualização do cache. O tempo de atualização do cache pode demorar até 10 minutos. Permita que esse período considere alterações na lógica de padronização de preço que devem resultar de alterações nos dados da Dimensão de preço.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributos da tabela de Dimensões de preço
As seções a seguir fornecem informações sobre os diferentes atributos na tabela **Dimensões de preço**.

### <a name="pricing-dimension-name"></a>Nome da dimensão de preço
Esse valor deve ser igual ao nome do esquema do campo adicionado à tabela **Preço da função** para dimensões de preço personalizadas. Para obter mais informações sobre como adicionar campos à tabela **Preço da função**, consulte [Adicionar campos personalizados para configuração de preço e entidades transacionais](add-custom-fields-price-setup-transactional-entities.md)

### <a name="type-of-dimension"></a>Tipo de dimensão
Há dois tipos de dimensões de preço:
  
  - **Dimensões baseadas em valor**: os valores da dimensão do contexto de entrada são associados aos valores de dimensão na linha **Preço da função** e preço/custo é padronizado diretamente na tabela **Preço da função**.
  - **Dimensões baseadas em markup**: são dimensões nas quais o seguinte processo de três etapas para obter o preço/custo é usado:
 
    1. Os valores de dimensões não baseadas em markup do contexto de entrada são correspondidos à linha Preço da Função para obter a taxa base.
    2. Os valores de dimensões do contexto de entrada são correspondidos à linha **Markup de Preço da Função** para obter um percentual de markup.
    3. O percentual de markup da segunda etapa é aplicado à taxa base obtida da tabela **Preço da Função** na primeira etapa para obter o preço/custo final.
   
   A tabela a seguir mostra o cálculo de markups de preço.
  
| Função        | Unidades Organizacionais    |Local de Trabalho      |Título padrão      |Horas de trabalho do recurso      |  Markup|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Cabral India|No local            |                    |Horas Extras                 |15     |
|             | Cabral India|Local             |                    |Horas Extras                 |10     |
|             | Cabral EUA   |Local             |                    |Horas Extras                 |20     |


Se um recurso da Contoso India cuja taxa base é USD 100 estiver trabalhando no local e registrar 8 horas de trabalho normal e 2 horas extra na entrada de hora, o mecanismo de precificação usará a taxa base de 100 para as 8 horas para registrar USD 800. Para as 2 horas extra, um markup de 15% será aplicado à taxa base de 100 para obter um preço unitário de USD 115 e registrará um custo total de USD 230.

### <a name="applicable-to-cost"></a>Aplicável ao Custo 
Caso seja configurado como **Sim**, indica que o valor da dimensão do contexto de entrada deve ser usado para corresponder a **Preço da função** e **Markup do preço da função** ao recuperar as taxas de custo e markup.

### <a name="applicable-to-sales"></a>Aplicável a Vendas
Caso seja configurado como **Sim**, indica que o valor da dimensão do contexto de entrada deve ser usado para corresponder a **Preço da função** e **Markup do preço da função** ao recuperar as taxas de faturamento e markup.

### <a name="applicable-to-purchase"></a>Aplicável à Compra
Caso seja configurado como **Sim**, indica que o valor da dimensão do contexto de entrada deve ser usado para corresponder a **Preço da função** e **Markup do preço da função** ao recuperar o preço de compra. Não há suporte para cenários de subcontratação, portanto, este campo não é usado. 

### <a name="priority"></a>Prioridade
Definir a prioridade da dimensão ajuda a precificação a gerar um preço mesmo quando não encontrar uma correspondência exata entre os valores de dimensão de entrada e os valores das tabelas **Preço da Função** e **Markup de Preço da Função**. Nesse caso, valores nulos serão usados para valores de dimensão não correspondidos pesando as dimensões de acordo com a prioridade.

- **Prioridade de custo**: o valor de uma prioridade de custo da dimensão indicará o peso dessa dimensão ao compará-la à configuração dos preços de custo. O valor de **Prioridade de custo** deve ser exclusivo nas dimensões **Aplicável ao custo**.
- **Prioridade de vendas**: o valor da prioridade de vendas da dimensão indicará o peso da dimensão ao compará-lo à configuração dos preços de vendas ou das taxas de faturamento. O valor de **Prioridade de vendas** deve ser exclusivo nas dimensões **Aplicável a vendas**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]