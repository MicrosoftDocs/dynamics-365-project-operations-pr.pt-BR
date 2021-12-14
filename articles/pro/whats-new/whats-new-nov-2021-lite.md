---
title: Novidades de novembro de 2021 – implantação do Project Operations lite
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de novembro de 2021 da implantação do Project Operations lite.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e8560e7c7d6bae1bb2fda389a63bde1c57654bcb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827267"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Novidades de novembro de 2021 – implantação do Project Operations lite

_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_

Este tópico se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em uma versão 4.26.0.145, 4.26.0.148 ou 4.26.0.150 do ambiente do Dataverse
  
## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

- As interfaces de programação de aplicativos (APIs) de agendamento de projetos agora permitem criar e excluir buckets de projetos

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-in-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Cobrança e preço | 2358236 | A correção da fatura deve permitir correções com linhas de preço zero. |
| Gerenciamento de Recursos | 2410072 | Permita a configuração de um recurso atribuído à tarefa como um gerente de projeto. |
| Cobrança e preço | 2430234 | Corrija um problema de cálculo de desempenho de custo. |
| Tempo e Despesa | 2436978 | Permita que o tempo seja inserido no formato hh:mm. |
| Cobrança e preço | 2448623 | Permita que listas de preços sejam atualizadas após serem associadas a uma unidade organizacional. |
| Tempo e Despesa | 2460396 | Permita que uma entrada de tempo seja excluída limpando a célula. |
| Cobrança e preço | 2467386 | Permita que um projeto com uma tarefa seja excluído, mesmo quando a tarefa esteja associada a uma cotação ganha. |
| Tempo e Despesa | 2461744 | A exibição **Minha aprovação com falha** contém apenas aprovações de projetos no estágio **Enviado**. |
| Tempo e Despesa | 2464082 | Remova o link de aprovações de projeto para o conjunto de aprovações quando um status de destino for correspondido. |
| Tempo e Despesa | 2468108 | O trabalho de agendamento não deve definir um status **Processando** para o conjunto de aprovações. |
| Tempo e Despesa | 2471503 | Exclua conjuntos de aprovações com sete dias. |
| Cobrança e preço | 2480687 | A referência da linha de cotação não deve ser removida quando uma etapa de linha de cotação é criada. |
