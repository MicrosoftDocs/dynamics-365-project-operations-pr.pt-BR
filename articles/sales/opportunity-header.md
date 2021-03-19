---
title: Cabeçalho/resumo da oportunidade
description: Este tópico fornece informações sobre negócios baseados em projeto e linhas de oportunidade com base em projeto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c58c3696ae03e8a33a25a9483825a4b7cbf850be
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277684"
---
# <a name="opportunity-settings"></a>Configurações de oportunidade

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_


O cabeçalho da oportunidade, ou resumo, captura as informações gerais sobre um negócio baseado em projeto que se aplica a todas as linhas em uma oportunidade baseada em projeto.

As oportunidades baseadas em projeto no Dynamics 365 Project Operations são extensões de oportunidades no Dynamics 365 Sales. Essas extensões fornecem funcionalidade adicional que é específica e necessária para oportunidades baseadas em projetos. Essas extensões podem incluir novos campos e ações da faixa de opções disponíveis em oportunidades baseadas em projeto. Você pode encontrar alguns campos, funcionalidades e lógica padrão que estão disponíveis no Sales e não estão disponíveis no Operações de Projeto.

A tabela a seguir inclui os campos de uma oportunidade baseada em projeto que são exclusivos do Project Operations ou têm algumas mudanças importantes no comportamento de Oportunidades em comparação ao Sales.

| **Campo** | **Local** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Digitar | Guia geral (oculta) | O campo de conjunto de opções tem as seguintes opções:</br>- Baseado no trabalho (disponível apenas com o Project Operations)</br>- Baseado no item (disponível apenas quando o Project Operations e Sales estão instalados)</br>- Baseado em serviço de manutenção (disponível quando o Field Service está instalado) | Quando você usa o Project Operations, o valor deste campo é automaticamente definido como **Baseado em trabalho**, o que classifica a oportunidade como baseada em projeto. Uma oportunidade deve ser baseada em projeto para habilitar todas as extensões e funcionalidades específicas do projeto no processo de vendas posterior para este negócio. |
| Empresa Proprietária | Guia Geral | É a empresa ou pessoa jurídica que entregará o projeto para o cliente. | As informações deste campo serão copiadas para o campo correspondente na cotação do projeto que é criada a partir desta oportunidade. |
| Contato | Guia Geral | Referência ao contato principal do cliente para este negócio. | |
| Conta | Guia Geral | Referência à empresa do cliente ou registro de conta. | |
| Gerente de Contas | Guia Geral | O nome do gerente de contas desta oportunidade baseada em projeto. | O gerente de contas é responsável por gerenciar o relacionamento com o cliente até a conclusão deste projeto. Com base no registro de recurso reservável vinculado ao gerente de contas, a unidade de contratação é padronizada. |
| Unidade de Contratação | Guia Geral | A unidade organizacional responsável pela entrega do projeto ou projetos associados a este negócio. | A unidade de contratação é a divisão da empresa que concluirá os projetos após o fechamento do negócio. Cada unidade de contratação tem uma moeda, e essa moeda é usada para relatar os custos estimados e reais incorridos durante o projeto. |

Para todos os outros campos e seções da guia **Resumo** da oportunidade, consulte [Criar ou editar oportunidades (Sales and Hub de Vendas)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).


[!INCLUDE[footer-include](../includes/footer-banner.md)]