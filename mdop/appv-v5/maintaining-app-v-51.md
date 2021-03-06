---
title: Manutenção do App-V 5.1
description: Manutenção do App-V 5.1
author: dansimp
ms.assetid: 5abd17d3-e8af-4261-b914-741ae116b0e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 431ad65507a5699358159c73eaf9f3cf0dee33b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796293"
---
# Manutenção do App-V 5.1


Depois de concluir todos os planejamentos necessários e, em seguida, a implantação do App-V 5,1, você pode usar as seguintes informações para manter a infraestrutura do App-V 5,1.

## <a href="" id="move-the-app-v-5-1-server-"></a>Mover o servidor do App-V 5,1


O servidor do App-V 5,1 se conecta ao banco de dados do App-V 5,1. Portanto, você pode instalar o componente de gerenciamento em qualquer computador na rede e, em seguida, conectá-lo ao banco de dados do App-V 5,1.

[Como mover o servidor do App-V para outro computador](how-to-move-the-app-v-server-to-another-computer51.md)

## <a href="" id="determine-if-an-app-v-5-1-application-is-running-virtualized-"></a>Determinar se um aplicativo App-V 5,1 está em execução virtualizado


ISVs (fornecedores independentes de software) que desejam determinar se um aplicativo está em execução virtualizada com o App-V 5,1 ou superior, deve abrir um objeto nomeado chamado **AppVVirtual- &lt; pid &gt; ** no namespace padrão. Por exemplo, a API do Windows **GetCurrentProcessId ()** pode ser usada para obter a ID do processo atual, por exemplo, 4052, e, em seguida, se um objeto de evento nomeado chamado **AppVVirtual-4052** puder ser aberto com êxito usando **OpenEvent ()** no namespace padrão para acesso de leitura, o aplicativo será virtual. Se a chamada **OpenEvent ()** falhar, o aplicativo não será virtual.

Além disso, os ISVs que desejam virtualizar ou não virtualizam explicitamente chamadas em APIs específicas com o App-V 5,1 e superior podem usar as funções **VirtualizeCurrentThread ()** e **CurrentThreadIsVirtualized ()** implementadas no módulo AppEntSubsystems32.dll. Elas fornecem uma maneira de fazer uma referência a um componente downstream em que a chamada deve ou não ser virtualizada.






## Outros recursos para manter o App-V 5,1


[Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





