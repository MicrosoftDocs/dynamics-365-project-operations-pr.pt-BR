---
title: Copiar contratos de projeto - lite
description: Este artigo fornece informações sobre como copiar contratos de projeto no Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a1846af677f7cea3ec22fdba4408f2bbd7db8a3c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932604"
---
# <a name="copy-project-contracts---lite"></a>Copiar contratos de projeto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Você pode criar facilmente novos contratos de projeto fazendo cópias dos contratos existentes de uma das seguintes maneiras: 

  - Na página de listagem **Contratos de Projeto**, selecione um contrato de projeto e selecione **Copiar**.
  - Na página **Contrato de Projeto**, selecione **Copiar**.

Uma página de diálogo será aberta, onde você poderá selecionar os parâmetros do contrato copiado. Os campos a seguir são incluídos no diálogo. Dependendo dos valores que você selecionar nesse diálogo, o processo de cópia poderá mudar.

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Tópico | Insira o tópico do contrato de destino. Quando a página de diálogo for aberta, o sistema definirá esse campo com o nome do contrato de origem com **cópia** acrescentado. | Não há impacto posterior para esse campo. |
| Cliente | Referência à empresa do cliente ou registro de conta. Quando a caixa de diálogo for aberta, o sistema definirá esse campo para a conta no contrato de origem. | Esse campo é o cliente principal no contrato. |
| Unidade de Contratação | A Unidade organizacional responsável pela entrega do projeto ou projetos associados a este negócio. Quando a página de diálogo for aberta, o sistema irá configurá-lo para a unidade de contratação no contrato de origem. | A unidade de contratação é a divisão da empresa que executará os projetos após o fechamento do negócio. Cada unidade contratante tem uma moeda. Essa moeda é usada para relatar os custos estimados e reais incorridos durante o projeto. |
| Moeda | A moeda de transação do negócio. Quando a página de diálogo for aberta, o sistema definirá o campo como a moeda do contrato de origem. A moeda pode ser alterada. Se for, o campo **Copiar Preços** sempre será definido como **Não** porque as listas de preços no contrato de origem não serão mais relevantes. | A moeda é usada para listas de preços padrão, para a criação de estimativas financeiras no contrato e para faturar o cliente quando o negócio for ganho. |
| Data de Entrega da Solicitação | A data de entrega solicitada pelo cliente. | Essa data é usada como a data de término quando você criar datas de faturamento ao longo de uma frequência específica. |
| Copiar precificação | Indica se os preços no contrato deverão ser copiados do contrato de origem. | Se o campo estiver definido como **Sim**, as referências de lista de preços de projeto e produto serão copiadas do contrato de origem para o contrato de destino. Se **Não** estiver selecionado, as listas de preços terão o padrão baseado nas listas de preços mais recentes nos parâmetros de conta ou de projeto. |

Quando você seleciona **OK** na página de diálogo, o sistema cria uma cópia do contrato com base nos parâmetros selecionados. O novo contrato será aberto.

As seguintes informações não são copiadas da **Origem** para o **Contrato de Destino**:

  - Agendamento de faturas
  - Clientes de contrato e de linha de contrato
  - Referência de projeto nas linhas de contrato baseadas em projeto
  - Informações de orçamento do cliente

Como essas informações são específicas para cada contrato, esses campos e registros não são copiados. Linhas de contrato para projetos e produtos, estimativas em detalhes da linha de contrato e valores que não devem ser excedidos no nível de contrato são copiados. Os padrões de preço e taxa de custo dependem da seleção no campo **Preços de cópia** na página de diálogo **Parâmetros de Cópia**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]