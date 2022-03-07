---
title: Novidades ou alterações na Versão de Atualização 22 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 22 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 6a5109b1ffedfce99fc50c035bcbe5810abcf3b71f88679b47561d69daa9f3ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004297"
---
# <a name="project-service-automation-update-release-22-v3"></a>Versão de Atualização 22, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 22. Esta versão apresenta o número de compilação V 3.10.33.48 e está disponível para o público em geral por meio de uma atualização automática em junho de 2020.

## <a name="update-release-22"></a>Versão de Atualização 22

### <a name="bug-fixes"></a>Correções de bug



**Tempo e Despesa**

Os seguintes problemas foram corrigidos:

- As **Entradas de horas** não são adicionadas automaticamente na agenda de Entradas de horas após a importação.
- O seletor de data da grade **Entrada de Horas** não reconhece as configurações regionais de um usuário.

**Gerenciamento de Recursos**

Os seguintes problemas foram corrigidos:

- No modo manual, as alterações em contornos da **Atribuição de Recurso** não são reconhecidas ao gerar os **Requisitos de Recurso**.
- As **Solicitações de Recursos** não oferecem suporte aos status de solicitação.

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- Usar o clique duplo em EstimateGridControl não analisará os números no formato holandês corretamente.
- Os horários atribuídos não são atualizados corretamente quando as atribuições são alteradas usando o suplemento de cliente de desktop do Microsoft Project.
- As grades de Rastreamento e Estimativas do Projeto exibem o código de moeda de venda incorreto quando a moeda de contrato é diferente da moeda do cliente e a organização está configurada para exibir códigos de moeda em vez de símbolos da moeda.
- A data de término de um membro da equipe adicionará um dia se o agendamento de horas de trabalho for 24 horas por dia.
- No Agendamento de Projeto, adicionar uma Categoria de Transação a uma tarefa não aciona o salvamento automático.
- O seguinte erro é exibido ao adicionar um membro da equipe ao Modelo do Projeto: "Requisitos de recurso não podem ser associados a modelos de projeto". 
- O script de regra da faixa de opções "msdyn.Approval.CanApproveOrReject" exibe um erro de tempo limite.

**Sales**

Os seguintes problemas foram corrigidos:

- A mensagem de erro de validação não é exibida quando uma Lista de Preços de Custo é selecionada na pesquisa de Lista de Preços no formulário/entidade "Nova Lista de Preços do Projeto de Cotação".
- Fechar a cotação como ganha não direciona para o contrato criado se um Fluxo do Processo Empresarial anexado à cotação estiver no estágio final.
- A reversão de **Vendas Não Cobradas** está vinculada ao custo original quando uma entrada de hora é recuperada.
- Depois de selecionar o botão **Confirmar**, o status da fatura não é alterado para **Confirmado** a menos que a fatura seja atualizada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]