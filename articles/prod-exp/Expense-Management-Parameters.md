---
title: Parâmetros de gerenciamento de despesas
description: Os parâmetros a seguir controlam o comportamento no gerenciamento de despesas.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 41d78726f6d0aa6b5e647dbb359824950cb6ca72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993701"
---
# <a name="expense-management-parameters"></a>Parâmetros de gerenciamento de despesas


Os parâmetros controlam o comportamento geral no gerenciamento de despesas.

### <a name="general"></a>Geral

| **Campo**                                                | **Descrição**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Taxa padrão de quilometragem**                             | Insira a taxa de reembolso para despesas de quilometragem. A taxa será multiplicada pela quilometragem inserida na despesa para calcular o valor reembolsado pelas despesas de viagem.                       |
|**Despesas pessoais pagas por**                             | Selecione quem é responsável pelo pagamento de quaisquer valores de transação de cartão de crédito categorizados como pessoais.                                                                                                     |
|**Exibir o relatório de despesas inteiro em drillback**               | Selecione esta opção para exibir todas as despesas de um relatório de despesas quando exibir os detalhes do documento original para um comprovante específico que foi gerado quando o relatório de despesas foi lançado.              |
|**A pré-autorização da viagem é obrigatória**                 | Selecione esta opção para exigir que uma requisição de viagem seja enviada e aprovada antes que um funcionário possa enviar um relatório de despesas.                                                                    |
|**Permitir a edição de distribuições antes do lançamento**            | Selecione se as distribuições de um relatório de despesas podem ser editadas antes da postagem.                                                                                                                 |
|**Avaliar as políticas de gerenciamento de despesas**                     | Selecione quando as despesas são avaliadas para determinar se uma política de despesas foi violada. Pode-se verificar se há violações nas despesas quando a entrada de despesas é inserida e salva ou quando a despesa é enviada para aprovação. As regras de política para recibos exigidos serão verificadas quando a linha de despesa for salva.                   |
|**Permitir linhas de despesa intercompanhia**                         | Selecione deve ser permitida a entrada de despesas para outras entidades legais em um relatório de despesas.                                                                                                          |
|**Permitir a edição da taxa de câmbio para despesas de cartão de crédito** | Selecione esta opção para permitir que o usuário edite a taxa de câmbio para despesas de cartão de crédito importadas.                                                                        |
|**Campos de hierarquia em vários níveis a serem exibidos**                  | Selecione quais campos do aprovador são exibidos quando o tipo de atribuição de fluxo de trabalho do relatório de despesas é definido como uma hierarquia, e a seleção de hierarquia é definida para usar a hierarquia de aprovação com vários níveis de despesas. Quando a hierarquia de aprovação com vários níveis for usada para um fluxo de trabalho, os campos selecionados serão exibidos e editáveis no relatório de despesas. |
|**Inserir o número do cartão de crédito do funcionário (atualização de julho de 2017)**     | Selecione se um número de 15 ou 16 caracteres pode ser inserido e salvo no campo **ID do Cartão** na página **Cartões de crédito** de um funcionário.                                                                          |

### <a name="financial"></a>Financeiro

| **Campo**                                                            | **Descrição**     |
|----------------------------------------------------------------------|------------------------------------|
|**Nome de diário-razão**                                         | Selecione o nome do diário-razão no qual os relatórios de despesas aprovados são lançados.            |
|**Habilitar a restituição de imposto de despesas**                                  | Selecione esta opção para habilitar a restituição de imposto de despesa para despesas elegíveis. Esta opção não poderá ser habilitada se as regras de imposto sobre vendas e sobre o uso dos EUA estiverem habilitadas.      |
|**Lançar adiantamentos em dinheiro imediatamente**                                     | Selecione esta opção para postar um adiantamento de dinheiro aprovado quando o processo para Pagar e Transferir estiver concluído. Se esta opção não estiver selecionada, o processo Pagar e Transferir gerará um diário geral não postado. |
|**Data de contabilização correta durante lançamento**                             | Selecione esta opção para atualizar a data contábil ao postar despesas se o período atual estiver em espera ou fechado. A data contábil será definida para o próximo período em aberto.   |
|**Permitir o agrupamento de transações com base na contrapartida especificada no método de pagamento**      | Selecione esta opção para resumir as transações de despesas de um relatório de despesas, com base na contrapartida especificada no método de pagamento das despesas.   
|**Imposto incluído**                                                   | Selecione esta opção para incluir o imposto sobre vendas no valor das despesas por padrão.             |
|**Liberar os ônus no fechamento das requisições de viagem**            | Selecione esta opção para liberar fundos onerados ao fechar uma requisição de viagem aprovada.                                                                                   |
|**Permitir envio de requisição de viagem sobre orçamento excedido para registro de orçamento e orçamento de projeto** | Selecione esta opção para permitir que os funcionários enviem requisições de viagem para aprovação que excedam o orçamento permitido definido no registro de orçamento ou o orçamento permitido para um projeto.            |
|**Permitir envio de relatório de despesas sobre orçamento excedido para registro de orçamento e orçamento de projeto**    | Selecione esta opção para permitir que os funcionários enviem relatórios de despesas para aprovação que excedam o orçamento permitido definido no registro de orçamento ou o orçamento permitido para um projeto.                |
|**Permitir aprovação de relatório de despesas sobre orçamento excedido somente para registro de orçamento**                | Selecione esta opção para conceder aos aprovadores a permissão de aprovar relatórios de despesas que excedem o orçamento permitido definido no registro de orçamento.                                                                       |

### <a name="per-diem"></a>Diária

| **Campo**                             | **Descrição**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Mínimo de horas para diária**           | Insira o número mínimo padrão de horas que um funcionário deve trabalhar em um dia para ser considerado elegível para receber uma diária referente a despesas de viagem.  Esse valor é usado apenas como valor padrão para o campo Mínimo de horas em níveis de taxas de diária.                                                                                      |
|**Porcentagem de refeição**                          | Insira a porcentagem padrão da diária para refeições usada no primeiro e no último dia das despesas relacionadas à viagem quando o campo **Calcular redução de refeições por** for definido como **Tipo de refeição por dia** ou **Número de refeições por dia**. O dia de trabalho no primeiro e no último dias pode ser mais curto do que um dia de trabalho padrão. Portanto, o valor da diária nesses dias pode diferir do valor padrão. Se a porcentagem for definida como 0, as deduções do primeiro e do último dias serão 0,00. |
|**Porcentagem de hotel**                        | Insira a porcentagem padrão da diária para hotéis usada no primeiro e no último dia das despesas relacionadas à viagem. O dia de trabalho no primeiro e no último dias pode ser mais curto do que um dia de trabalho padrão. Portanto, o valor da diária nesses dias pode diferir do valor padrão. Se a porcentagem for definida como 0, as deduções do primeiro e do último dias serão 0,00.                                              |
|**Outra porcentagem**                        | Insira a porcentagem padrão da diária para despesas diversas usada no primeiro e no último dia das despesas relacionadas à viagem. O dia de trabalho no primeiro e no último dias pode ser mais curto do que um dia de trabalho padrão. Portanto, o valor da diária nesses dias pode diferir do valor padrão. Se a porcentagem for definida como 0, as deduções do primeiro e do último dias serão 0,00.                                                                                                     |
|**Redução da porcentagem para café da manhã** | Insira o valor da diária com a dedução para café da manhã. Por exemplo, se um funcionário receber um café da manhã de cortesia, você poderá reduzir o valor da diária em 10%.                               |
|**Redução da porcentagem para almoço**    | Insira o valor da diária com a dedução para o almoço. Por exemplo, se um funcionário receber um almoço de cortesia, você poderá reduzir o valor da diária em 15%.                                       |
|**Redução da porcentagem para jantar**   | Insira o valor da diária com a dedução para o jantar. Por exemplo, se um funcionário receber um jantar de cortesia, você poderá reduzir o valor da diária em 25%.                                     |
|**Calcular redução de refeições por**         | Informe como o sistema deve calcular a redução de refeição da diária, selecionando se a redução é baseada no tipo de refeição, por viagem, por dia, ou se a redução é baseada no número de refeições permitidas por dia.|
|**Arredondamento da diária**                  | Selecione o tipo de arredondamento usado para despesas de diária. Se você selecionar o arredondamento normal, qualquer despesa de diária com valor de 0,50 será arredondado para 1,00 e qualquer despesa de diária com valor inferior a 0,50 será arredondado para 0,00.                                                                                              |
|**Basear o cálculo de diária em**         | Selecione se um valor de diária é baseado em um dia do calendário ou em um período de 24 horas.       |

### <a name="fax-cover-pages"></a>Folhas de rosto de fax

| **Campo**                      | **Descrição**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instruções**                   | Insira as instruções que os funcionários devem seguir ao criar uma folha de rosto para um fax que é usado para enviar recibos relacionados a um relatório de despesas. Clique no botão **Traduções** para inserir o texto específico do idioma que será exibido com base no idioma do usuário. |
|**ID do usuário (informações do código de barras)** | Selecione esta opção para armazenar o identificador exclusivo do funcionário no código de barras usado na folha de rosto do fax.                 |
|**Código de barras**                      | Selecione o código de barras usado na folha de rosto do fax. Os códigos de barras 39 e 128 têm suporte no Gerenciamento de despesas.               |

### <a name="anti-corruption"></a>Anticorrupção

|                 <strong>Campo</strong>                 |                                                                                                                                                                                            <strong>Descrição</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Exibir atestado de anticorrupção</strong>  | Selecione esta opção para exibir o texto de anticorrupção ao criar um novo relatório de despesas. Dessa forma, as categorias de despesas específicas poderão ser habilitadas, o que exigirá que o atestado de anticorrupção seja selecionado no relatório de despesas. Por exemplo, uma categoria de presente relacionada à despesa de uma autoridade do governo pode exigir que o funcionário confirme que a despesa atende à política da empresa relacionada a autoridades do governo. |
| <strong>Mensagem de anticorrupção para emissor</strong> |                                                                                             Insira o texto que será exibido para o funcionário ao criar um novo relatório de despesas. Clique no botão <strong>Traduções</strong> para inserir o texto específico do idioma que será exibido com base no idioma do usuário.                                                                                             |
| <strong>Mensagem de anticorrupção para aprovador</strong>  |                                                                                             Insira o texto que será exibido para o aprovador ao criar um novo relatório de despesas. Clique no botão <strong>Traduções</strong> para inserir o texto específico do idioma que será exibido com base no idioma do usuário.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]