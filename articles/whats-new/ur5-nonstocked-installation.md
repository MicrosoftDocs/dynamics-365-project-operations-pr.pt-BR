---
title: Atualizar o Project Operations em seu ambiente do Finance
description: Este tópico fornece informações sobre como atualizar o Project Operations no seu ambiente do Dynamics 365 Finance.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816611"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Atualizar o Project Operations em seu ambiente do Finance

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_


Este tópico fornece informações sobre como atualizar o Dynamics 365 Project Operations no seu ambiente do Dynamics 365 Finance. Existem três procedimentos necessários para atualizar o Project Operations para a Atualização 5 (UR5):

- [Importar o pacote para o seu projeto de versão preliminar](#import)
- [Aplicar a atualização](#apply)
- [Atualizar seu ambiente do Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importar o pacote para o seu projeto do LCS

1. Entre no [Lifecycle Services (LCS)](https://lcs.dynamics.com/) como proprietário do projeto ou gerente de ambiente.
2. Na lista de projetos, selecione seu projeto do LCS.
3. Na página **Projeto**, no grupo **Ambientes**, abra o ambiente que deseja atualizar.
4. Verifique se o ambiente está sendo executado. Se não tiver sido iniciado, inicie o ambiente.
5. Na seção **Nova versão** em **Atualizações disponíveis**, selecione **Ver atualização** para 10.0.15.

![Botão Visualizar atualização](media/view-update.png)

6. Na página **Atualizações de binário**, selecione **Salvar pacote**.
7. Na página **Revisar e salvar atualizações**, selecione **Salvar pacote**.
8. No painel **Salvar pacote na biblioteca de ativos** que abrir, digite o nome do pacote e selecione **Salvar pacote**.
9. Quando o LCS terminar de salvar o pacote, o botão **Concluído** será habilitado. Selecione **Concluído**. O LCS irá verificar o pacote. A verificação pode levar alguns minutos ou até uma hora.


## <a name="apply-the-package-update"></a><a name="apply"></a>Aplicar a atualização de pacote

1. No LCS, na página **Detalhes do ambiente**, selecione **Manter** > **Aplicar atualizações**.
2. Na lista, selecione o pacote que você salvou anteriormente e selecione **Aplicar**.
3. Selecione **Sim** para confirmar que deseja implantar o pacote.

![Confirmar a caixa de diálogo de implantação do pacote](media/confirm-package-deployment.png)

4. Selecione **Sim** para confirmar que deseja atualizar o aplicativo.

![Confirmar a caixa de diálogo de atualização do aplicativo](media/confirm-application-update.png)

A implantação e atualização do aplicativo serão iniciadas. 

Na página **Detalhes do ambiente**, no canto superior direito, o status do ambiente será atualizado para **Manutenção**. Em aproximadamente duas horas, a atualização estará concluída. As informações de versão do aplicativo serão atualizadas para **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** e o status do ambiente será atualizado para **Implantado**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Atualizar seu ambiente do Dataverse

1. Entre no [centro de administração da Power Platform](https://admin.powerplatform.com/).
2. Na lista, encontre e abra o ambiente que você usou para instalar o Project Operations.
3. Na página **Ambientes**, selecione **Recurso** > **Aplicativos do Dynamics 365**.
4. Na lista, localize **Microsoft Dynamics 365 Project Operations**, e na coluna **Status**, selecione **Atualização disponível**.
5. Selecione a caixa de seleção **Eu aceito os termos de serviço**, em seguida, selecione **Atualizar**. A versão mais recente da solução será instalada.

Após a conclusão da instalação, você terá a versão 4.5.0.134 instalada.

## <a name="configure-new-features"></a>Configurar novos recursos

### <a name="enable-dual-write-mapping"></a>Habilitar mapeamento de gravação dupla

Depois de concluir a atualização nos ambientes do Finance e Dataverse, você pode ativar os mapeamentos de gravação dupla necessários. Conclua os seguintes procedimentos para habilitar mapeamentos de gravação dupla.

- [Atualizar as configurações de segurança no ambiente do Customer Engagement](#security)
- [Atualizar entidades de dados](#refresh)
- [Atualizar e executar os mapeamentos de gravação dupla](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Atualizar as configurações de segurança no ambiente do Dataverse

As seguintes atualizações para os privilégios de segurança para entidades são necessárias como parte da atualização para UR5.

1. No seu ambiente do Dataverse, vá para **Configurações** e no grupo **Sistema**, selecione **Segurança**.

![Configurações do ambiente do Dataverse](media/Picture21.png)

2. Selecione **Direitos de Acesso**.
3. Na lista de direitos, selecione **usuário de aplicativo de gravação dupla** e selecione a guia **Entidades personalizadas**. 
4. Verifique se o direito tem permissões para **Ler** e **Anexar a** para:

      - **Tipo da taxa de câmbio de moeda**
      - **Tabela de contas** 
      - **Calendário fiscal** 
      - **Razão**

5. Depois que o direito de acesso for atualizado, vá para **Configurações** > **Segurança** > **Equipes**. Verifique se a função **usuário de aplicativo de gravação dupla** foi aplicada à equipe. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Atualizar entidades de dados com base na atualização

1. Em seu ambiente do Finance, abra o espaço de trabalho **Gerenciamento de dados** e, em seguida, abra a página **Parâmetros da estrutura**.
2. Na guia **Configurações de entidade**, selecione **Atualizar lista de entidades**.
3. Selecione **Fechar** para confirmar a atualização da entidade.

 > [!NOTE]
 > Esse processo levará aproximadamente 20 minutos para ser concluído. Você será notificado quando a atualização for concluída.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Atualizar mapeamentos de gravação dupla

1. No espaço de trabalho **Gerenciamento de dados**, selecione **Gravação dupla**.
2. Selecione **Aplicar soluções**, selecione ambas as soluções na lista e, em seguida, selecione **Aplicar**.
3. Na página **Gravação dupla**, selecione os seguintes mapas de tabela e, em seguida, selecione **Parar**.

    - **Valores reais da integração do Project Operations (msdyn_actuals)**
    - **Categorias de despesas do projeto de integração do Project Operations (msdyn_expensecategories)**
    - **Entidade de exportação de despesas do projeto dados reais de integração do Project Operations (msdyn_expenses)**

4. Na página **Versão do mapa de tabela**, aplique uma nova versão do mapa a cada uma das três entidades.
5. Na página **Gravação dupla**, selecione executar para reiniciar os mapas.
6. Na lista de mapas, selecione o mapa **Razão (msdyn_ledgers)** com todos os pré-requisitos e marque a caixa de seleção **Sincronização inicial**. 
7. No campo **Mestre para sincronização inicial**, selecione **Aplicativos Finance and Operations** e então selecione **Executar**.
 
 ![Sincronização de mapa de razão](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]