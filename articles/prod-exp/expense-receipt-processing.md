---
title: Processamento de recibo de despesas
description: Este artigo fornece informações sobre o processamento de OCR (reconhecimento óptico de caracteres) para recibos. Esse recurso foi desenvolvido para melhorar a experiência do usuário quando relatórios de despesas são criados no Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 5a72802e3c52b6a9e55ac779aa36c32072dc8b8b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911398"
---
# <a name="expense-receipt-processing"></a>Processamento de recibo de despesas

A entrada de despesas foi aprimorada com a introdução do processamento de reconhecimento óptico de caracteres (OCR) para recibos. Esse recurso foi projetado para melhorar a experiência do usuário ao criar relatórios de despesas.

## <a name="key-features"></a>Recursos principais

- O nome do comerciante, a data e o valor total são extraídos dos recibos.
- O recurso tenta combinar os recibos não anexados com as transações de despesas não anexadas.
- Usuários podem criar transações de despesas inseridas manualmente a partir de recibos.

## <a name="usage-examples"></a>Exemplos de uso

Para anexar automaticamente recibos que incluam transações de cartão de crédito quando um relatório de despesas for criado, faça o seguinte:

  1. Abra o espaço de trabalho **Gerenciamento de despesas**.
  2. Na guia **Recibos**, verifique se existem recibos não anexados. Você também pode carregar recibos na guia **Recibos**.
  3. Na guia **Despesas**, verifique se existem despesas não anexadas. Normalmente, o administrador de despesas importa essas despesas da operadora do cartão de crédito.
  4. Selecione **Novo relatório de despesas**. Observe que você também pode incluir despesas e recibos ao criar um relatório de despesas. Se você adicionar despesas e recibos, a comparação automática dos recibos com as despesas será disparada.

Para criar uma despesa ou comparar uma despesa de um recibo, faça o seguinte:

  1. Em um relatório de despesas, na v **Recibos**, anexe um recibo selecionando **Adicionar recibos**.
  2. Abaixo da imagem carregada do recibo, observe as opções **Criar** e **Comparar**.

      - Selecione **Criar** para criar uma transação de despesas inserida manualmente e preencha os valores que são extraídos do recibo.
      - Se você selecionar **Comparar**, o sistema tentará corresponder uma despesa existente ao recibo.

## <a name="installation"></a>Instalação

Este recurso funciona em combinação com o recurso **Relatórios de despesas reinventados** para ajudar a simplificar a experiência de despesas. Este recurso está disponível apenas para ambientes Nível 2+, que são Área restrita e Produção.

Para usar esses recursos avançados de despesa, instale o suplemento Serviço de Gerenciamento de Despesas para o Microsoft Dynamics 365 Finance e ative os recursos na instância. Você pode acessar o suplemento do seu projeto no Microsoft Dynamics Lifecycle Services (LCS).

1. Entre no LCS e abra o ambiente desejado.
2. Vá para **Detalhes completos**.
3. Selecione **Manter** ou role para baixo até a FastTab **Suplementos de ambiente**.
4. Selecione **Instalar um novo suplemento**.
5. Selecione **Serviço de Gerenciamento de Despesas**.
6. Siga o guia de instalação e concorde com os termos e condições.
7. Selecione **Instalar**.

No espaço de trabalho **Gerenciamento de recursos**, ative os seguintes recursos:

- Relatórios de despesas reinventados
- Faça a correspondência automática e crie despesas a partir do recibo

Quando você ativa esses recursos, ocorrem as seguintes ações:

- O espaço de trabalho **Gerenciamento de despesas** existente é substituído pelo novo espaço de trabalho.
- Um novo item de menu para visibilidade do campo de despesas é adicionado.
- Você ainda pode abrir a página **Relatórios de despesas** anterior acessando **Gerenciamento de despesas > Minhas despesas > Relatórios de despesas**.
- Fluxos de trabalho e aprovações ainda levam você para a página de relatórios de despesas existentes.
- Os recibos serão processados por meio de Microsoft Azure Cognitive Services e metadados serão extraídos e adicionados.
- Foi adicionada uma opção que permite criar um relatório de despesas que inclui recibos não anexados correspondentes.
- Uma opção adicionada aos relatórios de despesas permite que você crie uma linha de despesas a partir de um recibo ou tente fazer a correspondência de um recibo existente com uma linha de despesas existente.

Para obter mais informações sobre o recurso Relatórios de despesas reinventados, consulte [Relatórios de despesas reinventados](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Perguntas frequentes

**A Microsoft usa meus dados nos modelos dela?**

Não, a Microsoft criou um modelo geral de aprendizado de máquina para o serviço de processamento de recibos. Este modelo não se baseia nos recibos carregados.

**Onde este recurso está disponível e é processado?**

Atualmente, há suporte para os Estados Unidos.

**Para onde vão meus recibos?**

O departamento de finanças entrará em contato com Serviços Cognitivos para extrair dados do campo. Os Serviços Cognitivos manterão uma cópia do seu recibo por até 24 horas durante o processamento. Após a conclusão do processamento, os Serviços Cognitivos removerão o recibo. Os recibos ainda estão armazenados em Finanças.

Para obter mais informações, consulte [Habilite a compreensão do recibo com o novo recurso de Reconhecimento de Formulários](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]