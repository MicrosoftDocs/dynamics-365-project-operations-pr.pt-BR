---
title: Aplicar dados de demonstração a um ambiente hospedado na nuvem do Finance
description: Este tópico explica como aplicar dados de demonstração do Project Operations a ambientes hospedados na nuvem do Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365224"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Aplicar dados de demonstração a um ambiente hospedado na nuvem do Finance

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

> [!IMPORTANT]
> Este tópico é aplicável apenas ao Microsoft Dynamics 365 Finance versão 10.0.13 e pode ser executado apenas em um ambiente hospedado na nuvem. Conclua as etapas neste tópico **ANTES** de aplicar atualizações de qualidade ao ambiente.

1. Em seu projeto do LCS, abra a página **Detalhes do ambiente**. Observe que ela inclui os detalhes necessários para se conectar ao ambiente usando o protocolo RDP (Remote Desktop Protocol).

![Detalhes do ambiente do ](./media/1EnvironmentDetails.png)

O primeiro conjunto de credenciais destacadas são as credenciais da conta local e contém um hiperlink para a conexão de área de trabalho remota. As credenciais incluem o nome de usuário e a senha do administrador do ambiente. O segundo conjunto de credenciais é usado para fazer logon no SQL Server neste ambiente.

2. Faça conexão remota ao ambiente pelo hiperlink em **Contas locais** e use as **Credenciais da conta local** para autenticar.
3. Acesse **Serviços de Informação da Internet** > **Pools de Aplicativos** > **AOSService** e interrompa o serviço. Você está interrompendo o serviço neste ponto para que possa continuar a substituir o Banco de Dados SQL.

![Interromper o AOS](./media/2StopAOS.png)

4. Acesse **Serviços** e interrompa os dois itens a seguir:

- Microsoft Dynamics 365 Unified Operations: Batch Management Service
- Microsoft Dynamics 365 Unified Operations: Data Import Export Framework

![Interromper Serviços](./media/3StopServices.png)

5. Abra o Microsoft SQL Server Management Studio. Faça logon com as credenciais do servidor SQL e use o usuário administrador axdb e a senha da página **Detalhes de ambientes** do LCS.

![SQL Server Management Studio](./media/4SSMS.png)

6. No Explorador de Objetos, **Banco de dados** e localize **AXDB**. Você substituirá o banco de dados por um novo banco de dados localizado no [Centro de Download](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Copie o arquivo zip para a VM em que você está conectado remotamente e extraia o conteúdo do zip.
8. No SQL Server Management Studio, clique com o botão direito do mouse em **AxDB** e selecione **Tarefas** > **Restaurar** > **Banco de Dados**.

![Restaurar banco de dados](./media/5RestoreDatabase.png)

9. Selecione **Dispositivo de Origem** e navegue até o arquivo extraído do zip que você copiou.

![Dispositivos de Origem](./media/6SourceDevice.png)

10. Selecione **Opções** e, em seguida, **Substituir o banco de dados existente** e **Fechar conexões existentes para o banco de dados de destino**. 
11. Selecione **OK**.

![Restaurar Configurações](./media/7RestoreSetting.png)

Você receberá a confirmação de que a restauração do AXDB foi bem-sucedida. Depois de receber essa confirmação, você poderá fechar o SQL Services Management Studio.

12. Acesse novamente **Serviços de Informação da Internet** > **Pools de Aplicativos** > **AOSService** e inicie o AOSService.
13. Acesse **Serviços** e inicie os dois serviços interrompidos anteriormente.

14. Localize a ferramenta AdminUserProvisioning nesta VM. Procure em: K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Execute o arquivo .ext usando seu endereço de usuário no campo **Endereço de email**. 
16. Selecione **Enviar**.

![Provisionamento de Usuário Administrador](./media/8AdminUserProvisioning.png)

Isso pode levar alguns minutos para ser concluído. Você deverá receber uma mensagem de confirmação de que o usuário administrador foi atualizado com sucesso.

17. Por último, execute o Prompt de Comando como administrador e execute iisreset

![Redefinição do IIS](./media/9IISReset.png)

18. Feche a sessão da área de trabalho remota e use a página **Detalhes do ambiente** do LCS para fazer logon no ambiente para confirmar se ele está funcionando conforme o esperado.

![Finance and Operations](./media/10FinanceAndOperations.png)
