---
title: Configurar contabilidade para projetos cobráveis
description: Este tópico fornece informações sobre as opções de contabilidade para projetos faturáveis.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1159a31ba4f30f09734bf9c5a9e594b5c77a831e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596450"
---
# <a name="configure-accounting-for-billable-projects"></a>Configurar contabilidade para projetos cobráveis

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations oferece suporte a várias opções de contabilidade para projetos faturáveis que incluem transações de hora e material e de preço fixo.

- **Transações de tempo e material**: essas transações são faturadas à medida que o trabalho avança, com base no consumo de horas, despesas, itens ou taxas no projeto. Esses custos de transação podem ser combinados com a receita de cada transação e o projeto é faturado à medida que o trabalho avança. A receita do projeto também pode ser acumulada no momento da transação. Durante o faturamento, a receita é reconhecida e, se aplicável, a receita acumulada é revertida.
- **Transações de preço fixo**: essas transações são faturadas de acordo com uma agenda de faturamento baseada no contrato do projeto. A receita de transações de preço fixo pode ser reconhecida no faturamento ou calculada e lançada periodicamente, de acordo com os métodos **Contrato concluído** ou **Porcentagem concluída**.

Um projeto é considerado faturável quando está associado a uma ou mais linhas de contrato. Uma linha de contrato define por si mesma qual método de cobrança e quais tipos de transação são permitidos.

Por exemplo, a Fabrikam Robotics ganhou um contrato de projeto com a Adatum Corporation para a otimização de equipamentos. A Adatum pagará uma quantia fixa de US$10.000 para cobrir as despesas incorridas do projeto. Esse é um método de cobrança de preço fixo. As horas e as taxas do projeto serão cobradas por uso. Esse é um método de cobrança por tempo e material. Todo o trabalho será monitorado em um único projeto denominado Otimização de equipamentos da Adatum.

Um membro da equipe do projeto registra 8 horas de trabalho no projeto de otimização de equipamentos da Adatum. Quando o gerente de projeto aprova essas horas, o sistema usa o método de cobrança por tempo e material para criar transações reais, uma fatura e uma conta. Essa transação não será incluída no cálculo de estimativa de receita de preço fixo.

Outro membro da equipe do projeto registra uma despesa de viagem no valor de US$2.000,00 referente ao projeto de otimização de equipamentos da Adatum. Quando o gerente de projeto aprova esse registro, o sistema usará o método de cobrança de preço fixo para criar transações reais e uma conta para as despesas desse projeto. O cliente não será faturado com base nessa transação. Em vez disso, ele será faturado usando etapas de cobrança configuradas separadamente. Essa transação da despesa, junto com as estimativas de despesas, será incluída no cálculo de estimativa de receita de preço fixo.

Os princípios de contabilidade para transações de projeto são definidos nos perfis de custo e receita do projeto. Para cada transação de projeto, o sistema determina o custo de projeto apropriado e o perfil de receita usando o custo de projeto e as regras de perfil de receita que foram configuradas.

## <a name="define-project-cost-and-revenue-profiles"></a>Definir perfis de custo e receita do projeto 

Os perfis de custo e receita do projeto determinam as regras de contabilidade para transações do projeto. Esses perfis são configurados em Gerenciamento e contabilidade de projeto. 

Execute as seguintes etapas para criar um novo perfil de custo e receita do projeto. 

1. Vá para **Gerenciamento e contabilidade de projeto** > **Configuração** > **Lançamento** > **Perfis de custo e receita do projeto**. 
2. Selecione **Novo** para criar um perfil de custo e receita do projeto.
3. No campo **Nome**, insira o nome e uma breve descrição do perfil.
4. No campo **Método de cobrança**, selecione **Tempo e material** ou **Preço fixo**.
5. Expanda a FastTab **Razão**. Os campos nesta guia definem os princípios de contabilidade que são usados quando as transações do projeto são lançadas em diário usando o diário de integração do Project Operations e faturadas por meio da proposta de fatura do Projeto.
6. Selecione as informações apropriadas nos seguintes campos na FastTab **Razão**:

    - **Lançar custos – hora**:

       - *Sem razão*: o custo de transações de horas não será lançado no Razão quando o diário de integração do Project Operations for lançado. No entanto, o contador pode lançar custos usando a função Lançar custos posteriormente.
       - **Saldo**: o custo de transações de horas será debitado no tipo de conta contábil, *WIP ‑ Valor de custo* e creditado na *Conta de alocação da folha de pagamento* na configuração de lançamento contábil. O contador usará a função Lançar custos para mover esse custo de uma Conta de saldo para uma Conta de lucros e perdas periodicamente.
       - **Lucros e perdas**: ao lançar o diário de integração de Project Operations, o custo de transação de tempo será debitado no tipo de conta contábil *Custo* e creditado na *Conta de alocação da folha de pagamento* definida na guia **Custo** na página **Configurar lançamento contábil** (**Gerenciamento e contabilidade de projeto** \> **Configuração** \> **Lançamento** \> **Configuração de lançamento contábil**). Essa é a configuração mais comum para transações de tempo e material.
        - *Nunca o Razão*: o custo para transações de horas nunca será lançado no Razão.

    - **Lançar custos – despesa**:

         - **Saldo**: ao lançar o diário de integração do Project Operations, o custo de transação de despesas será debitado no tipo de conta contábil *WIP ‑ Valor de custo* conforme definido na guia **Custo** na página **Configuração de lançamento do razão** e creditado na contrapartida da linha do diário. As contrapartidas de despesas estão definidas em **Gerenciamento e contabilidade de projeto** > **Configuração** \> **Lançamento** \> **Contrapartida padrão para despesas**. O contador usará a função **Lançar custos** para mover esse custo de uma conta de saldo para a conta de lucros e perdas periodicamente.
        - **Lucros e perdas**: ao lançar o diário de integração do Project Operations, o custo de transação de despesas será debitado no tipo de conta contábil *Custo* conforme definido na guia **Custo** na página **Configuração de lançamento do razão** e creditado na contrapartida da linha do diário. As contrapartidas de despesas estão definidas em **Gerenciamento e contabilidade de projeto** \> **Configuração** \> **Lançamento** \> **Contrapartida padrão para despesas**.
      
    - **Lançar custos – item**:

         - **Saldo**: ao lançar o diário de Integração do Project Operations, o custo de transação do item será debitado da conta Razão tipo *WIP - Valor de custo - item* conforme definido na guia **Custo** na página **Configuração de lançamento contábil** e creditado no seguinte:
    
              - Para o uso de tipo de documento: conta **Custo - item** na **Configuração de lançamento contábil**.  
              - Para compra do tipo de documento: **Conta de integração da aquisição** em **Parâmetros de gerenciamento e contabilidade de projetos**.
           O contador usará a função **Lançar custos** para mover esse custo de uma conta de saldo para a conta de lucros e perdas periodicamente.
        - **Lucros e perdas**: ao lançar o diário de Integração do Project Operations, o custo de transação do item será debitado da conta Razão tipo *Custo* conforme definido na guia **Custo** na página **Configuração de lançamento contábil** e creditado no seguinte:
         
             - Para o uso de tipo de documento: conta **Custo - item** na **Configuração de lançamento contábil**.  
             - Para compra do tipo de documento: **Conta de integração da aquisição** em **Parâmetros de gerenciamento e contabilidade de projetos**.
       
    - **Faturamento por conta**:

        - **Saldo**: ao lançar a Proposta de fatura do projeto, uma transação por conta (etapa de cobrança) será creditada no tipo de conta contábil *WIP Faturado - por conta* conforme definido na guia **Receita** na página **Configuração de lançamento contábil** e debitada na conta de saldo do cliente.
         - **Lucros e perdas**: ao lançar a Proposta de fatura do projeto, uma transação por conta (etapa de cobrança) será creditada no tipo de conta contábil *Receita faturada - por conta* conforme definido na guia **Receita** na página **Configuração de lançamento contábil** e debitada na conta de saldo do cliente. As contas de saldo do cliente são definidas em **Contas a receber** \> **Configuração** \> **Perfis de lançamentos de cliente**.

   Ao definir os perfis de lançamento para os métodos de cobrança por tempo e material, você tem a opção de acumular receita por tipo de transação (hora, despesa, item e taxa). Se a opção **Acumular receita** estiver definida como **Sim**, as transações de vendas não faturadas no Diário de integração do Project Operations serão registradas na Contabilidade. O valor da venda é debitado na conta **WIP ‑ valor de venda** e creditado na conta **Receita acumulada ‑ valor de venda** que foi configurada na página **Configuração do lançamento contábil**, na guia **Receita**. 
  
  > [!NOTE]
  > A opção, **Acumular receita** está disponível somente quando o tipo de transação **Custo** respectivo for lançado na conta de lucros e perdas.
    
7. Expanda a FastTab **Estimativa**. Os campos nesta guia definem as configurações de cálculo para estimativas de receita de preço fixo. Os campos nesta guia se aplicam somente a Perfis de custo e receita do projeto com um método de cobrança de **Preço fixo**.
8. Selecione as informações apropriadas nos seguintes campos na FastTab **Estimativa**:

    - **Princípio usado para cálculos de conclusão de projeto**:

        - **Contrato concluído**: a correspondência de custos e reconhecimento de receita não ocorrem até o final do projeto. Os custos são refletidos como WIP no saldo até que o projeto seja concluído.
        - **Percentual concluído**: a receita acumulada é calculada e lançada no razão a cada período com base na porcentagem de conclusão do projeto. Existem vários métodos disponíveis para calcular a porcentagem de conclusão. Esses métodos podem ser automáticos com base na configuração, ou manuais.
        - **Sem WIP**: esta configuração é usada para projetos de preço fixo com um intervalo de tempo curto e quando a fatura e os custos ocorrem no mesmo período. Nesse caso, o valor do campo **Faturamento por conta** na FastTab **Razão** é automaticamente definido como **Lucros e perdas** para garantir que a receita seja reconhecida no faturamento. O processo de estimativa de receita não será usado para este perfil de custo e receita do projeto.

    - **Princípio de correspondência**: este campo determina como o valor de venda calculado (receita acumulada) será lançado no razão.

        - Usando o princípio do **Valor de venda**, o sistema calculará o valor de venda associando custos e receitas e, em seguida, lançará um único valor.
        - Usando o princípio **Produção e lucro**, o sistema dividirá o valor de venda em custos realizados e lucro calculado. Eles são lançados separadamente.

    - **Modelos de custo**: permitem que as transações de projeto sejam agrupadas com base no tipo de transação e na categoria de projeto, além de definirem as regras de cálculo da porcentagem de conclusão para esses grupos.
    - **Códigos de período**: definem a frequência na qual as estimativas de receita são calculadas para um determinado perfil de custo e receita do projeto.
    - **Categorias para estimativas**: usadas para o lançamento do valor de venda (receita acumulada) para transações do Projeto. Primeiro, configure a categoria de projeto dedicada para um tipo de transação **Taxa** e depois defina o sinalizador **Estimativa** para essa categoria de projeto. Em seguida, dependendo do princípio de correspondência selecionado, escolha esta categoria de projeto no valor **Vendas** ou o campo **Lucro** no perfil de custo e receita do Projeto.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Configurações de amostra para Perfis de custo e receita do projeto

Tempo e materiais – sem WIP

![Perfil de custo e receita: tempo e materiais – sem WIP.](media/time-material-no-wip.png)

Tempo e materiais – WIP (receita)

![Perfil de custo e receita: tempo e materiais – WIP.](media/time-material-with-wip.png)

Preço fixo – Sem WIP

![Perfil de custo e receita: preço fixo – sem WIP.](media/fixed-price-no-wip.png)

Preço Fixo – contrato concluído

![Perfil de custo e receita: preço fixo – contrato concluído.](media/fixed-price-completed-contract.png)

Preço Fixo – porcentagem de conclusão

![Perfil de custo e receita: preço fixo – porcentagem de conclusão.](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Exemplos de evento contábil para exemplos de Perfis de custo e receita do projeto.

| Evento Contábil                  | Tempo e Material – Sem WIP                       | Tempo e Material – WIP                                                                                           | Preço fixo – sem WIP                                            | Preço fixo – Contrato concluído                                                                            | Preço Fixo – Porcentagem de conclusão                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Lançar transações de horas em diário    | Débito – Custo <br>Crédito – Alocação de folha de pagamento          | Débito ‑ Custo <br>Crédito – Alocação de Folha de Pagamento <br>Débito – WIP Valor de venda <br>Crédito – Valor de Venda da Receita Acumulada                | Débito – Custo <br>Crédito – Alocação de folha de pagamento                         | Débito – Custo <br>Crédito – Alocação de folha de pagamento                                                                    | Débito – Custo <br>Crédito – Alocação de folha de pagamento                       |
| Lançar transações de despesas em diário | Débito – Custo <br>Crédito – Contrapartida para despesas | Débito – Custo <br>Crédito – Contrapartida para despesas <br>Débito – WIP Valor de venda <br>Crédito – Valor de Venda da Receita Acumulada      | Débito – Custo <br>Crédito – Contrapartida para despesas                 | Débito – Custo<br> Crédito – Contrapartida para despesas                                                            | Débito – Custo <br>Crédito – Contrapartida para despesas               |
| Cliente do faturamento                | Débito – Saldo do cliente <br>Crédito – Receita faturada | Débito – Saldo do cliente <br>Crédito – Receita faturada <br>Crédito – WIP Valor de venda Débito – Valor de Venda da Receita Acumulada | Débito – Saldo do cliente <br>Crédito – Receita faturada - por conta | Débito – Saldo do cliente <br>Crédito – WIP – Receita faturada por conta                                                  | Débito – Saldo do cliente <br>Crédito – WIP - Receita faturada por conta    |
| Lançar Estimativa de Receita             | Não aplicável                                   | Não aplicável                                                                                                    | Não Aplicável                                                  | Débito – WIP Valor de Custo <br>Crédito – Custo                                                                         | Débito – WIP ‑ Valor de venda <br>Crédito – Valor de venda da Receita acumulada |
| Eliminar                         | Não aplicável                                   | Não aplicável                                                                                                    | Não Aplicável                                                  | Crédito – WIP Valor de Custo <br>Débito – Custo <br>Crédito – Receita Acumulada ‑ Valor de venda <br>Débito – WIP Receita faturada por conta | Débito – WIP – Receita faturada por conta <br>Crédito – WIP Valor de venda     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Configurar regras de Perfil de custo e receita

As regras do Perfil de custo e receita determinam o perfil de custo e receita que deve ser usado ao processar quaisquer transações de projeto faturáveis. Defina as regras acessando **Gerenciamento e contabilidade de projeto** \> **Configuração** \> **Lançamento** \> **Regras do perfil de custo e receita do projeto**.

As regras podem ser definidas por contrato de projeto, grupo de projeto ou por um projeto específico. O sistema sempre escolherá a regra de granularidade mais alta primeiro.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
