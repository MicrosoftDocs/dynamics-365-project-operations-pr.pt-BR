---
title: Configurar materiais não estocados e faturas de fornecedor pendentes
description: Este tópico explica como habilitar materiais não estocados e faturas de fornecedor pendentes.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a84245a246f49ab69466aba0fec332f0489eec6c
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880619"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Configurar materiais não estocados e faturas de fornecedor pendentes

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

## <a name="minimum-version-requirement"></a>Requisição de versão mínima

O uso de materiais não estocados e faturas de fornecedores pendentes para cenários não estocados/baseados em recursos do Dynamics 365 Project Operations exige as seguintes versões:

Soluções do Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 ou superior
- Solução de orquestração de aplicativo de gravação dupla - 2.2.2.23 ou superior

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) ou superior. Verifique se o ambiente do Finance está atualizado e se todas as atualizações de qualidade são aplicadas para atender aos requisitos mínimos de versão.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Execute mapas de gravação dupla para materiais não estocados e integração de fatura do fornecedor

Esta seção fornece informações sobre os mapas específicos necessários para materiais não estocados e faturas de fornecedores. Verifique se os mapas de pré-requisitos listados no tópico [Provisione um novo ambiente](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) estão em execução em seu ambiente.

1. Acesse Lifecycle Services (LCS), navegue até o projeto LCS e acesse a página **Detalhes do ambiente**.
2. Na seção **Informações de ambiente do Common Data Service**, selecione **Link para CDS para Aplicativos**. Depois de selecionar o link, você será redirecionado para a lista de entidades nos mapeamentos.
3. Verifique se os mapas a seguir estão em execução. Se eles não estiverem em execução, inicie-os e inclua todos os mapas de tabela relacionados.

    - O CDS lançou produtos distintos (produtos)
    - Fornecedores v2 (msdyn_vendors)
    - Tabela do Project Operations para estimativas de material (msdyn_estimatelines)
    - Entidade de exportação de fatura de fornecedor do projeto de integração do Project Operations (msdyn_projectvendorinvoices)
    - Entidade de exportação de linha de fatura de fornecedor do projeto de integração do Project Operations (msdyn_projectvendorinvoicelines)
    - Dados reais da integração do Project Operations (msdyn_actuals). Verifique se você está executando a versão do mapa 1.0.0.14 ou superior. É possível ver a versão ativa do mapa na coluna **Versão** na página **Gravação Dupla**. Você pode ativar uma nova versão do mapa selecionando **Versão do mapa de tabela** e salvando a versão selecionada.

Se você estiver usando dados de demonstração padrão, talvez também precise parar e reiniciar os seguintes mapas de entidade com a sincronização inicial:
  - Dias de pagamento CDS V2 (msdyn_paymentdays)
  - Agenda de pagamentos (msdyn_paymentschedules)
  - Condições de pagamento (msdyn_paymentterms)
  - Grupos de fornecedores (msdyn_vendorgroups)
  - Unidades (uom)

> [!NOTE]
> A sincronização inicial para grupos e unidades de fornecedores pode falhar para alguns registros no conjunto de dados de demonstração existente. Você pode ignorar as falhas, pois elas não o impedirão de usar dados de demonstração com o Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Configurar pré-requisitos no Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Ative o fluxo de trabalho para criar contas com base na entidade do fornecedor

A solução Dual Write Orchestration fornece [Integração mestre de fornecedores](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Como pré-requisito para este recurso, os dados do fornecedor devem ser criados na entidade **Contas**. Ative um processo de fluxo de trabalho de modelo para criar fornecedores na tabela **Contas**, conforme descrito em [Alternar entre designs de fornecedores](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch#use-the-extended-vendor-design-for-vendors-of-the-organization-type).

### <a name="set-products-to-be-created-as-active"></a>Definir produtos a serem criados como ativos

Os materiais não estocados devem ser configurados como **Produtos liberados** no Finance. A solução Dual Write Orchestration oferece uma [Integração pronta para o uso de produtos liberados para o catálogo de produtos do Dataverse](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Por padrão, os produtos do Finance são sincronizados para o Dataverse em estado de rascunho. Para sincronizar o produto para um estado ativo para que possa ser usado diretamente em documentos de uso de material ou faturas de fornecedores pendentes, acesse **Sistema** > **Administração** > **Administração do sistema** > **Configurações do sistema** e, na guia **Vendas**, defina **Criar produtos no estado ativo** como **Sim**.

## <a name="configure-prerequisites-in-finance"></a>Configurar pré-requisitos no Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Habilite a chave do recurso para faturas de fornecedores pendentes

Conclua as etapas a seguir para habilitar a funcionalidade de adicionar detalhes do projeto em linhas de fatura de fornecedores pendentes.

1. No Finance, acesse o espaço de trabalho **Gerenciamento de Recursos**.
2. Na lista de recursos, encontre o recurso **Habilite faturas de fornecedores pendentes no Project Operations para cenários baseados em recursos/não estocados** e selecione **Habilitar**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definir grupos de categorias e categorias de projetos para itens

Configure pelo menos um grupo de categorias para o tipo de transação **Item** e pelo menos uma categoria de projeto usando este grupo. Para obter mais informações, consulte [Configurar categorias de projeto](../project-accounting/configure-project-categories.md#category-groups).

Revise os perfis de custo e receita do projeto e configure a configuração de lançamento contábil para transações de itens. Para obter mais informações, consulte [Configure a contabilidade para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Configurar um produto fora do catálogo

No Project Operations, você pode registrar estimativas de material e uso para produtos do catálogo que estão configurados no catálogo de produtos liberados e para produtos fora do catálogo. O uso de produtos fora do catálogo exige um único produto liberado que seja configurado no Finance para essa finalidade. Conclua as etapas a seguir para configurar um produto fora do catálogo. Repita essas etapas em cada entidade legal que está usando o Project Operations para cenários de recursos/sem estoque.

1. No Finance, acesse **Gerenciamento de informações do produto** > **Produtos** > **Produtos liberados** e selecione **Novo**.
2. No campo **Tipo de produto**, selecione **Item**; no campo **Subtipo de produto**, selecione **Produto**.
3. Insira o número do produto (WRITEIN) e o nome do produto (Produto Fora do Catálogo).
4. Selecione o grupo de modelos de itens. Verifique se o grupo de modelos de itens que você selecionou tem o campo **Política de estoque - Produto em estoque** definido como **Falso**.
5. Selecione valores nos campos **Grupo de itens**, **Grupo de dimensão de armazenamento** e **Grupo de dimensão de rastreamento**. Use **Dimensão de armazenamento** apenas para **Local** e não defina dimensões de acompanhamento.
6. Selecione valores nos campos **Unidade de estoque**, **Unidade de compra** e **Unidade de vendas**. Em seguida, salve as alterações.
7. Na guia **Plano**, defina as configurações de ordem padrão e no guia **Estoque**, defina o site e o depósito padrão.
8. Acesse **Gerenciamento e contabilidade de projetos** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto** e abra **Project Operations no Dynamics 365 Dataverse**. 
9. Na guia **Materiais**, no campo **Produto fora do catálogo**, selecione o produto que você criou.
10. Na ambiente Dataverse, no mapa do site, abra a entidade **Produtos** e encontre o registro do produto fora do catálogo. 
11. Abra os detalhes do registro e defina o estado do produto como **Aposentado**. Este estado do produto evita que alguém acidentalmente use este registro diretamente em estimativas de material e documentos de uso.

### <a name="set-up-a-procurement-integration-account"></a>Configure uma conta de integração de compras

A conta de integração de compras é usada como conta de compensação ao lançar uma fatura de fornecedores pendentes com linhas atribuídas a um projeto.

Quando o sistema posta uma fatura de fornecedor pendente, esta conta é usada para o valor de custo do projeto. Os detalhes da fatura do fornecedor são processados no Dataverse e um projeto real correspondente é criado. As informações do projeto real são adicionadas ao diário de integração do Project Operations. Quando você posta o diário de integração, o valor é compensado da conta de integração de compras e registrado no custo do projeto.

1. Para configurar a conta de integração de compras, acesse **Gerenciamento e contabilidade de projetos** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto** e abra **Project Operations no Dynamics 365 Dataverse**. 
2. Selecione a guia **Materiais** e selecione um valor no campo **Conta de integração de compras**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Configurar padrões de categoria de projeto para um item

1. No Finance, acesse **Gerenciamento e contabilidade de projetos** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto** e abra **Project Operations no Dynamics 365 Dataverse**. 
2. Na guia **Padrões de categoria de projeto**, no campo **Item**, selecione um valor. Esta categoria de projeto será usada para transações de material se a categoria do projeto não tiver sido definida no registro de dados reais do projeto.
