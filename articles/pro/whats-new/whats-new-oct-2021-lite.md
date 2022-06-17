---
title: Novidades de outubro de 2021 – implantação do Project Operations lite
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de outubro de 2021 da implantação do Project Operations lite.
author: sigitac
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7199853bea7e8e99a2a1ce19d6ce88736edb38f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921932"
---
# <a name="whats-new-october-2021---project-operations-lite-deployment"></a>Novidades de outubro de 2021 – implantação do Project Operations lite

_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_

Este artigo se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations no ambiente do Microsoft Dataverse versão 4.25.0.91


## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

[Gerenciamento de subcontratos](../subcontracting/managing-subcontracts-overview.md): este recurso oferece a possibilidade de criar um subcontrato com o fornecedor, discriminar todas as compras como itens de linha no subcontrato, ajustar os preços e associar os contatos.


## <a name="quality-updates"></a>Atualizações de qualidade

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Cobrança e preço | 2209402 | Corrigidas as validações que impediam que os valores retidos fossem faturados quando um contrato de projeto fosse confirmado. |
| Gerenciamento de oportunidades | 2227414 | Os campos **Produto**, **Fora do Catálogo** e **IsProductOverriden** são copiados para os detalhes da linha da cotação e para os detalhes da linha do contrato. |
| Cobrança e preço | 2338357 | A moeda no registro de uso de material deverá usar como padrão a moeda do projeto quando o projeto for selecionado. |
| Horas e despesas | 2414777 | Deve ser possível cancelar uma aprovação quando a entrada de despesas ou horas tiver mais de uma aprovação de projeto associada. |
