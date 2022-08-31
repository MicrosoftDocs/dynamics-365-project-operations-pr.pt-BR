---
title: Verificação de faturas de fornecedores com valores reais aprovados
description: Este artigo explica como o Microsoft Dynamics 365 Project Operations permite que gerentes de projeto verifiquem as faturas de fornecedores com os valores reais que foram aprovados conforme os contratados realizavam o trabalho e registravam as horas, e as despesas e materiais que foram usados pelos membros da equipe de projeto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ab9f69e36aa58bfe3a2f8e3455db66b6bceea968
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261732"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificação de faturas de fornecedores com valores reais aprovados

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

O Microsoft Dynamics 365 Project Operations permite que gerentes de projeto verifiquem as linhas da fatura de fornecedor das seguintes maneiras:

- Usando o campo **Status da verificação** nas linhas da fatura de fornecedor.
- Se as linhas da fatura de fornecedor fizerem referência a uma linha de subcontrato, vincule os dados reais de custo da atividade do subcontratado a essas linhas da fatura de fornecedor. O link é criado combinando os dados reais de custo com as linhas da fatura de fornecedor.

    > [!NOTE]
    > Embora seja possível rastrear o status de verificação de linhas da fatura de fornecedor que não fazem referência a um subcontrato, os dados reais de custo não podem ser vinculados a essas linhas da fatura de fornecedor.

## <a name="verification-status"></a>Status da verificação

O campo **Status da verificação** em uma linha da fatura de fornecedor indica esse status da verificação. Há suporte para os seguintes status:

1. Não Iniciado
2. Em andamento
3. Concluída

Linhas da fatura de fornecedor que têm o status de verificação **Não iniciado** podem ser editadas.

Linhas da fatura de fornecedor que têm o status de verificação **Em andamento** não podem mais ser editadas. Para uma linha da fatura de fornecedor que faz referência a um subcontrato, o status de verificação é definido automaticamente como **Em andamento** assim que o primeiro dado real de custo corresponde à linha da fatura de fornecedor.

Linhas da fatura de fornecedor que têm o status de verificação **Concluído** não podem mais ser editadas. Quando todas as linhas de uma fatura de fornecedor tiverem esse status de verificação, a fatura do fornecedor poderá ser confirmada.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Correspondendo os dados reais de custo com as linhas da fatura de fornecedor

A correspondência de dados reais de custo ajuda no processo de verificação em uma linha da fatura de fornecedor. Para corresponder os dados reais de custo com uma linha da fatura de fornecedor, siga estas etapas.

1. Abra a linha da fatura de fornecedor e selecione a guia **Dados de custo não correspondentes**. Uma grade mostra uma lista de dados reais de custo que fazem referência à mesma linha de subcontrato que a linha da fatura de fornecedor.
2. Selecione um ou mais dos dados reais de custo e selecione **Fazer a correspondência** na barra de ferramentas acima da grade. O sistema confirma se os dados reais de custo selecionados podem ser correspondidos. Depois que a validação é aprovada, os dados reais de custo são vinculados à linha da fatura de fornecedor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Critérios de validação usados para vincular dados reais de custo às linhas da fatura de fornecedor

Durante o processo de correspondência, será possível estabelecer um vínculo entre um dado real de custo e uma linha da fatura de fornecedor somente se as duas condições a seguir forem atendidas:

- Os campos **Status de ajuste** de todos os dados reais de custo selecionados devem estar em branco. Em outras palavras, os dados reais de custo não podem ter sido substituídos por outros dados reais de custo durante um processo de recall, cancelamento de aprovação ou diário de correção.
- É feita a correspondência dos valores dos campos a seguir entre a linha da fatura de fornecedor e dado real de custo selecionado. Se algum campo não estiver definido na linha da fatura de fornecedor, ele não será considerado para a correspondência.

    - Contrato de projeto
    - Linha de contrato do projeto
    - Classe da transação
    - Projeto
    - Tarefa
    - Categoria de recurso
    - Categoria da transação
    - Produto
    - Linha de subcontrato
    - Recurso reservável

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Desfazendo a correspondência de dados reais de custo com uma linha da fatura de fornecedor

A não correspondência de dados reais de custo também pode ajudar no processo de verificação em uma fatura de fornecedor, permitindo que links estabelecidos previamente sejam removidos. É possível cancelar a correspondência entre dados reais de custo e linhas da fatura de fornecedor que têm o status de verificação **Em andamento**. Para cancelar a correspondência de dados reais de custo com uma linha da fatura de fornecedor, siga estas etapas.

1. Abra a linha da fatura de fornecedor e selecione a guia **Dados de custo correspondentes**. Uma grade mostra uma lista de dados reais de custo que fazem referência à linha da fatura de fornecedor.
2. Selecione um ou mais dos dados reais de custo e selecione **Sem fazer a correspondência** na barra de ferramentas acima da grade.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
