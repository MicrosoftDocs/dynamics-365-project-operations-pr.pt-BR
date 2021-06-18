---
title: Usar recurso reservável como uma dimensão de preço
description: Este tópico fornece informações sobre como usar um recurso reservável como uma dimensão de preço.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0ffbb1f7aa25e723c7842259f1c0127b3d2e26d6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012077"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Usar recurso reservável como uma dimensão de preço

[!include [banner](../includes/psa-now-project-operations.md)]

Este tópico fornece informações sobre como usar um recurso reservável como uma dimensão de preço. Antes de começar, se você ainda não criou uma solução de dimensão de precificação, será necessário criar uma. Se você já possui uma solução de dimensão de precificação, poderá fazer suas alterações nessa solução. Se você não criou uma solução de dimensão de precificação para sua organização, conclua os procedimentos no tópico [Criar campos e entidades personalizados](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Adicionar recurso reservável a formulários e exibições
Para tornar visíveis os campos na interface do usuário na solução de dimensão de preço, você precisará passar por todos os formulários e exibições das principais entidades do Project Service e adicionar esses campos aos formulários e exibições dessas entidades.
A tabela a seguir apresenta uma lista abrangente de formulários e exibições prontos para uso, listados por entidade, que precisarão ser atualizados. Se houver qualquer exibição ou formulário adicional em suas personalizações nessas entidades, adicione os novos campos a eles também.
Abra o Gerenciador de Soluções para a solução de dimensão de preço e clique em **Publicar Todas as Personalizações**.


|   Entidade        | Formulários   |Exibições        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preço da Função|• Informações |• Preços Ativos de Categorias de Recursos<br> • Exibição Associada de Preços de Categorias de Recursos|
|  Markup de Preço da Função|• Informações|• Markup de Preço da Função Ativo<br>• Exibição Associada do Markup de Preço da Função|
|  Detalhes da linha de cotação|• Informações do Projeto<br>• Criação Rápida do ProJeto|• Detalhes da Linha de Cotação Ativos<br>• Detalhes Combinados da Linha de Cotação<br>• Exibição Associada de Detalhes da Linha de Cotação|
|  Detalhe da Linha de Contrato do Projeto|• Informações do Projeto<br>• Criação Rápida do ProJeto|• Detalhes Combinados da Linha de Contrato<br>• Detalhes da Linha de Contrato Ativa<br>• Exibição Associada de Detalhes da Linha de Contrato|
|  Tarefa do Projeto|• Informações<br>• Novo Formulário||
|  Membro da Equipe do Projeto|• Informações<br>• Novo Formulário|• Membros Ativos da Equipe do Projeto<br>• Membros da Equipe do Projeto<br>• Exibição Associada de Membros da Equipe do Projeto|
|  Entrada de Horas|• Informações<br>• Criar Entrada de Hora|• Minhas Entradas de Hora por Data<br>• Minhas Entradas de Horas para Esta Semana<br>• Entradas de hora para aprovação|
|  Linha do Diário|• Informações<br>• Criação rápida:|• Linhas de diário ativas<br>• Exibição Associada de Linhas de Diário|
|  Detalhes da Linha da Fatura|• Informações<br>• Criação rápida:|• Detalhes de Linha de Fatura Ativos<br>• Transações de Fatura Passíveis de Cobrança<br>• Transações de Fatura Complementares<br>• Exibição Associada de Detalhes de Linha de Fatura<br>• Transações de Fatura Não Passíveis de Cobrança|
|  Real|• Informações<br>• Dados Reais Ativos|• Exibição Associada de Dados Reais|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Configurar recurso reservável como uma dimensão de preço

1. Na interface da Web, vá para **Project Service** > **Configurações** > **Parâmetros**. Na página **Parâmetro**, na guia **Dimensões de Preço Baseadas em Valor**, observe que a grade na guia mostra os registros na entidade de dimensões de preço. 
2. Adicione **Recurso Reservável** a essa lista de dimensões de preço como **msdyn_bookableresource**. 
3. Indique o contexto no qual o recurso reservável funciona como uma dimensão de preço e defina os valores de **Aplicável ao custo** e **Aplicável a vendas**.
4. No campo **Tipo de Dimensão**, selecione **Baseado em Valor**. 
5. Selecione a prioridade de vendas e custo para o recurso reservável. Normalmente, quando incluído como uma dimensão de preço, um recurso reservável tem a prioridade mais alta, de modo que definir esse valor para **1** (ou **0** dependendo de como você conta a prioridade) garantiria esse comportamento.

## <a name="set-up-pricing-dimension-field-names"></a>Configurar nomes de campo de dimensão de preço

Quando o nome do campo de uma dimensão de preço na tabela **Preço da Função** for diferente do seu nome de campo em qualquer uma das outras entidades onde a padronização de preço precisa funcionar, o registro de dimensão de preço deve estar ciente dos nomes diferentes.    
Para recurso reservável, a entidade **Membros da Equipe do Projeto** tem um nome de campo ligeiramente diferente (**msdyn_bookableresourceid**) do que é chamado na entidade **Preço da função** (**msdyn_bookableresource**). O registro de dimensão de preço para **msydn_bookableresource** deve ser conscientizado disso. 
1. Para isso, clique duas vezes na linha da grade **Dimensões de Preço** para abrir a página da dimensão de **msdyn_bookableresource**.
2. Na página da dimensão, na guia **Relacionado**, clique em **Nomes de Campos da Dimensão de Preço**.

 ![Guia Nomes de campos da dimensão de preço](media/PD-fieldname.png)

4. Na exibição associada que é aberta, clique em **Adicionar Novo Nome de Campo da Dimensão de Preço**.

 ![Adicionar Novos Nomes de Campo da Dimensão de Preço](media/Add-NewPD-fieldname.png)


Isso abre a página **Novo nome de campo da dimensão de preço** para **msdyn_bookableresource**. 

5. Adicione **msdyn_projectteam** ao campo **Nome Lógico da Entidade** e **msdyn_bookableresourceid** ao campo **Nome do Campo**. Salve o registro.

 ![Formulário Novo nome de campo da dimensão de preço](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]