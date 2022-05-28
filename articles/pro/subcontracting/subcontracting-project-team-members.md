---
title: Subcontratando membros da equipe do projeto
description: Este tópico explica como subcontratar membros da equipe do projeto no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f43f817e59ef83fbf4dda6267327080f7c56e0f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587817"
---
# <a name="subcontracting-project-team-members"></a>Subcontratando membros da equipe do projeto

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

No Microsoft Dynamics 365 Project Operations, você pode optar por subcontratar membros da equipe do projeto sem recursos ou com recursos.

- Os membros da equipe do projeto sem recursos têm um recurso genérico atribuído.
- Os membros da equipe com recursos têm um recurso nomeado atribuído.

Quando você vincula um membro da equipe do projeto a uma linha de subcontrato, qualquer atribuição a tarefas que o membro da equipe tenha será refeita com base na lista de preços de compra anexada ao subcontrato.  Na guia **Estimativas** na página **Detalhes do Projeto**, selecione o botão **Atualizar preços** para ver os preços e/ou custos atualizados resultantes da decisão de subcontratar. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontratação de um membro da equipe do projeto sem recursos
A página **Detalhes do membro da equipe** tem campos de subcontrato e linha de subcontrato que permitem que um gerente de projeto expresse como gostaria de extrair a capacidade necessária de um subcontrato. Para subcontratar um membro da equipe do projeto como um recurso genérico, siga estas etapas:

1.  Escolha um subcontrato na página **Detalhe do membro da equipe**.

2.  Você só pode selecionar subcontratos com status **Rascunho** ou **Confirmado**. Subcontratos **Fechados** ou **Cancelados** não podem ser selecionados. 

3.  O campo **Linha de contrato** fica visível depois que você seleciona um subcontrato.

4.  No campo **Linha de subcontrato**, você só pode selecionar linhas de subcontrato que são por tempo. Não é possível selecionar linhas de subcontrato para despesas ou materiais.

5.  A função para o registro do membro da equipe do projeto precisa corresponder à função na linha de subcontrato. Isso garante que o tempo para a função que está sendo estimada no projeto seja a mesma função adquirida na linha de subcontrato. 

Quando um membro de equipe genérico é associado a um subcontrato e uma linha de subcontrato, o campo **Tipo de trabalhador** na linha do membro de equipe genérico será atualizado para **Trabalhador do Contrato** e **Validade de Subcontrato** será definido como **Válido**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontratação de um membro da equipe do projeto com recursos
Assim como os membros de equipe genéricos ou sem recursos, a capacidade do membro da equipe necessária em um projeto também pode ser vinculada a um subcontrato. Para subcontratar um membro da equipe do projeto nomeado, siga estas etapas:

1.  Certifique-se de que o recurso nomeado esteja configurado como um tipo de recurso reservável de trabalhador contratado. Além disso, certifique-se de que o campo **Fornecedor** no recurso reservável corresponda ao fornecedor no subcontrato selecionado. 

2.  Você só pode selecionar subcontratos com status **Rascunho** ou **Confirmado**. Subcontratos **Fechados** ou **Cancelados** não podem ser selecionados. 

3.  O campo **Linha de contrato** fica visível depois que você seleciona um subcontrato.

4.  No campo **Linha de subcontrato**, você só pode selecionar linhas de subcontrato que são por tempo. Não é possível selecionar linhas de subcontrato para despesas ou materiais.

5.  A função para o registro do membro da equipe do projeto precisa corresponder à função na linha de subcontrato. Isso garante que o tempo para a função que está sendo estimada no projeto seja a mesma função adquirida na linha de subcontrato. 

Os membros da equipe do projeto configurados nomeados como um tipo de trabalhador contratado de **Recurso reservável** serão exibidos com um status de validade de subcontrato de **Não válido** se não estiverem vinculados a um subcontrato. Quando um membro da equipe do projeto nomeado estiver associado a um subcontrato e uma linha de subcontrato, o campo **Tipo de trabalho** na linha do membro da equipe será atualizado para **Trabalhador do Contrato** e **Validade de Subcontrato** será definido como **Válido**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
