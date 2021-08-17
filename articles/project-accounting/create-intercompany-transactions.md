---
title: Criar transações intercompanhia
description: Este tópico fornece informações sobre como criar transações intercompanhia.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4ce3a45e5a09b7ac5b5663cf9983e3bed7bf7e0d3fedede2e4524c51069a800b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005467"
---
# <a name="create-intercompany-transactions"></a>Criar transações intercompanhia

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

As transações intercompanhia são transações de tempo e despesas de um contrato de projeto que pertence a uma empresa ou unidade organizacional, enquanto os recursos no contrato do projeto fazem parte de uma empresa ou unidade organizacional diferente.

Quando uma transação intercompanhia é aprovada, as transações reais a seguir são criadas

| **Tipo de transação** | **Lista de preços aplicada** | **Moeda da transação** |
| --- | --- | --- |
| Custo | Lista de preços de custo da unidade de contratação | Moeda na linha de preço |
| Vendas não cobradas. Elas são criadas somente para horas trabalhadas associadas a uma linha de contrato com o tipo de cobrança, horas e materiais. | Lista de preços de venda do projeto do contrato | Moeda do contrato |
| Custo da unidade de recursos | Lista de preços de custo da unidade de recursos | Moeda na linha de preço |
| Vendas entre unidades organizacionais | Lista de preços de custo da unidade de contratação | Moeda na linha de preço |

O custo, o custo da unidade de recursos e os preços e a moeda de transação de vendas entre unidades organizacionais são derivados da **unidade organizacional**. É importante lembrar disso ao decidir como estruturar empresas e unidades organizacionais em sua implementação.

Quando você cria oportunidades, cotações, contratos de projeto e registros de projetos, o sistema verifica se a moeda da unidade de contratação corresponde à moeda contábil da empresa contratante. Quando elas não são iguais, não é possível criar esses registros. A moeda da unidade organizacional é definida no Dynamics 365 Project Operations acessando **Dataverse** > **Configurações** > **Unidades organizacionais**. A moeda contábil de uma empresa é definida no Dynamics 365 Finance acessando **Contabilidade** > **Configuração do razão** > **Razão**. A moeda é sincronizada com seu ambiente do Dataverse usando o mapa de Gravação Dupla do Razão.

O sistema cria custos de unidade de recursos e vendas reais entre unidades organizacionais nas seguintes situações:

  - Quando a unidade de recursos difere da unidade contratante
  - Quando a empresa de recursos difere da empresa contratante

No entanto, somente as transações que tenham uma empresa de recursos diferente da empresa contratante serão transferidas para o ambiente do Dynamics 365 Finance para contabilidade adicional.

A contabilidade dos valores reais do projeto é registrada no diário de integração do Project Operations no Finance. O sistema cria as linhas de diário a seguir.

| **Tipo de transação** | **Pessoa jurídica** | **Cria a transação de projeto no lançamento** | **Remetente padrão das dimensões financeiras** | **Grupo de impostos de cobrança padrão e grupo de impostos do item de cobrança** |
| --- | --- | --- | --- | --- |
| Custo | Não é adicionado ao diário de integração | N/A | N/A | N/A |
| Vendas não cobradas | O diário de integração da entidade legal que toma o empréstimo | Sim | Project | **Grupo de impostos de cobrança**: com base no **cliente do contrato** <br/> **Grupo de impostos do item de cobrança**: da categoria de projeto de entidade legal atual na linha do diário |
| Custo da unidade de recursos | Diário de integração da entidade legal que faz o empréstimo | No | Cliente intercompanhia | **Grupo de impostos de cobrança**: com base no **cliente intercompanhia** <br/> **Grupo de impostos do item de cobrança**: da categoria de projeto de entidade legal atual na linha do diário |
| Vendas entre organizações | Diário de integração da entidade legal que faz o empréstimo | No | Cliente intercompanhia | **Grupo de impostos de cobrança**: com base no **cliente intercompanhia** <br/> **Grupo de impostos do item de cobrança**: da categoria de projeto de entidade legal atual na linha do diário |

### <a name="example-intercompany-transactions"></a>Exemplo: transações intercompanhia

Marcela Teles, desenvolvedora empregada na GBPM, registra 10 horas de trabalho em um projeto da USPM da Adventure Works, que é aprovado pelo gerente de projeto. O custo do desenvolvedor na GBPM é de 88 GBP por hora. A GBPM cobrará a USPM 120 USD por hora de desenvolvedor. A USPM cobrará do cliente Adventure Works, 200 USD pelo trabalho realizado pelo recurso da GBPM. Para obter mais informações, consulte [Configurar o faturamento intercompanhia](configure-intercompany-invoicing.md).

1. No Project Operations, acesse **Recursos** e selecione **Marcela Teles** na lista. Na guia **Agendamento**, no campo **Empresa**, selecione **GBPM**.
2. Acesse **Vendas** > **Clientes** e selecione **Novo** para criar um novo registro de cliente para a Adventure Works.
    1. Defina a empresa como **USPM**.
    2. Defina **Tipo de relacionamento** como **Cliente**.
    3. Selecione **Grupo de clientes 10 – Doméstico**.
    4. Defina a moeda como **USD**.
    5. Salve o registro.
3. Acesse **Vendas** > **Contratos do Projeto** e crie um contrato de projeto para a Adventure Works.
    1. Defina a empresa proprietária como **USPM** e a unidade contratante como **Contoso Robotics US**.
    2. Selecione Adventure Works como o cliente.
    3. Selecione uma lista de preços de produtos e salve o registro.
    4. Na guia **Linhas de Contrato**, crie uma linha de contrato. Defina um nome e selecione **Tempo e Material** como o método de cobrança.
    5. Crie um projeto e associe-o à linha de contrato.
4. Entre como o recurso **Marcela Teles**. Acesse **Projetos** > **Entradas de hora** e crie uma entrada de hora para o projeto da Adventure Works.
5. Entre como o Gerente de projeto. Acesse **Projetos** > **Aprovações** e aprove a transação de entrada de horas registrada por Marcela Teles.
6. Navegue até o projeto da Adventure Works e selecione **Relacionado** > **Dados Reais**. As transações reais a seguir serão criadas.

| **Tipo de transação** | **Preço** | **Moeda da transação** | **Valor** |
| --- | --- | --- | --- |
| Custo | 120 | USD | 1200 |
| Vendas não cobradas | 200 | USD | 2000 |
| Custo da unidade de recursos | 88 | GBP | 880 |
| Vendas entre unidades organizacionais | 120 | USD | 1200 |

7. Entre como um contador da USPM. Abra a instância do Finance do Project Operations e selecione a empresa **USPM**. 
8. Acesse **Gerenciamento e contabilidade de projeto** > **Atividades Periódicas** > **Project Operations no Customer Engagement** > **Importar da preparação** e selecione para executar o processo periódico. Esse processo periódico preencherá o diário de integração no Project Operations.
9. Acesse **Gerenciamento e contabilidade de projeto** > **Diários** > **Diário de integração do Project Operations** e revise as linhas do diário. O sistema cria a linha a seguir.

    | **Tipo de transação** | **Preço** | **Moeda da transação** | **Valor** |
    | --- | --- | --- | --- |
    | Vendas não cobradas | 200 | USD | 2000 |

    Se o sistema estiver configurado para acumular receita para este projeto, o seguinte será lançado:

    - Débito: Projeto – Valor de vendas do WIP 200 USD
    - Crédito: Projeto – Receita Acumulada 200 USD

    Esta venda não cobrada agora está pronta para faturamento. A fatura do cliente Adventure Works pode ser lançada financeiramente quando necessário.

10. Entre como o contador da **GBPM**. Abra a instância do Finance do Project Operations e abra a empresa **GBPM**. 
11. Acesse **Gerenciamento e contabilidade de projetos** > **Periódico** > **Integração do Project Operations** > **Importar da tabela de preparo** e execute o processo periódico para preencher o diário de Integração do Project Operations.
12. Acesse **Gerenciamento e contabilidade de projeto** > **Diários** > **Diário de integração do Project Operations** e revise as linhas. O sistema cria as linhas a seguir.

    | **Tipo de transação** | **Preço** | **Moeda da transação** | **Valor** |
    | --- | --- | --- | --- |
    | Custo da unidade de recursos | 88 | GBP | 880 |
    | Vendas entre unidades organizacionais | 120 | USD | 1200 |

    Lançar esses registros resulta nas seguintes transações de comprovante:

    - Débito: Projeto custa 88 GBP
    - Crédito: Alocação de folha de pagamento 88 GBP

    Se o sistema estiver configurado para acumular receita intercompanhia, o seguinte será lançado:

    - Débito: Projeto – Valor de vendas do WIP 120 USD
    - Crédito: Projeto – Receita Acumulada 120 USD

    O sistema agora está pronto para criar uma fatura de cliente intercompanhia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
