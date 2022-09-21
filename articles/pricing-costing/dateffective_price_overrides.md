---
title: Substituições de preço com data de efetivação
description: Este artigo explica como configurar substituições de preços para preços específicos na lista de preços.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445960"
---
# <a name="date-effective-price-overrides"></a>Substituições de preço com data de efetivação 

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

*Substituições de preço com data de efetivação* fornecem uma maneira de substituir ou alterar preços específicos na lista de preços. Por exemplo, você tem uma lista de preços padrão com data de efetivação de 1º de janeiro de 2022 a 31 de dezembro de 2022. Esta lista de preços tem preços para muitas funções. O preço configurado para a função **Técnico de Rede** é de 100 dólares americanos (USD) por hora. Quando um técnico de rede registra o tempo entre 1º de janeiro de 2022 e 31 de dezembro de 2022, o preço do tempo é de 100 USD. Em 1º de outubro de 2022, você deve ajustar o preço *somente* para a função **Técnico de Rede**, de 100 USD por hora para 110 USD por hora. O recurso **Substituições de preço com data de efetivação** permite configurar essa alteração como uma substituição da linha para esse preço de função específico. Portanto, você não precisa copiar toda a lista de preços e alterar o preço de apenas uma linha.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Substituições de preço com data de efetivação para preços de mão de obra

O processo de configuração de substituições de preço com data de efetivação para tempo de trabalho em um projeto consiste em duas etapas básicas.

1. Habilite o recurso **Substituições de preço com data de efetivação**.
1. Configure uma substituição de preço com data de efetivação.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Habilite o recurso Substituições de preço com data de efetivação.

> [!NOTE]
> Depois que o recurso **Substituições de preço com data de efetivação** for ativado, ele não poderá ser desativado.

Para habilitar o recurso **Substituições de preço com data de efetivação**, siga estas etapas.

1. Vá para **Configurações** \> **Parâmetros**.
1. Abra o registro **Parâmetros**.
1. No Painel de Ação, na guia **Controle de Recursos**, selecione **Habilitar Substituições de Preço com Data de Efetivação**.
1. Na caixa de diálogo de confirmação, selecione **OK**.
1. Após alguns momentos, atualize o navegador. Os recursos de substituição de preço com data de efetivação agora devem estar disponíveis. Você saberá que esses recursos foram habilitados se a opção **Habilitar Substituições de Preço com Data de Efetivação** não aparecer mais no Painel de Ação.

### <a name="set-up-a-date-effective-price-override"></a>Configurar uma substituição de preço com data de efetivação

As substituições de preço com data de efetivação podem ser configuradas nas listas de preços **Custo**, **Vendas** ou **Compra**.

> [!NOTE]
>O comportamento das **Substituições de preço com data de efetivação** atualmente tem as seguintes limitações:
>
> - Somente preços de função e markups de preço de função são compatíveis com o recurso **Substituições de preço com data de efetivação** no Project Operations.
> - Ao copiar uma lista de preços usando a ação **Copiar** na página **Detalhes da lista de preços** e ao criar uma lista de preços de projeto usando uma lista de preços padrão ou personalizada durante a criação do contrato, as substituições de preço com data de efetivação **não** são copiadas da lista de preços de origem.

Para configurar uma substituição de preço de data de efetivação para um preço de função ou uma markup de preço de função, siga estas etapas.

1. Abra a página da lista de preços para a qual você deseja configurar a substituição de preço de data de efetivação.
1. Selecione a guia **Preços da função**, que lista todos os registros **Preço da função** na lista de preços.
1. Selecione o registro **Preço da função** para o qual você deseja configurar um novo preço de substituição de data efetiva e toque duas vezes (ou clique duas vezes) em **Preço da função** para abrir a página **Detalhes do preço da função**.
1. Selecione a guia **Substituições de preço com data de efetivação**, cuja grade lista todas as substituições de preço com data de efetivação para o registro **Preço da função** selecionado.
1. Na barra de ferramentas acima da grade, selecione **Nova substituição de preço de função**. O controle deslizante **Nova substituição de preço de função** é aberto.
1. Especifique a data de início de vigência, a unidade e o novo preço para a substituição de preço. Em seguida, selecione **Salvar** e feche o formulário.

> [!NOTE]
> - Uma substituição de preço com data de efetivação para um preço de função ou uma markup de preço de função é aplicável à mesma combinação de valores de dimensão de preço que existe na linha principal **Preço da função** ou **Markup de Preço da Função**.
> - A data selecionada no campo **Início da Vigência** deve estar dentro das datas de efetivação da lista de preços principal. A substituição de preço entrará em vigor na data selecionada no campo **Início da Vigência** e será aplicada até o final da data de término da lista de preços principal. Se você configurar outra substituição de preço de data de efetivação para o mesmo preço de função, a primeira substituição de preço entrará em vigor na data selecionada no campo **Início da Vigência** e será aplicada até o início da segunda substituição.

## <a name="examples"></a>Exemplos

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Exemplo 1: determinar a data de vigência de um preço de função que tem substituições de preço de função

O exemplo a seguir mostra como a data de vigência é determinada para um preço de função específico para o qual as substituições de preço de função estão configuradas.

**Lista de preços: 1º de janeiro a 30 de junho**

*Preço da função*

| Preço da função | Unidade | Preço | Efeito no preço das transações recebidas |
|---|---|---|---|
| Técnico de Rede | Hora | 100 | Este preço será usado em todas as transações em que a data da transação estiver entre 1º de janeiro e 14 de março. |

*Substituição de preço de função*

| Início da vigência | Unidade | Preço | Efeito no preço das transações recebidas |
|---|---|---|---|
| Março de 15 | Hora | 110 | Este preço será usado em todas as transações em que a data da transação estiver entre 15 de março e 30 de março. |
| Abril 1 | Hora | 120 | Este preço será usado em todas as transações em que a data da transação estiver entre 1º de abril e 30 de junho. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Exemplo 2: determinar a data de vigência para uma markup de preço de função que tem substituições de markup de preço de função

O exemplo a seguir mostra como a data de vigência é determinada para uma markup de preço de função específica para a qual as substituições de markup de preço de função estão configuradas.

**Lista de preços: 1º de janeiro a 30 de junho**

*Preço da função*

| Preço da função | Horário de trabalho | Unidade | Preço | Efeito no preço das transações recebidas |
|---|---|---|---|---|
| Técnico de Rede | Regular | Hora | 100 | Este preço será usado em todas as transações em que a data da transação estiver entre 1º de janeiro e 14 de março. |

*Markup de Preço da Função*

| Unidade organizacional | Horário de trabalho | % de markup |
|---|---|---|
| Cabral EUA | Horas Extras | 10% |

*Substituições de markup de preço de função*

| Início da vigência | Preço | Efeito no preço das transações recebidas |
|---|---|---|
| Março de 15 | 20% | Esta porcentagem de markup será usada em todas as transações em que a data da transação estiver entre 15 de março e 30 de março. |
| Abril 1 | 25% | Este markup será usado em todas as transações em que a data da transação estiver entre 1º de abril e 30 de junho. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
