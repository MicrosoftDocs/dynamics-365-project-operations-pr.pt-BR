---
title: Etapas da linha de subcontrato
description: Este tópico explica como criar e manter uma agenda de faturamento com base em marcos para um subcontrato com um fornecedor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d1c30f48e0d43aa55e2c1650637f7f102fb200de
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579108"
---
# <a name="subcontract-line-milestones"></a>Etapas da linha de subcontrato

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

No Dynamics 365 Project Operations, uma linha de subcontrato com um método de cobrança de preço fixo pode especificar uma agenda de fatura baseada em marcos com o fornecedor.

Os marcos para o faturamento do fornecedor podem ser gerados automaticamente usando uma frequência definida ou você pode criá-los manualmente.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Crie automaticamente uma agenda de fatura baseada em marcos para uma linha de subcontrato

Conclua as etapas a seguir para gerar automaticamente uma agenda de fatura baseada em marcos para um conjunto fixo de marcos igualmente distribuídos.

1. Acesse **Configurações** > **Frequências de Fatura** e configure a frequência da fatura para as linhas de subcontrato.
2. Abra a página **Subcontratos**, abra o subcontrato com o qual deseja trabalhar e, em seguida, abra a linha de subcontrato de preço fixo para a qual você criará uma agenda de marcos.
3. Na guia **Marcos da Linha de Subcontrato**, selecione **Gerar Marcos Periódicos**.
4. Na caixa de diálogo, insira ou selecione um intervalo de datas, o número de marcos e a frequência da fatura. Você pode selecionar uma data de início ou pode selecionar o número de marcos e a frequência da fatura ou data de início, ou pode selecionar a data de término e a frequência da fatura. Você não pode selecionar a data de término e o número de marcos.
Usando essas informações, o sistema gera marcos e registros mostrados na grade **Marcos**.

   - **Nome do Marco** - o nome do marco é definido com a data do marco com base na frequência da fatura.
   - **Data do Marco** - a data com base na frequência da fatura.
   - **Valor do Marco** - calculado por meio da divisão do valor do subtotal na linha de subcontrato pelo número de marcos.

Se a linha de subcontrato tiver um valor no campo **Valor Estimado do Imposto**, esse valor será adicionado a cada marco igualmente ao gerar marcos periódicos.

A soma dos valores de marco da linha de subcontrato deve ser igual ao valor da linha de subcontrato. Se elas não forem iguais, ocorrerá um erro. Você pode corrigir o erro e verificar se o total do marco é igual ao valor da linha de subcontrato criando, editando ou excluindo valores do marco e impostos. Depois que as alterações forem feitas, salve e atualize a página para garantir que não haja mais erros.

## <a name="manually-create-subcontract-line-milestones"></a>Criar manualmente marcos de linha de subcontrato

Os marcos de preço fixo em uma linha de subcontrato poderão ser gerados manualmente quando não forem divididos periodicamente. Para criar um marco de linha de subcontrato manualmente, conclua as etapas a seguir.

1. No painel de navegação, selecione **Subcontratos** e abra o subcontrato com o qual deseja trabalhar.
2. Abra a linha de subcontrato de preço fixo para a qual deseja criar um marco.
3. Na guia **Marcos de linha de subcontrato**, na subgrade, selecione **+ Novo Marco de Linha de Subcontrato**.
4. Na página **Novo Marco de Linha de Subcontrato**, insira as informações necessárias com base na tabela a seguir.

    | Campo | Descrição |Impacto funcional|
    | --- | --- |----------------------|
    | Nome da Etapa | O nome da etapa. |Isso será exibido como a primeira coluna em todas as pesquisas baseadas em etapas da linha de subcontrato. A linha da fatura do fornecedor criada com base nesta etapa também usará o nome da etapa da linha de subcontrato como o nome padrão da linha da fatura do fornecedor.|
    | Descrição | Uma descrição do marco. |A linha da fatura do fornecedor criada com base nesta etapa também usará a descrição da etapa da linha de subcontrato como a descrição padrão da linha da fatura do fornecedor.|
    | Data da Etapa | A data em que o processo de criação automática de fatura deve procurar o status desse marco para considerá-lo para o faturamento.| Este valor será usado como a data padrão da linha da fatura do fornecedor ao faturar para esta linha do subcontrato. |
    | Amount | A quantidade ou valor da etapa que será faturada para o cliente. |Este valor é usado como o valor padrão na linha da fatura do fornecedor ao faturar para esta linha do subcontrato. |
    | Imposto | O valor do imposto aplicado na etapa.| Este valor é usado como o valor padrão do imposto na linha da fatura do fornecedor ao faturar para esta linha do subcontrato. |
    | Valor após imposto | Este campo somente leitura é calculado como Valor + Imposto.|Este valor é usado como o padrão na linha da fatura do fornecedor ao faturar para esta linha do subcontrato. |
    | Status da Fatura | Quando o marco for criado, esse status sempre será definido como **Não está pronto para faturamento**.|  Quando o status for **Pronto para Faturar**, a criação da fatura do fornecedor incluirá esse marco na fatura do fornecedor. |

5. Selecione **Salvar e Fechar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
