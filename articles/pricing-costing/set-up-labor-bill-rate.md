---
title: Configurar taxas de cobrança de mão de obra
description: Este tópico fornece informações sobre como configurar as taxas de cobrança de mão de obra no Project Operations.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0267fce673bbd0080022a8abf2dd0020cc8b662
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877386"
---
# <a name="set-up-labor-bill-rates"></a>Configurar taxas de cobrança de mão de obra

_ **Aplicável a:** Project Operations para cenários baseados em recursos/sem estoque

Cada lista de preços tem um conjunto de preços de função, ou taxas de mão de obra, que são efetivos para o contexto e data efetiva incluídos no cabeçalho da lista de preços. As taxas de cobrança por hora no Dynamics 365 Project Operations podem ser configuradas em apenas uma moeda, que é a moeda no cabeçalho da Lista de preços.

1. Para configurar as taxas da conta de trabalho para uma lista de preços de venda, acesse **Vendas** > **Clientes** > **Lista de Preços** e selecione **Novo** para criar uma nova lista de preços. 
2. Na guia **Preços da Função**, na subgrade, selecione **Novo Preço de Função**. 
3. No painel **Criação Rápida**, insira a combinação de função e unidade organizacional para a qual você precisa configurar a taxa de cobrança.

   A tabela a seguir inclui os campos da guia **Geral** e o painel **Criação Rápida** de uma linha de preço de função que você precisa ter em mente ao criar preços de função em uma lista de preços de venda:

    | Campo | Localização | Descrição | Impacto a jusante |
    | --- | --- | --- | --- |
    | Função | Guia **Geral** e painel **Criação Rápida** | Selecione a função para a qual você está definindo a taxa de cobrança. | A função na estimativa de entrada ou real será comparada com esta linha para a taxa de cobrança padrão da função. |
    | Empresa de Recursos | Guia **Geral** e painel **Criação Rápida** | Selecione a empresa ou entidade legal da qual pertence a função. Por exemplo, um desenvolvedor da Fabrikam India ou um desenvolvedor da Fabrikam USA. | A empresa de recursos na estimativa de entrada ou real será comparada com esta linha para definir a taxa de cobrança da função. |
    | Unidade de Recursos | Guia **Geral** e painel **Criação Rápida** | Selecione a unidade organizacional ou divisão da empresa de onde vem a função. Por exemplo, um desenvolvedor da divisão de robótica da Fabrikam India ou um desenvolvedor da divisão de software da Fabrikam USA. | A unidade de recursos na estimativa de entrada ou real será comparada com esta linha para definir a taxa de cobrança da função. |
    | Preço | Guia **Geral** e painel **Criação Rápida** | Configure a taxa de cobrança para a função, empresa de recursos e combinação de unidade de recursos. Por exemplo, um desenvolvedor da Fabrikam India tem uma taxa de cobrança de 100 USD ou um desenvolvedor da Fabrikam USA tem uma taxa de cobrança de 150 USD. | Esse preço é a taxa de cobrança padrão no preço por unidade da estimativa de entrada ou linha real para a classe de transação Hora. |
    | Moeda | Guia **Geral** e painel **Criação Rápida**| Por padrão, o valor da moeda vem da moeda no cabeçalho da lista de preços de venda. Em uma lista de preços de venda, a moeda não pode ser substituída. | Essa moeda é a moeda padrão no preço por unidade da linha de vendas real de entrada para a classe de transação Hora. |
    | Agenda da Unidade | Guia **Geral** e painel **Criação Rápida** | Esse agendamento da unidade tem como padrão o Tempo e não pode ser alterado na entidade Preço da Função porque é usado para expressar taxas por unidades de tempo. | Não há impacto posterior para este campo. |
    | Unidade | Guia **Geral** e painel **Criação Rápida** | O valor da unidade vem do campo **Unidade de Tempo** no cabeçalho da lista de preços de venda. Mas o valor pode ser substituído. Por exemplo, um desenvolvedor da Fabrikam India tem uma taxa de cobrança de 1000 USD por **Dia da Índia**. Um desenvolvedor da Fabrikam USA tem uma taxa de cobrança de 1.500 USD por **Dia dos EUA**. | Quando o preço por unidade é padronizado em uma estimativa de entrada ou linha real, o sistema usa o sistema de unidades e conversão em unidades básicas para calcular um preço por unidade. Por exemplo, a estimativa é de 10 **Dias da Índia** de trabalho para um desenvolvedor da Índia, e a unidade Dia da Índia é definida como 10 horas. Ao definir o preço dessa linha de estimativa, o aplicativo calcula o preço unitário na estimativa como 1000 USD/10 horas = 100 USD por hora. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Transferir preços ou configurar taxas de cobrança para recursos de outras unidades ou divisões organizacionais 

As empresas baseadas em projetos costumam usar funcionários de diferentes entidades legais e diferentes divisões dentro da entidade legal para trabalhar em projetos. Os projetos podem ser executados a partir de uma determinada entidade legal e divisão, enquanto os funcionários ou consultores que trabalham nos projetos podem vir da mesma entidade legal e divisão ou de outra. O projeto também pode ser composto por uma combinação de pessoas de diferentes entidades e divisões legais. No Project Operations, a entidade legal que possui a entrega do projeto é chamada **Empresa Proprietária** e a divisão que possui a entrega é chamada **Unidade de Contratação**. Todas as outras entidades legais que fornecem recursos são chamadas de **Empresas de Recursos** e as divisões que fornecem recursos são chamadas de **Unidades de recurso**. Dadas as diferenças nos custos de mão de obra em várias geografias e mercados de trabalho em todo o mundo, as taxas de cobrança de mão de obra também são configuradas de forma diferente para diferentes regiões.

Por exemplo, um desenvolvedor da divisão de robótica da Fabrikam India que trabalha em um projeto nos EUA é cobrado a uma taxa de 100 USD por hora. Um desenvolvedor da divisão de robótica da Fabrikam US que trabalha no projeto dos EUA é cobrado a 150 USD por hora. 

### <a name="example-set-up-a-bill-rate"></a>Exemplo: configurar uma taxa de cobrança 

1. Crie uma lista de preços de venda chamada de *Taxas de cobrança da Fabrikam US* e defina a data de validade.
2. Na lista de preços de venda, insira as seguintes informações de taxa:

    | Função | Empresa de recursos | Unidade de recursos | Taxa de cobrança |
    | --- | --- | --- | --- |
    | Developer | Fabrikam India | Fabrikam India - Robotics | US$ 100 |
    | Developer | Fabrikam Philippines | Fabrikam Philippines - Robotics | US$ 90 |
    | Developer | Fabrikam US | Fabrikam US - Robotics | US$ 150 |

3. Anexe a lista de preços de venda **Taxas de cobrança da Fabrikam US** à lista de preços do projeto do contrato de projeto ou a uma determinada conta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
