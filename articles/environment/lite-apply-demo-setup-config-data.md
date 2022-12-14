---
title: Aplicar configuração de demonstração e dados de configuração - lite
description: Este artigo fornece informações sobre como aplicar a configuração de demonstração e dados de configuração ao Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811011"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicar configuração de demonstração e dados de configuração para o Project Operations - lite 

_**Fazer implantação do Project Operations Lite - gerenciar faturamento pro forma_



## <a name="prerequisites"></a>Pré-requisitos

Antes de iniciar a configuração, é necessário ter um ambiente do Dataverse provisionado para o Dynamics 365 Project Operations.


## <a name="instructions"></a>Instruções

1. Baixe o [Pacote de dados de configuração](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Navegue até a pasta *ProjOpsSampleSetupData - CE apenas CMT* e execute o arquivo executável, *DataMigrationUtility*.
1. Na página 1 do Assistente de migração de configuração (CMT) do Common Data Service, selecione **Importar dados** e então selecione **Continuar**.

    ![Migração de configuração.](./media/1ConfigurationMigration.png)

1. Na página 2 do assistente CMT, selecione **Microsoft 365** como **Tipo de implantação**.
1. Marque as caixas de seleção **Exibir uma lista de organizações disponíveis** e **Mostrar avançado**.
1. Selecione a região do seu locatário, insira suas credenciais e selecione **Logon**.

   ![Entrada na configuração.](./media/2ConfigurationSignin.png)

1. Na página 3, na lista de organizações no locatário, selecione a organização para a qual deseja importar os dados de demonstração e selecione **Logon**.
1. Na página 4, selecione o arquivo zip, *SampleSetupAndConfigData* da pasta descompactada, *ProjOpsSampleSetupData - CE apenas CMT*.

   ![Arquivo compactado.](./media/3ZipFile.png)

   ![Selecionar um arquivo.](./media/4SelectAFile.png)

1. Depois que o arquivo zip for selecionado, selecione **Importar dados**.

   ![Importar dados.](./media/5ImportData.png)

1. A importação será executada por aproximadamente dois a dez minutos, dependendo da velocidade da rede. Após da conclusão, saia do Assistente do CMT. 
1. Verifique se há dados na sua organização nas 18 entidades a seguir:

    -   Moeda
    -   Conta
    -   Unidade Organizacional
    -   Contato
    -   Unidade
    -   Grupo de Unidades
    -   Lista de Preços
    -   Lista de Preços do Parâmetro do Projeto 
    -   Frequência da Fatura
    -   Categoria de Recurso Reservável
    -   Categoria da Transação
    -   Categoria de Despesa
    -   Preço da Função
    -   Preço da Categoria da Transação
    -   Característica
    -   Recurso Reservável
    -   Associação de Categoria de Recurso Reservável
    -   Característica de Recurso Reservável

    ![Concluir importação.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
