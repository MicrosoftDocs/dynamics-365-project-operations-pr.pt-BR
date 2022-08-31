---
title: Opções de subcontratação para membros da equipe do projeto
description: Este artigo explica as opções de subcontratação para membros da equipe do projeto no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5e0955d58365a4ecbe1c053882736f196758816e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261591"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opções de subcontratação para membros da equipe do projeto

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

No Microsoft Dynamics 365 Project Operations, é possível avaliar as opções de subcontratação disponíveis para um ou mais membros da equipe do projeto. As opções de subcontratação disponíveis permitem:

- Criar um subcontrato e/ou linhas em um subcontrato existente para os membros da equipe do projeto selecionados. 
- Reservar em um subcontrato e linha de subcontrato já existentes. 

Você pode escolher entre as opções de subcontratação disponíveis para membros genéricos da equipe do projeto ou escolher entre os membros da equipe do projeto que foram contratados com um recurso nomeado que é um trabalhador contratado. 

Não há opções de subcontratação disponíveis para o seguinte:

- Membros da equipe do projeto que foram contratados com um funcionário. 
- Membros da equipe do projeto que já estão associados a um subcontrato e linha de subcontrato. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontratação de um membro da equipe do projeto sem recursos

Para revisar e escolher entre as opções de subcontratação disponíveis para um membro da equipe do projeto genérico ou sem recursos, siga estas etapas:

1. Selecione um ou mais registros de membros da equipe do projeto em que o recurso é um recurso genérico.
2. Certifique-se de que nenhum dos registros de membros da equipe do projeto selecionados já esteja subcontratado. 
3. Selecione **Opções de subcontratação** na subgrade de membros da equipe do projeto. A caixa de diálogo **Opções de subcontratação** é aberta. 
4. Se você selecionou apenas um registro de membro da equipe do projeto na etapa 1, as seguintes opções estarão disponíveis:
    - Crie linhas de subcontrato. 
    - Reservar em um subcontrato existente. Se você selecionou vários registros de membros da equipe do projeto na etapa 1, a única opção disponível é criar linhas de subcontrato.
5. A opção de reservar em uma linha de subcontrato existente permite selecionar um subcontrato e uma linha de subcontrato na qual você deseja reservar. Ao selecionar uma linha de subcontrato para capacidade reserva, você deve garantir que a linha de subcontrato selecionada seja por tempo e que a função exigida no membro da equipe do projeto corresponda à função que foi adquirida na linha de subcontrato.
6. Ao selecionar a criação de linhas de subcontrato para os membros da equipe do projeto, o sistema permitirá que você selecione o subcontrato que deseja criar para essas linhas. O subcontrato selecionado para criar linhas deve estar no status **Rascunho**. Com essa opção para criar linhas de subcontrato para os membros da equipe do projeto selecionados, o sistema criará uma linha de subcontrato por tempo para cada membro da equipe do projeto. A função, horas e datas serão copiadas do membro da equipe do projeto para cada linha de subcontrato criada. 
7. Quando um membro de equipe genérico é associado a um subcontrato e uma linha de subcontrato, o campo **Tipo de trabalhador** na linha do membro de equipe genérico será atualizado para **Trabalhador do Contrato** e o valor **Validade de Subcontrato** será definido como **Válido**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontratação de um membro da equipe do projeto com recursos

Assim como os membros de equipe genéricos ou sem recursos, você também pode exibir as opções de subcontratação para um membro da equipe do projeto com recursos, desde que este seja um trabalhador contratado. Para revisar e escolher entre as opções de subcontratação disponíveis para um membro da equipe do projeto com recursos ou nomeado, siga estas etapas:

1. Selecione um ou mais registros de membros da equipe do projeto em que o recurso é um trabalhador contratado nomeado.
2. Certifique-se de que nenhum dos registros de membros da equipe do projeto selecionados já esteja subcontratado. 
3. Selecione **Opções de subcontratação** na subgrade de membros da equipe do projeto. A caixa de diálogo **Opções de subcontratação** é aberta. 
4. Se você selecionou apenas um registro de membro da equipe do projeto na etapa 1, as seguintes opções estarão disponíveis:
      - Crie linhas de subcontrato.
      - Reserve em um subcontrato existente.
  Se você selecionou vários registros de membros da equipe do projeto na etapa 1, a única opção disponível é criar linhas de subcontrato.
5. A opção de reservar em uma linha de subcontrato existente permite selecionar um subcontrato e uma linha de subcontrato na qual você deseja reservar. Ao selecionar uma linha de subcontrato para capacidade reserva, você deve garantir o seguinte:
      - A linha de subcontrato selecionada é por tempo. 
      - A função exigida no membro da equipe do projeto corresponde à função adquirida na linha de subcontrato. 
      - O fornecedor ao qual o trabalhador contratado está associado é o mesmo que o fornecedor no subcontrato.
6. Ao selecionar a criação de linhas de subcontrato para os membros da equipe do projeto, o sistema permitirá que você selecione o subcontrato que deseja criar para essas linhas. Com essa opção, você deve garantir que o fornecedor ao qual o trabalhador contratado pertence seja o mesmo fornecedor do subcontrato. 
7. O subcontrato selecionado para criar linhas deve estar no status **Rascunho**. Com essa opção para criar linhas de subcontrato para os membros da equipe do projeto selecionados, o sistema criará uma linha de subcontrato por tempo para cada membro da equipe do projeto. A função, horas e datas serão copiadas do membro da equipe do projeto para cada linha de subcontrato criada.  
8. Quando um membro de equipe nomeado é associado a um subcontrato e uma linha de subcontrato, o campo **Tipo de trabalhador** na linha do membro de equipe nomeado será atualizado para **Trabalhador do Contrato** e o valor **Validade de Subcontrato** será definido como **Válido**.

## <a name="re-costing-subcontractor-assignments"></a>Nova precificação de atribuições de subcontratados

Quando um membro da equipe do projeto (genérico ou nomeado) é vinculado a linhas de subcontrato usando a caixa de diálogo **Opções de subcontratação**, todas as atribuições de tarefas que o membro da equipe tiver serão recalculadas com base na lista de preços de compra anexada ao subcontrato. Na guia **Estimativas** na página **Detalhes do Projeto**, selecione o botão **Atualizar preços** para ver os preços e/ou custos atualizados resultantes da decisão de subcontratar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
