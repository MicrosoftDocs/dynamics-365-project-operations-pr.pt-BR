---
title: Unidades e grupos de unidades
description: Este artigo fornece informações sobre como criar unidades e grupos de unidades no Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a46b7d182d3d7fc77c1275c108f5dc569ffebff1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921426"
---
# <a name="units-and-unit-groups"></a>Unidades e grupos de unidades

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As unidades são as quantidades ou as medidas em que você vende seus produtos ou serviços. Por exemplo, se você vende produtos de jardinagem, é possível vender sementes em unidades de pacotes, caixas e paletes. Um grupo de unidades é uma coleção dessas unidades diferentes.

Para concluir as etapas deste artigo, verifique se você foi atribuído à função de administrador do sistema ou gerente profissional de vendas ou se tem permissões equivalentes.

## <a name="create-a-unit-group"></a>Criar um grupo de unidades

1. No mapa do site, selecione **Unidades**.
2. Selecione **Novo** e, na caixa de diálogo **Criar Grupo de Unidades**, insira o nome da unidade.
3. No campo **Unidade principal**, insira a menor unidade de medida comum em que o produto será vendido. Por exemplo, você pode inserir "peça" ou "onça".
4. Selecione **OK**.

## <a name="add-units-to-a-unit-group"></a>Adicionar unidades a um grupo de unidades

1. Abra um grupo de unidades e, na guia **Relacionado**, selecione **Unidades**. Você verá que a unidade principal já foi adicionada.
2. Selecione **Adicionar Nova Unidade** e, na página **Criação Rápida: Unidade**, no campo **Nome**, insira o nome da unidade.
3. No campo **Quantidade**, insira a quantidade que a unidade conterá. Por exemplo, se uma caixa contiver duas peças, insira "2". 
4. No campo **Unidade base**, selecione uma unidade base para estabelecer a menor unidade de medida para a unidade. Por exemplo, você pode selecionar "Peça".
5. Selecione **Salvar**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]