---
title: Novidades em abril de 2022 – Project Operations para cenários baseados em recurso/sem estoque
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de abril de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613238"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em abril de 2022 – Project Operations para cenários baseados em recurso/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.41.0.45
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.26

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

As categorias de compras podem ser usadas em ordens de compra do projeto e faturas de fornecedor pendentes. Para obter mais informações, consulte [Usar categorias de compras com ordens de compra do projeto e faturas de fornecedor pendentes](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

A tabela a seguir mostra os mapas de gravação dupla que foram modificados ou adicionados na versão de março de 2022 do Project Operations.

| Mapa de entidade | Versão atualizada | Comentários |
| -------------- | ------------------- | ------------|
| Entidade de exportação de linha de fatura de fornecedor do projeto de integração do Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Este mapa oferece suporte ao uso de categorias de compras com ordens de compra e faturas de fornecedor pendentes. |

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, à medida você atualizar a solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| ------------ | ---------------- | -------------- |
| Horas e despesas | 2573900 | O recurso **Aprovação Moderna** deve ser habilitado por padrão. |
| Cobrança e preço | 2603313 | Corrigido um erro de registro duplicado que impedia a adição de linhas de contrato e cotação que tivessem um produto. |
| Implantação e configuração | 2611368 | Os clientes devem ser capazes de adicionar até cinco entidades personalizadas à solução usando o designer de aplicativo moderno. |
| Horas e despesas | 2628285 | Corrigido um problema que afetava a capacidade de definir a categoria de recurso correta durante a importação de entrada de hora. |
| Gerenciamento de oportunidades| 2628815 | Atualize o limite de caracteres da descrição de detalhes da linha de cotação para corresponder ao limite de caracteres do assunto da tarefa, de modo que a importação seja bem-sucedida para tarefas em que o assunto tenha mais de 100 caracteres. |
| Horas e despesas| 2629547 | O campo **Enviado por** de aprovações de projeto deve apontar para o usuário que enviou o registro. |
| Horas e despesas| 2629865 | O campo **Copiar categoria** em tarefas quando os projetos são copiados. |
| Horas e despesas| 2636463 | Corrigidos os filtros de aprovações em formulários de aprovações modernos. |
| Planejamento e acompanhamento de projeto | 2648300 | Corrigido um problema que impedia que o proprietário do projeto fosse alterado. |
| Cobrança e preço | 2563000 | As linhas de diário para uma venda não cobrada em que a moeda difere da moeda do contrato não devem ser permitidas. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gerenciamento e contabilidade de projetos no Dynamics 365 Finance

Para obter informações sobre as correções de bug incluídas nesta atualização, entre no Microsoft Dynamics Lifecycle Services (LCS) e consulte o [artigo da Base de Dados de Conhecimento](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
