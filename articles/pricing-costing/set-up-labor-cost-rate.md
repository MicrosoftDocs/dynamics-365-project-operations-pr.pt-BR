---
title: Configurar taxas de custo de mão de obra
description: Este tópico fornece informações sobre como definir taxas para o custo de mão de obra no Project Operations
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2c41bab8626087e3cadc075b02011ef974b5eecb16e83ed67f78f4e020a83dd8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986162"
---
# <a name="set-up-labor-cost-rates"></a>Configurar taxas de custo de mão de obra

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_


Cada lista de preços tem um conjunto de taxas de mão de obra (preços de funções) que se alinham com o conteúdo e a validade da data da lista de preços.

1. Crie uma lista de preços e na guia **Preço da Função**, na subgrade, selecione **Nova Função**.
2. Na página **Criação Rápida**, selecione a função e a unidade organizacional.
3. Insira qualquer outra informação de campo obrigatória.

A tabela a seguir inclui alguns dos campos que são importantes ao criar taxas de mão de obra em uma lista de preços de custo.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Função | Guia **Geral** e páginas de **Criação Rápida** | Selecione a função à qual a taxa de custo se aplica. | A função na estimativa de entrada ou real será comparada com esta linha para padronizar o custo da função. |
| Empresa de Recursos | Guia **Geral** e páginas de **Criação Rápida** | Selecione a entidade legal à qual a função está atribuída. Por exemplo, um desenvolvedor da Fabrikam India ou um desenvolvedor da Fabrikam USA. | A empresa de recursos na estimativa de entrada ou real será comparada com esta linha para definir a taxa de custo da função. |
| Unidade de Recursos | Guia **Geral** e páginas de **Criação Rápida** | Selecione a unidade organizacional ou divisão da empresa de onde essa função será usada. Por exemplo, um desenvolvedor da divisão de robótica da Fabrikam India ou um desenvolvedor da divisão de software da Fabrikam USA. | A unidade de recursos na estimativa de entrada ou real será comparada com esta linha para definir o custo da função. |
| Preço | Guia **Geral** e páginas de **Criação Rápida** | Configure a taxa de custo para a função, empresa de recursos e combinação de unidade de recursos. Por exemplo, um desenvolvedor da Fabrikam India custa 1000 INR ou um desenvolvedor da Fabrikam USA custa 150 USD. | O preço é a taxa de custo que padroniza o custo por unidade da estimativa de entrada ou linha real para a classe de transação **Hora**. |
| Moeda | Guia **Geral** e páginas de **Criação Rápida** | Por padrão, o valor da moeda vem da moeda no cabeçalho da lista de preços de custo, mas pode ser substituído. Por exemplo, um desenvolvedor da Fabrikam India custa 1000 INR. Um desenvolvedor da Fabrikam USA custa 150 USD. | Esta moeda padroniza o custo por unidade da linha de custo real de entrada para a classe de transação **Hora**. Em uma estimativa de projeto, o valor da moeda é convertido para a moeda do projeto e mostrado na exibição em fases da estimativa. |
| Agenda da Unidade | Guia **Geral** e páginas de **Criação Rápida** | O agendamento da unidade tem como padrão o Tempo e não pode ser alterado na entidade Preço da Função porque é usado para expressar taxas por unidades de tempo. | Não há impacto posterior. |
| Unidade | Guia **Geral** e páginas de **Criação Rápida** | Por padrão, o valor vem do campo **Unidade de Tempo** no cabeçalho da lista de preços de custo. O valor pode ser substituído. Por exemplo, um desenvolvedor da Fabrikam India custa 1000 INR por **Dia da Índia**. Um desenvolvedor da Fabrikam dos EUA custa 150 USD por **Dia dos EUA**. | O sistema usa o sistema de unidades e conversão em unidades básicas para calcular um custo por unidade para calcular o preço padrão por unidade em uma estimativa de entrada ou linha real. Por exemplo, uma estimativa é de 10 **Dias da Índia** de trabalho para um desenvolvedor da Índia, e a unidade **Dia da Índia** é definida como 10 horas. Ao calcular o custo dessa linha de estimativa, o aplicativo calcula o custo unitário na estimativa como: 1000 INR/10 horas = 100 INR por hora que é convertido em USD e mostrado como o custo unitário na página **Estimativas do Projeto**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Transferência de preços e custos para recursos fora de sua divisão ou entidade legal

Em empresas baseadas em projetos, é comum usar funcionários de diferentes entidades legais ou divisões nos projetos. Um projeto pode ser executado por uma entidade legal, mas os funcionários ou consultores que trabalham no projeto podem vir da mesma entidade legal ou de uma diferente, ou pode haver uma combinação de ambas. No Dynamics 365 Project Operations, a entidade legal proprietária da entrega do projeto é a **Empresa Proprietária** e a divisão proprietária da entrega é a **Unidade de Contratação**. Outras entidades legais que fornecem recursos são as **Empresas de Recursos** e as divisões que fornecem recursos são as **Unidades de recurso**. Na maioria dos países/regiões, as empresas são obrigadas a garantir que a entidade legal ou divisão que fornece recursos cobra da empresa proprietária e da unidade contratante pelo uso dos recursos.

Por exemplo, a empresa Fabrikam deve garantir que a Fabrikam India-Robotics negociou uma tabela de preços de custo com a Fabrikam US-Robotics ou Fabrikam UK-Robotics.

Um desenvolvedor da Fabrikam India-Robotic cobra US$ 100 quando emprestado à Fabrikam US-Robotics e US$ 150 quando emprestado à Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Configurar custos para recursos externos

1. Crie uma lista de preços de custo chamada *Taxas de custo da Fabrikam US-Robotics* e defina um intervalo de data efetiva.
2. Na lista de preços de custo, configure as taxas usando as informações da tabela a seguir. 

| Função | Empresa de Recursos | Unidade de Recursos | Taxa de custo |
| --- | --- | --- | --- |
| Developer | Fabrikam India | Fabrikam India-Robotics | US$ 100 |
| Developer | Fabrikam Philippines | Fabrikam Philippines-Robotics | US$ 90 |
| Developer | Fabrikam US | Fabrikam US-Robotics | US$ 150 |

3. Anexe esta lista de preços de custo à unidade organizacional Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Configurar os preços de transferência para um recurso na moeda apropriada 

No Project Operations, o preço dos recursos pode ser definido em qualquer moeda. A moeda é padronizada como a que está no cabeçalho da lista de preços, mas pode ser alterada.

Usando o exemplo para definir o preço de transferência, as informações podem ser alteradas para:

A empresa Fabrikam deve garantir que a Fabrikam India-Robotics tenha uma taxa de custo negociada com a Fabrikam US-Robotics ou Fabrikam UK-Robotics.

Um desenvolvedor da Fabrikam India-Robotics custa 5.000 INR quando emprestado à Fabrikam US-Robotics e 5.500 INR quando emprestado à Fabrikam UK-Robotics.

Na lista de preços de custo da Fabrikam US-Robotics, as taxas de custo podem ser expressas como:

| Função | Empresa de Recursos | Custo |
| --- | --- | --- |
| Developer | Fabrikam India | 5.000 INR |
| Developer | Fabrikam US | 115 USD |

Na lista de preços de custo da Fabrikam UK-Robotics, as taxas de custo podem ser expressas como:

| Função | Empresa de recursos | Custo |
| --- | --- | --- |
| Developer | Fabrikam India | 5.500 INR |
| Developer | Fabrikam UK | 115 GBP |

A lista de preços de custo pode fornecer taxas de mão de obra em várias moedas. Ao gerar uma estimativa de custo do projeto, o Project Operations vai converter essas taxas de custo na moeda do projeto e exibi-las ao usuário. Quando uma entrada de hora é aprovada e um custo real é criado, o custo real é calculado na moeda dessa linha de preço de função correspondente na lista de preços de custo. Os custos reais por hora em um único projeto podem ser registrados em várias moedas. No entanto, ao acumular ou resumir os custos reais de mão de obra no nível do projeto, o Project Operations vai converter todos os valores de custo de mão de obra na moeda do projeto, que o usuário pode visualizar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]