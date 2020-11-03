---
title: Unidades e grupos de unidades
description: Este tópico fornece informações sobre como criar unidades e grupos de unidades no Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071551"
---
# <a name="units-and-unit-groups"></a>Unidades e grupos de unidades

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

As unidades são as quantidades ou as medidas em que você vende seus produtos ou serviços. Por exemplo, se você vende produtos de jardinagem, é possível vender sementes em unidades de pacotes, caixas e paletes. Um grupo de unidades é uma coleção dessas unidades diferentes.

Para concluir as etapas neste tópico, verifique se você foi atribuído à função Administrador do Sistema ou Gerente do Sales Professional ou se tem permissões equivalentes.

## <a name="create-a-unit-group"></a>Criar um grupo de unidades

1. No mapa do site, selecione **Unidades**.
2. Selecione **Novo** e, na caixa de diálogo **Criar Grupo de Unidades** , insira o nome da unidade.
3. No campo **Unidade principal** , insira a menor unidade de medida comum em que o produto será vendido. Por exemplo, você pode inserir "peça" ou "onça".
4. Selecione **OK**.

## <a name="add-units-to-a-unit-group"></a>Adicionar unidades a um grupo de unidades

1. Abra um grupo de unidades e, na guia **Relacionado** , selecione **Unidades**. Você verá que a unidade principal já foi adicionada.
2. Selecione **Adicionar Nova Unidade** e, na página **Criação Rápida: Unidade** , no campo **Nome** , insira o nome da unidade.
3. No campo **Quantidade** , insira a quantidade que a unidade conterá. Por exemplo, se uma caixa contiver duas peças, insira "2". 
4. No campo **Unidade base** , selecione uma unidade base para estabelecer a menor unidade de medida para a unidade. Por exemplo, você pode selecionar "Peça".
5. Selecione **Salvar**.
