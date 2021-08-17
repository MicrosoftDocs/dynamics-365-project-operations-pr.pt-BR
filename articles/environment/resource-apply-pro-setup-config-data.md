---
title: Configurar e aplicar dados de configuração no Common Data Service
description: Este tópico fornece informações sobre a configuração e aplicação de dados de configuração no Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26f49ad3b9fb08824071699128f8b907ec98bb54505c6fea3c97288cbaf31633
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986612"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Configurar e aplicar dados de configuração no Common Data Service 

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Pré-requisitos

Antes de começar a configurar os dados no Common Data Service (CDS), os seguintes pré-requisitos devem ser atendidos:

1.  Provisione um ambiente CDS e um ambiente do Dynamics 365 Finance para o Project Operations.
2.  As informações de pessoa jurídica do Dynamics 365 Finance são compartilhadas no ambiente CDS. Isso significa que a entidade **Empresa** no CDS tem os seguintes registros da empresa:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Instalar dados de configuração

1. Baixe, desbloqueie e descompacte o [Pacote de dados de configuração](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Navegue até a pasta descompactada e execute o arquivo executável *DataMigrationUtility*.
3. Na página 1 do Assistente de migração de configuração (CMT) do Common Data Service, selecione **Importar dados** e então selecione **Continuar**.

![Migração de configuração.](./media/1ConfigurationMigration.png)

4. Na página 2 do Assistente CMT, selecione **Microsoft 365** como o **Tipo de Implantação**.
5. Marque as caixas de seleção **Exibir uma lista de organizações disponíveis** e **Mostrar avançado**.
6. Selecione a região do seu locatário, insira suas credenciais e selecione **Logon**.

![Entrada na configuração.](./media/2ConfigurationSignin.png)

7. Na página 3, na lista de organizações no locatário, selecione a organização para a qual deseja importar os dados de demonstração e selecione **Logon**.
8. Na página 4, selecione o arquivo zip *SampleSetupAndConfigData* da pasta descompactada.

![Seleção do arquivo zip.](./media/3ZipFile.png)

![Selecionar um arquivo.](./media/4SelectAFile.png)

9. Depois que o arquivo zip for selecionado, selecione **Importar dados**.

![Importar dados.](./media/5ImportData.png)

10. A importação será executada por aproximadamente dois a dez minutos, dependendo da velocidade da rede. Após a conclusão da importação, saia do Assistente do CMT. 
11. Verifique se há dados na sua organização nas 26 entidades a seguir:

  - Moeda
  - Plano de Contas
  - Calendário fiscal
  - Tipos de Taxa de Câmbio da Moeda
  - Dia do Pagamento
  - Agenda de Pagamento
  - Condição de Pagamento
  - Unidade Organizacional
  - Contato
  - Grupo tributário
  - Grupo de Clientes
  - Grupo de Fornecedores
  - Unidade
  - Grupo de Unidades
  - Lista de Preços
  - Lista de Preços do Parâmetro do Projeto
  - Frequência da Fatura
  - Categoria de Recurso Reservável
  - Categoria da Transação
  - Categoria de Despesa
  - Preço da Função
  - Preço da Categoria da Transação
  - Característica
  - Recurso Reservável
  - Associação de Categoria de Recurso Reservável
  - Característica de Recurso Reservável

![Concluir importação.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Atualizar configurações do Project Operations

1. Navegue até o ambiente CE. Você pode encontrá-lo ao abrir o [Centro de Administração da Power Platform](https://admin.powerplatform.microsoft.com/environments), selecionar o ambiente e, em seguida, **Abrir Ambiente**. 

![Abrir ambiente.](./media/7OpenEnvironment.png)

2. Acesse **Projetos** > **Recursos** e selecione **Novo** para criar um recurso reservável para seu usuário.

![Recursos reserváveis.](./media/8BookableResources.png)

3. Na guia **Geral**, selecione seu usuário administrador. Verifique se o fuso horário corresponde ao que você está. 

![Novo recurso reservável.](./media/9NewBookableResource.png)

4. Na guia **Agendamento**, no campo **Empresa**, escolha a empresa **USPM** e selecione **Salvar**. 

![Guia Agendamento.](./media/10SchedulingTab.png)

5. Selecione a guia **Horas de Trabalho**.  

![Horário de trabalho.](./media/11WorkHours.png)

6. Clique duas vezes em qualquer valor no calendário e selecione **Editar** > **Todos os eventos da série**. 

![Calendário de trabalho.](./media/12WorkCalendar.png)

7. Altere as horas de trabalho para um dia de trabalho de oito (8) horas, marque os finais de semana como dias não úteis e certifique-se de que o fuso horário corresponda ao seu. 
8. Selecione **Salvar e fechar**.

![Atualizar calendário.](./media/13UpdateCalendar.png)

9. Acesse **Configurações** > **Modelos de calendário** e selecione **Novo**.
 
 ![Modelos de calendário.](./media/14CalendarTemplates.png)
 
 10. Insira um nome, selecione o recurso do modelo que você criou e, em seguida, **Salvar**. 
 
 ![Salvar modelo de calendário.](./media/15SaveCalendarTemplate.png)
 
 11. Acesse **Parâmetros** e clique duas vezes no registro. 
 
 ![Parâmetros do projeto.](./media/16ProjectParameters.png)
 
12. Atualize os seguintes campos:

 - **Empresa Padrão**: USPM
 - **Unidade Organizacional Padrão**: Contoso Robotics Global
 - **Frequência da Fatura**: sétimo e último dia
 - **Modelo de horas de trabalho**: altere para o modelo que você criou.

13. Selecione **Salvar**. 

![Atualizar parâmetros do projeto.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
