---
title: Configurar parâmetros de gerenciamento de despesas
description: Este tópico descreve os parâmetros que controlam o comportamento geral no Gerenciamento de despesas.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8ecbd0abc16d0a29eea47d6bd1653a204a83de4c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071310"
---
# <a name="configure-expense-management-parameters"></a>Configurar parâmetros de gerenciamento de despesas

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico descreve os parâmetros que controlam o comportamento geral no Gerenciamento de despesas.

## <a name="general"></a>Geral

| Campo                                                    | Descrição |
|----------------------------------------------------------|-------------|
| Taxa padrão de quilometragem                                 | Insira a taxa de reembolso para despesas de quilometragem. Essa taxa é multiplicada pela quilometragem inserida na despesa para calcular o valor que será reembolsado pelas despesas de viagem. |
| Validar propósito de despesa                                 | Ative esta opção para limitar usuários a um conjunto de valores existente configurado no campo **Finalidade do relatório de despesas** quando eles criarem relatórios de despesas. |
| Despesas pessoais pagas por                                | Selecione quem é responsável pelo pagamento de quaisquer valores de transação de cartão de crédito classificados como pessoais. |
| Exibir o relatório de despesas inteiro em drillback               | Selecione esta opção para mostrar todas as despesas de um relatório de despesas quando os detalhes do documento original forem exibidos para um voucher específico que foi gerado quando o relatório de despesas foi lançado. |
| A pré-autorização da viagem é obrigatória                 | Selecione esta opção para exigir que uma requisição de viagem seja enviada e aprovada antes que um funcionário possa enviar um relatório de despesas. |
| Permitir a edição de distribuições antes do lançamento            | Selecione se as distribuições de um relatório de despesas podem ser editadas antes dele ser publicado. |
| Avaliar as políticas de gerenciamento de despesas                     | Selecione quando as despesas são avaliadas para determinar se houve violação de alguma política de despesa. As despesas podem ser avaliadas quanto a violações quando a entrada de despesa é inserida e salva ou quando a despesa é enviada para aprovação. As regras de política para recibos exigidos serão avaliadas quando a linha de despesa for salva. |
| Permitir linhas de despesa intercompanhia                         | Selecione se as despesas de outras entidades legais podem ser inseridas em um relatório de despesas. |
| Permitir a edição da taxa de câmbio para despesas de cartão de crédito | Selecione esta opção para permitir que o usuário edite a taxa de câmbio para despesas de cartão de crédito importadas. |
| Campos de hierarquia em vários níveis a serem exibidos                  | Selecione quais campos do aprovador são exibidos quando o tipo de atribuição de fluxo de trabalho é definido como uma hierarquia, e a seleção de **Hierarquia** é definida para usar a hierarquia de aprovação, aprovação com vários níveis de despesas. Quando a hierarquia de aprovação com vários níveis é usada para um fluxo de trabalho, os campos selecionados serão exibidos no relatório de despesas e podem ser editados. |
| Inserir o número do cartão de crédito do funcionário                        | Selecione se um número de 15 ou 16 caracteres pode ser inserido e salvo no campo **ID do Cartão** na página **Cartões de crédito** de um funcionário. |
| Validar finalidade de requisição de viagem                      | Ative esta opção para limitar usuários a um conjunto de valores existente configurado no campo **Finalidade do relatório de despesas** quando eles criarem requisições de viagem. |

## <a name="financial"></a>Financeiro

| Campo                                                                                    | Descrição |
|------------------------------------------------------------------------------------------|-------------|
| Nome de diário-razão                                                                | Selecione o nome do diário-razão no qual os relatórios de despesas aprovados são lançados. |
| Habilitar a restituição de imposto de despesas                                                        | Selecione esta opção para habilitar a restituição de imposto de despesa para despesas elegíveis. Esta opção não pode ser selecionada se as regras de imposto sobre vendas e sobre o uso dos EUA estiverem habilitadas. |
| Lançar adiantamentos em dinheiro imediatamente                                                           | Selecione esta opção para lançar um adiantamento de dinheiro aprovado quando o processo Pagar e Transferir for concluído. Se esta opção não for selecionada, o processo Pagar e Transferir gera um diário geral não lançado. |
| Data de contabilização correta durante lançamento                                                   | Selecione esta opção para atualizar a data contábil quando as despesas forem lançadas, se o período atual estiver em espera ou fechado. A data contábil será definida para o próximo período em aberto. |
| Permitir o agrupamento de transações com base na contrapartida especificada no método de pagamento       | Selecione esta opção para resumir as transações de despesas de um relatório de despesas, com base na contrapartida especificada no método de pagamento das despesas. |
| Imposto incluído                                                                             | Selecione esta opção para incluir o imposto sobre vendas no valor das despesas por padrão. |
| Liberar os ônus no fechamento das requisições de viagem                                      | Selecione esta opção para liberar fundos onerados ao fechar uma requisição de viagem aprovada. |
| Permitir envio de requisição de viagem sobre orçamento excedido para registro de orçamento e orçamento de projeto | Selecione esta opção para permitir que os funcionários enviem requisições de viagem para aprovação, mesmo se excederem o orçamento permitido definido no registro de orçamento ou o orçamento permitido para um projeto. |
| Permitir envio de relatório de despesas sobre orçamento excedido para registro de orçamento e orçamento de projeto     | Selecione esta opção para permitir que os funcionários enviem relatórios de despesas para aprovação, mesmo se excederem o orçamento permitido definido no registro de orçamento ou o orçamento permitido para um projeto. |
| Permitir aprovação de relatório de despesas sobre orçamento excedido somente para registro de orçamento                 | Selecione esta opção para conceder aos aprovadores a permissão de aprovar relatórios de despesas que excedem o orçamento permitido definido no registro de orçamento. |

## <a name="per-diem"></a>Diária

| Campo                                 | Descrição |
|---------------------------------------|-------------|
| Mínimo de horas para diária            | Insira o número mínimo padrão de horas que um funcionário deve trabalhar em um dia para ser considerado elegível para receber uma diária referente a despesas de viagem. Esse valor é usado como valor padrão somente para o campo **Mínimo de horas** para camadas de taxas de diária. |
| Porcentagem de refeição                          | Insira a porcentagem padrão da diária para refeições usada no primeiro e no último dia das despesas relacionadas à viagem quando o campo **Calcular redução de refeições por** for definido como **Tipo de refeição por dia** ou **Número de refeições por dia**. O dia de trabalho no primeiro e no último dia pode ser mais curto que um dia de trabalho padrão. Portanto, o valor da diária nesses dias pode diferir do valor padrão. Se a porcentagem for definida como **zero** (0), as deduções do primeiro e do último dia serão 0,00. |
| Porcentagem de hotel                         | Insira a porcentagem padrão da diária para hotéis usada no primeiro e no último dia das despesas relacionadas à viagem. O dia de trabalho no primeiro e no último dia pode ser mais curto que um dia de trabalho padrão. Portanto, o valor da diária nesses dias pode diferir do valor padrão. Se a porcentagem for definida como **zero** (0), as deduções do primeiro e do último dia serão 0,00. |
| Outra porcentagem                         | Insira a porcentagem padrão da diária para despesas diversas usada no primeiro e no último dia das despesas relacionadas à viagem. O dia de trabalho no primeiro e no último dia pode ser mais curto que um dia de trabalho padrão. Portanto, o valor da diária nesses dias pode diferir do valor padrão. Se a porcentagem for definida como **zero** (0), as deduções do primeiro e do último dia serão 0,00. |
| Redução da porcentagem para café da manhã | Insira o valor da diária com a dedução do café da manhã. Por exemplo, se um funcionário receber um café da manhã de cortesia, você poderá reduzir o valor da diária em 10%. |
| Redução da porcentagem para almoço     | Insira o valor da diária com a dedução do almoço. Por exemplo, se um funcionário receber um almoço de cortesia, você poderá reduzir o valor da diária em 15%. |
| Redução da porcentagem para jantar    | Insira o valor da diária com a dedução do jantar. Por exemplo, se um funcionário receber um jantar de cortesia, você poderá reduzir o valor da diária em 25%. |
| Calcular redução de refeições por           | Especifique como o sistema deve calcular a redução de refeição da diária selecionando se a redução é baseada no tipo de refeição, por viagem, por dia, ou se ela é baseada no número de refeições permitidas por dia. |
| Arredondamento da diária                     | Selecione o tipo de arredondamento usado para despesas de diária. Se você selecionar o arredondamento normal, qualquer despesa de diária com valor de 0,50 será arredondado para 1,00 e qualquer despesa de diária com valor inferior a 0,50 será arredondado para 0,00. |
| Basear o cálculo de diária em          | Selecione se um valor de diária é baseado em um dia do calendário ou em um período de 24 horas. |

## <a name="fax-cover-pages"></a>Folhas de rosto de fax

| Campo                          | Descrição |
|--------------------------------|-------------|
| Instruções                   | Insira as instruções que os funcionários devem seguir ao criar uma folha de rosto para um fax que é usado para enviar recibos relacionados a um relatório de despesas. Para inserir o texto específico do idioma que será mostrado, com base no idioma do usuário, selecione **Traduções**. |
| ID do usuário (informações do código de barras) | Selecione esta opção para armazenar o identificador exclusivo do funcionário no código de barras usado na folha de rosto do fax. |
| Código de barras                       | Selecione o código de barras usado na folha de rosto do fax. Os códigos de barras 39 e 128 são compatíveis com o Gerenciamento de despesas. |

## <a name="anti-corruption"></a>Anticorrupção

| Campo                                 | Descrição |
|---------------------------------------|-------------|
| Exibir atestado de anticorrupção   | Selecione esta opção para mostrar o texto de anticorrupção ao criar um relatório de despesas. Dessa forma, as categorias de despesas específicas poderão ser habilitadas, o que exigirá que o atestado de anticorrupção seja selecionado no relatório de despesas. Por exemplo, uma categoria de presente relacionada à despesa de uma autoridade do governo pode exigir que o funcionário confirme que a despesa atende à política da empresa relacionada a autoridades do governo. |
| Mensagem de anticorrupção para emissor | Insira o texto que deve ser mostrado a um funcionário que está criando um relatório de despesas. Para inserir o texto específico do idioma que será mostrado, com base no idioma do usuário, selecione **Traduções**. |
| Mensagem de anticorrupção para aprovador  | Insira o texto que deve ser mostrado para o aprovador quando um relatório de despesas é criado. Para inserir o texto específico do idioma que será mostrado, com base no idioma do usuário, selecione **Traduções**. |
