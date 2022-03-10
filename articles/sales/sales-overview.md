---
title: Visão geral do processo de vendas
description: Este tópico fornece informações sobre os processos de vendas básicos.
author: rumant
ms.date: 10/29/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 3bda8a11d0cb6fe97a3daa640bf95717ef9913000e6b1a28a0a27a35527dbf6f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991832"
---
# <a name="sales-process-overview"></a>Visão geral do processo de vendas

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os processos de vendas que são usados em uma organização baseada em projeto diferem dos processos de vendas que são usados em uma organização baseada em produto. Isso ocorre porque os ciclos de vendas de organizações baseadas em projeto são mais longos e exigem técnicas de estimativa personalizadas para analisar e criar cotações para cada negociação. O Dynamics 365 Project Operations utiliza algumas das seguintes funcionalidades usadas em um processo de vendas:

- Um registro de Cliente Potencial é usado para rastrear o processo de vendas.
- Os clientes potenciais qualificados são rastreados como oportunidades.
- Todos os artefatos relacionados de uma oportunidade são acessíveis. Esses artefatos incluem a equipe de vendas, participantes, probabilidade, classificação, estágios da venda e processos empresariais.
- Várias cotações são criadas para uma oportunidade.
- Uma cotação recebe o status **Fechada como Ganha** para criar um pedido de venda. No Project Operations, o pedido de venda é personalizado e chamado de contrato de projeto.

## <a name="estimate-a-sale"></a>Estimar uma venda
O valor de uma venda pode ser estimado com base nos projetos que foram entregues anteriormente e na complexidade desses projetos. Em projetos que envolvem extensões para projetos anteriores, ou projetos em que a experiência do fornecedor é alta e em que modelos de trabalho reconhecidos são usados, você pode usar um processo de estimativa mais simples. Os projetos mais complexos geralmente têm um processo de compra mais longo. Portanto, há mais estágios no processo de estimativa de vendas. No início do processo, a equipe de vendas usa a entrada dos gerentes de conta e SMEs (especialistas no assunto) para criar uma estimativa de alto nível para cada componente distinto de trabalho que é cotado. Esses componentes de trabalho são representados pelas linhas de cotação. 

Você pode criar uma estimativa de alto nível da cotação. Por fim, essa estimativa de alto nível será substituída por uma estimativa mais detalhada que se baseia em um plano de projeto que você cria usando modelos de projeto padronizados. Esses modelos ajudam você a criar uma agenda e determinar os valores monetários na cotação e seus componentes (linhas de cotação). 

É possível criar várias cotações para um projeto e agrupá-las sob um único registro de oportunidade. Eventualmente, uma das cotações é marcada como **Fechada como Ganha** e um contrato de projeto ou SOW (declaração de trabalho) é criado. Um contrato de projeto mantém o valor contratado para cada componente (linha de contrato) que é aceito pelo cliente para entrega. Uma SOW geralmente é criada como um documento do Microsoft Word. Todas as faturas que são enviadas ao cliente durante o curso da entrega do projeto fazem referência ao contrato de projeto ou à SOW.

Também é possível criar cotações alternativas sob um registro de oportunidade ou configurar o sistema para que um contrato de projeto seja criado quando uma cotação for ganha. Nesse caso, você pode anexar um documento do Word que represente a SOW ao registro do contrato do projeto.

## <a name="configure-the-sales-process"></a>Configurar o processo de vendas
Você pode usar fluxos de processos empresariais para configurar seu processo de vendas. Esses fluxos fornecem uma interface visual guiada para avançar as negociações pelos estágios do processo de vendas.

Por exemplo, sua empresa pode ter os seis seguintes estágios no processo de vendas:

1. Qualificar
2. Estimativa
3. Revisão interna
4. Contrato
5. Entregar
6. Fechar
 
Sua organização pode usar entidades diferentes para representar a mesma negociação conforme evolui. No início do processo de vendas, uma negociação é representada pela entidade Oportunidade. Conforme o tempo passa e mais detalhes surgem, é possível usar estimativas de alto nível para criar uma ou mais cotações. Se uma dessas cotações for revisada pelos participantes internos ou do cliente, a entidade Cotação representará a negociação. Depois que o cliente aceita a cotação, um contrato de projeto ou SOW representa a negociação. Para dar suporte a esse comportamento, os BPFs são estruturados para que cada estágio no processo seja vinculado a uma tabela de banco de dados diferente.

O estágio **Qualificar** no processo de vendas pode ser rastreado por uma entidade Oportunidade. Os estágios **Estimativa** e **Revisão Interna** podem ser apoiados por uma entidade Cotação. Os estágios **Contrato**, **Entrega** e **Fechamento** podem ser apoiados por uma entidade Contrato de Projeto.

À medida que as negociações avançam pelos estágios, é solicitada a criação do registro da entidade apropriado para ajudar e guiar você pelo processo. Os estágios podem ser condicionais. Por exemplo, se você exigir uma revisão interna de uma cotação apenas se a cotação usar uma lista de preços personalizada, será possível configurar essa condição no estágio apropriado do processo empresarial. O estágio **Revisão Interna** será mostrada somente para cotações que usam uma lista de preços personalizada. Para todas as outras negociações e cotações, o estágio **Estimativa** é seguido pelo estágio **Contrato**.

> [!NOTE]
> O Project Operations tem páginas específicas para registros das entidades Oportunidade, Cotação, Ordem e Fatura. Você deve criar esses registros usando as páginas de informações do projeto dessas entidades. Caso contrário, você não poderá abrir os registros da página **Informações do projeto**. Se quiser abrir um registro da página **Informações do projeto**, você deverá excluir o registro e recriá-lo usando a página **Informações do projeto** na qual a lógica de negócios de cada um desses tipos de entidade garante que o campo **Tipo** do registro seja definido corretamente e que todos os conceitos obrigatórios sejam inicializados de forma adequada.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Rastrear revisões em cotações e planos de projeto no ciclo de vendas
No Project Operations, não é possível rastrear revisões realizadas em uma cotação. Em vez disso, você deve marcar a cotação existente **Fechada como Perdida** e criar uma nova cotação. É possível copiar uma cotação ou clonar uma cotação baseada em projeto.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Rastrear comentários e aprovações de cotações e contratos de projeto
Você pode gerenciar a revisão e aprovação de cotações e contratos de projeto usando postagens e murais de registro. Sua organização pode criar fluxos de trabalho e plug-ins personalizados para atribuir, redirecionar, escalonar e gerenciar notificações de revisão e a aprovação de itens de trabalho.


[!INCLUDE[footer-include](../includes/footer-banner.md)]