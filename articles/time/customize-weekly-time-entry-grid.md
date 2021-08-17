---
title: Estendendo entradas de hora
description: Este tópico fornece informações sobre como os desenvolvedores podem estender o controle de entrada de hora.
author: stsporen
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c36a47b09e6012925a047f81318e89167d5c506facaae8d72b0bb6e8e267a7d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993317"
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
Cada entrada de hora está associada a um registro de fonte de hora. Esse registro determina como e quais aplicativos devem processar a entrada de hora.

As entradas de hora são sempre um bloco contíguo de tempo com início, fim e duração vinculados.

A lógica automaticamente atualizará o registro de entrada de hora nas seguintes situações:

- Se dois dos seguintes três campos forem fornecidos, o terceiro será calculado automaticamente: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Os campos **msdyn_start** e **msdyn_end** se ajustam ao fuso horário automaticamente.
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

1. Adicione o campo personalizado à caixa de diálogo de criação rápida.
2. Configure a grade para mostrar o campo personalizado.
3. Inclua o campo personalizado no fluxo de tarefas de edição de linha ou no fluxo de tarefas de edição de células.

Verifique se o novo campo tem as validações necessárias no fluxo de tarefas de edição de linha ou célula. Como parte dessa etapa, bloqueie o campo, com base no status da entrada de hora.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adicionar o campo personalizado à caixa de diálogo de criação rápida
Adicione o campo personalizado à caixa de diálogo **Criação Rápida de Entrada de Hora**. Quando as estradas de hora são adicionadas, um valor pode ser inserido selecionando **Novo**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar a grade para mostrar o campo personalizado
Existem duas maneiras de adicionar um campo personalizado à grade de entrada de hora semanal:

  - Personalizar uma exibição e adicionar um campo personalizado
  - Criar uma entrada de hora personalizada padrão 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Personalizar uma exibição e adicionar um campo personalizado

Personalize a exibição **Minhas Entradas de Hora Semanais** e adicione o campo personalizado a ela. Você pode escolher a posição e o tamanho do campo personalizado na grade, editando as propriedades na exibição.

#### <a name="create-a-new-default-custom-time-entry"></a>Criar uma entrada de hora personalizada padrão

Essa exibição deve conter os campos **Descrição** e **Comentários Externos**, além das colunas que você deseja ter na grade. 

1. Escolha a posição, o tamanho e a ordem de classificação padrão da grade editando essas propriedades na exibição. 
2. Configure o controle personalizado dessa exibição para que seja um controle **Grade de Entrada de Hora**. 
3. Adicione esse controle à exibição e selecione-o para Web, telefone e tablet. 
4. Configure os parâmetros para a grade de entrada de hora semanal. 
5. Defina o campo **Data de Início** como **msdyn_date**, defina o campo **Duração** como **msdyn_duration** e defina o campo **Status** como **msdyn_entrystatus**. 
6. Para a exibição padrão, o campo **Lista de status somente leitura** está definido como **192350002,192350003,192350004**. O campo **Fluxo de Tarefas de Edição de Linha** está definido como **msdyn_timeentryrowedit**. O campo **Fluxo de Tarefas de Edição de Célula** está definido como **msdyn_timeentryedit**. 
7. Você pode personalizar esses campos para adicionar ou remover o status somente leitura ou usar uma experiência baseada em tarefas (TBX) diferente para edição de linhas ou células. Esses campos agora estão limitados a um valor estático.


> [!NOTE] 
> Ambas as opções removerão alguma filtragem predefinida nas entidades **Projeto** e **Tarefa do Projeto** para que todas as exibições de pesquisa das entidades fiquem visíveis. Com a predefinição, apenas as exibições de pesquisa relevantes são visíveis.

Determine o fluxo de tarefas apropriado para o campo personalizado. Se você adicionou o campo na grade, ele deve estar no fluxo de tarefas de edição de linha que é usado para campos que se aplicam a toda a linha de entradas de hora. Se o campo personalizado tiver um valor exclusivo todos os dias, como um campo personalizado para **Hora de término**, ele deverá estar no fluxo de tarefas de edição de célula.

Para adicionar o campo personalizado a um fluxo de tarefas, arraste um elemento **Campo** para a posição apropriada na página e defina as propriedades do campo. Defina a propriedade **Fonte** como **Entrada de Hora** e defina a propriedade **Campo de Dados** como o campo personalizado. A propriedade **Campo** especifica o nome para exibição na página de TBX. Selecione **Aplicar** para salvar as alterações no campo e depois selecione **Atualizar** para salvar as alterações na página.

Para usar uma nova página de TBX personalizada, crie um processo. Defina a categoria como **Fluxo do Processo Empresarial**, defina a entidade como **Entrada de Hora** e defina o tipo de processo de negócios como **Executar processo como fluxo de tarefas**. Em **Propriedades**, a propriedade **Nome da página** deve ser definida como o nome para exibição da página. Adicione todos os campos relevantes à página de TBX. Salve e ative o processo. Atualize a propriedade de controle personalizado para o fluxo de tarefas relevante para o valor de **Nome** no processo.

### <a name="add-new-option-set-values"></a>Adicionar novos valores do conjunto de opções
Para adicionar valores do conjunto de opções a um campo predefinido, abra a página de edição do campo e, em **Tipo**, selecione **Editar** ao lado do conjunto de opções. Adicione uma nova opção que tenha um rótulo e cor personalizados. Se você deseja adicionar um novo status de entrada de hora, o campo predefinido é denominado **Status da Entrada**, não **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designar um novo status de entrada de hora como somente leitura
Para designar um novo status de entrada de hora como somente leitura, adicione o novo valor de entrada de hora à propriedade **Lista de Status somente Leitura**. A parte editável da grade de entrada de hora será bloqueada para as linhas que têm o novo status.
Em seguida, adicione regras de negócios para bloquear todos os campos nas páginas de TBX **Edição da Linha de Entrada de Hora** e **Edição da Entrada de Hora**. É possível acessar as regras de negócios dessas páginas, abrindo o editor de fluxo do processo empresarial da página e selecionando **Regras de Negócios**. Você pode adicionar o novo status à condição nas regras de negócios existentes ou adicionar uma nova regra de negócios para o novo status.

### <a name="add-custom-validation-rules"></a>Adicionar regras de validação personalizadas
Há dois tipos de regras de validação que você pode adicionar à experiência da grade de entrada de hora semanal:

- Regras de negócios do lado do cliente que funcionam em caixas de diálogo de criação rápida e em páginas de TBX.
- Validações de plug-in do lado do servidor que se aplicam a todas as atualizações de entrada de hora.

#### <a name="business-rules"></a>Regras de negócios
Use regras de negócios para bloquear e desbloquear campos, inserir valores padrão nos campos e definir validações que requerem informações apenas do registro de entrada de hora atual. Você pode acessar as regras de negócios para uma página de TBX, abrindo o editor de fluxo do processo empresarial da página e selecionando **Regras de Negócios**. Você pode editar as regras de negócios existentes ou adicionar uma nova regra de negócios. Para validações ainda mais personalizadas, você pode usar uma regra de negócios para executar o JavaScript.

#### <a name="plug-in-validations"></a>Validações de plug-in
Use validações de plug-in para validações que exijam mais contexto do que o disponível em um registro de entrada de hora único ou para as validações que deseja executar nas atualizações em linha na grade. Para concluir a validação, crie um plug-in personalizado na entidade **Entrada de Hora**.

### <a name="copying-time-entries"></a>Copiar entradas de hora
Use a exibição **Copiar Colunas de Entrada de Hora** para definir a lista de campos a serem copiados durante a entrada de hora. **Data** e **Duração** são campos obrigatórios e não devem ser removidos da exibição.


[!INCLUDE[footer-include](../includes/footer-banner.md)]