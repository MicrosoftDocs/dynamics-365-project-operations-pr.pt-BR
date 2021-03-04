---
title: Gerenciar clientes potenciais
description: Este tópico fornece informações sobre como gerenciar clientes potenciais baseados em projeto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 16f5dbb283eee12cf10ca7145ea9e17c5ef8923e
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513820"
---
# <a name="manage-leads"></a>Gerenciar clientes potenciais

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Os clientes potenciais baseados em projeto podem ser gerenciados e qualificados no Projeto Operations. O processo de gerenciamento de leads inclui a criação e a qualificação de clientes potenciais baseados no trabalho. 

## <a name="project-sales-leads"></a>Clientes potencial de vendas do projeto

No seção **Vendas**, no painel de navegação esquerdo, abra a página **Lista de clientes potenciais** para ver uma lista de todos os registros de cliente potencial no sistema. A lista de clientes potenciais exibida é baseada no trabalho e outros tipos de clientes potenciais que podem ser criados se você também tiver os aplicativos Dynamics 365 Sales ou Dynamics 365 Field Service.

Para criar uma exibição filtrada para ver apenas clientes potenciais baseados em projeto, você pode criar um filtro no valor **Tipo**. Por exemplo, você pode selecionar para mostrar apenas clientes potenciais baseados em trabalho.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Crie um novo cliente potencial para uma oferta baseada em projeto

Quando um cliente potencial baseado em projeto é qualificado, uma oportunidade e uma conta são criadas. Uma oportunidade baseada em projeto é o ponto de partida para atividades de busca de vendas na fase Oportunidade. As oportunidades baseadas em projetos têm recursos exclusivos necessários para vender o trabalho do projeto. Esses recursos incluem:

- Métodos de cobrança Hora, Material e Preço Fixo
- Listas de preços com várias datas de vigência para recursos humanos, despesas e materiais incorridos em projetos

Para que um cliente potencial qualificado crie automaticamente uma oportunidade, defina o atributo **Tipo** como **Baseado no trabalho** quando você criar o cliente potencial. Se você escolher um tipo diferente, o cliente potencial não criará uma oportunidade baseada em projeto quando for qualificado. Se a oportunidade baseada em projeto não for criada, os recursos específicos do projeto não estarão disponíveis nos processos de vendas posteriores.

A tabela a seguir inclui informações de campo importantes para um cliente potencial e as implicações posteriores desses campos.
 
| **Campo** | **Local** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tópico | Guia Geral | Este campo de texto deve conter uma breve descrição do negócio. | O tópico do lead será padronizado como o tópico da oportunidade, e o nome da cotação e o contrato do projeto. |
| Digitar | Guia Geral | O campo de conjunto de opções tem as seguintes opções:</br>- Baseado no trabalho (disponível apenas quando o Project Operations está instalado)</br>- Baseado no item (disponível apenas quando o Project Operations e Sales estão instalados)</br>- Baseado em serviço de manutenção (disponível quando o Field Service está instalado) | Quando o valor deste campo é definido como **Baseado no trabalho** no cliente potencial, o cliente potencial é qualificado para criar uma Oportunidade baseada em projeto. Uma oportunidade baseada em projeto é necessária para habilitar todas as extensões e funcionalidades específicas do projeto no processo de vendas posterior para este negócio. |
| Nome | Guia Geral | Nome do contato do colaborador potencial | Quando o cliente potencial é qualificado, uma conta, um contato e uma oportunidade são criados. O nome do contato é o valor definido aqui. |
| Sobrenome | Guia Geral | Sobrenome do contato do colaborador potencial | Quando o cliente potencial é qualificado, uma conta, um contato e uma oportunidade são criados. O sobrenome do contato o valor definido aqui. |
| Empresa | Guia Geral | O nome da empresa do cliente potencial | Quando o cliente potencial é qualificado, uma conta, um contato e uma oportunidade são criados. O nome da conta criada é o valor definido aqui. |
| Moeda | Guia Detalhes | Moeda do cliente em potencial | Quando o cliente potencial é qualificado, uma conta, um contato e uma oportunidade são criados. A moeda da conta criada é o valor definido aqui. |

## <a name="qualify-a-new-project-based-lead"></a>Qualificar um cliente potencial baseado em projeto

Clientes potenciais que têm o valor **Tipo** definido como **Baseado no trabalho** são chamados de clientes potenciais baseados em projeto. Quando um cliente potencial baseado em projeto é qualificado, o seguinte é criado:

- Uma conta que usa o campo **Empresa** do cliente potencial.
- Um registro de contato associado à conta com base nos valores dos campos **Nome** e **Sobrenome** no cliente potencial.
- Uma oportunidade baseada em projeto que tem o campo **Tipo** definido como **Baseado em trabalho**.

Para obter informações mais detalhadas sobre clientes potenciais qualificados, consulte [Qualificar ou converter clientes potenciais](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Qualificação de cliente potencial e informações da entidade legal 

Quando você executa as operações do projeto usando o modo de implantação, as operações do projeto para cenários baseados em recursos/não estocados, cada cliente e oportunidade exigirá ter o conjunto de campos **Empresa proprietária**. A empresa proprietária é uma entidade legal em sua organização que possui a entrega do projeto. Cada cliente, ou conta com tipo de relacionamento de cliente, deve ter o valor do campo **Empresa proprietária** definido para a entidade legal que contrata e negocia com este cliente. Um cliente só pode pertencer a uma entidade legal.

Quando um lead é qualificado, os registros de cliente e oportunidade criados terão o campo **Empresa proprietária** definido para a empresa do registro de recurso reservável do usuário atual.

Se o registro de recurso reservável do usuário atual estiver vazio, o valor do campo **Empresa proprietária** no registro do usuário é usado como padrão no cliente e nos registros de oportunidade.

## <a name="business-process-flow-for-project-based-deals"></a>Fluxo de processo empresarial para negócios baseados em projetos

Os seguintes fluxos de processo empresariais são compatíveis com negócios baseados em projetos no Project Operations:

- Processo empresarial Cliente Potencial até a Oportunidade
- Processo de vendas de oportunidade

O processo empresarial Cliente Potencial até a Oportunidade oferece suporte aos seguintes estágios:

| Nome do estágio | Entidade mapeada | Funcionalidade |
| --- | --- | --- |
| Qualificar | Lead | Qualificar o cliente potencial para criar uma conta, contato e/ou oportunidade. |
| Desenvolver | Oportunidade | Desenvolver a oportunidade para adicionar mais informações sobre o trabalho envolvido, os principais participantes e a concorrência. |
| Propor | Oportunidade | Desenvolver a proposta e obter aprovação da equipe de revisão interna. |
| Fechar | Oportunidade | Vencer a oportunidade para fechar o negócio. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]