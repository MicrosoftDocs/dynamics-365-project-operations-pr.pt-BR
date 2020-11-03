---
title: Aplicar instalação de demonstração e dados de configuração
description: Este tópico fornece informações sobre como aplicar os dados de configuração e instalação de demonstração para Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071293"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Aplicar instalação de demonstração e dados de configuração para implantação do Project Operations Lite - transação para faturamento pró-forma

_**Fazer implantação do Project Operations Lite - gerenciar faturamento pro forma_

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

- Moeda
- Unidade Organizacional
- Contato
- Grupo tributário
- Grupo de Clientes
- Unidade
- Grupo de Unidades
- Lista de Preços
- Lista de Preços do Parâmetro do Projeto
- Frequência da Fatura
- Detalhe da Frequência da Fatura
- Categoria de Recurso Reservável
- Categoria da Transação
- Categoria de Despesa
- Preço da Função
- Preço da Categoria da Transação
- Característica
- Recurso Reservável
- Associação de Categoria de Recurso Reservável
- Característica de Recurso Reservável

![Concluir importação](./media/6CompleteImport.png)
