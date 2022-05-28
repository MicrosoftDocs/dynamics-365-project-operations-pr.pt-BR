---
title: Implementar campos personalizados para o aplicativo móvel Microsoft Dynamics 365 Project Timesheet no iOS e Android
description: Este tópico fornece padrões comuns para usar extensões para implementar campos personalizados.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 79ef62d6911b393248536e4cc73475f6c35a22e2
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682739"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementar campos personalizados para o aplicativo móvel Microsoft Dynamics 365 Project Timesheet no iOS e Android

[!include [banner](../includes/banner.md)]

Este tópico fornece padrões comuns para usar extensões para implementar campos personalizados. Os tópicos a seguir são abordados:

- Os vários tipos de dados que a estrutura de campos personalizados oferece suporte
- Como mostrar campos personalizados editáveis ou somente leitura em entradas de folha de pagamento e salvar valores fornecidos pelo usuários de volta ao banco de dados
- Como mostrar campos personalizados somente leitura no cabeçalho da folha de pagamento
- Como integrar outra lógica de negócios personalizada para inserir valores padrão em campos e fazer validações adicionais

## <a name="audience"></a>Público-alvo

Este tópico destina-se a desenvolvedores que estão integrando seus campos personalizados ao aplicativo móvel Microsoft Dynamics 365 Project Timesheet que está disponível para Apple iOS e Google Android. Pressupõe-se que os leitores estejam familiarizados com o desenvolvimento em X++ e com a funcionalidade de folha de ponto do projeto.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Contrato de dados — classe TSTimesheetCustomField de X++

A classe **TSTimesheetCustomField** é o contrato de dados de X+ que representa as informações sobre um campo personalizado para a funcionalidade de folha de ponto. Lista os objetos do campo personalizado no contrato de dados TSTimesheetDetails e no contrato de dados TSTimesheetEntry para mostrar campos personalizados no aplicativo móvel.

- **TSTimesheetDetails** — o contrato do cabeçalho da folha de ponto.
- **TSTimesheetEntry** — o contrato de transação da folha de ponto. Grupos desses objetos que tenham as mesmas informações do projeto e o valor **timesheetLineRecId** constituem um linha,

### <a name="fieldbasetype-types"></a>fieldBaseType (Tipos)

A propriedade **FieldBaseType** no objeto **TsTimesheetCustom** determina o tipo de campo que é exibido no aplicativo. Ha suporte aos seguintes valores de **Tipos**:

| Valor de tipos | Digitar              | Anotações |
|-------------|-------------------|-------|
| 0           | Cadeia de Caracteres (e Enumeração) | O campo é exibido como um campo de texto. |
| 1           | Integer           | O valor é exibido como um número sem casas decimais. |
| 2           | Real              | O valor é exibido como um número com casas decimais.<p>Para mostrar o valor real como uma moeda no aplicativo, use a propriedade **fieldExtenededType**. Você pode usar a propriedade **numberOfDecimals** para definir o número de casas decimais exibidas.</p> |
| 3           | Data              | Os formatos de data são definidos pela configuração **formato de data, hora e número** do usuário, que está especificada em **Preferência de idioma e país/região** em **Opções do usuário**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Se a propriedade **stringOptions** não for fornecida no objeto **TSTimesheetCustomField**, um campo de texto livre será fornecido ao usuário.

    A propriedade **stringLength** pode ser usada para definir o tamanho máximo da cadeia de caracteres que os usuário poderão inserir.

- Se a propriedade **stringOptions** for fornecida no objeto **TSTimesheetCustomField**, os valores dessa lista de elementos serão os únicos que os usuários poderão selecionar usando os botões de opção.

    Nesse caso, o campo de cadeia de caracteres pode agir como um valor de enumeração para fins de entrada do usuário. Para salvar o valor de um banco de dados como uma enumeração, mapeie manualmente o valor da cadeia de caracteres de volta ao valor da enumeração antes de salvar no banco de dados usando a cadeia de comando (consulte a seção "Usar cadeia de comando na classe TSTimesheetEntryService para salvar uma entrada de folha de ponto do aplicativo de volta no banco de dados" posteriormente neste tópico para obter um exemplo).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Você pode usar essa propriedade para formatar valores reais como moeda. Essa abordagem é aplicável somente quando o valor **fieldBaseType** for **Real**.

- **TSCustomFieldExtendedType:None** — nenhuma formatação é aplicada.
- **TSCustomFieldExtendedType::Currency** — formata o valor como moeda.

    Quando a formatação da moeda está ativa, o campo **stringValue** pode ser usado para passar o código da moeda que deve ser exibido no aplicativo. O valor é somente leitura.

    O campo **realValue** contém o valor monetário que deve ser salvo no banco de dados.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Você pode usar essa propriedade para especificar quando o campo personalizado deve ser exibido no aplicativo.

- **TSCustomFieldSection::Header** — o campo será exibido na seção **Exibir mais detalhes** no aplicativo. Esses campos sempre são somente leitura.
- **TSCustomFieldSection::Line** — o campo será exibido após todos os campos de linha prontos para uso nas entradas da folha de ponto. Esses campos podem ser editáveis ou somente leitura.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Essa propriedade identifica o campo quando os valores que o aplicativo fornece são salvos de volta no banco de dados.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Essa propriedade identifica o campo quando os valores que o aplicativo fornece são salvos de volta no banco de dados.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Defina essa propriedade como **Sim** para especificar que o campo na seção de entrada da folha de ponto deve ser editável pelos usuários. Defina a propriedade como **Não** para fazer com que o campo seja somente leitura.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Defina essa propriedade como **Sim** para especificar que o campo na seção de entrada da folha de ponto deve ser obrigatório.

### <a name="label-str"></a>label (str)

Essa propriedade especifica o rótulo que é exibido ao lado do campo no aplicativo.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Lista de Cadeias de Caracteres)

Essa propriedade é aplicável somente quando **fieldBaseType** é definido como **Cadeia de Caracteres**. Se a propriedade **stringOptions** estiver definida, os valores de cadeia de caracteres que estão disponíveis para seleção por meio dos botões de opção serão especificados pelas cadeias de caracteres na lista. Se nenhuma cadeia de caracteres for fornecida, a entrada de texto livre no campo de cadeia de caracteres será permitida (consulte a seção "Usar a cadeia de comando na classe TSTimesheetEntryService para salvar uma entrada de folha de ponto do aplicativo de volta no banco de dados" posteriormente neste tópico para obter um exemplo).

### <a name="stringlength-int"></a>stringLength (int)

Essa propriedade especifica o tamanho máximo de um campo de cadeia de caracteres. Ela é aplicável somente quando **fieldBaseType** é definido como **Cadeia de Caracteres**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Essa propriedade especifica o número de casas decimais exibidas para um campo real. Ela é aplicável somente quando **fieldBaseType** é definido como **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Essa propriedade controla a ordem na qual os campos personalizados são exibidos no aplicativo quando mais de um campo personalizado é especificado. Campos com números mais baixos são exibidos primeiro.

### <a name="booleanvalue-boolean"></a>booleanValue (booliano)

Para campos do tipo **Booliano**, essa propriedade passa o valor booliano do campo entre o servidor e o aplicativo.

### <a name="guidvalue-guid"></a>guidValue (guid)

Para campos do tipo **GUID**, essa propriedade passa o valor do identificador global exclusivo (GUID) do campo entre o servidor e o aplicativo.

### <a name="int64value-int64"></a>int64Value (int64)

Para campos do tipo **Int64**, essa propriedade passa o valor de Int64 do campo entre o servidor e o aplicativo.

### <a name="intvalue-int"></a>intValue (int)

Para campos do tipo **Int**, essa propriedade passa o valor de int do campo entre o servidor e o aplicativo.

### <a name="realvalue-real"></a>realValue (real)

Para campos do tipo **Real**, essa propriedade passa o valor real do campo entre o servidor e o aplicativo.

### <a name="stringvalue-str"></a>stringValue (str)

Para campos do tipo **Cadeia de Caracteres**, essa propriedade passa o valor da cadeia de caracteres do campo entre o servidor e o aplicativo. Ela também é usada para campos do tipo **Real** que são formatados como moeda. Para esses campos, a propriedade é usada para passar o código de moeda para o aplicativo.

### <a name="datevalue-date"></a>dateValue (data)

Para campos do tipo **Data**, essa propriedade passa o valor de data do campo entre o servidor e o aplicativo.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Mostrar e salvar um campo personalizado na seção de entrada de folha de ponto

Abaixo encontra-se uma captura de tela do aplicativo móvel de uma criação de entrada de folha de ponto. Ela mostra os campos prontos para uso e um campo personalizado na seção "Entrada de horas" chamado "Cadeia de caracteres de teste" com um valor de enumeração de "Segunda opção" já definido.

![Campo Cadeia de caracteres de teste no aplicativo.](media/timesheet-entry.jpg)



Abaixo encontra-se uma captura de tela do usuário do aplicativo móvel selecionando uma das opções de enumeração disponíveis para o campo personalizado "Cadeia de caracteres de teste".  As duas opções são "Primeira opção" e Segunda opção", exibidas como botões de opção. A segunda opção está selecionada.

![Botões de opção para o campo personalizado Cadeia de caracteres de teste.](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Estender a tabela TSTimesheetLine para que ela tenha um campo personalizado

Em cenários típicos, é provável que os dados de um campo personalizado na seção de entrada da folha de ponto sejam salvos na tabela TSTimesheetLine. No entanto, outras tabelas podem ser usadas se os dados puderem se recuperados com base em um registro de TSTimesheetTrans que seja fornecido, ou se não tiverem um contexto de registro específico (por exemplo, se o campo for definido como somente leitura nos parâmetros do projeto).

Observe que os campos personalizados não têm nenhum registro de banco de dados de backup. Eles podem ser gerados dinamicamente com base na lógica de X++. Essa abordagem é útil em cenários somente leitura (consulte a seção "Usar a cadeia de comando na classe TSTimesheetDetails, método buildCustomFieldListForHeader para preencher detalhes da folha de ponto" para obter um exemplo de valores de campos personalizados gerados dinamicamente).

Abaixo encontra-se uma captura de tela do Visual Studio da árvore de objetos do aplicativo. Ela mostra uma extensão da tabela TSTimesheetLine com o campo TestLineString adicionado como um campo personalizado.

![Cadeia de caracteres de linha.](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Usar a cadeia de comando no método buildCustomFieldList da classe TSTimesheetSettings para mostrar um campo na seção de entrada de folha de ponto

Esse código controla as configurações de exibição do campo no aplicativo. Por exemplo, ele controla o tipo de campo, o rótulo, se o campo é obrigatório e em qual seção o campo é exibido.

O exemplo a seguir mostra um campo de cadeia de caracteres em entradas de horas. Esse campo tem duas opções, **Primeira opção** e **Segunda opção**, que estão disponíveis por meio dos botões de opção. O campo no aplicativo está associado ao campo **TestLineString**, que está adicionado à tabela TSTimesheetLine table.

Observe o uso do método **TSTimesheetCustomField::newFromMetatdata()** para simplificar a inicialização das propriedades do campo personalizado: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** e **numberOfDecimals**. Você também pode definir esses parâmetros manualmente, como preferir.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Usar a cadeia de comando no método buildCustomFieldListForEntry da classe TSTimesheetEntry para inserir valores em uma entrada de folha de ponto

O método **buildCustomFieldListForEntry** é usado para inserir valores nas linhas salvas da folha de ponto em um aplicativo móvel. Ele pega um registro de TSTimesheetTrans como parâmetro. Campos desse registro podem ser usados para preencher o valor do campo personalizado no aplicativo.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Usar a cadeia de comando na classe TSTimesheetEntryService para salvar uma entrada de folha de ponto do aplicativo de volta no banco de dados

Para salvar um campo personalizado de volta no banco de dados em uso típico, você deve estender vários métodos:

- O método **timesheetLineNeedsUpdating** é usado para determinar se o registro da linha foi alterado pelo usuário no aplicativo e deve ser salvo no banco de dados. Se o desempenho for uma preocupação, esse método pode ser simplificado para que ele sempre retorne **true**.
- Os métodos **populateTimesheetLineFromEntryDuringCreate** e **populateTimesheetLineFromEntryDuringUpdate** podem ser estendidos para que eles insiram valores no registro do banco de dados TSTimesheetLine a partir do registro do contrato de dados que é fornecido. No exemplo a seguir, observe como o mapeamento entre o campo do banco de dados e o campo de entrada é feito manualmente por meio de código X++.
- O método **populateTimesheetWeekFromEntry** também poderá ser estendido se o campo personalizado que é mapeado para o objeto **TSTimesheetEntry** tiver que gravar de volta na tabela TSTimesheetLineweek do banco de dados.

> [!NOTE]
> O exemplo a seguir salva o valor de **firstOption** ou de **secondOption** que o usuário selecionar no banco de dados como um valor de cadeia de caracteres bruto. Se o campo do banco de dados for um campo do tipo **Enumeração**, esses valores podem ser mapeados manualmente para um valor de enumeração e depois salvos no campo de enumeração na tabela do banco de dados.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Mostrar um campo personalizado na seção do cabeçalho da folha de ponto

Abaixo encontra-se uma captura de tela do aplicativo móvel de um usuário exibindo uma folha de ponto. O botão "Mais informações" foi selecionado no canto superior direito para mostrar a opção "Exibir mais detalhes".  

![Comando Exibir mais detalhes.](media/show-more.png)

Abaixo encontra-se uma captura de tela do aplicativo móvel exibindo a seção "Mais" de uma folha de ponto. Um campo personalizado chamado "Taxa de utilização desta folha de ponto (campo personalizado calculado) foi adicionado à seção do cabeçalho da folha de ponto. Um valor somente leitura de "0,667" é definido no campo personalizado.

![Seção Mais.](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Estender a tabela TSTimesheetTable para que ela tenha um campo personalizado

Em cenários típicos, é provável que os dados de um campo personalizado na seção do cabeçalho sejam extraídos da tabela TSTimesheetHeader. No entanto, outras tables podem ser usadas se os dados puderem se recuperados com base em um registro de TSTimesheetTable que seja fornecido, ou se não tiverem um contexto de registro específico (por exemplo, se o campo for definido como somente leitura nos parâmetros do projeto).

Observe que os campos personalizados não têm nenhum registro de banco de dados de backup. Eles podem ser gerados dinamicamente com base na lógica de X++. O exemplo a seguir mostra essa abordagem.

Os campos na seção do cabeçalho são sempre somente leitura no aplicativo.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Usar a cadeia de comando no método buildCustomFieldList da classe TSTimesheetSettings para mostrar um campo na seção do cabeçalho

Esse código controla as configurações de exibição do campo no aplicativo. Por exemplo, ele controla o tipo de campo, o rótulo, se o campo é obrigatório e em qual seção o campo é exibido.

O exemplo a seguir mostra um valor calculado na seção do cabeçalho no aplicativo.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Usar a cadeia de comando no método buildCustomFieldListForHeader da classe TSTimesheetDetails para preencher os detalhes em uma folha de ponto

O método **buildCustomFieldListForHeader** é usado para preencher os detalhes do cabeçalho em uma folha de ponto no aplicativo móvel. Ele pega um registro de TSTimesheetTable como parâmetro. Campos desse registro podem ser usados para preencher o valor do campo personalizado no aplicativo. O exemplo a seguir não lê qualquer valor do banco de dados. Em vez disso, ele usa a lógica de X++ para gerar uma valor calculado que então é exibido no aplicativo.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Outras oportunidades de capacidade de configuração/extensão

### <a name="adding-additional-validation-for-the-app"></a>Adicionando outras validações para o aplicativo

A lógica existente para a funcionalidade de folha de ponto no nível do banco de dados funcionará como o esperado. Para interromper a conclusão de operações de salvamento ou envio e exibir uma mensagem de erro específica, você pode adicionar **throw error("mensagem para o usuário")** ao código por meio de uma extensão de cadeia de comando. Veja três exemplos de métodos extensíveis úteis:

- Se **validateWrite** na tabela TSTimesheetLine retornar **false** durante uma operação de salvamento de uma linha da folha de ponto, uma mensagem de erro será exibida no aplicativo móvel.
- Se **validateSubmit** na tabela TSTimesheetTable retornar **false** durante uma operação de envio no aplicativo, uma mensagem de erro será exibida ao usuário.
- A lógica que preenche os campos (por exemplo, **Line Property**) durante o método **insert** na tabela TSTimesheetLine ainda será executado.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Ocultando e marcando campos prontos para uso como somente leitura por meio de configuração

Nos parâmetros do projeto, você pode tornar campos prontos para uso em somente leitura ou em campos ocultos no aplicativo móvel. Defina as opções na seção **Folhas de ponto móveis** na guia **Folhas de ponto** da página **Parâmetros de gerenciamento e contabilidade de projeto**.

![Parâmetros do projeto.](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Alterar as atividades disponíveis para seleção por meio de extensões

As atividades disponíveis para seleção de um projeto são preenchidas por meio dos métodos **getActivitiesForProject()** e **getActivityQuery()** na classe **TsTimesheetProjectService**. Você pode usar a cadeia de comando para alterar esse comportamento para corresponder ao seu cenário comercial para as atividades que estão disponíveis para seleção para um projeto específico.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Inserindo uma categoria de projeto padrão nas entradas de folha de ponto

A entrada de uma categoria de projeto padrão nas entradas de o quadro de folha de ponto ocorre em três níveis. Você pode usar a cadeia de comando para estender o comportamento em qualquer um ou todos esses níveis para atingir o comportamento desejado. A seguinte hierarquia é usada:

1. O aplicativo tenta colocar a categoria padrão a partir do recurso do projeto. Essa categoria padrão é definida nos métodos **getCurrentUserResource** e **getDelegatedResourcesForCurrentUser** na classe **TSTimesheetSettingsService**.
2. Se a categoria padrão não for fornecida no nível do recurso do projeto, o aplicativo tentará extraí-la da atividade do projeto. Esta categoria padrão é definida no método **getActivitiesForProject** na classe **TSTimesheetProjectService**.
3. Se a categoria padrão não for fornecida no nível da atividade do projeto, a categoria padrão será extraída dos parâmetros do projeto. Essa categoria padrão é definida no método **getProjectDetailsbyRule** na classe **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]