---
title: Como aplicar o arquivo de configuração do usuário usando o PowerShell
description: Como aplicar o arquivo de configuração do usuário usando o PowerShell
author: dansimp
ms.assetid: f7d7c595-4fdd-4096-b53d-9eead111c339
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95ae5840f5eee04a29431716a956ddec7d0487aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796499"
---
# Como aplicar o arquivo de configuração do usuário usando o PowerShell


O arquivo de configuração de usuário dinâmico é aplicado quando um pacote é publicado em um usuário específico e determina como o pacote será executado.

Use o procedimento a seguir para especificar um arquivo de configuração específico do usuário. O procedimento a seguir se baseia no exemplo:

**c:\\Packages\\Contoso\\MyApp.appv**

**Para aplicar um arquivo de configuração do usuário**

1.  Para adicionar o pacote ao computador usando o console do PowerShell, digite o seguinte comando:

    **Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.AppV**.

2.  Use o comando a seguir para publicar o pacote para o usuário e especificar o arquivo de configuração do usuário dinâmico atualizado:

    **Publish-AppVClientPackage $pkg-DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml**

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)

 

 





