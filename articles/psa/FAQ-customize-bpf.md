---
title: Como posso personalizar o fluxo do processo empresarial Estágios do projeto?
description: Uma visão geral de como personalizar o fluxo do processo empresarial Estágios do Projeto.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7efbb19161878e13a1b0d33bc1bc4e06521445c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596956"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Como posso personalizar o fluxo do processo empresarial Estágios do projeto?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Há uma limitação conhecida em versões anteriores do aplicativo Project Service, em que os nomes dos estágios do fluxo do processo empresarial Estágios do projeto devem corresponder exatamente aos nomes esperados em inglês (**Quote**, **Plan**, **Close**). Caso contrário, a lógica de negócios, que depende dos nomes dos estágios em inglês, não funciona conforme esperado. Por isso, você não vê ações conhecidas como **Alternar Processo** ou **Editar Processo** disponíveis no formulário do projeto. Além disso, não é recomendável personalizar o fluxo do processo empresarial. 

Essa restrição foi solucionada na versão 2.4.5.48 e posterior. Este artigo fornece soluções alternativas sugeridas para versões anteriores, caso seja necessário personalizar o fluxo do processo empresarial padrão.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>A lógica de negócios exige uma correspondência exata com nomes dos estágios em inglês

O fluxo do processo empresarial Estágios do projeto inclui uma lógica de negócios que leva aos seguintes comportamentos no aplicativo:
- Quando o projeto é associado a uma cotação, o código define o fluxo do processo empresarial para o estágio **Quote**.
- Quando o projeto é associado a um contrato, o código define o fluxo do processo empresarial para o estágio **Plan**.
- Quando o fluxo de processo empresarial avança para o estágio **Close**, o registro do projeto é desativado. Quando o projeto é desativado, o formulário do projeto e a estrutura de detalhamento de trabalho (WBS) são definidos como somente leitura, as reservas de recursos nomeados são liberadas, e todas as listas de preços associadas são desativadas.

Essa lógica de negócios depende dos nomes em inglês para os estágios do projeto. Essa dependência dos nomes dos estágios em inglês é o motivo principal pelo qual a personalização do fluxo do processo empresarial Estágios do projeto não é recomendável. Essa também é a razão pela qual você não vê ações do fluxo do processo empresarial como **Alternar Processo** ou **Editar Processo** na entidade de projeto.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>O que acontece se os nomes de estágios não correspondem aos nomes em inglês?

Na versão 1.x do aplicativo Project Service na plataforma 8.2, quando os nomes dos estágios no fluxo do processo empresarial não correspondem exatamente aos nomes dos estágios em inglês, a lógica de negócios que define o estágio adequado para cotações ou contratos, ou que encerra o projeto, é ignorada. Nenhuma mensagem de erro é exibida. Por isso, parece que você pode personalizar o fluxo do processo empresarial Estágios do projeto. Entretanto, não verá nenhum processo automático funcionando para cotações, contratos e fechamentos de projetos.

Na versão 2.4.4.30 ou anterior do aplicativo Project Service na plataforma 9.0, houve uma alteração significativa na arquitetura para fluxos do processo empresarial, que exigiu a regravação da lógica de negócios do fluxo do processo empresarial. Consequentemente, se os nomes dos estágios do processo não corresponderem aos nomes esperados em inglês, você receberá uma mensagem de erro. 

Portanto, se você quiser personalizar o fluxo do processo empresarial Estágios do projeto para a entidade de projeto, você só pode adicionar novos estágios ao fluxo do processo empresarial padrão para a entidade de projeto, mantendo os estágios **Quote**, **Plan** e **Close** da maneira em que se encontram. Essa restrição garante que você não receba erros da lógica de negócios que espera os nomes dos estágios em inglês no fluxo do processo empresarial.

Em uma versão 2.4.5.48 ou futura, a lógica de negócios descrita neste artigo é removida do fluxo do processo empresarial padrão para a entidade de projeto. A atualização para a versão ou posterior permitirá que você personalize ou substitua o fluxo do processo empresarial padrão por um que seja seu. 

## <a name="workarounds-for-earlier-versions"></a>Soluções alternativas para versões anteriores

Se a atualização não for uma opção, será possível personalizar o fluxo do processo empresarial Estágios do projeto para a entidade de projeto de uma destas duas maneiras:

1. Adicione mais estágios à configuração padrão, mantendo os nomes dos estágios em inglês para **Quote**, **Plan** e **Close**.


![Captura de tela da adição de estágios à configuração padrão.](media/FAQ-Customize-BPF-1.png)
 
2. Crie seu próprio fluxo do processo empresarial e o torne o fluxo do processo empresarial principal para a entidade de projeto, permitindo que você tenha qualquer nome de estágio que quiser. Entretanto, se você quiser usar os mesmos estágios do projeto padrão, **Quote**, **Plan** e **Plan**, será necessário fazer algumas personalizações baseadas em seus nomes de estágios personalizados. A lógica mais complexa está no fechamento do projeto, que você ainda pode acionar por meio da desativação do registro do projeto.

![Personalização do BPF.](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Considerações adicionais para a versão 2.4.4.30 ou anterior do aplicativo Project Service na plataforma 9.0

Na versão 2.4.4.30 ou anterior do Project Service na plataforma 9.0, com um fluxo do processo empresarial personalizado, o campo **Nome de estágio** na entidade de projeto usada no gráfico **Projeto por estágio** e exibições de listas do projeto não serão atualizados, pois estão acoplados ao fluxo do processo empresarial padrão Estágios do projeto. Você pode resolver esse problema com uma as seguintes ações:

- Adicione um campo personalizado para capturar o estágio atual do fluxo do processo empresarial que é atualizado conforme o usuário avança no fluxo de processo empresarial personalizado.

- Modifique o gráfico **Projeto por estágio** para trabalhar com o seu campo personalizado em vez da configuração padrão.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Etapas para criar seu próprio fluxo do processo empresarial para a entidade de projeto

Para criar seu próprio fluxo do processo empresarial para a entidade de projeto, faça o seguinte:

1. Vá para **Configurações** > **Centro de processos**. Não copie o fluxo do processo empresarial Estágios do projeto porque isso também copiará a lógica de negócios do Project Service.

  ![Criar processo.](media/FAQ-Customize-BPF-3.png)

2. Use o designer de processo para criar os nomes de estágios que quiser. Caso queira a mesma funcionalidade dos estágios padrão para **Quote**, **Plan** e **Close**, é necessário criá-la com base nos nomes dos estágios do fluxo do processo empresarial personalizado.

   ![Captura de tela do designer de processo usado para personalizar o BPF.](media/FAQ-Customize-BPF-4.png) 

3. No designer de processo, clique em **Ordenar Fluxo do Processo** para tornar o fluxo do processo empresarial personalizado o fluxo do processo empresarial principal para a entidade de projeto ao movê-lo acima do fluxo do processo empresarial Estágios do projeto para o topo da lista.


   [Captura de tela do uso de Ordenar Fluxo do Processo](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>As etapas a seguir se aplicam à versão 2.4.4.30 ou anterior do aplicativo Project Service na plataforma 9.0

4. Adicione um novo campo personalizado à entidade de projeto para capturar as etapas personalizadas no fluxo do processo empresarial personalizado. Será necessário adicionar a lógica de negócios (plug-in/fluxo de trabalho) para atualizar esse campo quando o estágio no fluxo do processo empresarial personalizado for atualizado.

   ![Captura de tela da personalização da entidade de projeto.](media/FAQ-Customize-BPF-6-720.png)

5. Modifique o gráfico **Projeto por estágio** para usar o novo campo personalizado para os estágios.

   ![Captura de tela do uso do gráfico Projeto por estágio.](media/FAQ-Customize-BPF-7-720.png)

6. Modifique todas as exibições para a entidade de projeto para incluir o novo campo personalizado para os estágios.

   ![Captura de tela das modificações de exibições na entidade de projeto.](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
