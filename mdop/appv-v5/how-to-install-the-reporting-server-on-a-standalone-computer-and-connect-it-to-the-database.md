---
title: Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados
description: Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados
author: dansimp
ms.assetid: d186bdb7-e522-4124-bc6d-7d5a41ba8266
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f20f1ce16c3f0168d1c797efd816d4125c0f1f53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796386"
---
# Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados


Use o procedimento a seguir para instalar o servidor de relatório em um computador autônomo e conectá-lo ao banco de dados.

**Importante**  
Antes de executar o procedimento a seguir, você deve ler e entender [sobre relatórios do App-V 5,0](about-app-v-50-reporting.md).



**Para instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados**

1.  Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo. Para iniciar a instalação do App-V 5,0 Server, clique com o botão direito do mouse e execute **appv\_server\_setup.exe** como administrador. Clique em **Instalar**.

2.  Na página de **introdução** , examine e aceite os termos de licença e clique em **Avançar**.

3.  Na página **usar o Microsoft Update para ajudar a manter seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).** Para desabilitar o Microsoft Updates, selecione **não quero usar o Microsoft Update**. Clique em **Avançar**.

4.  Na página **seleção de recursos** , marque a caixa de seleção **servidor de relatório** e clique em **Avançar**.

5.  Na página **local de instalação** , aceite o local padrão e clique em **Avançar**.

6.  Na página **configurar banco de dados de relatórios existente** , selecione **usar um SQL Server remoto**e digite o nome do computador que executa o Microsoft SQL Server, por exemplo, **SqlServerMachine**.

    **Observação**  
    Se o Microsoft SQL Server estiver implantado no mesmo servidor, selecione **usar SQL Server local**.



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.
~~~

7. Na página **Configurar servidor de relatórios** .

   -   Especifique o nome do site que você deseja usar para o serviço de relatório. Deixe o padrão inalterado se você não tiver um nome personalizado.

   -   Para a **Associação de portabilidade**, especifique um número de porta exclusivo que será usado pelo App-V 5,0, por exemplo, **55555**. Você também deve certificar-se de que a porta especificada não está sendo usada por outro site.

8. Clique em **Instalar**.

   **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Sobre a emissão de relatórios do App-V 5.0](about-app-v-50-reporting.md)

[Implantação do App-V 5.0](deploying-app-v-50.md)

[Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)









