---
title: O que há de novo em julho de 2021 - Implantação lite do Project Operations
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de julho de 2021 da implantação lite do Project Operations.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8cff4c37e1c2df29041ef86cdcf05afa6093f890565a855024202e87fd533ea5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009202"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>O que há de novo em julho de 2021 - Implantação lite do Project Operations

_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations na versão 4.12.0.148 ou 4.12.0.152 do ambiente do Dataverse.

## <a name="quality-updates"></a>Atualizações de qualidade
| **Área do recurso**              | **Número de referência** | **Atualização de qualidade**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cobrança e preço           | 2224046              | O campo **Classe de Transação** é editável na guia **Detalhes da Linha de Cotação**, mas fica bloqueado se você estiver trabalhando usando a página **Detalhes da Linha de Cotação**.                                                                     |
| Cobrança e preço           | 2224400              | A ação **Fechar Cotação como Ganha** falha quando uma cotação não tem marcos de data.                                                                                                                                    |
| Cobrança e preço           | 2234089              | Quando você insere manualmente uma descrição de produto, ela é removida depois que você insere uma quantidade para uma estimativa de material.                                                                                                                         |
| Cobrança e preço           | 2234100              | A grade **Configuração de Cobrança da Tarefa** não inclui a coluna **Material** e seu valor na guia **Cobrança da Tarefa** do projeto.                                                                                                       |
| Cobrança e preço           | 2277409              | O ID do produto não está disponível no detalhe da linha do contrato para uma linha de tipo de material.                                                                                                                                        |
| Cobrança e preço           | 2281728              | A criação de uma linha de contrato reavalia desnecessariamente os valores reais, que causam aumentos significativos no volume de dados, o que afeta o desempenho.                                                                                |
| Cobrança e preço           | 2298668              | As linhas do diário associadas a uma despesa recuperada e excluída não serão removidas.                                                                                                                                     |
| Cobrança e preço           | 2300192              | Quando vários usuários estão editando uma fatura, é possível que um novo detalhe da linha da fatura seja criado em uma fatura confirmada.                                                                                   |
| Cobrança e preço           | 2301569              | As faturas não podem ser corrigidas se um \$retentor com valor 0 foi aplicado.                                                                                                                                        |
| Cobrança e preço           | 2307965              | Ocorre um erro, se um preço de categoria for criado com valores ausentes.                                                                                                                           |
| Cobrança e preço           | 2326870              | Ocorre um erro no **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** se **producttypecode** for nulo.                                                                            |
| Cobrança e preço           | 2332732              | Ocorre um erro se um marco de linha de contrato for criado sem uma linha de ordem.                                                                                                                |
| Planejamento e acompanhamento de projeto | 2181094              | A API de Agendamento do Project agora oferece suporte a Logs de PSS e Logs do Conjunto de Operações, que são armazenados durante 90 dias.                                                                                                                  |
| Planejamento e acompanhamento de projeto | 2254201              | O rótulo **Modo de Agendamento** é atualizado com detalhes que descrevem a lógica padrão.                                                                                                                                      |
| Planejamento e acompanhamento de projeto | 2300252              | O cache de resposta do **openProject** é atualizado e inclui o proprietário do token na chave do cache, **Url base** e a **URL do Segmento**, de forma que a **Url de Solicitação** sempre possa ser recriada, se a **Url base** for alterada. |
| Planejamento e acompanhamento de projeto | 2301312              | **msdyn_membershipstatus** foi removido da exibição **Membro da Equipe do Projeto**.                                                                                                                                        |
| Planejamento e acompanhamento de projeto | 2302759              | Os produtos são obtidos desnecessariamente nas guias **Atribuições de Recurso**, **Estimativas** e **Estimativas de Despesas**.                                                                                                        |
| Planejamento e acompanhamento de projeto | 2308050              | **CopyProject** falha com o erro "Falha ao obter o token para falar com o serviço remoto".                                                                                                                           |
| Planejamento e acompanhamento de projeto | 2322650              | A exibição **Lista de Tarefas do Projeto** foi atualizada para exibir a data da tarefa, por padrão.                                                                                                            |
| Planejamento e acompanhamento de projeto | 2327266              | **CopyProject** gera o erro "Chave não encontrada no dicionário" ao copiar as estimativas.                                                                                                      |
| Planejamento e acompanhamento de projeto | 2328123              | **CopyProject** gera o erro "Falha ao obter o token para falar com o serviço remoto".                                                                                                                          |
| Planejamento e acompanhamento de projeto | 2336258              | **CopyProject** copia incorretamente os nomes das posições dos recursos.                                                                                                                                                 |
| Cobrança e preço           | 2224476              | O campo **Recurso Reservável** não é padronizado corretamente para o usuário conectado na página **Uso de Material**.                                                                                                            |
| Gerenciamento de Recursos           | 2277249              | Ocorre um erro quando um requisito de recurso não baseado em projeto é atualizado.                                                                                                            |
| Gerenciamento de Recursos           | 2323869              | A utilização de recursos não reconhece corretamente os recursos filtrados.                                                                                                                                             |
| Tempo e Despesa              | 2176538              | Operadores de filtro incorretos são aplicados ao controle **Entrada de Hora**.                                                                                                                                                   |
| Tempo e Despesa              | 2177462              | A exclusão de uma entrada de hora na grade não atualiza os status dos botões **Enviar**, **Recuperar**, **Excluir** e **Editar Entrada**, conforme o esperado.                                                                                        |
| Tempo e Despesa              | 2299985              | **TimeEntriesImportFromResourceAssignment** não mantém a hora de início/término dos contornos da atribuição.                                                                                                  |
| Tempo e Despesa              | 2318426              | Depois que uma entrada de hora é enviada, os campos bloqueados ainda podem ser editados.                                                                                                                                   |
| Tempo e Despesa              | 2323749              | Ocorre um erro quando uma despesa é criada usando a guia **Relacionado** de um recurso reservável.                                                                                                      |
| Tempo e Despesa              | 2327678              | Quando você cria uma entrada de hora a partir da guia **Relacionado** de um recurso reservável, o recurso pai não é passado para o controle de entrada de hora.                                                                            |
| Geral                       | 2296857              | Rastreamento de progresso para trabalhos de execução prolongada.                                                                                                                                                                        |
| Geral                       | 2253682              | A solução de gravação dupla do Project Operations não deve ser instalada quando a solução principal de gravação dupla é instalado em um ambiente sem a solução de orquestração de gravação dupla.                                                |
| Geral                       | 2316420              | O provisionamento principal do Project service falhará se a unidade de negócios do usuário do aplicativo for alterada.                                                                                                                     |
| Geral                       | 2376405              | Foi corrigido o problema da atualização controlada pelo editor (A atualização de qualidade está disponível na versão 4.12.0.152)                                                                                                                     |
