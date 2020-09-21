---
title: Configurar faturamento intercompanhia de projetos
description: Este tópico mostra como configurar o faturamento de projetos entre duas empresas em sua organização.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: 72d6c257-f2d3-483b-8ff2-445263796963
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b199c85736f6268bc5914fddaa10e4cabd44ef1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749033"
---
# <a name="configure-intercompany-project-invoicing"></a>Configurar faturamento intercompanhia de projetos

[!include [task guide banner](../../includes/task-guide-banner.md)]

Este tópico mostra como configurar o faturamento de projetos entre duas empresas em sua organização. Esta tarefa usa o conjunto de dados USSI.

1. No painel de navegação, acesse **Módulos > Contas a pagar > Fornecedores > Todos os fornecedores**.
2. Na lista **Todos os fornecedores**, encontre e selecione o registro desejado.
3. No Painel de Ações, selecione **Geral**.
4. Selecione **Intercompanhia**.
5. Defina **Ativo** como **Sim** para habilitar o comércio intercompanhia.
6. No campo **Empresa do cliente**, insira ou selecione um valor.
7. No campo **Minha conta**, insira ou selecione um valor.
8. Selecione **Salvar**.
9. Feche as páginas para retornar à home page.
10. No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Parâmetros de gerenciamento e contabilidade de projeto**.
11. Selecione a guia **Intercompanhia**.
12. Mova o controle deslizante para **Sim** para habilitar o agendamento e as folhas de ponto dos recursos.
13. Na lista, marque a linha selecionada.
14. Selecione **Novo**.
15. No campo **Entidade legal que toma o empréstimo**, insira ou selecione um valor.
16. Marque a caixa de seleção **Acumular receita**.
17. No campo **Categoria de folha de ponto padrão**, insira ou selecione um valor.
18. No campo **Categoria de despesa padrão**, insira ou selecione um valor.
19. Selecione **Salvar**.
20. Feche a página.
21. No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Lançamento > Configuração de lançamento contábil**.
22. No campo **Tipos de conta contábil**, insira ou selecione um valor.
23. Selecione **Novo**.
24. No campo **Conta principal** da nova linha, especifique os valores desejados.
25. Selecione **Salvar**.
26. Feche a página.
27. No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de transferência**.
28. Selecione **Novo**.
29. No campo **Data de efetivação**, insira uma data.
30. No campo **Entidade legal que toma o empréstimo**, insira ou selecione um valor.
31. No campo **Modelo de preço de transferência**, insira ou selecione um valor.
32. No campo **Preço**, insira um número.
33. Selecione **Salvar**.

