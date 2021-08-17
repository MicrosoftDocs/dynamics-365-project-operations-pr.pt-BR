---
title: Novidades ou alterações na Versão de Atualização 13 do Project Service Automation V3
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado na Versão da Atualização 13 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3a20cf32e578bc818f3ef6ed916784c32b559c3342162bcb7857f5e9cc520d9c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006662"
---
# <a name="project-service-automation-update-release-13-v3"></a>Versão de Atualização 13, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o orgulho de anunciar a versão mais recente do aplicativo Dynamics 365 Project Service Automation (PSA). Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e vá para a página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 13. Esta versão possui um número de compilação da V3.10.3.18 e está disponível na seguinte agenda:

- **Disponibilidade geral (atualização automática):** Novembro de 2019
- **Atualização automática:** Dezembro de 2019


## <a name="update-release-13"></a>Versão de Atualização 13 

### <a name="bug-fixes"></a>Correções de bugs

- Tempo e Despesa

     - Corrigido: A funcionalidade de pesquisa na página **Aprovação da experiência** não funciona ao pesquisar por finalidade de despesa.

- Gerenciamento de Recursos

     - Corrigido: Os números na reconciliação foram atualizados para serem justificados à direita.
     - Corrigido: Os Recursos Nomeados não podem ser atribuídos às tarefas por meio da guia **Agendar**.

- Gerenciamento de projetos

     - Corrigido: Exceção de referência nula ao atribuir um membro da equipe quando **TransactionType** não tiver as informações de configuração para **Unidade** e **DefaultGroup**.

- Sales

     - Corrigido: Os registros do tipo de transação duplicados retornam um erro quando os registros de preço da função são criados.
     - Corrigido: os botões extras para **Nova Oportunidade**, **Cotação**, **Linha da Ordem** e **Adicionar Produto** estão visíveis nos comandos de Oportunidades, Cotações, Produtos da Ordem e na subgrade de Linhas baseadas em projeto.




[!INCLUDE[footer-include](../includes/footer-banner.md)]