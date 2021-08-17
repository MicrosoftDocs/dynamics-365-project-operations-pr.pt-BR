---
title: Copiar cotações baseadas em projeto
description: Este tópico fornece informações sobre como copiar cotações baseadas em projeto no Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 247f9d33bc2e7b0bcbeae8114bb436ed237efce660d0840e58d536d2a290639e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992147"
---
# <a name="copy-project-based-quotes"></a>Copiar cotações baseadas em projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Você pode criar facilmente uma nova cotação de projeto copiando uma existente. 

- Para copiar uma cotação de projeto, na página de lista **Cotações de projetos** ou a página de detalhes **Cotação de Projeto**, selecione a cotação do projeto que deseja copiar e, em seguida, selecione **Copiar**.

Isso abrirá uma página de diálogo onde você pode inserir os parâmetros da cópia. A tabela a seguir lista os campos que são incluídos na página de diálogo. Dependendo dos valores selecionados, o processo de cópia pode mudar.

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Tópico | Insira o tópico relevante, ou nome, da cotação alvo. Quando a caixa de diálogo for aberta, o sistema irá configurá-lo para o tópico da cotação de origem com **copiar** anexado a ela. | |
| Cliente em Potencial | Referência à empresa do cliente ou registro de conta. Quando a caixa de diálogo for aberta, o sistema irá configurá-lo para a conta na cotação de origem. | Este campo é o cliente principal da cotação. |
| Unidade de Contratação | A unidade organizacional responsável pela entrega do projeto ou projetos associados a este negócio.
Quando a caixa de diálogo for aberta, o sistema irá configurá-lo para a unidade de contratação na cotação de origem. | A unidade de contratação é a divisão da empresa que executará os projetos após o fechamento do negócio. Cada unidade contratante tem uma moeda. A moeda é usada para relatar os custos estimados e reais incorridos durante a execução do projeto. |
| Moeda | Esta é a moeda para o qual a oferta é transacionada. Quando a caixa de diálogo for aberta, o sistema irá configurá-lo para a moeda na cotação de origem. Isso pode ser modificado e se for alterado, o campo **Copiar preços** é sempre definido como **Não**. Isso ocorre porque as listas de preços na cotação da fonte não são mais relevantes. | A moeda é usada como padrão para uma lista de preços, para construir uma estimativa financeira na cotação e, eventualmente, para faturar o cliente quando o negócio for fechado. |
| Data de Entrega da Solicitação | Esta é a data de entrega solicitada pelo cliente. | Isso é usado como a data final ao criar datas de faturamento ao longo de uma frequência específica. |
| Copiar precificação | Um valor Sim/Não indica se o preço da cotação deve ser copiado da cotação original. | E se **Sim** for selecionado, a lista de preços do projeto e as referências da lista de preços do produto serão copiadas da cotação de origem para a cotação de destino. E se **Não** for selecionado, as listas de preços são padronizadas novamente com base nas listas de preços mais recentes que foram configuradas nos parâmetros da conta ou do projeto. |

Quando você seleciona **OK** na página da caixa de diálogo, o sistema cria uma cópia da cotação do projeto com base nos parâmetros selecionados na caixa de diálogo. A nova cotação do projeto é aberta. 

> [!NOTE]
> As seguintes informações não são copiadas da citação de origem para a de destino:
>
> - Agendamento de faturas
> - Cotação e clientes de linha de cotação
> - Referência do projeto nas linhas de orçamento baseadas no projeto - Informações sobre o orçamento do cliente
>
>Como essas informações são muito específicas para cada cotação, esses campos e registros não são copiados. Linhas de cotação para projetos e produtos, estimativas nos detalhes da linha de cotação e valores que não devem ser excedidos no nível de cotação são copiados. Os padrões de preço e taxa de custo dependem da opção **Preços de cópia** selecionada na página de diálogo **Parâmetros de cópia**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]