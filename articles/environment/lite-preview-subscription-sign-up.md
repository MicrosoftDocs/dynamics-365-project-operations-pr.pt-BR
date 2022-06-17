---
title: Inscreva-se para obter uma assinatura de versão preliminar – lite
description: Este artigo fornece informações sobre como inscrever-se e implantar o Project Operations lite - gerenciar faturamento pro forma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6953956c0b3401a6c64ee597f966ba4a4c0d07b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921242"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Inscreva-se para obter uma assinatura de versão preliminar – lite 

Este artigo explica como inscrever-se na oferta de avaliação e implantar o Dynamics 365 Project Operations lite - gerenciar faturamento pro forma.

> [!NOTE]
> Este processo mudará nas próximas versões de Project Operations.

## <a name="prerequisites"></a>Pré-requisitos
- O usuário que implementa a versão preliminar precisa ter direitos de administrador global no Locatário do Azure. Você pode criar um inquilino durante o primeiro resgate da oferta.

> [!IMPORTANT]
> Apenas uma pessoa, o administrador do locatário, em uma organização precisa executar esta tarefa. Se você não for o assinante dessa versão, espere até que sua organização se inscreva e você receba suas credenciais de usuário.
> 
> As avaliações são de uso único no locatário. Você só pode executar uma avaliação de cada vez. Recomendamos que você crie um novo locatário para o propósito de avaliação.

### <a name="dynamics-365-project-operations-trial"></a>Avaliação do Dynamics 365 Project Operations 

Antes de começar, verifique se está conectado a um navegador com a conta de trabalho do usuário no locatário em que deseja ter a versão preliminar do Project Operations.

1. Vá para [Avaliação do Project Operations](https://aka.ms/try-po) para resgatar o primeiro código da oferta, **Dynamics 365 Project Operations**.
2. Confirme a ordem.

  Você verá que a oferta de confirmação foi resgatada com sucesso.

## <a name="assign-licenses"></a>Atribuir licenças

> [!IMPORTANT]
> Você precisará de acesso administrativo ao Portal do Microsoft 365 da sua organização para concluir as etapas a seguir.


1. Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir licenças a seus usuários.
2. Na página **Usuários ativos**, selecione os usuários aos quais deseja atribuir uma licença.
3. Verifique se a licença do **Dynamics 365 Project Operations** foi selecionada. 
4. Selecione **Salvar alterações**.

## <a name="create-a-new-dataverse-environment"></a>Criar um novo ambiente do Dataverse

1. Provisione um novo ambiente de implantação do Project Operations Dataverse, seguindo as instruções no artigo, [Modelo de implantação do Dataverse](lite-deployment.md). Ao selecionar o tipo de ambiente, utilize **Avaliação (baseado em assinatura)**.

  ![Novo ambiente.](./media/19CreateEnvironment.png)

2. Selecione a configuração **Habilitar aplicações do Dynamics 365** e deixe em branco **Implantar automaticamente essas aplicações**.  
3. Selecione **Salvar** para criar o ambiente.

  ![Adicionar banco de dados.](./media/20CreateEnvironment1.png)

4. Depois de criar o ambiente, instale a solução **Microsoft Dynamics 365 Project Operations**. 

![Instalar Solução.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar uma configuração CDS e configurar dados de demonstração

Instale a configuração do CDS e configure dados de demonstração seguindo as instruções no artigo, [Aplicar configuração de demonstração e dados de configuração](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
