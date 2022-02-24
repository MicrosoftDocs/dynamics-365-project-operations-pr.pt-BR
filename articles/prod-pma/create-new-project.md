---
title: Criar um novo projeto
description: Este tópico fornece informações sobre como criar um novo projeto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270709"
---
# <a name="create-a-new-project"></a>Criar um novo projeto

[!include [banner](../includes/banner.md)]

Conclua as etapas a seguir para criar um novo projeto.

1. Na página **Gerenciamento de projetos**, selecione **Novo projeto** e insira estes valores:

    - **Tipo de projeto:** Tempo e material
    - **Nome do projeto:** Atualização do XYZ fase 2
    - **Grupo de projeto:** TM\_WIP
    - **ID do contrato de projeto:** 00000002

2. Selecione **Criar projeto**.

## <a name="assign-a-resource-to-a-project"></a>Atribuir um recurso a um projeto

1. Na página **Funcionários**, na lista **Funcionários**, selecione o registro do funcionário para o qual você anteriormente configurou as competências e abra o registro dele.
2. No Painel de ações, na guia **Projeto**, no grupo **Configuração**, selecione **Atribuir projetos**.
3. Na página **Atribuições de projetos de validação de recursos**, na guia **Projetos**, no campo **Adicionar o projeto aos projetos selecionados**, filtre pelo projeto **Atualização do XYZ fase 2**.
4. No painel **Projetos pendentes**, selecione um projeto e, em seguida, selecione o botão de seta para adicioná-lo ao painel **Projetos selecionados**.

Você também pode atribuir categorias a um recurso conforme sua necessidade. O tipo de categoria é **Custo** ou **Receita**. O tipo de categoria é determinado por sua organização. Se nenhuma categoria for atribuída a um recurso, o Finance procurará a categoria padrão nos preços por hora para custo e receita.

## <a name="set-up-project-resource-and-role-characteristics"></a>Configurar as características da função e recurso do projeto

Um gerente de projeto pode usar a funcionalidade de alocação de recursos do projeto para criar as funções necessárias para o projeto. As funções podem ser usadas se os recursos confirmados ainda forem desconhecidos quando os estiverem sendo reservados. As funções podem ser reservadas temporariamente como recursos planejados, para que você possa continuar as etapas de planejamento do projeto.

[![Exemplo de uma função](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Cenário:** a Contoso foi contratada para concluir um projeto de tempo e material que tem um termo de abertura aprovado. O gerente de projeto júnior ainda está preenchendo o escopo do projeto. O gerente de recursos está no momento identificando recursos específicos que serão reservados para trabalhar no novo projeto. Devido à natureza crítica do projeto, o patrocinador dele solicitou um gerente de projeto sênior como uma das funções. O gerente de recursos deve encontrar o novo recurso e definir a função no sistema, caso o gerente de projeto júnior precise das informações do recurso durante o planejamento do projeto.

As etapas a seguir mostram como o gerente de recursos pode configurar a função de gerente de projeto sênior e associar características de recursos a ela. Posteriormente, a função poderá ser usada para pesquisar recursos disponíveis que correspondam às competências de recursos necessárias.

1. Na página **Configurar funções**, selecione **Novo** e insira estes valores:

    - **ID da função:** Gerente de projeto sênior
    - **Descrição:** Gerente de projeto sênior

2. Selecione **Criar**.
3. Selecione a função **Gerente de projeto sênior** e, em seguida, **Configurar características**.
4. No campo **Tipo de característica**, selecione **Habilidade**.
5. No campo **Características disponíveis**, insira a habilidade para pesquisar.
6. No campo **Tipo de característica**, selecione **Certificado**.
7. No campo **Características disponíveis**, insira o tipo de certificado para pesquisar.

## <a name="assign-a-project-resource-to-a-project"></a>Atribuir um recurso a um projeto

1. Na página **Todos os projetos**, selecione o projeto **Atualização do XYZ fase 2**.
2. Na guia **Equipe do projeto e agendamento**, selecione **Adicionar**.
3. No campo **Função**, selecione **Membro da equipe**.
4. Selecione **Reservar do calendário**.
5. Na página **Disponibilidade do recurso**, selecione **Configurações de exibição**.
6. Na página **Ajustar configurações de exibição**, insira os seguintes valores:

    - **Formato da exibição do intervalo de datas:** Dia
    - **Exibir descrições de disponibilidade:** Sim
    - **Exibir capacidade restante:** Sim

7. Na lista de recursos, selecione um recurso.
8. Selecione **Reserva fixa** e **Capacidade total**.

## <a name="assign-a-resource-to-a-default-role"></a>Atribuir um recurso a uma função padrão

Para ajudar os gerentes de projeto ou de recursos, é possível se aprofundar mais nos recursos que podem ser reservados para um projeto. Você pode associar uma função padrão a um recurso existente ou a um recurso recém-adquirido. Por exemplo, quando Daniel foi contratado, ele tinha a experiência e as habilidades para preencher a função de analista de negócios. O gerente de recursos atribuiu essa função como a função padrão de Daniel. Portanto, o gerente de recursos adicionou Daniel a um grupo de analistas de negócios que estão disponíveis para trabalhar em projetos.

Durante a reserva de recursos, os gerentes de projeto podem filtrar os recursos de função que estão disponíveis para trabalhar em projetos. Eles podem usar essas informações como um critério ao realizar análises de decisão de vários critérios durante o preenchimento de recursos. Eles também podem adicionar outras características de recurso ao filtro para pesquisar recursos que tenham habilidades, formação e experiência específicas para um determinado projeto.

**Cenário:** um projeto aprovado foi iniciado e a função de gerente de projeto sênior foi reservada como um recurso planejado durante o estágio de planejamento do projeto. O gerente de recursos agora encontrou um recurso para ocupar a função de gerente de projeto sênior.

1. Na página **Lista de recursos**, selecione **Daniel Goldschmidt**.
2. Na página **Função do recurso**, selecione **Novo** e insira estes valores:

    - **Efetivo:** insira a data atual.
    - **Expiração:** insira **Nunca**.
    - **Função:** insira **Gerente de projeto sênior**.

3. Selecione **Salvar** e feche a página.
4. Na guia **Competências**, adicione a habilidade **ProjectMgmt** e o certificado **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]