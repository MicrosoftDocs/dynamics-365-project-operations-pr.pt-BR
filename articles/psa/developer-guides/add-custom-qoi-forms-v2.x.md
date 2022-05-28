---
title: Adicionar novos formulários de entidade personalizada (Project Service Automation 2.x)
description: Este tópico fornece informações sobre como adicionar formulários da entidade personalizada para oportunidades, cotações, ordens ou faturas no Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ffc702bbe9cedb2a0cc8da8d8f58e48005950127
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584306"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Adicionar novos formulários de entidade personalizada (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Campo Tipo 

O Dynamics 365 Project Service Automation depende do campo **Tipo** (**msdyn\_ordertype**) das entidades Oportunidade, Cotação, Ordem e Fatura para diferenciar versões **baseadas em trabalho** dessas entidades nas versões **baseadas em item** e **baseadas em serviço**. As versões baseadas no local dessas entidades são tratadas pelo PSA. Muito da lógica de negócios no cliente e servidor da solução depende do campo **Tipo**. Portanto, é importante que o campo seja inicializado com um valor correto quando as entidades são criadas. Um valor incorreto pode causar comportamentos incorretos, e alguma lógica de negócios pode não ser executada corretamente.

## <a name="automatic-form-switching"></a>Alternação automática de formulário

Para evitar a possível corrupção de dados e comportamentos inesperados que são causados pela inicialização e edição incorretas dos registros de entidade de vendas, o PSA agora inclui lógica para alternação automática de formulário em formulários prontos para uso. Essa lógica conduz os usuários ao formulário correto para trabalhar com a versão baseada em trabalho ou qualquer outro tipo de entidade Oportunidade, Cotação, Ordem ou Fatura. Quando um usuário abre a versão baseada em trabalho de uma entidade Oportunidade, Cotação, Ordem ou Fatura, o formulário é alternado para **Informações do Projeto**.

A lógica de alternância automática de formulário depende do mapeamento entre o valor **formId** e o campo **msdyn\_ordertype**. Todos os formulários prontos para uso foram adicionados a esse mapeamento. No entanto, os formulários personalizados devem ser adicionados manualmente para indicar com qual versão da entidade eles pretendem lidar. Isso se baseia no campo **msdyn\_ordertype**. Se a alternância de formulário não estiver no mapeamento, a lógica será alternada para o formulário pronto para uso, com base no valor que é salvo no campo **msdyn\_ordertype** da entidade.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Adicionar formulários personalizados e ativar a lógica de alternância de formulário

O exemplo a seguir mostra como adicionar um formulário **Informações do Meu Projeto** personalizado para que ele funcione com oportunidades baseadas em trabalho. O mesmo processo é usado para adicionar formulário personalizados para que eles funcionem com cotações, ordens e faturas.

Siga estas etapas para criar uma versão personalizada do formulário **Informações do Projeto**.

1. Na entidade Oportunidade, abra o formulário **Informações do Projeto** e salve uma cópia com o nome **Informações do Meu Projeto**.
2. Abra o novo formulário e, em seguida, nas propriedades, certifique-se de que os scripts de inicialização do formulário **Informações do Projeto** estejam presentes. 

    > [!IMPORTANT]
    > Não remova os scripts. Caso contrário, alguns dados podem ser inicializados incorretamente.

3. Verifique se o campo **Tipo** (**msdyn\_ordertype**) está presente no formulário. 

    > [!IMPORTANT]
    > Não remova esse campo. Caso contrário, os scripts de inicialização falharão.

4. Localize o valor **formId** do novo formulário. É possível concluir essa etapa de duas maneiras:

    - Exporte o formulário **Informações do Meu Projeto** como parte de uma solução não gerenciada e pesquise o valor **formId** no arquivo customization.xml da solução exportada.
    - Abra o formulário **Informações do Meu Projeto** no editor de formulários e procure o GUID (identificador global exclusivo) ao lado do parâmetro **fromId** na URL, conforme mostrado na ilustração a seguir.

    ![O valor formId do novo formulário na URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Crie um mapeamento **msdyn\_ordertype** para o valor **formId** editando o recurso da Web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Remova o código do recurso e substitua-o pelo código a seguir.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Salve e publique as personalizações.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
