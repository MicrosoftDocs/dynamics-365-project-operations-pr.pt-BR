---
title: Novidades ou alterações na Versão de Atualização 24 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 24 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 51d08dd147b7804cb5c9255159aeab2ecd94f4597d6e99c5fa92efe1246c44d0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998042"
---
# <a name="project-service-automation-update-release-24-v3"></a>Versão de Atualização 24, do Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 24. Esta versão tem um número de build V 3.10.42.43 e foi disponibilizada para o público em geral por meio de uma atualização automática em outubro de 2020.

## <a name="update-release-24"></a>Versão de Atualização 24

### <a name="bug-fixes"></a>Correções de bug

**Sales**

Os seguintes problemas foram corrigidos:

- Problema ao configurar a lista de preços padrão de produtos.
- O desempenho de Ganho de cotação é lento devido à lista de preços inserida e à cópia dos registros de preços da função.
- **Contrato de Projeto/Hub de Vendas** > **Item de Linha de Produtos/Quantidade de Linhas da Ordem** é automaticamente arredondado para o próximo inteiro.
- Eleve aos privilégios do sistema ao ler listas de preços.
- Copie os campos de endereço do cliente **address1_freighttermscode** e **address1_shippingmethodcode** para Cotação/Ordem. 


**Tempo e Despesa**

Os seguintes problemas foram corrigidos:

- A **Grade de Entrada de Hora** não é compatível com o comportamento de hora de **Somente Data**.
- **Entrada de Hora** não está sendo atualizado automaticamente. É necessária uma atualização manual.
- Não ser possível importar as entradas de hora de uma atribuição quando houver um intervalo (0 horas) nas atribuições de um recurso.
- Ao criar uma entrada de hora, defina o início como uma data igual a **msdyn_date**.
- Reabilite a edição em massa para entrada de tempo.

**Gerenciamento de Recursos**

Os seguintes problemas foram corrigidos:

- Tentar atualizar o status de uma reserva entre dias sem um requisito gerará uma exceção de referência nula.
- Erro ao carregar a **Exibição de Reconciliação**.


**Gerenciamento de projetos**

Os seguintes problemas foram corrigidos:

- Na **Agenda do Projeto**, ao mudar de **Manual** para **Automático**, o salvamento automático não está sendo concluído.
- Os custos de despesas não devem ser calculados em relação à variação na **Grade de Rastreamento de Projetos**.
- Comportamento inconsistente para colunas da **marca Estimativas** durante o carregamento versus a alteração do tipo **Fase do Tempo**.
- O custo real de um projeto pode não refletir os totais de **Dados Reais**.
- **Data Estimada de Conclusão** na guia **Resumo** não corresponde à **Agenda da WBS**.
- **Atualizar Horas Reais** no recuo à esquerda não funciona corretamente.
- Um gerente de projeto fora da raiz **BU** não consegue criar um projeto.
- As alterações feitas na tarefa ou categoria em **Estimativas de Despesas** não são persistentes.
- **Cópia do contrato** copia as agendas da fatura e o status de execução.
- O botão **Atualizar Dados Reais** calcula incorretamente tarefas de resumo.
- Suplemento do Microsoft Project: corrija o erro de referência nula se algum membro da equipe tiver uma unidade de recursos vazia.



[!INCLUDE[footer-include](../includes/footer-banner.md)]