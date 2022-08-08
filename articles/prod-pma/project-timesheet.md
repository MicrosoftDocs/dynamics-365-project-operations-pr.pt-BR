---
title: Aplicativo móvel Folha de ponto do projeto
description: Este artigo fornece informações sobre o aplicativo móvel do Microsoft Dynamics 365 Project Timesheet. O aplicativo móvel Folha de ponto do projeto permite que os usuários enviem e aprovem folhas de ponto para projetos em seus dispositivos móveis.
author: abruer
ms.date: 06/29/2022
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
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110961"
---
# <a name="project-timesheet-mobile-application"></a>Aplicativo móvel Folha de ponto do projeto

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Visão geral

O aplicativo móvel Microsoft Dynamics 365 Project Timesheet permite que os usuários enviem e aprovem folhas de ponto para projetos em seus dispositivos móveis (iPhone ou Android). Esse aplicativo móvel revela a funcionalidade de folha de ponto que reside na área Gerenciamento e contabilidade de projeto do Dynamics 365 Finance. Ele ajuda a melhorar a produtividade e a eficiência do usuário e também permite a entrada e aprovação oportuna das folhas de ponto do projeto.

## <a name="download-and-install-the-mobile-app"></a>Baixe e instale o aplicativo móvel

Baixe e instale o aplicativo móvel Microsoft Dynamics 365 Project Timesheet para Android ou iPhone na loja móvel do seu dispositivo.

## <a name="enable-the-app"></a>Habilite o aplicativo 

Em Finanças, o aplicativo móvel Quadro de Horários do Projeto deve estar habilitado. Para habilitar a funcionalidade, vá para **Parâmetros de gerenciamento e contabilidade de projeto \> Planilha de horário** e selecione o parâmetro **Habilitar Microsoft Dynamics 365 Project Timesheet**.

### <a name="resolve-sign-in-issues"></a>Resolver problemas de logon

**Problema:** durante a entrada no aplicativo Project Timesheet Mobile, os usuários recebem uma mensagem de erro informando que "não é possível acessar o aplicativo '2bc50526-cdc3-4e36-a970-c284c34cbd6e' nesse locatário."

**Problema:** durante a entrada no aplicativo Project Timesheet Mobile, os usuários recebem um erro semelhante a um dos seguintes exemplos:

- "AADSTS50020: a conta de usuário '[nome de usuário]' do provedor de identidade 'https://sts.windows.net/[id do aplicativo]' não existe no locatário '[id do locatário]' e não pode acessar o aplicativo '[id do aplicativo]' nesse locatário."
- "A conta de usuário selecionada não existe no locatário '[id do locatário]' e não pode acessar o aplicativo '[id do aplicativo]' nesse locatário."

**Explicação:** esses problemas são causados por uma alteração que foi feita no Azure Active Directory (Azure AD) em maio de 2022 e que está relacionada a usuários externos. Como essa alteração não foi feita nos aplicativos de finanças e operações, ela pode afetar os clientes em qualquer versão da plataforma ou do aplicativo.

**Correção:** todos os usuários externos devem ser convidados para o locatário por meio do Azure AD. Para obter mais informações, consulte [Convidar usuários com a colaboração B2B do Azure Active Directory](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Entrar no aplicativo

1.  Inicie o aplicativo no dispositivo móvel.

2.  Insira sua URL de finanças.

3.  Na primeira vez que você efetuar login, será solicitado seu nome de usuário e senha. Insira suas credenciais.

4. Você será conectado à sua empresa padrão.

## <a name="submit-a-project-timesheet"></a>Envie uma planilha de horas do projeto

Você pode criar e enviar uma planilha de horas do projeto no aplicativo. Você pode basear um novo quadro de horários nas informações de um quadro de horários anterior, linhas salvas ou atribuições de projeto. Se for designado como delegado, você poderá inserir também uma folha de ponto para outro trabalhador. Para criar uma folha de ponto como delegado, selecione o botão **Menu** e selecione o nome de um recurso.

A página do quadro de horários criará um novo quadro de horários para o período do quadro de horários, com base na data atual. A semana de trabalho será exibida. Se o período do quadro de horários abranger várias semanas, você pode selecionar outra semana de trabalho nas guias de semana de trabalho.
Se houver uma planilha de horas para a data atual, ela será exibida. Se você precisar criar um novo quadro de horários em um período diferente do quadro de horários, selecione o botão **Cardápio** e selecione **Nova planilha de horas**.

Você pode inserir informações do projeto clicando na ação **Adicionar tempo** ou a ação **Copiar hora de**. A ação **Copiar hora de** copiará as informações da linha do projeto, mas não as horas. O menu **Copiar hora de** inclui as seguintes opções:

- **Copiar da planilha de horas existente** - Copie as linhas do quadro de horários de um quadro de horários existente.

- **Copiar do favorito** - Crie novas linhas de quadro de horários usando as configurações de quadro de horários que você selecionou como favoritos.

- **Copiar da tarefa** - Crie novas linhas de quadro de horários a partir de projetos atribuídos.

As informações do projeto que são exibidas dependem dos parâmetros móveis que você definiu na página **Parâmetros de gerenciamento e contabilidade de projeto**.

No campo **Entidade legal**, selecione a entidade legal para a qual você executou o trabalho do projeto. O campo **Entidade legal** estará disponível apenas se o suporte a planilha de horas entre empresas tiver sido habilitado para sua entidade legal.

Selecione o cliente que está associado ao projeto para o quadro de horários. Para o lançamento inicial no Android, ainda não há suporte à entrada pelo cliente, pois é necessário selecionar o projeto primeiro. Se você selecionou o projeto primeiro, o campo **Cliente** é preenchido automaticamente.

No campo **Projeto**, selecione o projeto para o qual você está inserindo as horas. O campo **Cliente** é preenchido automaticamente.

As pesquisas de cliente e projeto permitem pesquisar clientes e projetos.

Selecione as informações no campo **Categoria**, **Atividade**, **Propriedade de linha**, **Grupo de impostos sobre vendas** e **Grupo de impostos sobre vendas de itens** conforme necessário. Esses campos podem ser substituídos.

O campo **Propriedade de linha** será definido com um valor padrão, com base nos parâmetros de gerenciamento e contabilidade do projeto. Quando os parâmetros de projeto/categoria e categoria/recurso estão ativados, o valor **Propriedade de linha** será definido como o valor padrão que você definiu para esta validação. Quando os parâmetros de projeto/categoria e categoria/recurso não estão habilitados, o valor de **Propriedade de linha** será o padrão de acordo com o campo **Habilitar propriedade de linha padrão** na página **Parâmetros de gerenciamento e contabilidade de projeto**. O valor **Propriedade de linha** pode ser substituído.

Selecione um dia para adicionar tempo. Insira o número de horas que você trabalhou por dia.

Para adicionar comentários sobre as horas que você estiver inserindo, clique em **Adicionar comentários** e insira comentários para um público interno, público de cliente ou ambos.
Comentários internos podem ser vistos por gerentes de projeto. Os comentários do cliente são incluídos nas faturas.

Para salvar a linha como favorita, marque a caixa de seleção e clique em **Salvar como favorito**.

A dimensão financeira e o suporte a anexos não são fornecidos no aplicativo móvel.

Continue adicionando linhas de projeto conforme necessário para completar sua planilha de horas.

Clique em **Enviar** para enviar a planilha de horas para o fluxo de trabalho de aprovação.

## <a name="review-timesheets"></a>Rever planilhas de horas

Uma lista das planilhas de horas que precisam ser revisadas está disponível no menu. Essa opção estará disponível apenas se você tiver sido designado como um aprovador de fluxo de trabalho. Há suporte para aprovação de cabeçalho e linha. A aprovação de nível de linha oferece a capacidade de marcar uma ou mais linhas para aprovação. Depois de revisar as informações do quadro de horários, clique em **Aprovar**, **Delegar** ou **Retornar** para continuar o fluxo de trabalho.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
