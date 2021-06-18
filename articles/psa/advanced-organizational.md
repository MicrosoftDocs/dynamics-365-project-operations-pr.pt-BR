---
title: Unidades organizacionais
description: Este tópico fornece informações sobre unidades organizacionais no Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3be18adfa1d346bdabae7e89375ca2c5a2dbda95
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009602"
---
# <a name="organizational-units"></a>Unidades organizacionais 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Dynamics 365 Project Service Automation, uma unidade organizacional é uma divisão ou um grupo distinto em uma empresa de serviços profissionais que emprega recursos cobráveis que têm taxas de custo.

Para empresas de serviços profissionais que empregam recursos técnicos em diversas áreas práticas ou linhas de negócios, o custo de preencher uma função em uma área prática ou linha de negócios é diferente do custo de preencher uma função em outra área prática ou linha de negócios. O conceito de unidades organizacionais ajuda neste cenário fornecendo uma maneira de agrupar um conjunto de funções cobráveis na divisão de uma empresa que tem uma estrutura de custo distinta para essas funções.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Principais atributos e associações de unidades organizacionais

No PSA, uma unidade organizacional tem uma moeda específica e listas de preços de custo específicas.

A moeda de uma unidade organizacional é a moeda primária usada para rastrear custos.

Uma ou mais listas de preços de custo podem ser anexadas a cada unidade organizacional. O PSA impõe as seguintes limitações nas listas de preços que podem ser anexadas a uma unidade organizacional:

- Listas de preços devem estar na moeda da unidade organizacional
- Listas de preços devem ser das listas de preços de custo

Além disso, há um atributo para a unidade organizacional na entidade Recurso. Cada recurso pode ser atribuído a uma unidade organizacional.

## <a name="roles-of-organizational-units"></a>Funções de unidades organizacionais

A unidade organizacional desempenha duas funções no PSA:

- **Unidade de contratação** – a unidade organizacional que representa o grupo ou a divisão da empresa que basicamente é responsável por efetuar vendas e gerenciar a prestação de trabalho e serviços ao cliente. A unidade de contratação é identificada pelo campo **Unidade de Contratação** na seção de cabeçalho das páginas **Oportunidade**, **Cotação**, **Contrato de Projeto** e **Projeto**.
- **Unidade recursos** – a unidade organizacional a que um recurso pertence ou está atribuído. Essa unidade organizacional pode fornecer seus recursos para algumas funções em SOWs (declarações de trabalho) e projetos que são de propriedade da unidade de contratação.

> ![Unidades de contratação e unidades de recursos](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Perguntas frequentes sobre unidade organizacional

Veja a seguir algumas das perguntas mais frequentes sobre unidades organizacionais.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Como a entidade Unidade Organizacional no PSA está relacionada à entidade Organização que já existe no Dynamics 365?

A entidade Organização no Microsoft Dynamics 365 representa o nome de uma instância global do Dynamics 365. Esse nome geralmente é o nome da empresa global.

A entidade Unidade Organizacional representa uma divisão ou um grupo na empresa global. Esse grupo ou divisão tem um conjunto de funções e uma lista de preços de custo para essas funções que são diferentes das funções e da lista de preços de outros grupos ou divisões na empresa.

Quando o PSA é instalado, uma unidade organizacional padrão é criada com base na organização. Todos os recursos existentes são atribuídos à unidade organizacional padrão. Se um novo usuário ou recurso do Active Directory for importado no Dynamics 365, o processo de importação de usuário os atribuirá à unidade organizacional padrão no PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Como a entidade DE unidade organizacional difere da entidade de unidade de negócios?

No Dynamics 365, a entidade Unidade de Negócios é uma construção de segurança. A associação de um usuário a uma unidade de negócios determina as entidades e os registro de entidade às quais o usuário tem acesso. Ela também determina as permissões (Criar, Ler, Gravar, Excluir, Anexar, Anexar a, Atribuir ou Compartilhar) que o usuário tem para esses registros de entidade.

A entidade Unidade Organizacional representa um grupo ou uma divisão da empresa que tem taxas de custo distintas para funcionários atribuídos a ele(a). A associação de um recurso a uma unidade organizacional determina o custo do recurso para participação em um projeto.

Ao implementar o Dynamics 365, otimize a autorização de segurança para a hierarquia de unidades de negócios e a atribuição de usuários a unidades de negócios. Atribua todos os usuários que normalmente devem acessar o mesmo conjunto de registros para a mesma unidade de negócios. A unidade organizacional não tem impacto na autorização de segurança nem no acesso.

#### <a name="example-of-organizational-units-and-business-units"></a>Exemplos de unidades organizacionais e unidades de negócios

A Contoso, Ltd. tem uma próspera prática de tecnologia Microsoft. Joaquim e Julia são desenvolvedores de C\#, mas Julia está nos Estados Unidos, enquanto Joaquim está na Índia. A maioria das participações em projetos requer recursos das unidades da Contoso Índia e Contoso EUA, e Joaquim e Julia exigem o mesmo nível de acesso de segurança a projetos nessa área prática. No entanto, o custo dos desenvolvedores da Contoso Índia é consideravelmente diferente do custo dos desenvolvedores da Contoso EUA.

Veja a seguir uma maneira excelente de projetar esse cenário usando o Dynamics 365 e o PSA.

1. Crie a prática de tecnologia Microsoft como uma unidade de negócios e associe Joaquim e Julia a ela. Dessa maneira, você ajuda a garantir que ambos os funcionários tenham o mesmo nível de acesso de segurança a quaisquer projetos nessa área prática. Ambos poderão verificar o andamento e relatar o tempo, as despesas e as atualizações de tarefa. 
2. Crie duas unidades organizacionais para ajudar a garantir que o custo para o projeto seja refletido corretamente. 
3. Associe Julia à Contoso EUA e Joaquim à Contoso Índia.
4. Atribua listas de preços de custo adequadas a ambas as unidades organizacionais. Dessa forma, você ajuda a garantir que os custos que são gravados no projeto para Joaquim e Julia reflitam precisamente a diferença em custos entre a Contoso EUA e a Contoso Índia.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>As unidades organizacionais estão relacionadas às regiões de vendas no Dynamics 365?

Não há associação nem relação entre regiões de vendas e unidades organizacionais. Uma região de vendas geralmente é uma área geográfica onde ocorrem as vendas. Uma lista de preços de vendas pode ser associada a cada região de vendas.

Uma unidade organizacional é um grupo ou uma divisão interna na empresa que rastreia custos para um conjunto de funções que ela vende para outras divisões ou clientes externos.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Exemplo de unidades organizacionais e regiões de vendas

A Contoso, Ltd. tem dois centros de desenvolvimento: Contoso EUA e Contoso Índia. Os custos de recursos são consideravelmente diferentes entre esses dois centros de desenvolvimento.

A Contoso vende seus serviços de TI em muitos mercados internacionais, como América Latina, América do Norte, Pacífico Asiático, Europa Ocidental e Oriente Médio. As taxas de cobrança para as mesmas funções de projeto podem variar amplamente nesses mercados.

A Contoso EUA e a Contoso Índia devem ser configuradas como unidades organizacionais, e cada unidade deve ter sua própria lista de preços de custo. Pacífico Asiático, América Latina, América do Norte, Europa Ocidental e o Oriente Médio devem ser configurados como regiões de vendas e cada região deve ter sua própria lista de preços de vendas.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Por que há uma limitação na associação de listas de preços às unidades organizacionais? 

O preço de vendas geralmente é exclusivo às áreas geográficas ou aos mercados onde os serviços são vendidos. As divisões internas de uma empresa geralmente não têm seus próprios preços de vendas para o mesmo tipo de serviço. No entanto, as divisões internas têm um COGS (custo dos produtos vendidos) diferente, dependendo das habilidades das pessoas que empregam e das condições da mão de obra da região onde elas operam. Como as unidades organizacionais são modeladas como divisões internas de uma empresa, elas podem ter apenas listas de preços de custo.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Por que não é possível associar listas de preços de vendas às unidades organizacionais?

No PSA, as listas de preços de vendas podem ser associadas a clientes e regiões de vendas. As entidades transacionais, como Oportunidade, Cotação, Contrato de Projeto e Projeto usam listas de preços de vendas que são anexadas à conta do cliente ou à região de vendas para determinar taxas de cobrança e possível receita na participação do projeto.

As listas de preços de custo são associadas às unidades organizacionais. As entidades transacionais, como Oportunidade, Cotação, Contrato de Projeto e Projeto usam listas de preços de custos que são anexadas à unidade de contratação para determinar custos para participação em um projeto.

### <a name="are-organizational-units-hierarchical-in-psa"></a>As unidades organizacionais são hierárquicas no PSA?

Nº Na versão atual do PSA, as unidades organizacionais não são hierárquicas. Isso significa que não é possível:

- Configurar um padrão para padronizar preços de custo que percorra uma hierarquia. 
- Relatar receita ou custo acumulados em diferentes níveis de hierarquia da unidade organizacional.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Somos uma grande multinacional com uma hierarquia complexa de vários níveis de centros de custos, divisões e escritórios de cobrança. Como podemos usar melhor o conceito de unidade organizacional nessa versão do aplicativo Project Service?

Quando você tem uma hierarquia complexa de centros de custos, divisões, escritórios de cobrança, etc., configure os nós folha dessa hierarquia como unidades organizacionais distintas.
O seguinte exemplo mostra uma hierarquia comum:

**ContosoÍndia**

  - Prática SAP 

    - Consultores técnicos 
    - Consultores funcionais 
    
  - Prática de tecnologia Microsoft 

    - Consultores técnicos
    - Consultores funcionais 
    
**Contoso EUA**

 - Prática SAP 

    - Consultores técnicos 
    - Consultores funcionais 
    
 - Prática de tecnologia Microsoft 

    - Consultores técnicos 
    - Consultores funcionais 
 
Se sua hierarquia for semelhante, você deverá configurá-la como uma lista plana, como mostrado aqui:
- Contoso Índia - Prática SAP – Consultores Técnicos 
- Contoso Índia - Prática SAP – Consultores Funcionais       
- Contoso Índia – Prática de Tecnologia Microsoft – Consultores Funcionais 
- Contoso Índia – Prática de Tecnologia Microsoft – Consultores Funcionais 
- Contoso Estados Unidos - Prática SAP – Consultores Técnicos  
- Contoso EUA - Prática SAP – Consultores Funcionais  
- Contoso EUA – Prática de Tecnologia Microsoft – Consultores Técnicos 
- Contoso EUA – Prática de Tecnologia Microsoft – Consultores Funcionais

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Somos uma pequena empresa de serviços profissionais que opera apenas como uma divisão. Como podemos usar melhor o conceito de unidade organizacional na versão atual do PSA?

Se sua empresa opera como uma unidade que tem uma lista de preços de custo, não será preciso configurar unidades organizacionais. Durante a instalação do PSA, o Dynamics 365 cria um unidade organizacional padrão que tem o mesmo nome da organização. Por padrão, todos os usuários são atribuídos a essa unidade organizacional. Sempre que o sistema exige que é uma unidade organizacional seja selecionada, essa unidade organizacional é selecionada por padrão.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Quando um projeto é criado com base em uma linha de contrato de projeto ou cotação, a unidade de contratação padrão se origina da cotação ou do contrato de projeto. Se um projeto foi criado antes das entidades de vendas, como cotação ou contrato de projeto, qual é a unidade de contratação padrão?

Quando um projeto é criado por si só, a unidade de contratação padrão do projeto é baseada no usuário que a cria. Esse usuário também é o gerente padrão do projeto. Se o projeto for mapeado para uma entidade de vendas, como um contrato de projeto ou cotação, a unidade de contratação no projeto será baseada na entidade de vendas. Nesse caso, as estimativas do projeto podem ser recalculadas, pois a lista de preços de custo é usada para calcular as alterações de estimativa de custo se a unidade de contratação for alterada. A lista de preços de vendas é usada para calcular as estimativas de vendas que serão alteradas para que estejam em sincronia com a lista de preços do projeto na cotação.

Os campos **Unidade de Contratação** e **Moeda** no projeto estão bloqueados para edição, pois eles devem estar em sincronia com os valores na entidade de vendas (cotação ou contrato de projeto) para a qual o projeto é mapeado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]