---
title: Definir um modelo padrão
description: Definir um modelo padrão
author: dansimp
ms.assetid: 07208b6b-cb3a-4f6c-9c84-36d4dc1486d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51a13c2c57e38adca883a6eb962d8c5eae4316db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797684"
---
# Definir um modelo padrão


Como um editor, você pode especificar quais dos modelos disponíveis serão o modelo padrão sugerido para todos os administradores de política de grupo criando novos objetos de política de grupo (GPOs).

**Observação**  Um modelo é uma versão não editável e estática de um GPO para uso como um ponto de partida para a criação de GPOs novos e editáveis.

 

Uma conta de usuário com a função de editor ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para definir o modelo padrão a ser usado ao criar novos GPOs**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia **modelos** para exibir os modelos disponíveis.

3.  Clique com o botão direito do mouse no modelo que deseja definir como padrão e, em seguida, clique em **definir como padrão**.

4.  Clique em **Sim** para confirmar.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O modelo padrão tem um ícone azul e o estado é identificado como **modelo (padrão)** na guia **modelos** .

### Considerações adicionais

-   Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter **conteúdo de lista** e criar permissões de **modelo** para o domínio.

-   Depois de definir um modelo como padrão, esse modelo será o primeiro selecionado na caixa de diálogo **novo GPO controlado** quando os administradores de política de grupo criarem novos GPOs. No entanto, eles terão a opção de selecionar qualquer outro modelo de GPO, incluindo ** &lt; GPO &gt; vazio**, que não inclui configurações.

-   Renomear ou excluir um modelo não afeta os GPOs criados a partir desse modelo.

-   Como não pode ser alterado, um modelo não tem um histórico.

### Referências adicionais

-   [Criação de um modelo e ajuste de um modelo padrão](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [Solicitar a criação de um novo GPO controlado](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 





