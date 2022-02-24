---
title: Contratos de projeto
description: Este tópico fornece exemplos de contratos de projeto que você pode criar para vários tipos de projetos e fontes de financiamento, e como você pode gerenciar contratos e faturar clientes do projeto.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071559"
---
# <a name="project-contracts"></a>Contratos de projeto

[!include [banner](../includes/banner.md)]

Este artigo fornece exemplos de contratos de projeto que você pode criar para vários tipos de projetos e fontes de financiamento, e como você pode gerenciar contratos e faturar clientes do projeto.

O tipo de projeto que você cria para um contrato de projeto determina o método que é usado para faturar clientes do projeto. Você pode alterar um contrato de projeto e o projeto relacionado, mas não pode alterar o tipo de projeto. 

Ao usar um contrato de projeto, você pode faturar um ou mais projetos ao mesmo tempo. O contrato de projeto também ajuda a garantir um procedimento de faturamento consistente para todos os subprojetos em uma estrutura de projetos. 

Cada projeto que será faturado deve estar associado a um contrato de projeto. As configurações de um contrato de projeto se aplicam a todos os projetos e subprojetos associados a esse contrato de projeto. 

Um contrato de projeto pode especificar uma ou mais fontes de financiamento. Portanto, você pode dividir a cobrança entre vários financiadores, definir limites de financiamento para que as fontes de financiamento não sejam cobradas mais do que um valor especificado e configurar regras de financiamento para cobrar despesas.

## <a name="funding-for-project-contracts"></a>Financiamento para contratos de projeto
Alguns contratos de projeto especificam que várias partes compartilham a responsabilidade pelo financiamento dos custos do projeto. Veja alguns exemplos:

-   Um grande cliente que tem várias divisões solicita que o financiamento de um projeto seja quebrado por divisão.
-   Sua empresa compartilha os custos de um grande projeto com uma organização externa.
-   Um projeto rodoviário é cofinanciado por dois municípios.
-   O projeto de uma ponte é financiado por uma concessão do governo e uma empresa privada.

No Dynamics 365 Finance, você pode dividir a cobrança de uma única transação ou de um projeto inteiro entre vários clientes, concessões ou organizações. 

Em projetos que têm vários financiadores, todas as partes que contribuem para o financiamento de um projeto de financiamento avançado são chamadas de fontes de financiamento. Depois que um cliente, organização ou concessão é definido como uma fonte de financiamento, ele pode ser atribuído a uma ou mais regras de financiamento. As regras de financiamento contêm os critérios que determinam como as cobranças são alocadas às várias fontes de financiamento de um projeto. 

Já que itens em estoque, como aqueles que aparecem nas requisições e pedidos de compra, não podem ser divididos, o valor do custo não pode ser dividido entre várias fontes de financiamento no momento da distribuição. Portanto, o valor da fonte de financiamento permanece 0 (zero) até que a saída do estoque seja lançada. Quando a saída do estoque é lançada, o valor do custo é distribuído de acordo com as regras de distribuição de contas do projeto.

Veja algumas etapas que você pode seguir para facilitar a divisão da cobrança entre várias fontes de financiamento:

-   Especificar que todas as transações inseridas para um projeto usem a mesma moeda de venda que o contrato de projeto.
-   Estabelecer limites de financiamento, de modo que uma fonte de financiamento não fature mais do que um valor especificado para um projeto.
-   Configurar regras e limites de financiamento para cada funcionário, item, categoria, grupo de categoria e tipo de transação (ou para todos os tipos de transação).
-   Selecionar datas de início e de término opcionais para definir o período em que cada regra de financiamento é válida.
-   Especificar a porcentagem pela qual cada fonte de financiamento é responsável.
-   Especificar qual fonte de financiamento é responsável pelas diferenças de arredondamento causadas por cálculos de alocação de financiamento.
-   Configurar regras que determinem como os custos do projeto são faturados para clientes externos e cobrados de organizações internas.
-   Registrar as transações em uma conta de financiamento retido até que um financiamento adicional possa ser obtido ou até que você decida arcar com os custos internamente.

Para determinar qual grupo de impostos associar a uma transação, é feita uma pesquisa no projeto em busca de uma atribuição de grupo de impostos. Se nenhuma atribuição de grupo de imposto foi feita no nível do projeto, é feita uma pesquisa no contrato de projeto.

### <a name="example-multiple-funding-sources-simple"></a>Exemplo: múltiplas fontes de financiamento (simples)

A tabela a seguir fornece cenários para gerenciar a alocação de financiamento entre várias fontes de financiamento. Esses cenários são baseados nas seguintes suposições:

-   As configurações de prioridade são levadas em consideração na alocação de fundos antes que outros critérios de regra de financiamento sejam aplicados.
-   Nenhum intervalo de datas foi especificado para definir o período quando a regra de financiamento é válida.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Cenário</strong></td>
<td><strong>Fonte de financiamento</strong></td>
<td><strong>Porcentagem de alocação</strong></td>
<td><strong>Prioridade de alocação</strong></td>
</tr>
<tr class="even">
<td>Você deseja alocar os custos a uma fonte de financiamento até que seus fundos se esgotem, alocar os custos a uma segunda fonte de financiamento até que seus fundos se esgotem e, por fim, alocar os custos restantes a uma terceira fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
<li>Fonte de financiamento 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Você deseja alocar 75% dos custos para uma fonte de financiamento e 25% para uma segunda fonte de financiamento. Quando os recursos dessas fontes de financiamento se esgotarem, você deseja pagar os custos restantes em uma terceira fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
<li>Fonte de financiamento 3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>0</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Você deseja alocar 75% dos custos para uma fonte de financiamento e 25% para uma segunda fonte de financiamento. Quando os recursos dessas fontes de financiamento se esgotarem, você deseja dividir custos restantes entre uma terceira e uma quarta fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
<li>Fonte de financiamento 3</li>
<li>Fonte de financiamento 4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>0</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Você deseja alocar os primeiros 25% dos custos para uma fonte de financiamento e o restante para uma segunda fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Exemplo: múltiplas fontes de financiamento (complexo)

Você tem três fontes de financiamento que deseja usar na seguinte ordem:

1.  Usar as fontes de financiamento 2 e 3 igualmente até que a fonte de financiamento 2 se esgote.
2.  Continuar a usar a fonte de financiamento 3 até que ela se esgote.
3.  Usar a fonte de financiamento 1 depois que a fonte de financiamento 3 se esgotar.

Para atingir essa meta, primeiro faça o seguinte:

-   Estabeleça limites de financiamento para as fontes de financiamento 2 e 3, para seus respectivos valores.
-   Crie as seguintes regras de financiamento:
    -   Regra 1 (prioridade 1): alocar 50% das transações para a fonte de financiamento 2 e 50% para a fonte de financiamento 3.
    -   Regra 2 (prioridade 2): alocar 100% das transações para a fonte de financiamento 3.
    -   Regra 3 (prioridade 3): alocar 100% das transações para a fonte de financiamento 1.

Essa configuração funciona porque as transações são verificadas em relação às regras e limites para determinar se alguma delas se aplica à transação. Se nenhuma regra ou limite específico se aplicar à transação, a regra Todas as transações se aplica. A regra Todas as transações corresponde a todas as transações. 

Se for encontrada uma regra que corresponda a uma transação, a porcentagem que foi alocada nessa regra será aplicada primeiro, mas somente depois que as correspondências forem verificadas em relação a quaisquer limites configurados. Se um limite foi atingido e os fundos de uma fonte de financiamento se esgotaram, a regra de financiamento associada ao limite de financiamento é desconsiderada e o programa verifica a próxima regra aplicável. 

Em alguns casos, apenas parte de uma transação pode ser alocada sob uma regra. Isso pode acontecer quando um limite é atingido ao alocar a transação. Nesse caso, apenas um determinado valor é alocado de acordo com essa regra, como 50% para cada fonte de financiamento. Esse é o caso da regra 1, descrita anteriormente nesta seção. O restante é alocado de acordo com a próxima regra na sequência. 

A tabela a seguir examina esse cenários em mais detalhes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Foco</strong></td>
<td><strong>Detalhes</strong></td>
</tr>
<tr class="even">
<td>Regras de financiamento</td>
<td><ul>
<li>Regra 1 (prioridade 1): todas as transações. Alocar a fonte de financiamento 2 em 50% e a fonte de financiamento 3 em 50%.</li>
<li>Regra 2 (prioridade 2): todas as transações. Alocar a fonte de financiamento 3 em 100%.</li>
<li>Regra 3 (prioridade 2): todas as transações. Alocar a fonte de financiamento 1 em 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Limites de financiamento</td>
<td><ul>
<li>Limite da fonte de financiamento 1 = 10.000,00</li>
<li>Limite da fonte de financiamento 2 = 500,00</li>
<li>Limite da fonte de financiamento 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transação 1</td>
<td><strong>Valor da transação:</strong> 100,00<strong>Financiamento:</strong> a transação é paga de acordo com a regra 1 apenas, porque a transação é totalmente paga após a aplicação da regra 1. A transação é financiada igualmente entre as fontes de financiamento 2 e 3.
<ul>
<li>Fonte de financiamento 2: 50,00</li>
<li>Fonte de financiamento 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transação 2</td>
<td><strong>Valor da transação:</strong> 5.000,00<strong>Financiamento:</strong> a transação é paga de acordo com as três regras. <strong>Regra 1</strong>
<ul>
<li>Fonte de financiamento 2: 450,00</li>
<li>Fonte de financiamento 3: 450,00</li>
</ul>
<strong>Regra 2</strong>
<ul>
<li>Fonte de financiamento 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Regra 3</strong>
<ul>
<li>Fonte de financiamento 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Total de fundos que são distribuídos para cada fonte de financiamento</td>
<td><ul>
<li>Fonte de financiamento 1: 3.850,00</li>
<li>Fonte de financiamento 2: 500,00</li>
<li>Fonte de financiamento 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Regras de cobrança
Ao negociar um contrato de projeto com um cliente, você define como e quando pode faturar o cliente pelo trabalho em um projeto. Depois de configurar o contrato de projeto e o projeto, você pode configurar as regras de cobrança do projeto. As regras de cobrança são baseadas nos termos do projeto especificados no contrato de projeto. As regras de cobrança que você pode criar dependem dos termos do contrato de projeto e do tipo de projeto (por exemplo, de tempo e material ou de preço fixo) que você associa à regra de cobrança. Você pode criar mais de uma regra de cobrança para um contrato de projeto. Você também pode atribuir uma regra de cobrança a vários projetos que estão associados ao mesmo contrato de projeto e têm termos de cobrança semelhantes. 

Você pode configurar os seguintes tipos de regras de cobrança:

-   **Unidade de entrega**: faturar um cliente ao concluir uma unidade de entrega. Você define as unidades de entrega no contrato.
-   **Progresso**: faturar um cliente quando você concluir uma porcentagem especificada do projeto. Você pode configurar uma regra de cobrança para calcular automaticamente a porcentagem de trabalho concluído, ou pode calcular manualmente a porcentagem de trabalho concluído e o valor para faturar o cliente.
-   **Etapa**: faturar um cliente pelo valor total de uma etapa do projeto quando ela for atingida.
-   **Taxa**: faturar um cliente por seus serviços, mais uma taxa de administração, que normalmente é uma porcentagem do custo dos serviços.
-   **Tempo e material**: faturar um cliente pelo valor do tempo e dos materiais usados em um projeto.

Para todos os tipos de regras de cobrança, você pode especificar uma porcentagem de retenção que é deduzida das faturas do cliente até que um projeto alcance um estágio combinado. A porcentagem de retenção de pagamento é especificada no contrato de projeto. O valor é calculado com base no valor total das linhas em uma fatura do cliente e subtraído dele. 

Para regras de cobrança de **Tempo e material** e **Progresso**, você pode atribuir categorias cobráveis. As categorias cobráveis indicam as transações que devem ser incluídas nas faturas do cliente. 

Quando você está pronto para faturar o cliente, o valor da fatura para o projeto é calculado com base nas regras de cobrança, e uma proposta de fatura do projeto é gerada. 

As seções a seguir fornecem exemplos que mostram como configurar e gerenciar regras de cobrança para um projeto.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Exemplo: criar uma regra de cobrança baseada no número de unidades entregues

Sua organização firma um contrato para fornecer um total de cinco sessões de treinamento para os funcionários de um cliente a um custo de 10.000 por sessão de treinamento. Você fatura o cliente após cada sessão de treinamento. 

Ao configurar as regras de cobrança para o contrato, você usa os seguintes valores:

-   A unidade de entrega é uma sessão de treinamento.
-   O preço unitário é 10.000 por sessão de treinamento.
-   O número total de unidades é cinco sessões de treinamento.

Quando tiver concluído uma sessão de treinamento, você poderá criar uma fatura de 10.000 para a primeira unidade que foi entregue, e enviar a fatura ao cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Exemplo: criar uma regra de cobrança com base em uma porcentagem especificada de conclusão do projeto (cálculo manual)

Sua organização, uma empresa de consultoria de software, celebra um contrato com um cliente para desenvolver parte de um produto que o cliente está desenvolvendo. Sua organização concorda em entregar o código do software em um período de seis meses. O cliente concorda em pagar à sua organização um total de 100.000 pelo trabalho. Você cria uma regra de cobrança para faturar o cliente com base na porcentagem de trabalho concluído no projeto, conforme especificado no contrato.

-   No final do primeiro mês, você se encontra com o cliente para determinar a porcentagem do trabalho concluído. Depois que você e o cliente analisam o projeto, você decide que ele está 15% concluído.
-   Você cria uma fatura de 15.000 (15% de 100.000) e a envia ao cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Exemplo: criar uma regra de cobrança com base em uma porcentagem especificada de conclusão do projeto (cálculo automático)

Sua organização, uma empresa de desenvolvimento de software, concorda em desenvolver um pacote de contabilidade da folha de pagamento para um cliente por 30.000. O cliente concorda em pagar à sua organização com base em uma porcentagem do trabalho concluído. Você estima que os custos do projeto são 20.000. O contrato do projeto especifica as categorias de trabalho que você usa no processo de cobrança. Você configura regras de cobrança que calculam automaticamente os valores da fatura para a porcentagem de trabalho concluído em cada categoria. Você configura um orçamento para cada categoria:

-   **Desenvolvimento**: custo de 15.000 e receita de 20.000
-   **Instalação**: custo de 5.000 e receita de 10.000

Quando você cria uma fatura do cliente pela primeira vez, o valor dela é calculado automaticamente com base nas seguintes informações:

-   Depois de um mês, o funcionário do projeto envia uma folha de ponto para o projeto. O custo das horas do funcionário é de 5.000 para desenvolvimento e 1.000 para instalação. O trabalho de desenvolvimento está 33% concluído (custo real de 5.000/custo orçado de 15.000) e o trabalho de instalação está 20% concluído (custo real de 1.000/custo orçado de 5.000).
-   O valor da fatura de 8.667 é calculado automaticamente (33% de 20.000 + 20% de 10.000).
-   Você cria uma fatura de 8.667 e a envia ao cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Exemplo: criar uma regra de cobrança baseada em etapas acordadas

Sua organização, uma empresa de consultoria de gestão, concorda em conduzir pesquisas de mercado para um produto de consumo que o cliente planeja vender. O cliente concorda em usar seus serviços por um período de três meses, começando em março, e concorda em pagar 50.000 à sua organização. O projeto tem três etapas:

-   Etapa 1: coletar dados de consumo – 31 de março
-   Etapa 2: analisar dados de consumo – 30 de abril
-   Etapa 3: apresentar uma proposta de viabilidade do produto – 31 de maio

O cliente concorda em pagar à sua organização 10.000 pela primeira etapa, 20.000 pela segunda e 20.000 pela terceira. 

Ao configurar o contrato de projeto, você concorda em cobrar o cliente com base na etapa que foi concluída. A configuração da regra de cobrança inclui os seguintes passos:

-   Definir as etapas do projeto.
-   Definir o valor para faturar o cliente quando cada etapa for concluída.

Quando a primeira etapa é concluída em 31 de março, você a marca como concluída e, em seguida, cria uma fatura de 10.000 e a envia ao cliente. Você não pode criar uma fatura para uma etapa até que tenha marcado essa etapa como concluída.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Exemplo: criar uma regra de cobrança baseada em serviços mais uma taxa de administração

Sua organização, uma empresa de consultoria de gestão, concorda em conduzir pesquisas de mercado para avaliar a viabilidade de um produto que o cliente, uma empresa de varejo, está desenvolvendo. Os termos do contrato especificam que você fornecerá os serviços de seus três principais consultores de gestão, que conduzirão a pesquisa com base no tempo e nos materiais utilizados. O cliente concorda em pagar 100 por hora, mais uma taxa de administração de 10% pelas horas de consultoria cobradas do projeto. 

Ao configurar o contrato do projeto, crie uma regra de cobrança para adicionar uma taxa de administração de 10% às horas de consultoria que são cobradas do projeto. 

Quando você cria uma fatura para o cliente, ele é cobrado uma taxa de administração de 10% mais o custo das horas de consultoria. Por exemplo, se os três consultores trabalharam um total de 200 horas no projeto, uma fatura de 22.000 será criada com base no seguinte cálculo:

-   200 horas a 100 por hora = 20.000
-   Taxa de administração de 10% = 2.000
-   Valor total da fatura = 22.000

Se as taxas forem tributáveis para um cliente e você selecionar um grupo de impostos sobre vendas no contrato de projeto, esse grupo será inserido automaticamente em uma regra de cobrança de taxas.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Exemplo: criar uma regra de cobrança para o valor de tempo e materiais

Sua organização, uma empresa de consultoria de software, concorda em fornecer cinco consultores técnicos para trabalhar em um projeto de desenvolvimento de software para um cliente nos próximos seis meses. O cliente concorda em pagar 150 por hora de consultoria, mais o custo do material de escritório. Sua organização envia uma fatura ao cliente no final de cada mês. 

Ao definir o contrato de projeto, você concorda em cobrar do cliente todo mês o tempo e os materiais do projeto. Você cria uma regra de cobrança que inclui as seguintes informações:

-   O período do contrato é de seis meses.
-   O tempo de consultoria é calculado a uma taxa de 150 por hora.
-   Os materiais de escritório são faturados pelo custo, e o custo total do projeto não deve exceder 10.000.
-   Você cria uma fatura do cliente no final de cada mês durante o projeto.

No primeiro mês, são registradas 800 horas pelos consultores do projeto. O custo do material de escritório cobrado do projeto é de 2.000. Portanto, ao final do mês, você cria uma fatura de 122.000, que é calculada como 800 horas a 150 por hora, mais 2.000 para materiais de escritório.



