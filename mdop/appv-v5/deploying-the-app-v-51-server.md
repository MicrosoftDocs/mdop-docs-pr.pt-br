---
title: Implantação do servidor App-V 5.1
description: Implantação do servidor App-V 5.1
author: dansimp
ms.assetid: 987b61dc-00d6-49ba-8f1b-92d7b948e702
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bcff2a3211ea3e2f666aff1d6f2ad919509aa3a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796531"
---
# Implantação do servidor App-V 5.1

Você pode instalar os recursos do servidor do Microsoft Application Virtualization (App-V) 5,1 usando diferentes configurações de implantação, descritas neste tópico. Antes de instalar os recursos do servidor, examine a seção do servidor das [considerações de segurança do App-V 5,1](app-v-51-security-considerations.md).

Para obter informações sobre a implantação do App-V Server, consulte [sobre o app-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).

> [!IMPORTANT]
> Antes de instalar e configurar os servidores do App-V 5,1, você deve especificar uma porta onde cada componente será hospedado. Você também deve adicionar as regras de firewall associadas para permitir que as solicitações de entrada acessem as portas especificadas. O instalador não modifica as configurações de firewall.

## <a href="" id="---------app-v-5-1-server-overview"></a> Visão geral do App-V Server 5,1

O servidor do App-V 5,1 é composto de cinco componentes. Cada componente serve a uma finalidade diferente no ambiente do App-V 5,1. Cada um dos cinco componentes é brevemente descrito aqui:

- Servidor de gerenciamento – oferece funcionalidade de gerenciamento geral para a infraestrutura do App-V 5,1.
- Banco de dados de gerenciamento – facilita as implantações de banco de dados do gerenciamento do App-V 5,1.
- Publishing Server – fornece funcionalidade de hospedagem e streaming para aplicativos virtuais.
- Servidor de relatórios – fornece o App-V 5,1 Reporting Services.
- Banco de dados de relatórios – facilita a implantação de bancos de dados para relatórios do App-V 5,1.

## <a href="" id="---------app-v-5-1-stand-alone-deployment"></a> Implantação autônoma do App-V 5,1

A implantação autônoma do App-V 5,1 fornece uma boa topologia para uma implantação pequena ou um ambiente de teste. Quando você usa esse tipo de implementação, todos os componentes do servidor são implantados em um único computador. Os serviços e bancos de dados associados serão concorrentes para os recursos do computador que executam os componentes do App-V 5,1. Portanto, você não deve usar essa topologia para implantações maiores.

[Como implantar o servidor do App-V 5.1](how-to-deploy-the-app-v-51-server.md)

[Como implantar o servidor App-V 5.1 usando um script](how-to-deploy-the-app-v-51-server-using-a-script.md)

## <a href="" id="---------app-v-5-1-server-distributed-deployment"></a> Implantação distribuída do App-V 5,1 Server

A topologia de implantação distribuída pode dar suporte a uma grande base de cliente do App-V 5,1 e permite que você gerencie e dimensione com mais facilidade seu ambiente. Quando você usa esse tipo de implantação, os componentes do servidor do App-V 5,1 são implantados em vários computadores, com base na estrutura e nos requisitos da organização.

[Como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[Como instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)

[Como implantar o servidor App-V 5.1 usando um script](how-to-deploy-the-app-v-51-server-using-a-script.md)

[Como instalar o servidor de publicação em um computador remoto](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[Como instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)

## Usando uma solução ESD (Enterprise Software Distribution) e o App-V 5,1

Você também pode implantar os clientes e pacotes do App-V 5,1 usando um ESD sem ter que implantar o App-V 5,1. Os recursos completos para a integração variam de acordo com o ESD que você usa.

> [!NOTE]
> O servidor de relatórios do App-V 5,1 e o banco de dados de relatórios ainda podem ser implantados junto com o ESD para coletar os dados de relatório dos clientes do App-V 5,1. No entanto, os outros três componentes do servidor não devem ser implantados, pois eles entrarão em conflito com a funcionalidade ESD.

[Implantação dos pacotes do App-V 5.1 usando a Distribuição eletrônica de software (ESD)](deploying-app-v-51-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-1-server-logs"></a> Logs do servidor do App-V 5,1

Você pode usar as informações de log do App-V 5,1 Server para ajudar a solucionar problemas de instalação do servidor e eventos operacionais durante o uso do App-V 5,1. As informações de log relacionadas ao servidor podem ser analisadas com o **Visualizador de eventos**. A linha a seguir exibe o caminho específico para eventos relacionados ao servidor:

**Visualizador de eventos \ \ logs de aplicativos e serviços \ \ Microsoft \ \ App V**

Os logs de instalação associados são salvos no seguinte diretório:

**Temp**

No App-V 5,0 SP3, alguns registros foram consolidados e movidos. Consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

## <a href="" id="---------app-v-5-1-reporting"></a> Relatórios do App-V 5,1

Os relatórios do App-V 5,1 permitem que os clientes do App-V 5,1 coletem dados e os enviem de volta para serem armazenados em um repositório central. Você pode usar essas informações para obter uma visão melhor do uso do aplicativo virtual dentro da sua organização. A lista a seguir mostra alguns dos tipos de informação que o cliente do App-V 5,1 coleta:

- Informações sobre o computador que executa o cliente App-V 5,1.
- Informações sobre pacotes virtualizados em um computador específico que executa o cliente App-V 5,1.
- Informações sobre abertura e desligamento de pacotes para um usuário específico.

As informações de relatório serão mantidas até que sejam enviadas com êxito para o banco de dados do servidor de relatórios. Depois que os dados estiverem no banco de dados, você poderá usar o Microsoft SQL Server Reporting Services para gerar os relatórios necessários.

Se quiser recuperar informações de relatório, você deve usar o Microsoft SQL Server Reporting Services (SSRS) que está disponível com o Microsoft SQL. O SSRS não é instalado quando você instala o servidor de relatórios do App-V 5,1 e deve ser implantado separadamente para gerar os relatórios associados.

Use o link a seguir para obter mais informações [sobre relatórios do App-V 5,1](about-app-v-51-reporting.md).

[Como habilitar relatórios no cliente do App-V 5.1 usando o PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)

## Outros recursos para o App-V Server

[Implantação do App-V 5.1](deploying-app-v-51.md)
