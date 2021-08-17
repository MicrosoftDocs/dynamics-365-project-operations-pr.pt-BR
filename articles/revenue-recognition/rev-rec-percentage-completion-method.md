---
title: Estimativa de receita de projeto de preço fixo
description: Este tópico fornece informações sobre receita de preço fixo em projetos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 451f0403f0111b5ea4de6c91b54eae157830e413d3a21f23bd841a66905e147b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006412"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Estimativa de receita de projeto de preço fixo 

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Quando você cria uma linha de contrato de projeto com os atributos a seguir no Dynamics 365 Project Operations no Microsoft Dataverse, o sistema cria automaticamente uma estimativa de projeto de receita de preço fixo. As informações neste projeto são baseadas em:

  - Um método de cobrança de preço fixo.
  - Um projeto associado.
  - Pelo menos um marco definido na guia **Agenda de faturas** na página **Linha de contrato do projeto**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Revisar estimativas de projetos de receita de preço fixo
Para revisar estimativas de projetos de receita de preço fixo, conclua as seguintes etapas:

1. No ambiente do Dynamics 365 Finance, acesse **Gerenciamento e contabilidade de projetos** > **Projetos** > **Estimativa de projetos de receita de preço fixo**.
2. Selecione o projeto que você deseja exibir e clique duas vezes em **Estimar ID do projeto** para abrir o registro e revisar os detalhes do projeto.
3. Expanda a guia **Projeto**. Você verá um projeto na grade **Projetos selecionados**. O sistema usa este como o projeto padrão porque ele é o projeto associado à linha de contrato do projeto. 
4. Para alterar a associação, selecione projetos adicionais e adicione-os à grade **Projetos selecionados**. Se vários projetos forem selecionados nesta grade, a porcentagem de conclusão do projeto e as estimativas de receita serão calculadas em conjunto para todos os projetos selecionados.

  O custo do projeto, o perfil de receita, o modelo de custo e o código do período podem ser definidos manualmente. Se eles não forem definidos manualmente, os valores serão padronizados durante o primeiro cálculo da estimativa para o projeto usando as regras configuradas para perfis de custo e receita do projeto.



[!INCLUDE[footer-include](../includes/footer-banner.md)]