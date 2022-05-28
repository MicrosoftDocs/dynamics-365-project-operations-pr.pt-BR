---
title: Aplicar configuração de demonstração e dados de configuração - lite
description: Este tópico fornece informações sobre como aplicar os dados de configuração e instalação de demonstração para Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ecb5da3bccf35f8ed7e2246f68dd4da2b145c6be
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586974"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicar configuração de demonstração e dados de configuração para o Project Operations - lite 

_**Fazer implantação do Project Operations Lite - gerenciar faturamento pro forma_



## <a name="prerequisites"></a>Pré-requisitos

Antes de iniciar a configuração, você deve ter um ambiente do Common Data Service (CDS) provisionado para o Dynamics 365 Project Operations.


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
