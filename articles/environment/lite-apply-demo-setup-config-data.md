---
title: Aplicar configuração de demonstração e dados de configuração - lite
description: Este artigo fornece informações sobre como aplicar a configuração de demonstração e dados de configuração ao Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9409963"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicar configuração de demonstração e dados de configuração para o Project Operations - lite 

_**Fazer implantação do Project Operations Lite - gerenciar faturamento pro forma_



## <a name="prerequisites"></a>Pré-requisitos

Antes de iniciar a configuração, é necessário ter um ambiente do Dataverse provisionado para o Dynamics 365 Project Operations.


## <a name="instructions"></a>Instruções

1. Faça o download do [Pacote de dados mestre](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Navegue até a pasta *ProjOpsSampleSetupData - CE apenas CMT* e execute o arquivo executável, *DataMigrationUtility*.
3. Na página 1 do Assistente de migração de configuração (CMT) do Common Data Service, selecione **Importar dados** e então selecione **Continuar**.

    ![Migração de configuração.](./media/1ConfigurationMigration.png)

4. Na página 2 do assistente CMT, selecione **Microsoft 365** como **Tipo de implantação**.
5. Marque as caixas de seleção **Exibir uma lista de organizações disponíveis** e **Mostrar avançado**.
6. Selecione a região do seu locatário, insira suas credenciais e selecione **Logon**.

   ![Entrada na configuração.](./media/2ConfigurationSignin.png)

7. Na página 3, na lista de organizações no locatário, selecione a organização para a qual deseja importar os dados de demonstração e selecione **Logon**.
8. Na página 4, selecione o arquivo zip, *SampleSetupAndConfigData* da pasta descompactada, *ProjOpsSampleSetupData - CE apenas CMT*.

   ![Arquivo compactado.](./media/3ZipFile.png)

   ![Selecionar um arquivo.](./media/4SelectAFile.png)

9. Depois que o arquivo zip for selecionado, selecione **Importar dados**.

   ![Importar dados.](./media/5ImportData.png)

10. A importação será executada por aproximadamente dois a dez minutos, dependendo da velocidade da rede. Após da conclusão, saia do Assistente do CMT. 
11. Verifique se há dados na sua organização nas 18 entidades a seguir:

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
