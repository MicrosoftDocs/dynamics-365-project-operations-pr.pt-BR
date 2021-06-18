---
title: Alterações de entidade, controle e interface de usuário (Project Service Automation 3.x)
description: Este tópico descreve alterações de solução para o Microsoft Dynamics Project Service Automation 3.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e3d6f515cec51cb30f83ff22a14ecb125dc81214
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007937"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Alterações de entidade, controle e interface de usuário (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Na versão do Microsoft Dynamics Project Service Automation (PSA) 3.x foram feitas muitas alterações nas entidades, nos controles, nas exibições e na interface de usuário. Este tópico fornece informações sobre essas importantes alterações.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relações entre pai e filho para documento de vendas, linha de documento de vendas, entidades de detalhes da linha de documento
Em versões do Dynamics 365 Project Service Automation (PSA) anteriores à versão 3.0, algumas das relações entre documentos de vendas, linhas de documento de vendas e entidades de detalhes da linha de documento eram implementadas por meio dos campos de cadeia de caracteres que mantinham a representação de uma cadeia de caracteres do GUID da entidade relacionada. Isso se devia às limitações da plataforma que exigiam código personalizado significativo nos lados do servidor e cliente da solução para fazer essas relações funcionarem de modo semelhante às relações de entidade típicas do Dynamics CRM e para fazer com que campos de cadeia de caracteres atuassem como campos de pesquisa.

O PSA 3.0 foi atualizado para aproveitar as novas relações de entidade entre documento de vendas e entidades de linha do documento de vendas.

Como os campos de pesquisa agora podem ser usados para indicar referências às entidades, os campos que mantinham o valor da cadeia de caracteres do GUID da entidade relacionada nas versões anteriores não são mais necessários e, portanto, foram preteridos. O código do lado do cliente e servidor personalizado que lida com as relações definidas pelos campos de cadeia de caracteres herdados também foi preterido.

### <a name="entity-schema-changes"></a>Alterações do esquema da entidade
A tabela a seguir apresenta uma lista um para um dos campos de cadeia de caracteres preteridos e os novos campos de pesquisa para as entidades. 

 Entidade |   Campo preterido (Cadeia de caracteres) | Novo campo (Pesquisa)
--- | --- | ---
invoicedetail (Linha da Fatura) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Real) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Agenda da Fatura da Linha de Contrato do Projeto) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Etapa da Linha de Contrato do Projeto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Fato) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Detalhes da Linha da Fatura) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Linha do Diário) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Categoria de Recurso da Linha de Contrato do Projeto) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Detalhes da Linha de Contrato do Projeto) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Categoria da Transação da Linha de Contrato do Projeto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Classificação da Transação da Linha de Contrato do Projeto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Agenda da Fatura da Linha de Cotação) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Categoria de Recurso da Linha de Cotação) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Etapa da Linha de Cotação) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Detalhes da Linha de Cotação) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Categoria de Transação da Linha de Cotação) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Classificação de Transação da Linha de Cotação) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Linha da Ordem) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Exibições e controles personalizados preteridos
Os controles e exibições personalizados a seguir e seus artefatos relacionados foram preteridos.

- Exibição dos encargos.
- Controles de grade personalizados para mostrar detalhes da linha de cotação na página **Informações do Projeto** para a linha da cotação.
- Controles de grade personalizados para mostrar detalhes da linha de contrato do projeto na página **Informações do Projeto** para a linha da ordem de venda.

> [!NOTE]
> Para obter a lista completa de recursos preteridos, consulte [Recursos da Web preteridos no Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Módulo do Aplicativo Interface do Cliente Unificada
Com a introdução dos Módulos do Aplicativo UCI (Interface do Cliente Unificada), as entradas do mapa do site do PSA foram removidas do sistema.  
A funcionalidade relacionada à alternância de formulário para Oportunidade, Cotação, Ordem, Fatura foi preterida, uma vez que ela não é mais necessária, pois o Módulo do Aplicativo UCI inclui apenas versões dos formulários do PSA.  

Os seguintes recursos da Web foram preteridos:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Para obter a lista completa de recursos preteridos, consulte [Recursos da Web preteridos no Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]