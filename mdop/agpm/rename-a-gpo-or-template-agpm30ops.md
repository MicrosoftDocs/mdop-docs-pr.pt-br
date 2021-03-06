---
title: Renomear um GPO ou modelo
description: Renomear um GPO ou modelo
author: dansimp
ms.assetid: 19d17ddf-8b58-4677-929e-9550fa388b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44d1cef33d8c0004ef3639311fbf135b4dea9d39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797341"
---
# Renomear um GPO ou modelo


Você pode renomear um objeto de política de grupo (GPO) controlado ou um modelo.

Uma conta de usuário com a função de editor ou administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo (AGPM) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para renomear um GPO ou um modelo**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **controlado** ou **modelos** para exibir o item a ser renomeado.

3.  Clique com o botão direito no GPO ou no modelo para renomear e clique em **renomear**.

4.  Digite o novo nome para o GPO ou modelo e um comentário e, em seguida, clique em **OK**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO ou modelo aparece sob o novo nome na guia **conteúdo** .

### Considerações adicionais

-   Por padrão, você deve ser o aprovador que criou ou controlado o GPO, um editor ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter a permissão **listar conteúdo** e **Editar configurações** para o GPO.

-   Quando você renomeia um GPO que foi implantado, o nome é alterado imediatamente no arquivo morto. O nome é alterado no ambiente de produção apenas quando o GPO é reimplantado. Até que o GPO seja reimplantado (ou que a cópia de produção seja excluída), o nome antigo ainda está em uso no ambiente de produção e, portanto, não pode ser usado para outro GPO. Da mesma forma, o GPO no arquivo não pode ser renomeado para seu nome original até que o GPO tenha sido implantado (alterando o nome da cópia de produção) ou que a cópia de produção tenha sido excluída.

### Referências adicionais

-   [Editando um GPO](editing-a-gpo-agpm30ops.md)

 

 





