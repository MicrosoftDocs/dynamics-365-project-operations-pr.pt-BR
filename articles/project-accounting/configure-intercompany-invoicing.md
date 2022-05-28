---
title: Configurar faturamento intercompanhia
description: Este tópico fornece informações e exemplos sobre como configurar o faturamento intercompanhia de projetos.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ad6022670048e5aa3635998852b78c49af461d4e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591574"
---
# <a name="configure-intercompany-invoicing"></a>Configurar faturamento intercompanhia

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Execute as seguintes etapas para configurar o faturamento intercompanhia de projetos no Dynamics 365 Project Operations. As transações intercompanhia são transações de tempo e despesas de um contrato de projeto que pertence a uma empresa ou unidade organizacional, enquanto os recursos no contrato do projeto fazem parte de uma empresa ou unidade organizacional diferente.

## <a name="example-configure-intercompany-invoicing"></a>Exemplo: configurar faturamento intercompanhia

No exemplo a seguir, a Contoso Robotics USA (USPM) é a entidade legal que toma o empréstimo e a Contoso Robotics UK (GBPM) é a entidade legal que faz o empréstimo. 

1. **Configure a contabilidade intercompanhia entre entidades legais**. Cada par de entidades jurídicas de empréstimo deve ser configurado na página de [Contabilidade intercompanhia](/dynamics365/finance/general-ledger/intercompany-accounting-setup) da Contabilidade.
    
    1. No Dynamics 365 Finance, acesse **Contabilidade** > **Configuração de lançamento** > **Contabilidade intercompanhia**. Crie um registro com as seguintes informações:

        - **Empresa de origem** = **GBPM**
        - **Empresa de destino** = **USPM**

2. **Configure a relação comercial entre entidades legais**. O registro do cliente que representa a entidade que toma o empréstimo deve ser criado na entidade que faz o empréstimo. O registro do fornecedor que representa a entidade que faz o empréstimo deve ser criado na entidade que toma o empréstimo.

     1. No Finance, selecione a entidade legal **GBPM**.
     2. Vá para **Contas a receber** > **Cliente** > **Todos os clientes**. Crie um registro para a entidade legal, **USPM**.
     3. Expanda **Nome**, filtre os registros por **Tipo** e selecione **Entidades legais**. 
     4. Localize e selecione o registro do cliente da **Contoso Robotics USA (USPM)**.
     5. Selecione **Usar correspondência**. 
     6. Selecione o grupo de clientes **50 - Clientes intercompanhia** e salve o registro.
     7. Selecione a entidade legal **USPM**.
     8. Vá para **Contas a pagar** > **Fornecedores** > **Todos os fornecedores**. Crie um registro para a entidade legal, **GBPM**.
     9. Expanda **Nome**, filtre registros por **Tipo** e selecione **Entidades legais**. 
     10. Localize e selecione o registro do cliente da **Contoso Robotics UK (GBPM)**.
     11. Selecione **Usar correspondência**, selecione o grupo de fornecedores e salve o registro.
     12. No registro do fornecedor, selecione **Geral** > **Configuração** > **Intercompanhia**.
     13. Na guia **Relação comercial**, defina **Ativo** como **Sim**.
     14. Defina o campo **Empresa do cliente** como **GBPM** e, em **Meu registro de conta**, selecione o registro do cliente que você criou anteriormente no procedimento.

3. **Defina as configurações intercompanhia em Parâmetros de gerenciamento e contabilidade de projeto**. 

    1. Selecione a entidade legal **USPM** e vá para **Gerenciamento e contabilidade de projeto** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto**.
    2. Na guia **Intercompanhia**, selecione a categoria de compras que será associada às faturas do fornecedor geradas automaticamente.
    3. Em **Categoria padrão**, selecione **Recursos intercompanhia**.
    4. Selecione a entidade legal **GBPM** e vá para **Gerenciamento e contabilidade de projeto** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto**.
    5. Na guia **Intercompanhia**, selecione uma categoria de projeto padrão para cada tipo de transação. As categorias de projeto são usadas para configuração de imposto quando a categoria faturada em transações intercompanhia existe somente na entidade legal que toma o empréstimo. Você pode optar por acumular receita para transações intercompanhia. O acúmulo ocorre quando as transações são lançadas por meio do Diário de integração do Project Operations na entidade legal que faz o empréstimo. O diário é revertido quando a fatura intercompanhia é lançada.
    6. No grupo **Ao emprestar recursos**, selecione **...** > **Novo**. 
    7. Na grade, selecione as informações a seguir:

          - **Entidade legal que toma o empréstimo** = **USPM**
          - **Acumular receita** = **Sim**
          - **Categoria de folha de ponto padrão** = **Padrão – Hora**
          - **Categoria de despesa padrão** = **Padrão – despesa**

4. **Definir contas de custo e de receita intercompanhia na Configuração de lançamento contábil**. A conta de receita intercompanhia é creditada quando a fatura de cliente intercompanhia é lançada na entidade legal que faz o empréstimo. A conta de custo intercompanhia é debitada quando a fatura de fornecedor pendente correspondente é lançada na entidade legal que toma o empréstimo. Essas contas são configuradas nas entidades legais correspondentes. 
      
     1. No Finance, selecione a entidade legal que toma o empréstimo **USPM**. 
     2. Vá para **Gerenciamento e contabilidade de projeto** > **Configuração** > **Lançamento** > **Configuração de lançamento contábil**. 
     3. Na guia **Contas de custo**, no **Tipo de contabilidade**, selecione **Custo intercompanhia**. Crie um registro com as seguintes informações:
      
        - **Entidade legal que faz o empréstimo** = **GBPM**
        - **Conta principal** = Selecione a conta principal de custo intercompanhia. Esta configuração é obrigatória. A configuração é usada para fluxos intercompanhia no Finance, mas não em fluxos intercompanhia relativos a projetos. Esta seleção não tem impacto downstream. 
        
     4. Selecione a entidade legal que faz o empréstimo, **GBPM**. 
     5. Vá para **Gerenciamento e contabilidade de projeto** > **Configuração** > **Lançamento** > **Configuração de lançamento contábil**. 
     6. Na guia **Contas de receita**, no **Tipo de contabilidade**, selecione **Receita intercompanhia**. Crie um registro com as seguintes informações:

        - **Entidade legal que toma o empréstimo** = **USPM**
        - **Conta principal** = Selecione a conta principal de receita intercompanhia. Esta configuração é obrigatória. A configuração é usada para fluxos intercompanhia no Finance, mas não em fluxos intercompanhia relativos a projetos. Esta seleção não tem impacto downstream. 

5. **Configurar preços de transferência para mão de obra**. Os preços de transferência intercompanhia são configurados no Project Operations em Dataverse. Configurar [taxas de custo de mão de obra](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) e [taxas de cobrança de mão de obra](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) para faturamento intercompanhia. O preço de transferência não é compatível com transações de despesas intercompanhia. O preço de venda da unidade interorganizacional sempre será definido com o mesmo valor que o preço de custo da unidade de recursos.

      O custo do recurso do desenvolvedor na Contoso Robotics UK é de 88 GBP por hora. A Contoso Robotics UK cobrará da Contoso Robotics USA 120 USD por hora trabalhada por esse recurso em projetos nos EUA. A Contoso Robotics USA cobrará do cliente Adventure Works 200 USD pelo trabalho realizado pelo recurso de desenvolvedor da Contoso Robotics UK.

      1. Em Project Operations no Dataverse, vá para **Venda** > **Listas de preços**. Crie uma lista de preços de custo denominada **Taxas de custo da Contoso Robotics UK**. 
      2. Na lista de preços de custo, crie um registro com as seguintes informações:
         - **Função** = **Desenvolvedor**
         - **Custo** = **88 GBP**
      3. Vá para **Configurações** > **Unidades organizacionais** e anexe essa lista de preços de custo à unidade organizacional **Contoso Robotics UK**.
      4. Vá para **Vendas** > **Listas de preços**. Crie uma lista de preços de custo denominada **Taxas de custo da Contoso Robotics USA**. 
      5. Na lista de preços de custo, crie um registro com as seguintes informações:
          - **Função** = **Desenvolvedor**
          - **Empresa de recursos** = **Contoso Robotics UK**
          - **Custo** = **120 USD**
      6. Vá para **Configurações** > **Unidades organizacionais** e anexe a lista de preços de custo das **taxas de custo da Contoso Robotics USA** à unidade organizacional **Contoso Robotics USA**.
      7. Vá para **Vendas** > **Listas de preços**. Crie uma lista de preços de vendas denominada **Taxas de fatura do Adventure Works**. 
      8. Na lista de preços de venda, crie um registro com as seguintes informações:
          - **Função** = **Desenvolvedor**
          - **Empresa de recursos** = **Contoso Robotics UK**
          - **Taxa de cobrança** = **200 USD**
      9. Vá para **Vendas** > **Contratos de projeto** e anexe a lista de preços das **Taxas de cobrança do Adventure Works** à lista de preços do projeto Adventure Works do contrato do projeto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
