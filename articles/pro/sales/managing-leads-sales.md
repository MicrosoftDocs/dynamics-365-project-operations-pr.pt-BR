---
title: Gerenciar clientes potenciais (Pro)
description: Este tópico fornece informações sobre como gerenciar clientes potenciais baseados em projeto (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896312"
---
# <a name="manage-leads-pro"></a>Gerenciar clientes potenciais (Pro)

_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_

Os clientes potenciais baseados em projeto podem ser gerenciados e qualificados no Projeto Operations. O processo de gerenciamento de leads inclui a criação e a qualificação de clientes potenciais baseados no trabalho. 

## <a name="list-of-project-sales-leads"></a>Lista de clientes potenciais de vendas do projeto

No seção **Vendas**, no painel de navegação esquerdo, abra a página **Lista de clientes potenciais** para ver uma lista de todos os registros de cliente potencial no sistema. A lista de clientes potenciais exibida é baseada no trabalho e outros tipos de clientes potenciais que podem ser criados se você também tiver os aplicativos Dynamics 365 Sales ou Dynamics 365 Field Service.

Para criar uma exibição filtrada para ver apenas clientes potenciais baseados em projeto, você pode criar um filtro no valor **Tipo**. Por exemplo, você pode selecionar para mostrar apenas clientes potenciais baseados em trabalho.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Criando um novo cliente potencial para um negócio baseado em projeto

Quando um cliente potencial baseado em projeto é qualificado, uma oportunidade e uma conta são criadas. Uma oportunidade baseada em projeto é o ponto de partida para atividades de busca de vendas na fase Oportunidade. As oportunidades baseadas em projetos têm recursos exclusivos necessários para vender o trabalho do projeto. Esses recursos incluem:

- Métodos de cobrança Hora, Material e Preço Fixo
- Listas de preços com várias datas de vigência para recursos humanos, despesas e materiais incorridos em projetos.

Para que um cliente potencial qualificado crie automaticamente uma oportunidade, defina o atributo **Tipo** como **Baseado no trabalho** quando você criar o cliente potencial. Se você escolher um tipo diferente, o cliente potencial não criará uma oportunidade baseada em projeto quando for qualificado. Se a oportunidade baseada em projeto não for criada, os recursos específicos do projeto não estarão disponíveis nos processos de vendas posteriores.

A tabela a seguir inclui informações de campo importantes para um cliente potencial e as implicações posteriores desses campos.

| **Campo** | **Local** | **Relevância, finalidade e orientação** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tópico | Guia Geral | Este campo de texto deve conter uma breve descrição do negócio. | O tópico do cliente potencial será padronizado como o tópico da oportunidade e o nome do contrato da cotação e o projeto. |
| Digitar | Guia Geral | O campo de conjunto de opções tem as seguintes opções:</br>- Baseado no trabalho (disponível apenas quando o Project Operations está instalado)</br>- Baseado no item (disponível apenas quando o Project Operations e Sales estão instalados)</br>- Baseado em serviço de manutenção (disponível quando o Field Service está instalado) | Quando o valor deste campo é definido como **Baseado no trabalho** no cliente potencial, o cliente potencial é qualificado para criar uma Oportunidade baseada em projeto. Uma oportunidade baseada em projeto é necessária para habilitar todas as extensões e funcionalidades específicas do projeto no processo de vendas posterior para este negócio. |
| Nome | Guia Geral | Nome do contato do colaborador potencial | Quando o cliente potencial é qualificado, uma conta, um contato e uma oportunidade são criados. O nome do contato é o valor definido aqui. |
| Sobrenome | Guia Geral | Sobrenome do contato do colaborador potencial | Quando o cliente potencial é qualificado, uma conta, um contato e uma oportunidade são criados. O sobrenome do contato é o valor definido aqui. |
| Empresa | Guia Geral | O nome da empresa do cliente potencial | Quando o cliente potencial é qualificado, uma conta, um contato e uma oportunidade são criados. O nome da conta criada é o valor definido aqui. |
| Moeda | Guia Detalhes | Moeda do cliente em potencial | Quando o cliente potencial é qualificado, uma conta, um contato e uma oportunidade são criados. A moeda da conta criada é o valor definido aqui. |

## <a name="qualify-a-new-project-based-lead"></a>Qualificar um cliente potencial baseado em projeto

Clientes potenciais que têm o valor **Tipo** definido como **Baseado no trabalho** são chamados de clientes potenciais baseados em projeto. Quando um cliente potencial baseado em projeto é qualificado, o seguinte é criado:

- Uma conta que usa o campo **Empresa** do cliente potencial.
- Um registro de contato associado à conta com base nos valores dos campos **Nome** e **Sobrenome** no cliente potencial.
- Uma oportunidade baseada em projeto que tem o valor do campo **Tipo** definido como &quot;**Baseado em trabalho**.

Para obter informações mais detalhadas sobre clientes potenciais qualificados, consulte[Qualificar ou converter clientes potenciais](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

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
