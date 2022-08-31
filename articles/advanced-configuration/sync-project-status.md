---
title: Sincronizar Status do Projeto para impedir a entrada em projetos fechados
description: Este artigo explica como sincronizar o status do projeto para impedir a entrada em projetos inativos ou fechados.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2022
ms.locfileid: "9347998"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sincronizar Status do Projeto para impedir a entrada em projetos fechados

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

## <a name="scenario"></a>Cenário

A Contoso está ativada com o Microsoft Dynamics 365 Project Operations para cenários de recursos/itens sem estoque. Como parte das atividades normais de negócios, os projetos podem ser concluídos ou suspensos. Você pode desativar o projeto para garantir que nenhuma despesa ou fatura seja gerada.

## <a name="solution"></a>Solução

### <a name="prerequisites"></a>Pré-requisitos

-   O Microsoft Dynamics 365 Finance 10.0.29 ou posterior deve estar instalado.
-   Mapa de gravação dupla 1.0.0.3 para Projetos V2 (msdyn\_ projetos) deve ser instalado ou configurado manualmente conforme descrito abaixo.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Criar uma versão atualizada do mapa de gravação dupla Projetos V2 de integração do Project Operations

Para atualizar o mapa de gravação dupla Projetos V2 do Project Operations:

1. No espaço de trabalho **Gerenciamento de dados**, selecione **Gravação dupla**.
2. Selecione o bloco **Gravação dupla**.
3. pela coluna T **Mapa da tabela**, localize e selecione **Projeto V2 (msdyn\_ projetos)** e, em seguida, selecione Parar.
4. Selecione o nome do mapa para abrir o mapa e selecione **[Nenhum]**.
5. Na caixa de diálogo Selecionar coluna, selecione **statecode\[Project Status\]** e, em seguida, selecione OK. Você pode digitar **state** no valor do filtro para restringir a lista.
6.  Selecione **Adicionar ou editar transformação** na coluna **tipo de mapa** para editar a transformação.
7.  Em **Tipo de transformação**, selecione **ValueMap**.
8.  Selecione **Adicionar mapeamento de valores** e, em seguida, adicione as seguintes **Chaves** e **Valores**:

   Key       | Valor 
   ----------|-------
   InProcess | 0     
   concluído | 0     

![Captura de tela mostrando o mapeamento de gravação dupla](media/projectstage-dw-mapping.png)

9. Selecione **Salvar**.
10. Da parte superior da página **Gravação dupla > Projetos V2 (msdyn_projects)**, selecione **Salvar como**.
11. Em **Adicionar tabela**, no campo **Editor**, selecione **Editor padrão CDS**.
12. Defina o campo **Versão** como 1.0.0.3.
13. Digite uma **Descrição** e selecione **Salvar**.
14. Da parte superior da página **Gravação dupla > Projetos V2 (msdyn_projects)**, selecione **Executar** para iniciar o mapa e, em seguida, selecione **Sim** para confirmar antes da execução. 

### <a name="close-a-newly-completed-project"></a>Fechar um projeto recém-concluído

O Dynamics 365 Finance usa o campo **fase do projeto** para diferenciar os projetos **em processo** ou **concluídos**. Projetos **Concluídos** não podem ter despesas nem ser faturados aos clientes.

1. Abra um projeto para desativar.
2. Na faixa de opções, selecione **Desativar**.

> [!NOTE]
> Você pode desativar ou fechar um projeto, pois o comportamento dos dois é o mesmo no contexto do Finance.

3. No Finance, abra a página **Lista de todos os projetos**.
4. Confirme se o projeto desativado não aparece na lista.
5. No filtro **mostrar projetos** acima da lista, altere o valor de **Ativo** para **Tudo**.
6. Agora você verá o projeto desativado.

Se você tentar registrar tempo ou despesas neste projeto no Finance, não deverá ver o projeto para seleção. Se você inserir manualmente o número do projeto em uma despesa, verá uma mensagem como "Fase do projeto concluído não permite gravação no projeto". Faturamento e outras funções de cobrança devem ser desabilitadas, pois estarão no contexto de um projeto fechado.

