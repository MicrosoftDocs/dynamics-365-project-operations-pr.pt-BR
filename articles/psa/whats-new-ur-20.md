---
title: Novidades ou alterações na Versão de Atualização 20 do Project Service Automation V3
description: Este tópico lista os recursos e as correções disponíveis na Versão de Atualização 20 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147099"
---
# <a name="project-service-automation-update-release-20-v3"></a>Versão de Atualização 20, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 20. Esta versão apresenta o número de compilação V 3.10.31.37 e está disponível para o público em geral por meio de uma atualização automática em junho de 2020.

## <a name="update-release-20"></a>Versão de Atualização 20

### <a name="bug-fixes"></a>Correções de bug

**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- A importação de membros da equipe do projeto com um método de alocação que requer horas resulta em uma mensagem de erro pouco clara quando as horas especificadas são zero.
- Os usuários recebem um erro incorreto quando o número máximo de caracteres foi inserido no campo **Descrição** para uma tarefa do projeto.
- A página de **download do suplemento do Microsoft Dynamics 365 Project Service Automation** redireciona para a página de download em inglês quando as configurações de idioma do usuário estão definidas como japonês.
- Quando ocorre um erro no servidor, o rótulo de sincronização na guia **Agenda** do formulário **Projetos** às vezes permanece.
- Atualizações redundantes de tarefas estão sendo enviadas ao servidor quando uma tarefa é modificada.

**Sales**

Os seguintes problemas foram corrigidos:

- No formulário **Contrato**, clicar duas vezes em **Criar recibo** cria duas faturas para um único registro de dados reais.
- No Internet Explorer 11, os usuários não conseguem criar entradas de despesas.
- A Reversão de Custo e a reversão de Dados Reais de Vendas não Faturadas não estão vinculadas.
- O botão **Atualizar Dados Reais** no formulário **Projeto** não atualiza **Horas Reais da Tarefa**.
- O plug-in **PreValidateProjectTeamMemberCreate** pode criar recursos reserváveis genéricos duplicados quando o atributo **msdyn_isgenericresourceprojectscoped** está definido como **Falso**.
- **Recalcular** limpa os custos passíveis de cobrança dos detalhes da linha de cotação baseadas em produto e dos detalhes da linha do contrato.
- Em cenários específicos, o plug-in **PostEstimateLineUpdate** exibe um erro de exceção de referência nula.
- A duração da fase de tempo no **Gráfico de Análise de Lucratividade** não corresponde à duração dos custos nos detalhes da linha de cotação de preço fixo da cotação.
- Os valores da unidade e do grupo de unidades não são padronizados corretamente para as categorias de despesas nos formulários **Detalhes da Linha do Contrato** e **Detalhes da Linha de Cotação**.
- As listas de **Preço de Custo Unitário da Organização** permitem sobreposições na data efetiva.
- Os usuários não têm permissão para alterar **OrgUnit** quando o tipo de ordem não for baseado no trabalho, pois levará a um erro de exceção de referência nula.
- Ao tentar navegar do formulário **Detalhes da Linha de Cotação** de volta à guia **Cotação**, o formulário é atualizado e exibe a guia **Resumo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]