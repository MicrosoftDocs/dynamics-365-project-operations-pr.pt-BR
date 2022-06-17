---
title: Desempenho de agendamento de recursos do projeto
description: Este artigo fornece informações sobre como melhorar o desempenho do planejamento de recursos para um grande número de projetos.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 072476d43fb3b3d4f96480ec2d3dc5f9db28e501
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921886"
---
# <a name="project-resource-scheduling-performance"></a>Desempenho de agendamento de recursos do projeto

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Problemas de desempenho relacionados ao agendamento de recursos podem ocorrer quando o número de projetos chega aos milhares. Para melhorar o desempenho do agendamento de recursos, está disponível um recurso que permite aos usuários reduzir o tempo que leva para iniciar o formulário de disponibilidade de recursos. Especificamente, isso remove o processo de sincronização de acúmulo da capacidade do recurso e usa a tabela **ResProjectResource** para acelerar a pesquisa de recursos. Observe que a tabela **ResRollup** não será mais usada.

> [!IMPORTANT]
> Se houver uma dependência do processo de sincronização de acumulação de capacidade do recurso ou da tabela **ResProjectResource**, não use o recurso.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Habilitar melhoria de desempenho de agendamento de recursos
Para habilitar o aprimoramento de desempenho do agendamento de recursos, conclua as etapas a seguir.

1. Acesse **Gerenciamento de recursos** > **Tudo** e, na lista de recursos, localize **Habilitar recurso de aprimoramento de desempenho de agendamento de recursos do projeto**.
2. Selecione **Habilitar agora**.

> [!NOTE]
> Se você não conseguir encontrar o recurso na lista, selecione **Verificar se há atualizações** para atualizar a lista.

3. Atualize seu navegador e acesse **Gerenciamento e contabilidade de projeto** > **Periódico** > **Recursos do projeto** > **Sincronizar a capacidade dos calendários de recursos em todas as empresas**.
4. Defina **Remover os registros de capacidade existentes** como **Sim** para remover dados anteriores. Se você quiser gerar dados incrementais, defina-o como **Não**.
5. No campo **Código de período**, selecione o período em que os dados devem ser gerados. Se você selecionar um código de período, uma data de início e de término não precisa ser definida.
6. Se você deixar o campo **Código de período** em branco, selecione datas de início e término específicas para gerar dados.
7. Selecione **OK**.

 > [!NOTE]
 > Isso distribuirá dados gerais para a tabela **ResCalendarCapacity** em todas as empresas em seu ambiente, de modo que o trabalho em lote só precisa ser executado em uma entidade legal. Os dados nesse trabalho em lote são necessários para calcular a capacidade do recurso por meio do calendário associado.

8. Acesse **Gerenciamento e contabilidade de projeto** > **Periódico** > **Recursos do projeto** > **PPreencher os recursos do projeto em todas as empresas** e selecione **OK**. Este é o script de atualização de dados para dados gerais nas tabelas **ResProjectResource**, **ResCalendarDateTimeRange** e **ResEffectiveDateTimeRange**. Os valores do campo **PSAPRojSchedRole.RootActivity** também são atualizados. Se não for executado, você receberá um aviso ao tentar executar operações de agendamento de recursos.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Desligar melhoria de desempenho de agendamento de recursos

1. Acesse **Gerenciamento de recursos** > **Tudo** e pesquise **Habilitar recurso de aprimoramento de desempenho de agendamento de recursos do projeto**.
2. Selecione o recurso e, em seguida, selecione o botão **Desabilitar**.
3. Atualize seu navegador.
4. Acesse **Gerenciamento e contabilidade de projeto** > **Periódico** > **Sincronização de capacidade** > **Sincronizar acúmulos de capacidade de recursos**.
5. Na página **Sincronização de acúmulo de capacidade**, defina **Remover os registros de capacidade existentes** como **Sim** para remover dados anteriores. Se você quiser gerar dados incrementais, defina-o como **Não**.
6. No campo **Código de período**, selecione o período em que os dados devem ser gerados. Se você selecionar um código de período, uma data de início e de término não precisa ser definida.
7. Se você deixar o campo **Código de período** em branco, selecione datas de início e término específicas para gerar dados.
8. Selecione **OK**.

> [!NOTE]
> Isso distribuirá dados gerais para a tabela **ResRollup** em todas as empresas em seu ambiente, de modo que o trabalho em lote só precisa ser executado em uma entidade legal. Esse trabalho em lote é necessário para todas as exibições **Disponibilidade do Recurso**. Se esse trabalho em lote não for executado, os dados **ResRollup** serão gerados imediatamente, o que pode levar algum tempo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]