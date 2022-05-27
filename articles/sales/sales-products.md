---
title: Produtos
description: Este tópico fornece informações sobre o catálogo de produtos que você pode usar para fornecer informações aos clientes sobre os produtos e preços que sua organização oferece.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 5c57b2596e1d480ff59591618f073ceb8f70a289
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574080"
---
# <a name="products"></a>Produtos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Produtos são a espinha dorsal da sua empresa. O catálogo de produtos no Dynamics 365 Sales Professional é uma coleção de produtos e as informações de preço. Facilita para os representantes de vendas aumentar suas vendas criando um catálogo de produtos rapidamente.

## <a name="add-a-product"></a>Adicionar um produto

1.  Verifique se você tem a função de gerente do Sales Professional ou administrador do sistema para poder adicionar produtos no Dynamics 365 Sales Professional.
2.  No mapa do site, em **Configuração**, selecione **Produtos**.
3.  Selecione **Adicionar Produto** e preencha as seguintes informações:

    -  **Nome**
    -  **ID do Produto (Product ID)**
    -  **Pai**: selecione uma família de produtos principal para o produto. Se estiver criando um produto secundário em uma família de produtos, o nome da família do produto principal é preenchido. Isso pode ser alterado depois que o registro for salvo.
    -  **Válido de**/**Válido até**: defina o período para o qual o produto é válido, selecionando uma data **Válido de** e **Válido até**.
    -  **Grupo de unidades**: Selecione um grupo de unidades. Um grupo de unidade é uma coleção de várias unidades na qual um produto é vendido e define como itens individuais são agrupados em quantidades maiores. Por exemplo, se você estiver adicionando sementes como um produto, você pode ter criado um grupo de unidades chamado “Sementes” e definido sua unidade principal como "pacote".
    -  **Unidade Padrão**: selecione a unidade mais comum na qual o produto será vendido. As unidades são as quantidades ou as medidas em que você vende seus produtos. Por exemplo, se adicionou sementes como um produto, você poderá vendê-las em pacotes, caixas ou paletes. Cada uma delas se torna uma unidade de produtos. Se as sementes forem vendidas na maior parte em pacotes, selecione isso como a unidade.
    -  **Lista de Preços Padrão**: se este for um produto novo, o campo será somente leitura. Antes de selecionar uma lista de preços padrão, preencha todos os campos obrigatórios e salve o registro. Embora a lista de preços padrão não seja necessária, é interessante definir uma lista de preços padrão para cada produto quando o registro do produto é salvo. Assim, se um registro de cliente não contiver uma lista de preços, o Sales poderá usar a lista de preços padrão para gerar cotações, pedidos e faturas.
    -  **Decimais Compatíveis**: insira um número inteiro entre 0 e 5. Se não for possível dividir o produto em quantidades fracionais, digite 0. A precisão do campo **Quantidade** no registro de cotação, pedido ou fatura do produto é validada em relação ao valor desse campo, caso o produto não tenha uma lista de preços associada.
    -  **Assunto**: associe este produto a um assunto. Você pode usar assuntos para categorizar seus produtos e filtrar relatórios.

4.  Selecione **Salvar**.
5.  Na guia **Detalhes Adicionais**, na seção **Itens da Lista de Preços**, selecione **Mais comandos** e, em seguida, selecione **Adicionar Novo Item da Lista de Preços**.
7.  Na guia **Detalhes Adicionais**, na seção **Relacionamento de Produto**, selecione o ícone **Mais comandos** e, em seguida, selecione **Adicionar Novo Relacionamento de Produto**.
8.  No formulário **Novo Relacionamento de Produto**, insira os seguintes detalhes e, na barra de comandos, selecione **Salvar e Fechar**:

    -   **Produto Relacionado**: selecione um produto que você deseja adicionar como um produto relacionado ao registro de produto existente no qual está trabalhando.
    -   **Tipo de Relacionamento de Vendas**: selecione se você deseja adicionar o produto como venda suplementar, venda cruzada, acessório ou produto substituto.
    -   **Direção**: selecione se o relacionamento entre os produtos será bidirecional ou unidirecional. Quando você seleciona Unidirecional, o produto selecionado em **Produtos Relacionados** será mostrado como uma recomendação para o produto existente, mas não vice-versa.

9.  No formulário Produto, selecione **Salvar**.

## <a name="import-products"></a>Importar produtos

Você pode usar modelos de importação para trazer dados de produtos em massa para o Dynamics 365 Sales.

## <a name="revise-a-product"></a>Revisar um produto

Mantenha o inventário do produto atualizado revisando rapidamente as propriedades de produtos conforme necessário e republicando as informações de forma que os agentes de vendas possam ver as alterações mais recentes do inventário.

1.  Certifique-se de ter um dos seguintes direitos de acesso ou permissões equivalentes: Administrador do Sistema, Personalizador de Sistema, Gerente de Vendas, Vice-presidente de Vendas, Vice-presidente de Marketing ou Diretor Executivo – Gerente Comercial.
2.  No mapa do site, selecione **Produtos**.
3.  Abra um produto ativo que deseja alterar e, na barra de comandos, selecione **Revisar**.
4.  Na caixa de diálogo **Confirmar Revisão**, selecione **Confirmar**. Isso altera o status do produto para **Sob Revisão**.
5.  Depois que você terminar de fazer alterações, na barra de comandos, selecione **Publicar**.

    > [!TIP]
    > Para reverter as alterações e continuar com a última versão ativa do produto, selecione **Reverter**. Isso altera o status do produto de volta para **Ativo**.

## <a name="clone-a-product"></a>Clonar um produto 

Ao criar um novo produto, ganhe tempo clonando um existente. Isso cria uma cópia do registro original com todos os detalhes exceto o nome e a ID.

1.  Certifique-se de ter um dos seguintes direitos de acesso ou permissões equivalentes: Administrador do Sistema, Personalizador de Sistema, Gerente de Vendas, Vice-presidente de Vendas, Vice-presidente de Marketing ou Diretor Executivo – Gerente Comercial.
2.  No mapa do site, selecione **Produtos**.
3.  Selecione um registro do produto que você deseja clonar e, na barra de comandos, clique em **Clonar**. Uma caixa de diálogo de confirmação é exibida.
4.  Selecione **Confirmar**.

Um novo registro do produto abrirá com os mesmos detalhes que o original, exceto nome e ID.

## <a name="retire-a-product"></a>Aposentar um produto 

Se a sua organização não vende mais um produto, aposente-o de forma que o produto não esteja mais disponível para os agentes de vendas.

1.  Certifique-se de que você tenha a função de administrador do sistema ou gerente do Sales Professional ou permissões equivalentes.
2.  No mapa do site, selecione **Produtos**.
3.  Abra um produto ativo que deseja desativar e, na barra de comandos, selecione **Desativar**.
4.  Na caixa de diálogo **Confirmar Desativação**, selecione **Confirmar**.


## <a name="delete-a-product"></a>Excluir um produto

Para parar de vender um produto, exclua-o.

> [!IMPORTANT]
> Você não pode recuperar um registro excluído.

1.  Certifique-se de que você tenha a função de administrador do sistema ou gerente do Sales Professional ou permissões equivalentes.
2.  No mapa do site, selecione **Produtos**.
3.  Selecione um registro do produto que você deseja excluir e, na barra de comandos, clique em **Excluir**.
4.  Na caixa de diálogo **Confirmar Exclusão**, selecione **Continuar**.
 
 ## <a name="quantity-factors-for-products"></a>Fatores de quantidade para produtos

Os fatores de quantidade oferecem suporte à venda de produtos baseados em assinatura. Para produtos baseados em assinatura, a quantidade na linha de contrato do projeto ou da cotação é expressada como o número de meses do usuário.

Geralmente, o preço do software por assinatura é armazenado no catálogo como o preço mensal por usuário. No entanto, você pode usar outras descrições de tempo. Durante o processo de vendas, o preço na linha de cotação normalmente é o preço mensal por usuário que foi negociado e descontado pelo agente de vendas de TI. Cada negociação tem um número diferente de usuários e um número diferente de meses de assinatura. A quantidade usada para calcular o valor da linha de cotação é um produto do número de usuários e do número de meses de assinatura.

Os fatores de quantidade dependem dos atributos de produto. Quando você configura propriedades específicas para um produto, é possível sinalizar um subconjunto dessas propriedades, ou todas as propriedades, como fatores de quantidade.

O sistema valida que apenas propriedades numéricas ou propriedades de produto que tenham um tipo de dados numérico sejam sinalizadas como fatores de quantidade. Quando um produto para o qual os fatores de quantidade são configurados é adicionado a uma linha de cotação,o campo **Quantidade** na linha de cotação se torna um campo somente leitura. Depois que você insere valores para propriedades do produto que são fatores de quantidade, a quantidade da linha de cotação é calculada.

Por exemplo, se houver as seguintes propriedades: 

- **Número de Usuários**: o número de usuários 
- **Número de Meses**: o número de meses de assinatura
- **SKU do Produto** 

As propriedades **Número de Usuários** e **Número de Meses** podem ser sinalizadas como fatores de quantidade editando as propriedades da linha de produtos. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]