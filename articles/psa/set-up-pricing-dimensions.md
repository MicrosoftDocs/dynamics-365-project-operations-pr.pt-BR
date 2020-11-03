---
title: Configuração de campos personalizados como dimensões de precificação
description: Esse tópico fornece informações sobre a configuração de dimensões de preço personalizadas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: fed8d1d478dfcceb7a1e848b6432563e3b94dcf8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071643"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Configuração de campos personalizados como dimensões de precificação 

Antes de começar, esse tópico presume que os procedimentos nos tópicos foram concluídos, [Criar campos personalizados e entidades](create-custom-fields-entities.md) e [Adicionar campos personalizados para configuração de preço e entidades transacionais](field-references.md). Se você não concluiu esses procedimentos, volte e conclua-os e retorne a este tópico. 

Esse tópico fornece informações sobre a configuração de dimensões de preço personalizadas. Na interface da Web do Project Service, na página **Parâmetros** , a guia **Dimensões de preço baseadas em valor** exibe os registros nas entidades de dimensão de preço. Por padrão, a instalação de Project Service cria 2 linhas na grade nessa tabela:

- **msdyn_resourcecategory** (Função)
- **msdyn_OrganizationalUnit** (Unidade Organizacional)

> [!IMPORTANT]
> Não exclua essas linhas. No entanto, se não precisar delas, você pode torná-las não aplicáveis em um contexto específico ao definir **Aplicável ao custo** , **Aplicável às vendas** e **Aplicável à compra** como **Não**. Definir esses valores de atributo como **Não** tem o mesmo efeito de não ter o campo como dimensão de preço.

Para que um campo se torne uma dimensão de preço, ele deve:

- Criado como um campo nas entidades **Preço da função** e **Markup de preço da função**. Para obter mais informações sobre esse procedimento, consulte [Adicionar campos personalizados para configuração de preço e entidades transacionais](field-references.md).
- Criado como uma linha na tabela **Dimensão de preço**. Por exemplo, adicione as linhas de dimensão de preço conforme exibido no gráfico a seguir. 

![Linhas de dimensões de preço baseadas em valor](media/Amt-based-PD.png)

Observe que as horas de trabalho do recurso ( **msdyn_resourceworkhours** ) foram adicionadas como uma dimensão baseada em markup e adicionadas à grade na guia **Dimensão de preço baseada em markup**.

![Linhas de dimensões de preço baseadas em markup](media/Markup-based-PD.png)

> [!IMPORTANT]
> Todas as alterações em dados de dimensões de preço nessa tabela, existentes ou novas, são propagadas na lógica de negócios de preço do Project Service somente após atualizar o cache. O tempo de atualização do cache pode demorar até 10 minutos. Permita que esse período considere alterações na lógica de padronização de preço que devem resultar de alterações nos dados da Dimensão de preço.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributos da tabela de Dimensões de preço
As seções a seguir fornecem informações sobre os diferentes atributos na tabela **Dimensões de preço**.

### <a name="pricing-dimension-name"></a>Nome da dimensão de preço
Esse valor deve ser igual ao nome do esquema do campo adicionado à tabela **Preço da função** para dimensões de preço personalizadas. Para obter mais informações sobre como adicionar campos à tabela **Preço da função** , consulte [Adicionar campos personalizados para configuração de preço e entidades transacionais](field-references.md)

### <a name="type-of-dimension"></a>Tipo de dimensão
Há dois tipos de dimensões de preço:
  
  - **Dimensões baseadas em valor** : os valores da dimensão do contexto de entrada são associados aos valores de dimensão na linha **Preço da função** e preço/custo é padronizado diretamente na tabela **Preço da função**.
  - **Dimensões baseadas em markup** : são dimensões nas quais o Project Service adotará o seguinte processo de 3 etapas para obter o preço/custo
 
    1. O Project Service corresponde aos valores de dimensão não baseada em markup do contexto de entrada da linha Preço da função para obter a taxa base.
    2. O Project Service associa todos os valores de dimensão do contexto de entrada na linha **Markup do preço da função** para obter um percentual de markup.
    3. O Project Service aplica o percentual de markup da segunda etapa à taxa base obtida da tabela **Preço da função** na primeira etapa para obter o preço/custo final.
   
   A tabela a seguir mostra o cálculo de markups de preço.
  
| Função        | Unidades Organizacionais    |Local de Trabalho      |Título padrão      |Horas de trabalho do recurso      |  Markup|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Cabral India|No local            |                    |Horas Extras                 |15     |
|             | Cabral India|Local             |                    |Horas Extras                 |10     |
|             | Cabral EUA   |Local             |                    |Horas Extras                 |20     |


Se um recurso de Cabral India cuja taxa base é USD 100 estiver trabalhando no local e registrarem 8 horas de trabalho normal e 2 horas de hora extra, o mecanismo de preço do Project Service usará a taxa base de 100 para as 8 horas para registrar USD 800 Para as 2 horas extra, um markup de 15% será aplicado à taxa base de 100 para obter um preço unitário de USD 115 e registrará um custo total de USD 230.

### <a name="applicable-to-cost"></a>Aplicável ao Custo 
Caso seja configurado como **Sim** , indica que o valor da dimensão do contexto de entrada deve ser usado para corresponder a **Preço da função** e **Markup do preço da função** ao recuperar as taxas de custo e markup.

### <a name="applicable-to-sales"></a>Aplicável a Vendas
Caso seja configurado como **Sim** , indica que o valor da dimensão do contexto de entrada deve ser usado para corresponder a **Preço da função** e **Markup do preço da função** ao recuperar as taxas de faturamento e markup.

### <a name="applicable-to-purchase"></a>Aplicável à Compra
Caso seja configurado como **Sim** , indica que o valor da dimensão do contexto de entrada deve ser usado para corresponder a **Preço da função** e **Markup do preço da função** ao recuperar o preço de compra. Atualmente o Project Service não é compatível com subcontratação, portanto, este campo não é usado. 

### <a name="priority"></a>Prioridade
Definir a prioridade da dimensão ajuda o processo de preço do Project Service a gerar um preço mesmo quando não encontrar uma correspondência exata entre os valores de dimensão de entrada e os valores das tabelas **Preço da função** e **Markup do preço da função**. Nesse caso, o Project Service usará valores nulos para valores de dimensão não correspondidos ao ponderar as dimensões de acordo com a prioridade.

- **Prioridade de custo** : o valor de uma prioridade de custo da dimensão indicará o peso dessa dimensão ao compará-la à configuração dos preços de custo. O valor de **Prioridade de custo** deve ser exclusivo nas dimensões **Aplicável ao custo**.
- **Prioridade de vendas** : o valor da prioridade de vendas da dimensão indicará o peso da dimensão ao compará-lo à configuração dos preços de vendas ou das taxas de faturamento. O valor de **Prioridade de vendas** deve ser exclusivo nas dimensões **Aplicável a vendas**.
