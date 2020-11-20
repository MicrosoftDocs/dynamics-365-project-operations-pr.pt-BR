---
title: Exibir horas trabalhadas passíveis de cobrança para recursos
description: Este tópico fornece informações sobre a exibição de horas trabalhadas do recurso.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: a1d1db532c65b2a13f3cf4e1281a5987490b96df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122149"
---
# <a name="view-chargeable-utilization-for-resources"></a>Exibir horas trabalhadas passíveis de cobrança para recursos
 
A **Exibição das Horas Trabalhadas** na página **Horas Trabalhadas do Recurso do Project Service** mostra as horas trabalhadas passíveis de cobrança de cada recurso reservável. Como a exibição é baseada no quadro de agendamento, você encontrará muitas funções iguais.

> ![Captura de tela da exibição Horas trabalhadas](media/FAQ-utilization-1.png)
 

O cálculo das horas trabalhadas passíveis de cobrança funciona da seguinte maneira:

   Horas trabalhadas passíveis de cobrança = (horas de dados reais passíveis de cobrança) / (capacidade do recurso)

As células representam as horas trabalhadas passíveis de cobrança calculadas para o período selecionado (dias, semanas ou meses).

As cores em cada célula mostram as horas trabalhadas passíveis de cobrança para um recurso em comparação com as horas trabalhadas passíveis de cobrança de destino. 

As horas trabalhadas de destino podem ser definidas na função padrão do recurso ou no recurso individual em si. O cálculo analisa o individual para o destino primeiro e, em seguida, para a função padrão do recurso.

## <a name="set-target-on-a-resource"></a>Definir destino em um recurso

1. Vá para **Recursos** \> **Recursos**. 
2. Selecione um recurso para abrir o registro. 
3. Na guia **Project Service**, você pode definir as horas trabalhadas de destino do recurso.

> ![Captura de tela do uso da guia Project Service para definir as horas trabalhadas de destino](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Definir horas trabalhadas de destino em uma função

1. Vá para **Recursos** \> **Funções do Recurso**. 
2. Selecione uma função e abra o registro. 
3. Defina as horas trabalhadas de destino para a função.

> ![Captura de tela do uso de Funções de recursos para definir as horas trabalhadas de destino](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Calcular horas trabalhadas passíveis de cobrança para um recurso

Para calcular as horas trabalhadas passíveis de cobrança para um recurso, é necessário preencher alguns pré-requisitos. 

### <a name="set-default-role-for-individual-resource"></a>Definir função padrão para recurso individual

Em primeiro lugar, as horas trabalhadas de destino devem ser definidas no recurso individual ou nas funções de recurso. Se você estiver usando funções de recursos para destinos, cada recurso individual deve ter uma função padrão. 

1. Para isso, vá para **Recursos** \> **Recursos**. 
2. Selecione um recurso, abra o registro e selecione a guia **Project Service**. 
3. Na grade **Função do Recurso**, verifique se há uma função para o recurso e se **É Padrão** está definido como **Sim**.
 
### <a name="change-billing-type-for-resource-role"></a>Alterar tipo de cobrança para função do recurso

As funções do recurso devem estar definidas para ter um tipo de cobrança **Passível de Cobrança**. 

1. Vá para **Recursos** \> **Funções do Recurso**. 
2. Abra o registro que deseja atualizar e defina o padrão do tipo de cobrança como **Passível de Cobrança**.

### <a name="set-working-hours-for-resource-role"></a>Definir horas de trabalho para a função do recurso
 
O recurso deve ter as horas de trabalho para o cálculo de capacidade. 

1. Vá para **Recursos** \> **Recursos**. 
2. Selecione um recurso para abrir o registro e selecione **Mostrar Horas de Trabalho**. 
3. Você pode atualizar em massa a lista de recursos aplicando um **Modelo de Horas de Trabalho** na exibição **Lista de Recursos**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Solucionando problemas de horas reais passíveis de cobrança

As horas reais passíveis de cobrança são provenientes da entidade **Dados reais**. Os dados reais com um tipo de cobrança **Passível de Cobrança** são incluídos no cálculo e, por isso, é necessário ter projetos em que os dados reais são passíveis de cobrança.

Se você não está vendo as horas trabalhadas passíveis de cobrança, veja a seguir alguns aspectos que você pode verificar:

- O recurso tem horas de trabalho definidas para a capacidade.
- O recurso tem horas trabalhadas de destino definidas individualmente ou tem uma função padrão atribuída a ele. A função tem horas trabalhadas de destino definidas para ela.
- Os dados reais têm um tipo de cobrança de **Passível de Cobrança** para o período pelo qual você está aguardando o cálculo de horas trabalhadas. Verifique o seguinte se você estiver vendo dados reais com tipos de cobrança diferentes de passível de cobrança:

  - A função usada nos dados reais tem em um tipo padrão de cobrança que não é passível de cobrança.
  - A função na linha de contrato de projeto dando suporte ao projeto foi definida como não passível de cobrança.
  - O projeto não tem uma linha de contrato associada.

