---
title: Importar um GPO de produção
description: Importar um GPO de produção
author: dansimp
ms.assetid: 35c2a682-ece8-4577-a083-7e3e9facfd13
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3d739a46d5ca078ec9d218c1cc1e5bd258c55601
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797780"
---
# Importar um GPO de produção


Se forem feitas alterações em um objeto de política de grupo (GPO) controlado fora do gerenciamento avançado de política de grupo (AGPM), você poderá importar uma cópia do GPO do ambiente de produção e salvá-la no arquivo para colocar o arquivo morto e o ambiente de produção em um estado consistente. Para importar um GPO não controlado, controle o GPO. Consulte [solicitação de controle de um GPO não controlado](request-control-of-an-uncontrolled-gpo-agpm30ops.md).)

Uma conta de usuário com a função de editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias inexigidamente é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para importar um GPO do ambiente de produção**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Clique com o botão direito do mouse no GPO e, em seguida, clique em **importar da produção**.

4.  Digite um comentário para a faixa de auditoria do GPO e, em seguida, clique em **OK**.

### Considerações adicionais

-   Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter **conteúdo da lista** e **Editar as configurações**, **implantar o GPO**ou excluir permissões de **GPO** para o GPO.

### Referências adicionais

-   [Criação, controle ou importação de um GPO](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 





