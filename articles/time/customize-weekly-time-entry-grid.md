---
title: Estendendo entradas de hora
description: Este artigo fornece informações sobre como os desenvolvedores podem estender o controle de entrada de horas.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914756"
---
# <a name="extending-time-entries"></a>Estendendo entradas de hora

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations inclui um controle personalizado de entrada de hora extensível. Esse controle inclui os seguintes recursos:

- Insira o tempo horizontalmente durante uma semana
- Totais por dia, linha ou semana
- Copiar linhas ou semanas
- Entrada de hora por HH:mm ou HH.hh (automaticamente converte para HH.hh)
- Importar de atribuições, reservas ou compromissos

A extensão das entradas de hora é possível em duas áreas:
- [Adicionar entradas de hora personalizadas para seu próprio uso](#add)
- [Personalizar a grade de Entrada de Hora semanal](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Adicionar entradas de hora personalizadas para seu próprio uso

As entradas de hora são uma entidade principal usada em vários cenários. No ciclo 1 de abril de 2020, a solução central TESA foi apresentada. TESA fornece uma entidade **Configurações** e um novo direito de acesso **Usuário da Entrada de Hora**. Os novos campos, **msdyn_start** e **msdyn_end**, que têm uma relação direta com **msdyn_duration**, também foram incluídos. A nova entidade, o direito de acesso e os campos permitem uma abordagem mais unificada do tempo em vários produtos.


### <a name="time-source-entity"></a>Entidade de fonte de hora
| Campo | Descrição | 
|-------|------------|
| Nome  | O nome da entrada de Fonte de hora usada como o valor de seleção ao criar entradas de hora. |
| Fonte de Hora Padrão [Fonte de Hora: isdefault] | Por padrão, somente uma Fonte de Hora pode ser marcada como padrão. Isso permite que as entradas sejam padronizadas como uma fonte de hora, caso nenhuma tenha sido especificada. |
|Tipo de Fonte de Hora [Fonte de Hora: sourcetype] | O tipo de fonte é uma opção (Tipo de Fonte de Entrada de Hora) que permite a associação entre a fonte de hora e um aplicativo. A Microsoft reserva valores maiores que 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entradas de hora e a Entidade de fonte de hora
Cada entrada de hora está associada a um registro de fonte de hora. Este registro determina quais aplicativos devem processar a entrada de hora e como.

As entradas de hora são sempre um bloco contíguo de tempo com início, fim e duração vinculados.

A lógica automaticamente atualizará o registro de entrada de hora nas seguintes situações:

- Se dois dos seguintes três campos forem fornecidos, o terceiro será calculado automaticamente: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Os campos **msdyn_start** e **msdyn_end** reconhecem o fuso horário.
- Entradas de hora criadas apenas com **msdyn_date** e **msdyn_duration** especificados começarão à meia-noite. Os campos **msdyn_start** e **msdyn_end** serão atualizados de acordo.

#### <a name="time-entry-types"></a>Tipos de entrada de hora

Os registros de entrada de hora têm um tipo associado que define o comportamento no fluxo de envio para o aplicativo associado.

|Label | Valor|
|-----|-----|
|Em intervalo   |192,355,000|
|Viagem | 192,355,001|
|Horas Extras   | 192,354,320|
|Trabalho   | 192,350,000|
|Ausência    | 192,350,001|
|Férias   | 192,350,002|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Personalizar o controle de entrada de Hora semanal
Os desenvolvedores podem incluir campos e pesquisas adicionais a outras entidades, além de implementar regras de negócios para oferecer suporte a cenários de negócios.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Adicionar campos personalizados com pesquisas a outras entidades
Existem três etapas principais para adicionar um campo personalizado à grade de entrada de hora semanal.

1. Adicione o campo personalizado à caixa de diálogo **Criação rápida**.
2. Configure a grade para mostrar o campo personalizado.
3. Adicione o campo personalizado à página **Edição de linha** ou **Edição da entrada de hora**, conforme apropriado.

Certifique-se de que o novo campo tem as validações necessárias na página **Edição de linha** ou **Edição da entrada de hora**. Como parte dessa tarefa, bloqueie o campo com base no status da entrada de hora.

Quando você adiciona um campo personalizado à grade **Entrada de hora** e, em seguida, cria entradas de hora diretamente nela, o campo personalizado para essas entradas é definido automaticamente para corresponder à linha. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adicionar o campo personalizado à caixa de diálogo Criação rápida
Adicione o campo personalizado à caixa de diálogo **Criação rápida: Criar entrada de hora**. Os usuários poderão inserir um valor adicionando as entradas de hora ao selecionar **Novo**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar a grade para mostrar o campo personalizado
Existem duas maneiras de adicionar um campo personalizado à grade **Entrada de tempo semanal**.

- Personalize a exibição **Minhas Entradas de Hora Semanais** e adicione o campo personalizado a ela. Você pode especificar a posição e o tamanho do campo personalizado na grade editando as propriedades na exibição.
- Crie uma nova exibição de entrada de hora personalizada e configure-a como a exibição padrão. Essa exibição deve conter os campos **Descrição** e **Comentários externos**, além das colunas que você deseja ter na grade. Você pode especificar a posição, o tamanho e a ordem de classificação padrão da grade editando as propriedades na exibição. Em seguida, configure o controle personalizado dessa exibição para que seja um controle **Grade de Entrada de Hora**. Adicione o controle à exibição e selecione-o para **Web**, **Telefone** e **Tablet**. Em seguida, configure os parâmetros para a grade **Entrada de tempo semanal**. Defina o campo **Data de início** como **msdyn\_date**, o campo **Duração** como **msdyn\_duration** e o campo **Status** como **msdyn\_entrystatus**. O campo **Lista de Status somente Leitura** está definido como **192350002 (Aprovada)**, **192350003 (Enviada)** ou **192350004 (Recuperação Solicitada)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Adicionar o campo personalizado à página de edição apropriada
As páginas usadas para editar uma entrada de hora ou uma linha de entradas de hora podem ser encontradas em **Formulários**. O botão **Editar entrada** na grade abre a página **Editar entrada** e o botão **Editar linha** abre a página **Edição de linha**. Você pode editar essas páginas para que incluam campos personalizados.

Ambas as opções removem alguma filtragem predefinida em entidades **Projeto** e **Tarefa do Projeto** para que todas as exibições de pesquisa das entidades fiquem visíveis. Com a predefinição, apenas as exibições de pesquisa relevantes são visíveis.

Você deve determinar a página apropriada para o campo personalizado. Provavelmente, se você adicionou o campo à grade, ele deve estar na página **Edição de linha** usada para campos que se aplicam a toda a linha de entradas de hora. Se o campo personalizado tiver um valor exclusivo na linha todos os dias (por exemplo, se for um campo personalizado para hora de término), ele deverá estar na página **Edição da entrada de hora**.

Para adicionar o campo personalizado a uma página, arraste um elemento **Campo** para a posição apropriada na página e defina as propriedades.

### <a name="add-new-option-set-values"></a>Adicionar novos valores do conjunto de opções
Para adicionar valores de conjunto de opções a um campo predefinido, siga estas etapas.

1. Abra a página de edição do campo e, em **Tipo**, selecione **Editar** ao lado do conjunto de opções.
2. Adicione uma nova opção que tenha um rótulo e cor personalizados. Se você quer adicionar um novo status de entrada de hora, o campo predefinido é chamado **Status da Entrada**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designar um novo status de entrada de hora como somente leitura
Para designar um novo status de entrada de hora como somente leitura, adicione o novo valor de entrada de hora à propriedade **Lista de Status somente Leitura**. Você deve adicionar o número, não o rótulo. Agora, a parte editável da grade de entrada de hora será bloqueada para as linhas que têm o novo status. Para definir a propriedade **Lista de Status somente Leitura** de forma diferente para diferentes exibições **Entrada de Hora**, adicione a grade **Entrada de hora** na seção **Controles personalizados** de uma exibição e configure os parâmetros conforme apropriado.

Em seguida, adicione regras de negócios para bloquear todos os campos nas páginas **Edição de Linha** e **Edição da entrada de hora**. Para acessar as regras de negócios dessas páginas, abra o editor de formulário de cada página e selecione **Regras de negócios**. Você pode adicionar o novo status à condição nas regras de negócios existentes ou adicionar uma nova regra de negócios para o novo status.

### <a name="add-custom-validation-rules"></a>Adicionar regras de validação personalizadas
Você pode adicionar dois tipos de regras de validação para a experiência em grade **Entrada de tempo semanal**:

- Regras de negócios do lado do cliente que funcionam em páginas
- Validações de plug-in do lado do servidor que se aplicam a todas as atualizações de entrada de hora

#### <a name="client-side-business-rules"></a>Regras de negócios do lado do cliente
Use regras de negócios para bloquear e desbloquear campos, inserir valores padrão nos campos e definir validações que requerem informações apenas do registro de entrada de hora atual. Para acessar as regras de negócios de uma página, abra o editor de formulário e selecione **Regras de negócios**. Você pode editar as regras de negócios existentes ou adicionar uma nova regra de negócios.

#### <a name="server-side-plug-in-validations"></a>Validações de plug-in do lado do servidor
Você deve usar validações de plug-in para quaisquer validações que exijam mais contexto do que o disponível em um registro de entrada de hora único. Você também deve usá-las para quaisquer validações que deseja executar em atualizações em linha na grade. Para concluir as validações, crie um plug-in personalizado na entidade **Entrada de Hora**.

### <a name="limits"></a>Limites
No momento, o limite de tamanho da grade **Entrada de hora** é de 500 linhas. Se houver mais de 500 linhas, as linhas em excesso não serão exibidas. Não é possível aumentar esse limite de tamanho.

### <a name="copying-time-entries"></a>Copiar entradas de hora
Use a exibição **Copiar Colunas de Entrada de Hora** para definir a lista de campos a serem copiados durante a entrada de hora. **Data** e **Duração** são campos obrigatórios e não devem ser removidos da exibição.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
