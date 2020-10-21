---
title: Cabeçalho de oportunidade
description: Este tópico fornece informações sobre negócios baseados em projeto e linhas de oportunidade com base em projeto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906063"
---
# <a name="opportunity-header"></a>Cabeçalho de oportunidade

_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_

O cabeçalho da oportunidade captura as informações gerais sobre um negócio baseado em projeto que se aplica a todas as linhas em uma oportunidade baseada em projeto.

Oportunidades baseadas em projeto no Dynamics 365 Project Operations são extensões de oportunidades no Dynamics 365 Sales. Essas extensões fornecem funcionalidade adicional que é específica e necessária para oportunidades baseadas em projetos. Essas extensões podem incluir novos campos e ações da faixa de opções disponíveis em oportunidades baseadas em projeto. Você pode encontrar alguns campos, funcionalidades e lógica padrão que estão disponíveis no Sales e não estão disponíveis no Operações de Projeto.

A tabela a seguir inclui os campos de uma oportunidade baseada em projeto que são exclusivos do Project Operations ou têm algumas mudanças importantes no comportamento de Oportunidades em comparação ao Sales.

| **Campo** | **Local** | **Relevância, finalidade e orientação** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Digitar | Guia geral (oculta) | O campo de conjunto de opções tem as seguintes opções:</br>- Baseado no trabalho (disponível apenas com o Project Operations)</br>- Baseado no item (disponível apenas quando o Project Operations e Sales estão instalados)</br>- Baseado em serviço de manutenção (disponível quando o Field Service está instalado) | Quando você usa o Project Operations, o valor deste campo é automaticamente definido como **Baseado em trabalho**, o que classifica a oportunidade como baseada em projeto. Uma oportunidade deve ser baseada em projeto para habilitar todas as extensões e funcionalidades específicas do projeto no processo de vendas posterior para este negócio. |
| Contato | Guia Geral | Referência ao contato principal do cliente para este negócio. | |
| Conta | Guia Geral | Referência à empresa do cliente ou registro de conta. | |
| Gerente de Contas | Guia Geral | O nome do gerente de contas desta oportunidade baseada em projeto. | O gerente de contas é responsável por gerenciar o relacionamento com o cliente até a conclusão deste projeto. Com base no registro de recurso reservável vinculado ao gerente de contas, a unidade de contratação é padronizada. |
| Unidade de Contratação | Guia Geral | A unidade organizacional responsável pela entrega do projeto ou projetos associados a este negócio. | A unidade de contratação é a divisão da empresa que concluirá os projetos após o fechamento do negócio. Cada unidade de contratação tem uma moeda, e essa moeda é usada para relatar os custos estimados e reais incorridos durante o projeto. |

Para todos os outros campos e seções da guia **Resumo** da oportunidade, consulte [Criar ou editar oportunidades (Sales and Hub de vendas)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
