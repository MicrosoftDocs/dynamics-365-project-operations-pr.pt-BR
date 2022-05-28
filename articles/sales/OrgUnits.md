---
title: Unidades organizacionais
description: Este tópico descreve o conceito de unidades organizacionais e explica como criar e manter unidades organizacionais no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581362"
---
# <a name="organizational-units-overview"></a>Visão geral de unidades organizacionais

No Microsoft Dynamics 365 Project Operations, uma *unidade organizacional* é uma divisão ou um grupo distinto em uma empresa de serviços profissionais que emprega recursos faturáveis que têm taxas de custo.

Nas empresas de serviços profissionais que empregam recursos técnicos em diferentes áreas de prática ou linhas de negócios, o custo de preencher uma função pode variar, a depender da área de prática ou da linha de negócios. Nesse cenário, o conceito de unidades organizacionais ajuda fornecendo uma maneira de agrupar um conjunto de funções faturáveis na divisão de uma empresa que tem uma estrutura de custo distinta para essas funções.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>O conceito de unidades organizacionais no Project Operations

No Project Operations, uma unidade organizacional tem uma moeda específica e listas de preços de custo específicas.

A moeda de uma unidade organizacional é a moeda primária usada para rastrear custos.

Uma ou mais listas de preços de custo podem ser anexadas a cada unidade organizacional. O Project Operations impõe as seguintes limitações quanto às listas de preços que podem ser anexadas a uma unidade organizacional:

- As listas de preços devem estar na moeda da unidade organizacional.
- As listas de preços devem ser das listas de preços de custo.

Além disso, a entidade Recurso inclui um atributo para a unidade organizacional. Cada recurso pode ser atribuído a uma unidade organizacional.

### <a name="roles-of-organizational-units"></a>Funções de unidades organizacionais

A unidade organizacional desempenha duas funções no Project Operations:

- **Unidade de contratação** – a unidade organizacional que representa o grupo ou a divisão da empresa que basicamente é responsável por efetuar vendas e gerenciar a prestação de trabalho e serviços ao cliente. A unidade de contratação é identificada pelo campo **Unidade de Contratação** na seção de cabeçalho das páginas **Oportunidade**, **Cotação**, **Contrato de Projeto** e **Projeto**.
- **Unidade recursos** – a unidade organizacional a que um recurso pertence ou está atribuído. Essa unidade organizacional pode fornecer seus recursos para algumas funções em SOWs (declarações de trabalho) e projetos que são de propriedade da unidade de contratação.

![Unidades de contratação e unidades de recursos.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Perguntas frequentes sobre unidade organizacional

Veja a seguir algumas das perguntas mais frequentes sobre unidades organizacionais.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>De que maneira a entidade Unidade Organizacional no Project Operations está relacionada à entidade Organização que já existe no Dynamics 365?

A entidade Organização do Dynamics 365 representa o nome de uma instância global do Dynamics 365. Esse nome geralmente é o nome da empresa global.

A entidade Unidade Organizacional representa uma divisão ou um grupo na empresa global. Esse grupo ou divisão tem um conjunto de funções e uma lista de preços de custo para essas funções que são diferentes das funções e da lista de preços de outros grupos ou divisões na empresa.

Quando o Project Operations é instalado, uma unidade organizacional padrão é criada com base na organização. Todos os recursos existentes são atribuídos à unidade organizacional padrão. Se um novo usuário ou recurso do Active Directory for importado para o Dynamics 365, o processo de importação de usuário os atribuirá à unidade organizacional padrão no Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Qual é a diferença entre a entidade Unidade Organizacional e a entidade Unidade de Negócios?

No Dynamics 365, a entidade Unidade de Negócios é uma construção de segurança. A associação de um usuário a uma unidade de negócios determina as entidades e os registro de entidade às quais o usuário tem acesso. Ela também determina as permissões (Criar, Ler, Gravar, Excluir, Anexar, Anexar a, Atribuir ou Compartilhar) que o usuário tem para esses registros de entidade.

A entidade Unidade Organizacional representa um grupo ou uma divisão da empresa que tem taxas de custo distintas para funcionários atribuídos a ele(a). A associação de um recurso a uma unidade organizacional determina o custo do recurso para participação em um projeto.

Ao implementar o Dynamics 365, otimize a autorização de segurança para a hierarquia de unidades de negócios e a atribuição de usuários a unidades de negócios. Atribua todos os usuários que normalmente devem acessar o mesmo conjunto de registros para a mesma unidade de negócios. A unidade organizacional não tem impacto na autorização de segurança nem no acesso.

**Exemplo que mostra uma possível diferença na modelagem de unidades organizacionais e unidades de negócios**

A unidade Cabral, Ltd. tem uma próspera prática de tecnologia Microsoft. Joaquim e Julia são desenvolvedores de C\#, mas Julia está nos Estados Unidos, enquanto Joaquim está na Índia. A maioria dos compromissos de projeto exige recursos da Contoso India e da Contoso US, e Joaquim e Julia precisam do mesmo nível de acesso de segurança a projetos nessa área de prática. No entanto, o custo dos desenvolvedores da unidade Cabral India é consideravelmente diferente do custo dos desenvolvedores da unidade Cabral US.

Veja a seguir uma maneira excelente de projetar esse cenário usando o Dynamics 365 e o Project Operations.

1. Crie a prática de tecnologia Microsoft como uma unidade de negócios e associe Joaquim e Julia a ela. Dessa maneira, você ajuda a garantir que os dois funcionários tenham o mesmo nível de acesso de segurança a quaisquer projetos nessa área de prática. Os dois poderão verificar o andamento e relatar as atualizações de horas, despesas, uso de material e tarefas.
2. Crie duas unidades organizacionais para ajudar a garantir que o custo do projeto seja refletido corretamente.
3. Associe Julia à Contoso US e Joaquim à Contoso India.
4. Atribua listas de preços de custo adequadas a ambas as unidades organizacionais. Dessa forma, você ajuda a garantir que os custos registrados no projeto para Joaquim e Julia reflitam precisamente a diferença de custos entre a Contoso US e a Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>As unidades organizacionais estão relacionadas às regiões de vendas no Dynamics 365?

Não há associação nem relação entre regiões de vendas e unidades organizacionais. Uma região de vendas geralmente é uma área geográfica onde ocorrem as vendas. Uma lista de preços de vendas pode ser associada a cada região de vendas.

Uma unidade organizacional é um grupo ou uma divisão interna na empresa que rastreia custos para um conjunto de funções que ela vende para outras divisões ou clientes externos.

**Exemplo que mostra uma possível diferença na modelagem de unidades organizacionais e regiões de vendas**

A unidade Cabral, Ltd. tem dois centros de desenvolvimento: Cabral US e Cabral India. O custo de recursos é consideravelmente diferente entre esses dois centros de desenvolvimento. A Contoso vende serviços de tecnologia da informação (TI) em muitos mercados internacionais, como América Latina, América do Norte, Pacífico Asiático, Europa Ocidental e Oriente Médio. As taxas de cobrança para as mesmas funções de projeto podem variar amplamente nesses mercados. A unidade Cabral US e a unidade Cabral India devem ser configuradas como unidades organizacionais, e cada unidade deve ter sua própria lista de preços de custo. Pacífico Asiático, América Latina, América do Norte, Europa Ocidental e o Oriente Médio devem ser configurados como regiões de vendas e cada região deve ter sua própria lista de preços de vendas.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Por que há uma limitação na associação de listas de preços às unidades organizacionais?

O preço de vendas geralmente é exclusivo às áreas geográficas ou aos mercados onde os serviços são vendidos. As divisões internas de uma empresa geralmente não têm seus próprios preços de vendas para o mesmo tipo de serviço. No entanto, as divisões internas têm um COGS (custo dos produtos vendidos) diferente, dependendo das habilidades das pessoas que empregam e das condições da mão de obra da região onde elas operam. Como as unidades organizacionais são modeladas como divisões internas de uma empresa, elas podem ter apenas listas de preços de custo.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Por que não é possível associar listas de preços de vendas a unidades organizacionais?

No Project Operations, as listas de preços de vendas podem ser associadas a clientes e regiões de vendas. As entidades transacionais, como Oportunidade, Cotação, Contrato de Projeto e Projeto, usam listas de preços de vendas que são anexadas à conta do cliente ou à região de vendas para determinar taxas de fatura e a receita potencial do compromisso de projeto.

As listas de preços de custo são associadas às unidades organizacionais. As entidades transacionais, como Oportunidade, Cotação, Contrato de Projeto e Projeto, usam listas de preços de custos que são anexadas à unidade de contratação para determinar os custos de um compromisso de projeto.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>As unidades organizacionais são hierárquicas no Project Operations?

Não. Na versão atual do Project Operations, as unidades organizacionais não são hierárquicas. Portanto, não é possível executar as seguintes tarefas:

- Configurar um padrão para inserir preços de custo padrão que percorram uma hierarquia.
- Relatar receita ou custo acumulado em diferentes níveis de hierarquia da unidade organizacional.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Somos uma grande multinacional que tem uma hierarquia complexa de vários níveis de centros de custos, divisões e escritórios de cobrança. Como podemos usar melhor o conceito de unidades organizacionais na versão atual do Project Operations?

Quando você tem uma hierarquia complexa de centros de custos, divisões, escritórios de cobrança, entre outros, configure os nós folha dessa hierarquia como unidades organizacionais distintas.

O exemplo a seguir mostra uma hierarquia comum.

**Cabral India**

- Prática SAP

    - Consultores técnicos
    - Consultores funcionais

- Prática de tecnologia Microsoft

    - Consultores técnicos
    - Consultores funcionais

**Cabral EUA**

- Prática SAP

    - Consultores técnicos
    - Consultores funcionais

- Prática de tecnologia Microsoft

    - Consultores técnicos
    - Consultores funcionais

Se a sua hierarquia se assemelha a esse exemplo, você deve configurá-la como uma lista plana, como mostrado aqui:

- Cabral India – Prática SAP – Consultores técnicos
- Cabral India – Prática SAP – Consultores funcionais
- Cabral India – Prática de tecnologia Microsoft – Consultores funcionais
- Cabral India – Prática de tecnologia Microsoft – Consultores funcionais
- Cabral US – Prática SAP – Consultores técnicos
- Cabral US – Prática SAP – Consultores funcionais
- Cabral US – Prática de tecnologia Microsoft – Consultores técnicos
- Cabral US – Prática de tecnologia Microsoft – Consultores funcionais

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Somos uma pequena empresa de serviços profissionais que opera apenas como uma divisão. Como podemos usar melhor o conceito de unidades organizacionais na versão atual do Project Operations?

Se sua empresa opera como uma unidade que tem uma lista de preços de custo, não será preciso configurar unidades organizacionais. A instalação do Project Operations cria um unidade organizacional padrão que tem o mesmo nome da organização. Por padrão, todos os usuários são atribuídos a essa unidade organizacional. Sempre que o sistema exige que é uma unidade organizacional seja selecionada, essa unidade organizacional é selecionada por padrão.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Quando um projeto é criado com base em uma linha de contrato de projeto ou cotação, a unidade de contratação padrão se origina da cotação ou do contrato de projeto. Qual é a unidade de contratação padrão se um projeto foi criado antes de entidades de vendas como Cotação ou Contrato de Projeto?

Quando um projeto é criado por si só, a unidade de contratação padrão do projeto é baseada no usuário que a cria. Esse usuário também é o gerente padrão do projeto. Se o projeto for mapeado para uma entidade de vendas, como um contrato de projeto ou cotação, a unidade de contratação do projeto será baseada na entidade de vendas. Nesse caso, as estimativas do projeto podem ser recalculadas, pois a lista de preços de custo é usada para calcular as alterações de estimativa de custo se a unidade de contratação for alterada. A lista de preços de vendas é usada para calcular as estimativas de vendas que serão alteradas para estarem sincronizadas com a lista de preços do projeto da cotação.

Os campos **Unidade de Contratação** e **Moeda** do projeto ficam bloqueados para edição porque devem estar sincronizados com os valores da entidade de vendas (cotação ou contrato de projeto) para a qual o projeto está mapeado.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Criar e manter unidades organizacionais no Project Operations

Para criar uma unidade organizacional no Project Operations, siga estas etapas.

1. Acesse **Configurações \> Unidades Organizacionais**.
2. Selecione **Nova**.
3. Na área **Geral**, no campo **Nome**, insira um nome para a unidade organizacional. Em seguida, defina os outros campos conforme necessário.
4. Selecione **Salvar** para criar o registro e poder continuar a editá-lo.
5. Em **Listas de Preços de Custo**, selecione o sinal de adição (**+**) para adicionar uma lista de preços. Você só pode adicionar listas de preços que têm o contexto de **Custo** aqui.
6. No campo **Nome**, selecione o botão **Pesquisar** e selecione a lista de preços que você quer disponibilizar para a unidade organizacional. Continue adicionando listas de preços conforme necessário.
7. Quando terminar de adicionar listas de preços, selecione **Salvar** no canto inferior direito da página.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
