---
title: Requisições de itens para contratos de projeto com várias fontes de financiamento
description: Este artigo contém informações sobre como configurar e usar requisições de itens com várias fontes de financiamento.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028459"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Requisições de itens para contratos de projeto com várias fontes de financiamento

_**Aplicável a:** Project Operations para cenários baseados em estoque/produção_

Alguns acordos contratuais para entregas baseadas em projeto podem exigir várias fontes de financiamento. Este artigo explica como selecionar e configurar as fontes de financiamento desejadas quando várias fontes são necessárias para um projeto ou contrato de projeto.

## <a name="terminology"></a>Terminologia

- **Fonte de financiamento** – A entidade que financia o trabalho de contrato do projeto. Essa entidade pode ser uma organização interna ou uma conta de fatura externa (cliente ou concessão).
- **Cliente do projeto** – A entidade à qual o trabalho do projeto é entregue.
- **Conta de fatura** – A entidade externa que paga pelo trabalho do projeto.

## <a name="example"></a>Exemplo

A Contoso ganhou um contrato de renovação de equipamento com dois de seus clientes: a Adatum US e a Adatum Corporate. O contrato inclui serviços instalação e hardware que serão prestados à Adatum US (cliente do projeto). O hardware será financiado pela Adatum Corporate (conta de fatura 1) e o trabalho de instalação, pela Adatum US (conta de fatura 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Configurar regras de padronização de conta de fatura para requisições de itens

### <a name="prerequisites"></a>Pré-requisitos

- O Microsoft Dynamics 365 Finance **versão 10.0.27 ou posterior** é necessário para usar requisições de itens que tenham várias contas de fatura.
- O administrador do sistema deve habilitar o recurso **Permitir requisições de itens com várias fontes de financiamento para cenários baseados em estoque/produção do Project Operations** no espaço de trabalho **Gerenciamento de recursos**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Configurar as regras de padronização da conta de fatura

Para configurar as regras padrão para a conta de fatura, siga estas etapas.

1. Vá para **Gerenciamento e contabilidade de projeto** \> **Configuração** \> **Parâmetros de gerenciamento e contabilidade de projeto**.
1. Na guia **Geral**, na seção **Pedidos de venda e Requisições de itens**, defina a opção **Permitir projetos com várias fontes de financiamento** como **Sim**.
1. No campo **Cliente padrão**, especifique de onde vem o cliente de entrega do projeto na requisição de itens por padrão:

    - **Da fonte de financiamento** – O cliente de entrega do projeto padrão é proveniente da fonte de financiamento. Se várias fontes de financiamento estiverem associadas ao contrato do projeto, será usada a primeira da lista.
    - **Do projeto** – O cliente de entrega do projeto padrão vem do cliente selecionado no campo **Conta de registro do projeto**.

1. Opcional: defina ou altere a conta de fatura padrão nos registros do projeto:

    1. Acesse **Gerenciamento e contabilidade de projeto** \> **Projetos** \> **Todos os projetos** e abra os detalhes do registro do projeto.
    2. Na guia **Geral**, defina ou atualize o campo **Conta de fatura padrão**. A conta que você especificar será usada como a conta de fatura padrão para novas requisições de itens criadas para o projeto. Se você deixar o campo em branco, por padrão será usada a conta da fatura da primeira fonte de financiamento do contrato do projeto. No entanto, os usuários poderão alterar a conta ao salvar o registro.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Selecionar a conta de fatura a ser usada ao criar uma requisição de itens

Para selecionar a conta de fatura a ser usada ao criar uma requisição de itens, siga estas etapas.

1. Acesse **Gerenciamento e contabilidade de projeto** \> **Projetos** \> **Todos os projetos** e selecione o registro do projeto.
1. Na guia **Plano**, selecione **Requisições de itens**.
1. Crie um novo registro de requisição de itens.

    - Por padrão, o campo **Conta de fatura** no registro é definido para a conta de fatura configurada para o projeto. Você pode alterar o valor do campo **Conta de fatura** e, em seguida, salvar o registro. Depois que o registro for salvo, você não poderá mais atualizar o valor **Conta de fatura**. Se precisar atualizar o valor **Conta de fatura** da requisição de itens, exclua a requisição existente e crie uma nova com o valor desejado.
    - Por padrão, o campo **Cliente** da requisição de itens é definido com base no valor **Cliente padrão** definido na página **Parâmetros de gerenciamento e contabilidade de projetos**.

    Quando o registro de requisição de itens é salvo, o sistema o associa ao registro de cabeçalho **Pedido de venda da requisição de itens**. Se nenhum cabeçalho de pedido de venda em aberto tiver a conta de fatura selecionada, o sistema criará uma e associará a linha de requisição de itens a ela.

> [!NOTE]
> As requisições de itens sempre são faturadas integralmente para a conta de fatura definida no registro. No momento, o sistema não aceita regras de alocação de financiamento que tenham requisições de itens e não dividirá o lançamento com base na configuração dessas regras.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Criar uma requisição de itens de um registro de previsão de itens

Para criar uma requisição de itens de um registro de previsão de itens, siga estas etapas.

1. Acesse **Gerenciamento e contabilidade de projeto** \> **Projetos** \> **Todos os projetos** e selecione o registro do projeto.
1. Na guia **Plano**, selecione **Previsões de itens**.
1. Crie um novo registro de previsão de itens.
1. Opcional: na guia **Projeto**, no campo **Fonte de financiamento**, selecione a conta de fatura desejada.
1. Selecione **Criar requisição de itens** e confirme a mensagem recebida.

    > [!NOTE]
    > O sistema copia o valor **Fonte de financiamento** do registro de previsão de itens para o registro de requisição de itens recém-criado.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Conta de fatura padrão quando o sistema cria automaticamente uma requisição de itens de uma linha de ordem de compra

Se a opção **Criar requisição de itens** está definida como **Sim** na página **Parâmetros de gerenciamento e contabilidade de projetos**, o sistema automaticamente cria uma requisição de itens quando uma nova linha de ordem de compra do projeto é salva. Por padrão, os campos **Conta de fatura** e **Requisição de itens** são definidos com o valor do campo **Conta de fatura padrão** no registro do projeto. No momento, o sistema não permite atualizar ou alterar a conta de fatura em registros desse tipo.
