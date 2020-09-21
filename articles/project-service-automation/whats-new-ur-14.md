---
title: Novidades na Versão de Atualização 14 do Project Service Automation V3
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado na Versão da Atualização 14 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749073"
---
# <a name="project-service-automation-v3-update-release-14"></a>Novidades na Versão de Atualização 14 do Project Service Automation V3
Temos o orgulho de anunciar a versão mais recente do aplicativo do Dynamics 365 Project Service Automation (PSA). Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e vá para a página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 14. Esta versão possui um número de compilação da V3.10.4.21 e está disponível na seguinte agenda:

- **Disponibilidade geral (atualização automática):** Janeiro de 2020
- **Atualização automática:** Fevereiro de 2020

## <a name="update-release-14"></a>Versão de Atualização 14

### <a name="enhancements"></a>Aprimoramentos

- Sales

     - Os valores de campos personalizados de **Detalhes da Linha de Cotação** são copiados para **Detalhes da Linha de Contrato do Projeto** quando uma cotação é atualizada para **Fechada como ganha**.
     - Os projetos confirmados podem ser **Fechado como perdido**.

- Gerenciamento de Recursos

     - Ao estender as reservas, os usuários visualizarão uma caixa de diálogo de confirmação para resumir os resultados da reserva e fornecer um link para Manter reservas.


### <a name="bug-fixes"></a>Correções de bugs

- Tempo e Despesa

     - Corrigido: Melhorou a experiência do usuário quando este não selecionava entradas a serem corrigidas.

- Gerenciamento de Recursos

     - Corrigido: Reservar um recurso múltiplas vezes excede o nome do recurso reservável.

- Sales

     - Corrigido: O preço de venda total não é calculado até que o usuário também insira um preço de custo para estimativas de despesas em um projeto.
     - Corrigido: Fechar uma cotação como **Ganha** gera uma falha se o contrato do projeto associado não estiver em um estado de **Rascunho**.

