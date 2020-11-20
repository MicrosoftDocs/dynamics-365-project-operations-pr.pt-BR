---
title: Criando um adiantamento ad hoc em um contrato – lite
description: Este tópico fornece informações sobre como criar um adiantamento em um contrato, conforme necessário.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181348"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Criando um adiantamento ad hoc em um contrato – lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

O Microsoft Dynamics 365 Project Operations oferece suporte a cenários de faturamento que envolvem pré-pagamentos e adiantamentos. O processo de uso de **Adiantamentos** no **Project Operations** é semelhante ao de contratos dos **Honorários**. 

Conclua as etapas a seguir para faturar o cliente por um adiantamento.

1. Vá até a página **Contrato do Projeto** e selecione a guia **Adiantamentos e Honorários**.
2. Na subgrade que lista todos os adiantamentos e pré-pagamentos registrados anteriormente, selecione **+ Novos honorários de contrato do Projeto**. 

    O formulário **Criação Rápida** é aberto para registrar um pré-pagamento ou adiantamento.
    
3. A tabela a seguir lista os campos para registrar um adiantamento e as considerações a ter em mente ao criar novos:

    | Campo | Descrição | Impacto a jusante |
    | --- | --- | --- |
    | **Cliente do Contrato do Projeto** | Este campo indica qual cliente no contrato será faturado para este adiantamento. | Se você tiver vários clientes no contrato e precisar faturar cada um deles por um valor específico de honorário ou adiantamento, crie manualmente um adiantamento para cada cliente individualmente. |
    | **Descrição** | A descrição do propósito ou momento do adiantamento para ajudar a identificar esse adiantamento. | Esta descrição é exibida na linha da fatura para este adiantamento. |
    | **Valor** | O valor do pré-pagamento ou adiantamento. | Este valor é exibido na linha da fatura para este adiantamento. |
    | **Data da Fatura** | A data em que esse adiantamento é faturado ao cliente. | Esta é a data para o processo automatizado de criação de fatura para criar uma linha de fatura para este adiantamento. |
    | **Status da Fatura** | Esta é uma configuração de opção que indica se este adiantamento é adicionado a uma fatura de rascunho para este cliente. Os valores possíveis são:</br>- **Não pronto para faturamento**</br>- **Pronto para faturamento** | Quando um adiantamento ou pré-pagamento é marcado como **Pronto para faturamento**, ele é adicionado como uma hora da linha em uma fatura de rascunho. Apenas um adiantamento totalmente faturado pode ser usado para reconciliar os custos do projeto para o próximo período da fatura. |

4. Selecione **Salvar e fechar** na caixa de diálogo de criação rápida para registrar o adiantamento ou o pré-pagamento.
