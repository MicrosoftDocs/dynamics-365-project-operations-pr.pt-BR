---
title: Processos de vendas
description: Este tópico fornece informações sobre os processos de vendas básicos.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 5f01ba14baa0a2378b0a230a46aed3a682342ce6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014192"
---
# <a name="sales-processes"></a>Processos de vendas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os processos de vendas que são usados em uma organização baseada em projeto diferem dos processos de vendas que são usados em uma organização baseada em produto. Essa diferença ocorre porque os ciclos de vendas para organizações baseadas em projeto são mais longos e exigem técnicas de estimativa personalizadas para analisar e criar cotações para cada negociação. O Dynamics 365 Project Service Automation usa algumas das mesmas funcionalidades que são usadas no processo de vendas do Dynamics 365 Sales. Veja alguns exemplos:

- A entidade Cliente Potencial é usada par rastrear os processos de vendas.
- Os clientes potenciais qualificados são rastreados como oportunidades. O processo de vendas também pode iniciar com oportunidade.
- Todos os artefatos relacionados para uma oportunidade são acessados. Esses artefatos incluem a equipe de vendas, participantes, probabilidade, classificação, estágios da venda e processos empresariais.
- Várias cotações são criadas para uma oportunidade.
- Uma cotação é marcada como **Fechada como Ganha** para criar um pedido de venda. No PSA, o pedido de venda é personalizado e chamado de contrato de projeto.

A seguinte ilustração mostra um processo de vendas típico em uma organização baseada em projeto.

> ![O processo de vendas em uma organização baseada em projeto](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Estimando uma venda
O valor de uma venda pode ser estimado com base em projetos que foram entregues anteriormente e na complexidade dos projetos. Em projetos que envolvem extensões para projetos anteriores, ou projetos em que a experiência do fornecedor é alta e em que modelos de trabalho reconhecidos são usados, você pode usar um processo de estimativa mais simples. Os projetos mais complexos geralmente têm um processo de compra mais longo. Portanto, há mais estágios no processo de estimativa de vendas. No início do processo, a equipe de vendas usa a entrada dos gerentes de conta e SMEs (especialistas no assunto) para iniciar a criação de uma estimativa de alto nível para cada componente distinto de trabalho que é cotado. Esses componentes de trabalho são representados pelas linhas de cotação. 

Você pode criar uma estimativa de alto nível da cotação. Por fim, essa estimativa de alto nível será substituída por uma estimativa mais detalhada que se baseia em um plano de projeto que você cria usando modelos de projeto padronizados. Esses modelos ajudam você a criar uma agenda e determinar os valores monetários na cotação e seus componentes (linhas de cotação). 

É possível criar várias cotações para um projeto e agrupá-las sob um único tipo de entidade de oportunidade. Por fim, uma dessas cotações é marcada como **Fechada como Ganha** e um contrato de projeto ou SOW (declaração de trabalho) é criado. Um contrato de projeto mantém o valor contratado para cada componente (linha de contrato) que é aceito pelo cliente para entrega. Uma SOW geralmente é criada como um documento do Microsoft Word. Todas as faturas que são enviadas ao cliente durante o curso da entrega do projeto fazem referência ao contrato de projeto ou à SOW.

Também é possível criar cotações alternativas sob um tipo de entidade de oportunidade ou configurar o sistema para que um contrato de projeto seja criado quando uma cotação é ganha. Nesse caso, você pode anexar um documento do Word que represente a SOW ao registro do contrato do projeto.

![Fechando uma cotação para criar um contrato de projeto](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Configurando o processo de vendas
Você pode usar BPFs (fluxos de processo empresarial) no Microsoft Dynamics 365 para configurar seu processo de vendas. Os BPFs proporcionam aos seus funcionários de vendas uma interface visual guiada que eles podem usar para avançar as negociações pelas fases que são típicas da sua empresa.

Por exemplo, sua empresa pode ter os seis seguintes estágios no processo de vendas:

1. Qualificar
2. Estimativa
3. Revisão interna
4. Contrato
5. Entrega
6. Fechar

Esses seis estágios são representados por setas (\>) que você seleciona para expandir em cada tipo de entidade de oportunidade que cria.

![Configuração do processo empresarial no Dynamics 365](media/basic-guide-3.png)
 
Sua organização pode usar entidades diferentes para representar a mesma negociação conforme evolui. No início do processo de vendas, uma negociação é representada pela entidade Oportunidade. Conforme o tempo passa e mais detalhes surgem, é possível usar estimativas de alto nível para criar uma ou mais cotações. Se uma dessas cotações for revisada pelos participantes internos ou do cliente, a entidade Cotação representará a negociação. Depois que o cliente aceita a cotação, um contrato de projeto ou SOW representa a negociação. Para dar suporte a esse comportamento, os BPFs são estruturados para que cada estágio no processo seja vinculado a uma tabela de banco de dados diferente.

O estágio **Qualificar** no processo de vendas pode ser rastreado por uma entidade Oportunidade. Os estágios **Estimativa** e **Revisão Interna** podem ser apoiados por uma entidade Cotação. Os estágios **Contrato**, **Entrega** e **Fechamento** podem ser apoiados por uma entidade Contrato de Projeto.

À medida que as negociações avançam pelos estágios, é solicitada a criação do registro da entidade apropriado para ajudar e guiar você pelo processo. Os estágios podem ser condicionais. Por exemplo, se você exigir uma revisão interna de uma cotação apenas se a cotação usar uma lista de preços personalizada, será possível configurar essa condição no estágio apropriado do processo empresarial. O estágio **Revisão Interna** será mostrada somente para cotações que usam uma lista de preços personalizada. Para todas as outras negociações e cotações, o estágio **Estimativa** é seguido pelo estágio **Contrato**.

> [!NOTE]
> O PSA tem páginas específicas para as entidades Oportunidade, Cotação, Ordem e Fatura. Você deve criar oportunidades, cotações, ordens e faturas de serviço de projeto usando as páginas de informações do projeto para essas entidades. Se você usar outra página para criar um registro, não será possível abrir o registro pela página **Informações do Projeto**. Se desejar abrir um registro na página **Informações do Projeto**, você deverá excluir o registro e recriá-lo usando a página **Informações do Projeto**. Na página **Informações do Projeto**, uma lógica de negócios para cada um desses tipos de entidade garante que o campo **Tipo** do registro seja definido corretamente e todos os conceitos obrigatórios sejam corretamente inicializados.

> ![Informações do projeto para uma nova ordem](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Diferenças entre o Project Service Automation e o Sales
Embora o processo de vendas no PSA use os recursos básicos do processo de vendas no Sales, ele tem algumas diferenças básicas devido a variações nas práticas de negócios das organizações baseadas em projeto. Veja alguns exemplos:

- **Cotações do projeto** – no Project Service Automation, uma cotação é fechada depois que um contrato de projeto é criado de uma cotação. No Sales, é possível manter uma cotação aberta depois que você a ganha. O motivo para essa diferença é que uma correspondência entre uma cotação e um contrato de projeto é melhor para organizações baseadas em projeto. 
- **Ativação e revisões** – no PSA, a ativação e as revisões não são aceitas para cotações de projeto. No Sales, uma cotação pode ser bloqueada para impedir edições adicionais.
- **Fechando uma cotação como perdida ou ganha** – no PSA, quando uma cotação de projeto é fechada como ganha ou perdida, a oportunidade permanece aberta. Todas as outras cotações na oportunidade são fechadas como perdidas. No Sales, quando uma cotação é fechada como ganha ou perdida, o usuário é solicitado a tomar uma medida na oportunidade. Dependendo da entrada do usuário, a oportunidade subjacente pode ser fechada ou deixada aberta.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Acompanhando revisões para cotações e planos de projeto no ciclo de vendas
No PSA, não é possível rastrear revisões que são feitas para uma cotação. Em vez disso, você deve marcar a cotação existente **Fechada como Perdida** e criar uma nova cotação. É possível copiar uma cotação ou clonar uma cotação baseada em projeto usando o PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Acompanhar comentários e aprovações de cotações e contratos de projeto
Você pode gerenciar a revisão e aprovação de cotações e contratos de projeto usando postagens e murais de registro. Sua organização pode criar fluxos de trabalho e plug-ins personalizados para atribuir, redirecionar, escalonar e gerenciar notificações de revisão e aprovação de itens de trabalho.


[!INCLUDE[footer-include](../includes/footer-banner.md)]