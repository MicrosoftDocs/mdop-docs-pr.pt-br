---
title: Como fazer upgrade de um aplicativo virtual existente
description: Como fazer upgrade de um aplicativo virtual existente
author: dansimp
ms.assetid: ec531576-2423-4c2c-9b9f-da74174a6858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 71fb096c103a0bcb9913d4eea33b1259a33a54ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796927"
---
# Como fazer upgrade de um aplicativo virtual existente


Você pode atualizar um aplicativo virtual existente para uma nova versão usando o sequenciador Application Virtualization (App-V). O processo de atualização é semelhante à criação de um novo aplicativo virtual. Você deve abrir o aplicativo virtual existente para uma atualização, fazer as atualizações necessárias e, em seguida, salvar o aplicativo virtual atualizado em um novo local no diretório raiz do pacote.

Você também pode usar o console do App-V Sequencer para fazer alterações em um aplicativo virtual existente sem realizar uma atualização. No entanto, você não pode fazer modificações no sistema de arquivos do aplicativo virtual usando esse método, pois o sequenciador do App-V não decodifica o arquivo. sft associado. Por exemplo; Você pode abrir um aplicativo virtual existente no console do sequenciador App-V selecionando **abrir** no menu **arquivo** . Você pode atualizar o **nome do pacote** e os **comentários**associados, e pode fazer alterações no sistema de arquivos virtual e no registro virtual. Você também pode criar um arquivo do Windows Installer.

Use o procedimento a seguir para atualizar um aplicativo virtual existente.

**Para atualizar um aplicativo virtual existente**

1.  Para iniciar o console do App-v Sequencer, no computador que executa o sequenciador app-v, selecione **Iniciar** / **programas** / **Microsoft Application**Virtualization / **Sequencer Virtualization**.

2.  Para abrir o aplicativo virtual existente, no console App-V, selecione **arquivo** / **abrir para atualização do pacote**. Use a caixa de diálogo **abrir para atualização de pacote** para localizar o arquivo SPRJ associado que você deseja abrir para atualização.

3.  Para especificar o local de onde o pacote será decodificado, clique em **Procurar pasta** e especifique o Q:\\. Esse é o local onde o diretório raiz do pacote será criado conforme especificado no arquivo SFT associado. Quando você cria a versão atualizada do pacote, ela será indicada com uma adição sequencial ao nome do diretório, por exemplo, "**1**a" será adicionada ao nome do diretório localizado na unidade Q:\\.

4.  Para abrir o assistente de sequenciamento, **Tools**selecione / **Assistente de sequenciamento**de ferramentas. Na página **informações do pacote** , opcionalmente, especifique o novo **nome do pacote** e adicione comentários opcionais que serão associados ao aplicativo virtual atualizado. Clique em **Avançar**.

5.  Na página **monitorar instalação** , para começar a monitorar a nova instalação, clique em **Iniciar Monitoramento**. Depois que o ambiente virtual terminar de carregar, instale a versão atualizada do aplicativo ou aplique atualizações ao aplicativo existente. Após concluir a atualização do aplicativo virtual, clique em **parar monitoramento**e em **Avançar**.

6.  Nos **arquivos adicionais a serem mapeados para a página do sistema de arquivos virtual (VFS)** , para especificar arquivos adicionais a serem adicionados ao VFS (sistema de arquivos virtual), clique em **Adicionar**. Navegue até o arquivo que você deseja adicionar e clique em **abrir**. Para limpar os arquivos existentes que foram adicionados, clique em **Redefinir**e, em seguida, clique em **Avançar**.

7.  Na página **configurar aplicativos** , configure os atalhos e associações de tipo de arquivo que serão associados ao aplicativo virtual atualizado. Selecione o elemento que você deseja atualizar e, em seguida, clique em **Editar locais**. Especifique as configurações na caixa de diálogo **locais do atalho** e, em seguida, clique em **Avançar**.

8.  Na página **iniciar aplicativos** , para iniciar o aplicativo e garantir que o pacote seja otimizado para streaming, selecione o pacote e clique em **Iniciar**. Esta etapa é útil para configurar como o aplicativo é executado inicialmente em computadores de destino e para aceitar qualquer contrato de licença associado antes de o pacote ser disponibilizado para os clientes. Se houver vários aplicativos associados a este pacote, você poderá selecionar **Iniciar tudo** para abrir todos os aplicativos. Para sequenciar a nova versão do aplicativo virtual, clique em **Avançar**.

9.  Para concluir e fechar o assistente de sequenciamento, na página **pacote de sequência** , clique em **concluir**.

10. Depois de atualizar com êxito o aplicativo virtual, para salvar o pacote, no console do App-V Sequencer, no menu **arquivo** , selecione **salvar**. O aplicativo virtual pode ser acessado no diretório especificado na etapa 3.

## Tópicos relacionados


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[Como fazer upgrade de um aplicativo virtual usando a linha de comando](how-to-upgrade-a-virtual-application-by-using-the-command-line.md)

 

 





