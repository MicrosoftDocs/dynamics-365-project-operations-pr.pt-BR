---
title: Gerenciamento de subcontratos no Project Operations
description: Este artigo fornece uma visão geral do processo de gerenciamento de subcontratos de ponta a ponta normalmente em organizações baseadas em projetos.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f5e025b5f741935494349fb1bdfd3a19bacb5e1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911490"
---
# <a name="subcontract-management-in-project-operations"></a>Gerenciamento de subcontratos no Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este artigo fornece uma visão geral do processo de gerenciamento de subcontratos de ponta a ponta em organizações baseadas em projetos. A subcontratação de serviços geralmente segue o fluxo do processo empresarial mostrado no diagrama a seguir.

![Fluxo do processo de subcontratação](../media/SubcontractingProcessFlow.png)

A lista a seguir fornece uma descrição passo a passo do processo de subcontratação.

1. O gerente de projeto cria um subcontrato com um fornecedor. Por padrão, as listas de preços anexadas ao registro do fornecedor são usadas para o subcontrato. A conta do fornecedor tem um tipo de relacionamento de **Fornecedor** ou **Provedor**.
2. O gerente de projeto pode discriminar todas as compras como itens de linha no subcontrato. As linhas do subcontrato podem ser por tempo, despesas ou produtos. A classe de transação da linha de subcontrato determina para que serve a linha.
3. O gerente de conta do fornecedor e o gerente de projeto podem iterar no subcontrato. O preço pode ser ajustado nas listas de preços de compra que são anexadas ao subcontrato.
4. Nesse ponto ou posteriormente no processo, se a linha de subcontrato for para tempo, o gerente de conta do fornecedor associa os contatos de fornecedor a cada linha de subcontrato. Essa associação fornece informações ao gerente de projeto que está trabalhando no subcontrato. Quando um contato de fornecedor é associado a uma linha de subcontrato, o sistema cria automaticamente um recurso reservável direto do contato, se um recurso reservável ainda não existir.
5. O método de faturamento em cada linha do subcontrato pode ser **Preço fixo** ou **Tempo e Material**. Para linhas do subcontrato de preço fixo, uma agenda de faturamento baseada em marcos é configurada.
6.  Depois que o subcontrato for configurado e a negociação for concluída, ele será confirmado. Os subcontratos confirmados não podem ser editados, mas se ocorrerem alterações, um subcontrato pode ser "reaberto para edição", o que define o status **Confirmado** novamente como **Rascunho** e a negociação pode ser reaberta. 
7.  Ao criar um membro genérico da equipe em um projeto, o membro da equipe poderá ser associado a uma linha de subcontrato. Isso indica a necessidade de equipar o membro da equipe genérico com capacidade de subcontratado.
8.  Os membros nomeados da equipe podem ser criados diretamente em um projeto ou criados reservando-os usando as experiências de agendamento de recursos. Se um membro nomeado da equipe do projeto for um trabalhador contratado, será possível associá-lo a uma linha de subcontrato. Isso reduzirá a capacidade disponível em uma linha de subcontrato.
9.  Os recursos do subcontratado podem registrar tempo, despesas e uso de material em projetos e tarefas de projeto e, em seguida, enviar para aprovação. Isso é semelhante para os funcionários. Ao registrar o tempo, um trabalhador contratado pode selecionar um subcontrato específico e uma linha de subcontrato.
10. Após a aprovação, o tempo aprovado pelos subcontratos registrará os custos reais do projeto com base no preço de compra do trabalhador contratado ou na função que desempenhou no projeto.
11. Faturas de fornecedor e itens de linha de faturas de fornecedor podem ser registrados no sistema para o trabalho executado por recursos do fornecedor ou produtos entregues pelo fornecedor. As linhas da fatura do fornecedor devem ser específicas para um projeto e para uma classe de transação de tempo, despesa, produto/material, marco ou valor. Opcionalmente, as linhas da fatura do fornecedor podem fazer referência a uma linha de subcontrato.
12. O sistema associará automaticamente todos os custos reais que correspondam à linha de subcontrato e ao projeto à fatura do fornecedor. Isso facilitará um processo de correspondência e verificação de 3 vias.
13. O gerente de projeto pode então revisar os dados reais do projeto correspondidos automaticamente, remover ou adicionar outros dados estatísticos de custo do projeto e concluir o processo de verificação.
14. Concluir o processo de verificação em todas as linhas marcará a fatura do fornecedor como **Pronto para Pagamento**. Nesse estágio, a fatura e as linhas do fornecedor podem ser transferidas para um sistema de Contabilidade ou Contas a Pagar para processar o pagamento ao fornecedor. Os custos do projeto registrados anteriormente serão revertidos e os custos reais da linha da fatura do fornecedor serão registrados no projeto.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Linhas de subcontrato baseadas em quantidade e linhas de subcontrato baseadas em trabalho

Uma linha de subcontrato pode ser baseada em quantidade ou baseada em trabalho. 

Quando uma linha de subcontrato for **baseada em quantidade**, a quantidade sendo comprada na linha de subcontrato para tempo, despesa ou material poderá ser usada em qualquer projeto.

Quando uma linha de subcontrato for **baseado em trabalho**, a linha de subcontrato será mapeada para um corpo de trabalho representado por um nó no plano do projeto. O valor da linha de subcontrato é a soma de todos os componentes necessários para entregar aquele corpo de trabalho. Eles são modelados como detalhes da linha de subcontrato e podem ser um conjunto de tempo, despesas ou materiais. Para uma linha de subcontrato baseada em trabalho, a linha de subcontrato também é dedicada a um único projeto. No momento, esses tipos de subcontratos não são aceitos pelo Project Operations.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

