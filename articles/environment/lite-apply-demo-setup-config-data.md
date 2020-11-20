---
title: Aplicar configuração de demonstração e dados de configuração - lite
description: Este tópico fornece informações sobre como aplicar os dados de configuração e instalação de demonstração para Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401249"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicar configuração de demonstração e dados de configuração para o Project Operations - lite 

_**Fazer implantação do Project Operations Lite - gerenciar faturamento pro forma_

## <a name="prerequisites"></a>Pré-requisitos

Antes de iniciar a configuração, você deve ter um ambiente Common Data Service (CDS) provisionado para o Dynamics 365 Project Operations.


## <a name="instructions"></a>Instruções

1. Faça o download do [Pacote de dados mestre](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Navegue até a pasta *ProjOpsDemoDataSetupAndMaster - CMT integrado* e execute o arquivo executável *DataMigrationUtility*.
3. Na página 1 do Assistente de migração de configuração (CMT) do Common Data Service, selecione **Importar dados** e então selecione **Continuar**.

![Migração de Configuração](./media/1ConfigurationMigration.png)

4. Na página 2 do Assistente CMT, selecione **Microsoft 365** como o **Tipo de Implantação**.
5. Marque as caixas de seleção **Exibir uma lista de organizações disponíveis** e **Mostrar avançado**.
6. Selecione a região do seu locatário, insira suas credenciais e selecione **Logon**.

![Entrar na configuração](./media/2ConfigurationSignin.png)

7. Na página 3, na lista de organizações no locatário, selecione a organização para a qual deseja importar os dados de demonstração e selecione **Logon**.
8. Na página 4, selecione o arquivo zip *MasterAndSetupData* da pasta descompactada *ProjOpsDemoDataSetupAndMaster - CMT integrado*.

![Arquivo compactado](./media/3ZipFile.png)

![Selecionar um arquivo](./media/4SelectAFile.png)

9. Depois que o arquivo zip for selecionado, selecione **Importar dados**.

![Importar dados](./media/5ImportData.png)

10. A importação será executada por aproximadamente dois a dez minutos, dependendo da velocidade da rede. Após da conclusão, saia do Assistente do CMT. 
11. Verifique se há dados na sua organização nas 20 entidades a seguir:

-   Moeda
-   Conta
-   Unidade Organizacional
-   Contato
-   Grupo tributário
-   Grupo de Clientes
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

![Concluir importação](./media/6CompleteImport.png)
