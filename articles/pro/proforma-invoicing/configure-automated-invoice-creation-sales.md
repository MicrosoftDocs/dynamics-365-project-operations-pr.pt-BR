---
title: Configurar a criação automática de fatura - lite
description: Este tópico fornece informações sobre a configuração da criação automática de faturas pro forma.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ce9cb9090c44762f370bf8d574d179077b6a821
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176552"
---
# <a name="configure-automatic-invoice-creation---lite"></a>Configurar a criação automática de fatura - lite
 
_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Você pode configurar a criação automática de faturas no Dynamics 365 Project Operations. O sistema cria um rascunho de fatura pro forma com base na agenda da fatura para cada contrato de projeto e linha de contrato. As programações de faturas são configuradas no nível da linha do contrato. Cada linha em um contrato pode ter uma agenda de fatura distinta ou a mesma agenda de fatura pode ser incluída em cada linha do contrato.

Quando você cria uma fatura, o sistema sempre cria pelo menos uma fatura por contrato de projeto. Em alguns casos, pode haver várias faturas criadas.

Por exemplo, se o contrato tiver vários clientes, o mesmo número de faturas será criado como o número de clientes que têm transações faturáveis para faturar nesse contrato de projeto.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Entenda como as transações são incluídas em uma fatura 

Às vezes, cada linha de contrato com base em projeto especifica uma agenda de fatura separada. Por exemplo, os serviços de implementação para o contrato Adatum têm as seguintes linhas de contrato:

- Trabalho de protótipo que tem um preço fixo com dois marcos criados manualmente.
- Trabalho de implementação que inclui Tempo e será cobrado a cada duas semanas às segundas-feiras.
- Despesas incorridas que precisam ser cobradas mensalmente na primeira segunda-feira de cada mês.

As programações de faturas definidas em cada um desses dois itens de linha se parecem com a seguinte tabela:

| Linha de contrato | Data de criação da fatura | Data de corte da transação | Data da etapa | Valor do marco |
| --- | --- | --- | --- | --- |
| Trabalho de protótipo | Segunda-feira, 5 de outubro | - | Segunda-feira, 5 de outubro | 5000 USD |
| - | Terça-feira, 3 de novembro | - | Terça-feira, 3 de novembro | 12,000 USD |
| Trabalho de implementação | Segunda-feira, 5 de outubro | Domingo, 4 de outubro | - | - |
| - | Segunda-feira, 19 de outubro | Domingo, 18 de outubro | - | - |
| - | Segunda-feira, 2 de novembro | Domingo, 1º de novembro | - | - |
| - | Segunda-feira, 16 de novembro | Domingo, 15 de novembro | - | - |
| Despesas incorridas | Segunda-feira, 5 de outubro | Domingo, 4 de outubro | - | - |
| - | Segunda-feira, 2 de novembro | Domingo, 1º de novembro | - | - |

Neste exemplo, quando o faturamento automático é executado em:

- **4 de outubro ou qualquer data antes**: nenhuma fatura é gerada para esse contrato porque a tabela **Agenda de Fatura** para cada uma dessas linhas de contrato não indica Domingo, 4 de outubro como uma data de execução da fatura.
- **Segunda-feira, 5 de outubro**: uma fatura é gerada para:

    - O trabalho de protótipo que inclui o marco, se ele estiver marcado como **Pronto para Faturar**.
    - Trabalho de implementação que inclui todas as transações de Tempo criadas antes da data limite da transação de Domingo, 4 de outubro, que está marcada como **Pronta para Faturar**.
    - Despesa incorrida que inclui todas as Transações de despesa criadas antes da data limite da transação de Domingo, 4 de outubro, que está marcada como **Pronta para Faturar**.
  
- **Em 6 de outubro ou em qualquer data antes de 19 de outubro**: nenhuma fatura é gerada para esse contrato porque a tabela **Agenda de Fatura** para cada uma dessas linhas de contrato não indica 6 de outubro ou qualquer data antes de 19 de outubro como uma data de execução da fatura.
- **Segunda, 19 de outubro**: uma fatura é gerada para trabalho de implementação que inclui todas as transações de Tempo criadas antes da data limite da transação de Domingo, 18 de outubro, que está marcada como **Pronta para Faturar**.
- **Segunda-feira, 2 de novembro**: uma fatura é gerada para:

    - Trabalho de implementação que inclui todas as transações de Tempo criadas antes da data limite da transação de Domingo, 1º de novembro, que está marcada como **Pronta para Faturar**.
    - Despesa incorrida que inclui todas as Transações de despesa criadas antes da data limite da transação de Domingo, 1º de novembro, que está marcada como **Pronta para Faturar**.

- **Terça-feira, 3 de novembro**: uma fatura é gerada para o trabalho de protótipo que inclui o marco para 12000 USD, se estiver marcado como **Pronto para faturar**.

## <a name="configure-automatic-invoicing"></a>Configurar o faturamento automático

Conclua as etapas a seguir para configurar a execução de uma fatura automatizada.

1. Em **Operações de Projeto**, vá para **Configurações** > **Configuração de Fatura Recorrente**.
2. Crie um trabalho em lote e denomine-o **Criar Faturas do Project Operations**. O nome do trabalho em lote deve incluir as palavras "criar faturas".
3. No campo **Tipo de Trabalho**, selecione **Nenhum**. Por padrão, os campos **Frequência Diária** e **Está Ativo** são definidos como **Sim**.
4. Selecione **Executar Fluxo de Trabalho**. Na caixa de diálogo **Pesquisar Registro**, você verá três fluxos de trabalho:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Selecione **ProcessRunCaller** e selecione **Adicionar**.
6. Na próxima caixa de diálogo, selecione **OK**. Um fluxo de trabalho **Suspender** é seguido por um fluxo de trabalho **Processar**. 

> [!NOTE]
> Também é possível selecionar **ProcessRunner** na etapa 5. Em seguida, quando você selecionar **OK**, um fluxo de trabalho **Processar** é seguido por um fluxo de trabalho **Suspender**.

Os fluxos de trabalho **ProcessRunCaller** e **ProcessRunner** criam faturas. **ProcessRunCaller** chama **ProcessRunner**. **ProcessRunner** é o fluxo de trabalho que de fato cria as faturas. O fluxo de trabalho passa por todas as linhas de contrato para as quais as faturas devem ser criadas e cria faturas para essas linhas. A fim de determinar as linhas de contrato para as quais as faturas devem ser criadas, o trabalho examina as datas de execução de fatura das linhas de contrato. Se as linhas de contrato que pertencem a um contrato tiverem a mesma data de execução de fatura, as transações serão combinadas em uma fatura que tenha duas linhas de fatura. Se não houver transações para as quais criar faturas, o trabalho pulará a criação de uma fatura.

Quando **ProcessRunner** termina de ser executado, ele chama **ProcessRunCaller**, fornece a hora de término e é fechado. **ProcessRunCaller** então inicia um timer que é executado por 24 horas a partir da hora de término especificada. Ao fim do timer, **ProcessRunCaller** é fechado.

O trabalho do processo em lote para criação de faturas é um trabalho recorrente. Se esse processo em lote for executado muitas vezes, várias instâncias do trabalho serão criadas e causarão erros. Portanto, você deve iniciar o processo em lote apenas uma vez e então reiniciar somente se a execução for interrompida.

> [!NOTE]
> O faturamento em lote no Project Operations só é executado para linhas de contrato de projeto configuradas por agendas de faturas. Uma linha de contrato com um método de cobrança de preço fixo deve ter marcos configurados. Uma linha de contrato do projeto com um método de cobrança de horas e de material precisará de uma configuração de agenda de faturas baseada em data.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]