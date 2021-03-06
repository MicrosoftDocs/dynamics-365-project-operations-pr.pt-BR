---
title: Provisionar um novo ambiente
description: Este tópico fornece informações sobre como provisionar um novo ambiente do Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949348"
---
# <a name="provision-a-new-environment"></a>Provisionar um novo ambiente

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico fornece informações sobre como provisionar um novo ambiente do Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Habilitar o provisionamento automatizado do Project Operations em um projeto do LCS

Use as etapas a seguir para habilitar o fluxo de provisionamento automatizado do Project Operations para seu projeto do LCS.

1. Acesse [LCS](https://lcs.dynamics.com/v2) e selecione o bloco **Gerenciamento versão prévia do recurso**.
2. Na lista **Versão prévia do recurso**, selecione **Project Operations** e **Versão prévia do recurso habilitada** para habilitar o Project Operations.

> [!NOTE]
> Esta etapa é realizada apenas uma vez por projeto do LCS.

## <a name="provision-a-project-operations-environment"></a>Provisionar um ambiente do Project Operations

1. Abra uma nova implantação de [ambiente de demonstração](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ou [área restrita/ambiente de produção](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) do Dynamics 365 Finance. 
2. Siga o assistente de **Provisionamento de ambiente**. 

> [!IMPORTANT]
> Certifique-se de que a versão do aplicativo selecionado seja 10.0.13 ou superior.

3. Para provisionar o Project Operations, em **Configurações avançadas**, selecione **Common Data Service**. 
4. Habilite a **Configuração do Common Data Service** selecionando **Sim** e insira as informações nos campos obrigatórios:

  - Nome
  - Região
  - Linguagem
  - Moeda
 
5. No campo **Modelo do Common Data Service**, selecione **Project Operations** 

6. Selecione o tipo de ambiente para sua implantação. Uma avaliação baseada em subscrição permitirá que você implante um ambiente CDS por 30 dias. 

![Configurações da implantação](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Selecione **Concordo** para aceitar os termos de serviço e, em seguida, **Concluído** para retornar às configurações de implantação.

![Consentimento de Implantação](./media/2DeploymentConsent.png)

7. Preencha os campos obrigatórios restantes no assistente e confirme a implantação. O tempo de provisionamento do ambiente varia de acordo com o tipo de ambiente. O provisionamento pode levar até seis horas.

  Depois que a implantação for concluída com sucesso, o ambiente será exibido como **Implantado**.

8. Para confirmar se o ambiente foi implantado com sucesso, selecione **Logon** e faça logon no ambiente para confirmar.

![Detalhes do ambiente do ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Aplicar no Project Operations os dados de demonstração do Finance (etapa opcional)

Aplique no Project Operations os dados de demonstração do Finance ao ambiente hospedado na nuvem da versão de serviço 10.0.13, conforme descrito [neste artigo](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Aplicar atualizações ao ambiente do Finance

O Project Operations requer um ambiente do Finance com aplicativo versão **10.0.13 (10.0.569.20009)** ou superior.

Poderá ser necessário aplicar atualizações de qualidade ao seu ambiente do Finance para receber esta versão.

1. No LCS, na página **Detalhes do ambiente**, na seção **Atualizações Disponíveis**, selecione **Exibir Atualização**.

![Exibir Atualizações](./media/5ViewUpdates.png)

2. Na página **Atualizações de binário**, selecione **Salvar pacote**.

![Salvar pacote](./media/6SavePackage.png)

3. Clique em **Selecionar tudo** e selecione **Salvar pacote**.

![Revisar e salvar atualizações](./media/7ReviewAndSaveUpdates.png)

4. Insira um nome e uma descrição do pacote e selecione **Salvar**. Dependendo da conexão com a Internet, esse processo pode levar algum tempo.

![Carregar pacote para Biblioteca de Ativos](./media/8UploadPackageToAssetsLibrary.png)

5. Depois que o pacote for salvo, selecione **Concluído** e salve esse pacote na Biblioteca de Ativos em seu projeto do LCS.

Salvar e validar o pacote pode levar cerca de 15 minutos.

6. Para aplicar a atualização, navegue até a página **Detalhes do ambiente** no LCS e selecione **Manter** > **Aplicar atualizações**.

![Manter Ambientes](./media/9MaintainEnvironment.png)

7. Na lista de atualizações, selecione o pacote que você criou e **Aplicar**.

![Aplicar Atualizações](./media/10ApplyUpdates.png)

A manutenção do ambiente levará algum tempo. Após a conclusão, o ambiente retornará ao estado implantado.

![Ambiente Implantado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Estabelecer uma conexão de Gravação Dupla 

1. Em seu projeto do LCS, acesse a página **Detalhes do ambiente**.
2. Em **Informações do ambiente do Common Data Service**, selecione **Link para o CDS para aplicativos**.
3. Depois que o link for concluído, selecione novamente **Link para o CDS para aplicativos**. Você será redirecionado para Gravação Dupla no Finance.

![Link para o CDS](./media/12LinktoCDS.png)

4. Selecione **Aplicar Solução** para acessar as entidades que serão mapeadas na integração.

![Aplicar Soluções](./media/13ApplySolutions.png)

5. Selecione ambas as soluções, **Mapa de Entidades de Gravação Dupla do Dynamics 365 Finance and Operations** e **Mapas de Entidades de Gravação Dupla do Dynamics 365 Project Operations** e selecione **Aplicar**.

![Confirmar Soluções](./media/14ConfirmSolutions.png)

Depois que as soluções forem aplicadas, as entidades de Gravação Dupla serão aplicadas ao ambiente.

![Aplicar Soluções](./media/15ApplyingSolutions.png)

Depois que as entidades forem aplicadas, todos os mapeamentos disponíveis serão listados no ambiente.

![Mapas de Gravação Dupla](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Atualizar as entidades de dados após a atualização

1. No Finance, acesse o espaço de trabalho de **Gerenciamento de dados**.

![Espaço de trabalho de Gerenciamento de Dados](./media/16DataManagement.png)

2. Selecione o bloco **Parâmetros da estrutura**.

![Parâmetros da Estrutura](./media/17FrameworkParameters.png)

3. Na página **Configurações de entidade**, selecione **Atualizar lista de entidades**.

![Atualizar Lista de Entidades](./media/18RefreshEntityList.png)

A atualização levará aproximadamente 20 minutos. Você receberá um alerta quando ela for concluída.

![Atualizar Confirmação](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Executar Mapas de Gravação Dupla do Project Operations

1. Em seu projeto do LCS, acesse a página **Detalhes do ambiente**.
2. Em **Informações do ambiente do Common Data Service**, selecione **Link para o CDS para aplicativos**. Depois de selecionar o link, você será redirecionado para a lista de entidades nos mapeamentos.
3. Inicie os mapas conforme descrito na tabela a seguir. Certifique-se de seguir a sequência listada.

| **Mapa de Entidade** | **Atualizar entidade** | **Sincronização inicial** | **Mestre para sincronização inicial** | **Executar pré-requisitos** | **Sincronização inicial dos pré-requisitos** |
| --- | --- | --- | --- | --- | --- |
| **Funções de Recursos do Projeto para Todas as Empresas (bookableresourcecategories)** | No | Sim | Common Data Service | No | N/A |
| **Entidades legais (cdm\_companies)** | No | Sim | Aplicativos do Finance and Operations | No | N/A |
| **Valores reais da integração do Project Operations (msdyn\_actuals)** | No | No | N/A | Sim | No |
| **Linhas de contrato do projeto (salesorderdetails)** | No | No | N/A | No | No |
| **Entidade de integração para relacionamentos de transações do projeto (msdyn\_transactionconnections)** | No | No | N/A | No | N/A |
| **Marcos da linha do contrato de integração do Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | N/A | No | N/A |
| **Entidade de integração do Project Operations para estimativas de despesas (msdyn\_estimateslines)** | No | No | N/A | No | N/A |
| **Entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments)** | No | No | N/A | No | N/A |
| **Entidade de exportação de despesas do projeto de integração do Project Operations (msdyn\_expenses)** | Sim | No | N/A | No | N/A |
| **Entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments)** | Sim | No | N/A | No | N/A |

4. Para atualizar a entidade, selecione o nome do mapa e, em seguida, **Atualizar entidades**. 
5. Continue executando o mapa depois que a atualização for concluída.

![Atualizar Mapa](./media/20RefreshMapping.png)

Antes de habilitar o próximo mapa, verifique se o mapa na tabela está em um estado **Em Execução**. Executar mapas com um número maior de pré-requisitos pode levar algum tempo.

Para executar um mapa com pré-requisitos, habilite o botão de alternância **Exibir mapas de entidades relacionadas**. Se a tabela indicar que **Sincronização inicial do pré-requisito** é **Não**, verifique se o indicador **Sincronização inicial** é **Desativado** em todos os mapas de pré-requisitos antes de executá-lo.

![Executar Mapa](./media/21RunMap.png)

6. Verifique se todos os mapas relacionados ao projeto estão no estado em execução.

![Todos os Mapas em Execução](./media/22AllMapsRunning.png)

Seu ambiente do Project Operations agora está provisionado e configurado.
