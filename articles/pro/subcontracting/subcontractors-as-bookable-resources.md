---
title: Configurar subcontratados como recursos reserváveis
description: Este tópico explica como configurar e manter recursos de subcontratados criados a partir de usuários e contatos no sistema, para que possam ser associados a subcontratos no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6d2f250063afc24de99e308d8d7583d1822bcabb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597232"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Configurar subcontratados como recursos reserváveis

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Siga estas etapas para configurar subcontratados como recursos reserváveis no Microsoft Dynamics 365 Project Operations.

1. Vá para **Projeto** \> **Recursos** e selecione **Novo**.
2. Na página **Novo Recurso Reservável**, no campo **Tipo de Recurso**, selecione uma das seguintes opções:

    - **Usuário** – Selecione este tipo de recurso se o subcontratado precisa acessar o Project Operations para inserir horas ou despesas. Se você selecionar **Usuário**, o subcontratado precisará de uma licença válida para acessar o sistema.
    - **Contato** ou **Conta** – Selecione um desses tipos de recursos se o subcontratado não precisa de acesso ao Project Operations, mas deve estar disponível para atribuições de tarefas ou reservas em projetos. Nenhum desses tipos de recursos fornece acesso ao sistema. Selecione **Conta** para representar a empresa do fornecedor como um recurso reservável. Selecione **Contato** para representar os funcionários individuais do fornecedor.

3. Dependendo do tipo de recurso selecionado, será solicitado que você selecione o usuário, a conta ou o registro do contato correspondente.
4. No campo **Tipo de Trabalhador**, selecione o "Trabalhador do contrato" para configurar o subcontratado como um recurso reservável.

    > [!NOTE]
    > Se você deixar o campo **Tipo de Trabalhador** em branco, o recurso reservável será considerado um funcionário.

5. Se você selecionou **Trabalhador do Contrato** como o tipo de trabalhador, selecione o fornecedor para o qual o recurso trabalha.
6. Escolha o fuso horário do recurso e selecione **Salvar**. Para atribuir um modelo de horas de trabalho ao recurso reservável, selecione **Definir calendário** na página da lista **Recurso Reservável**.

Para ser associado a uma linha de subcontrato, um recurso reservável deve atender às seguintes condições:

- O recurso reservável deve ser um trabalhador do contrato.
- Um recurso reservável do tipo **Contato** deve ser associado à conta do fornecedor como um contato. Um recurso reservável do tipo **Usuário** não deve ser associado à conta do fornecedor como um contato.
- O valor do campo **Fornecedor** para o recurso reservável deve corresponder ao valor do campo **Fornecedor** para o subcontrato.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Atualizar o tipo de mapeamento de trabalhador e fornecedor para recursos reserváveis

O campo **Tipo de trabalhador** para um recurso reservável determina se o recurso reservável é um trabalhador do contrato ou um funcionário. O campo **Fornecedor** define a conta do fornecedor à qual o recurso reservável está associado. Ao associar um recurso reservável a um fornecedor como contato, você indica que o contato é um funcionário da empresa do fornecedor.

Se os campos **Tipo de Trabalhador** e **Fornecedor** para um recurso reservável forem alterados, as alterações afetarão todas as validações futuras em novos registros que o recurso reservável criar, como entradas de hora. No entanto, as alterações não invalidam os registros existentes.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
