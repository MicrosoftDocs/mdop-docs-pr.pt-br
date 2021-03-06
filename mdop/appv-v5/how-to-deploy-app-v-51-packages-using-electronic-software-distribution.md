---
title: Como implantar pacotes do App-V 5.1 usando a Distribuição eletrônica de software
description: Como implantar pacotes do App-V 5.1 usando a Distribuição eletrônica de software
author: dansimp
ms.assetid: e1957a5a-1f18-42da-b2c1-a5ae5a4cca7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a9ed5fbb264f8fb9676d7fa18fe4de8019ea8e79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796436"
---
# Como implantar pacotes do App-V 5.1 usando a Distribuição eletrônica de software


Você pode usar um sistema ESD (Electronic Software Distribution) para implantar aplicativos virtuais do App-V 5,1 em clientes do App-V. Para obter detalhes, consulte a documentação disponível com o ESD que você está usando.

Para requisitos e opções de componentes para usar um ESD para implantar pacotes do App-V, consulte [planejando implantar o App-V 5,1 com um sistema de distribuição de software eletrônico](planning-to-deploy-app-v-51-with-an-electronic-software-distribution-system.md).

Use um dos seguintes métodos para publicar pacotes em computadores cliente do App-V com um ESD:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Funcionalidade fornecida por um ESD de terceiros</p></td>
<td align="left"><p>Use a funcionalidade em um ESD de terceiros.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Instalador autônomo do Windows</p></td>
<td align="left"><p>Instale o aplicativo no computador do cliente de destino usando o arquivo de instalação do Windows (. msi) associado que é criado quando você sequencia inicialmente um aplicativo. O arquivo do Windows Installer contém as informações do arquivo de pacote App-V 5,1 associadas usadas para configurar um pacote e copia os arquivos de pacote necessários para o cliente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Use cmdlets do PowerShell para implantar aplicativos virtualizados. Para obter mais informações sobre como usar o PowerShell e o App-V 5,1, consulte <a href="administering-app-v-51-by-using-powershell.md" data-raw-source="[Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md)"> administrando o app-v 5,1 usando o PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

 

**Para implantar pacotes do App-V 5,1 usando um ESD**

1.  Instale o sequenciador do App-V 5,1 em um computador no seu ambiente. Para obter mais informações sobre como instalar o sequenciador, consulte [como instalar o sequenciador](how-to-install-the-sequencer-51beta-gb18030.md).

2.  Use o sequenciador do App-V 5,1 para criar o aplicativo virtual. Para obter informações sobre como criar um aplicativo virtual, consulte [criando e gerenciando aplicativos virtualizados do App-V 5,1](creating-and-managing-app-v-51-virtualized-applications.md).

3.  Depois de criar o aplicativo virtual, implante o pacote usando a solução ESD.

    Se você estiver usando o System Center Configuration Manager, comece analisando [introdução ao gerenciamento de aplicativos no Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) para obter informações sobre como usar o App-V 5,1 e o System Center2012 Configuration Manager.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





