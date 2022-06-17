---
title: Recrutando trabalhadores contratados e capacidade subcontratada para um projeto
description: Este artigo explica como os requisitos do projeto podem ser atendidos usando trabalhadores contratados ou capacidade subcontratada no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 173e1c20d2d046ee2120ec178e51d4868b70847d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922070"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Recrutando trabalhadores contratados e capacidade subcontratada para um projeto

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Os membros genéricos da equipe do projeto podem ter funcionários ou trabalhadores contratados. Ao criar um projeto com trabalhadores contratados, você pode limitar suas opções de contratação a trabalhadores contratados específicos atribuídos a uma linha de subcontrato. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Pesquisar requisitos de recursos de equipe com trabalhadores contratados que pertencem a uma linha de subcontrato específica

Para pesquisar requisitos de recursos de equipe com trabalhadores contratados que pertencem a uma linha de subcontrato específica, siga estas etapas:

1. Crie um membro da equipe do projeto genérico que faça referência a um subcontrato e uma linha de subcontrato.
2. Gere um requisito de recurso para este membro da equipe do projeto genérico usando o botão **Gerar Requisito** na subgrade dos membros da equipe do projeto.
3. Selecione a linha do membro da equipe e depois o botão **Reservar** na subgrade. 
4. Isso abre o Painel de Agendamento com o contexto do requisito. Juntamente com outros atributos, como datas, função e campos de unidade organizacional, os filtros do Painel de Agendamento também são preenchidos automaticamente com os campos de fornecedor, subcontrato e linha de subcontrato do requisito do recurso.
5. O sistema procura os recursos que atendem aos critérios do filtro e os lista. 
6. Selecione um dos recursos filtrados e reserve o recurso para o requisito. 
7. Um membro da equipe do projeto é criado e atualizado com referências de subcontrato e linha de subcontrato. Acesse **Estimativas de projeto** e selecione **Atualizar preços** para ver o custo atualizado da atribuição de recursos. 

> [!NOTE]
> A atualização do membro da equipe do projeto com uma referência de subcontrato e linha de subcontrato nem sempre será possível durante a reserva se o recurso for atribuído a várias linhas de subcontrato. Se o sistema não puder atualizar o membro da equipe do projeto com um subcontrato e uma linha de subcontrato, abra o registro do membro da equipe do projeto e atualize manualmente esses campos para que a estimativa de custo financeiro reflita com precisão o custo do subcontratado.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Pesquisar requisitos de recursos da equipe com qualquer trabalhador contratado

Para pesquisar requisitos de recursos da equipe com qualquer trabalhador contratado, siga estas etapas:

1. Crie um membro da equipe do projeto genérico.
2. Gere um requisito de recurso para este membro da equipe do projeto genérico usando o botão **Gerar Requisito** na subgrade dos membros da equipe do projeto.
3. Selecione a linha do membro da equipe e depois o botão **Reservar** na subgrade. 
4. Isso abre o Painel de Agendamento com o contexto do requisito. Juntamente com outros atributos, como datas, função e campos de unidade organizacional, os filtros do Painel de Agendamento também são preenchidos automaticamente com os campos de fornecedor, subcontrato e linha de subcontrato do requisito do recurso. Como o requisito não tinha nenhum valor de subcontrato ou linha de subcontrato preenchido, esses atributos estarão vazios no painel de filtro.
5. O sistema procura os recursos que atendem aos critérios do filtro e os lista.
6. Atualize o campo **Tipo de trabalhador** no painel de filtro para **Trabalhador do Contrato** para limitar a pesquisa a trabalhadores contratados. Atualize o **Fornecedor** no painel de filtro para selecionar um fornecedor e limitar a pesquisa para mostrar apenas trabalhadores contratados que pertencem a uma empresa fornecedora específica.
7. Selecione um trabalhador contratado na lista e reserve o recurso para o requisito.
8. Um membro da equipe do projeto é criado. Contudo, o membro da equipe do projeto não é atualizado com nenhum subcontrato ou linha de subcontrato e, portanto, a atribuição de recursos não será custeada com o preço do subcontrato. Atualize manualmente o membro da equipe do projeto com uma linha de subcontrato e vá para **Estimativas do Projeto** e selecione **Atualizar preços** para ver o custo atualizado da atribuição de recursos.

> [!NOTE]
> Os membros da equipe do projeto com **Tipo de trabalhador** como **Trabalhador do Contrato**, mas sem uma referência de subcontrato, são sinalizados como **Inválidos** na grade **Membros da equipe de projeto**. Se houver algum membro da equipe do projeto com esse status, abra o registro do membro da equipe do projeto e atualize manualmente os campos de subcontrato e linha de subcontrato para que a estimativa de custo financeiro reflita com precisão o custo do subcontratado na guia **Estimativas**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
