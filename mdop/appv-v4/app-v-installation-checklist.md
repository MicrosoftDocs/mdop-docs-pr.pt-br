---
title: Lista de verificação para instalação do App-V
description: Lista de verificação para instalação do App-V
author: dansimp
ms.assetid: b17efaab-cd6d-4c30-beb7-c6e7c9c87657
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d6d83ac465a7e48dd35bd2fe966c3c51be24c96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797600"
---
# <span data-ttu-id="8225c-103">Lista de verificação para instalação do App-V</span><span class="sxs-lookup"><span data-stu-id="8225c-103">App-V Installation Checklist</span></span>


<span data-ttu-id="8225c-104">A lista de verificação a seguir destina-se a fornecer uma lista de alto nível de itens a serem considerados e descreve as etapas que devem ser seguidas para instalar os servidores do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="8225c-104">The following checklist is intended to provide a high-level list of items to consider and outlines the steps you should take to install the Microsoft Application Virtualization (App-V) servers.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8225c-105">Etapa</span><span class="sxs-lookup"><span data-stu-id="8225c-105">Step</span></span></th>
<th align="left"><span data-ttu-id="8225c-106">Referência</span><span class="sxs-lookup"><span data-stu-id="8225c-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8225c-107">Instale o servidor de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="8225c-107">Install the App-V Management Server.</span></span> <span data-ttu-id="8225c-108">Se você estiver instalando o serviço Web de gerenciamento, o console de gerenciamento ou o repositório de dados em servidores diferentes, poderá usar a opção de instalação personalizada.</span><span class="sxs-lookup"><span data-stu-id="8225c-108">If you are installing the Management Web Service, Management Console, or the Data Store on different servers, you can use the custom installation option.</span></span></p></td>
<td align="left"><p><a href="how-to-install-application-virtualization-management-server.md" data-raw-source="[How to Install Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)"><span data-ttu-id="8225c-109">Como instalar o Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="8225c-109">How to Install Application Virtualization Management Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8225c-110">Instale o serviço Web de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="8225c-110">Install the App-V Management Web Service.</span></span> <span data-ttu-id="8225c-111">(Opcional ¹)</span><span class="sxs-lookup"><span data-stu-id="8225c-111">(Optional ¹)</span></span></p></td>
<td align="left"><p><a href="how-to-install-the-management-web-service.md" data-raw-source="[How to Install the Management Web Service](how-to-install-the-management-web-service.md)"><span data-ttu-id="8225c-112">Como instalar o Management Web Service</span><span class="sxs-lookup"><span data-stu-id="8225c-112">How to Install the Management Web Service</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8225c-113">Instale o console de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="8225c-113">Install the App-V Management Console.</span></span> <span data-ttu-id="8225c-114">(Opcional ¹)</span><span class="sxs-lookup"><span data-stu-id="8225c-114">(Optional ¹)</span></span></p></td>
<td align="left"><p><a href="how-to-install-the-management-console.md" data-raw-source="[How to Install the Management Console](how-to-install-the-management-console.md)"><span data-ttu-id="8225c-115">Como instalar o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="8225c-115">How to Install the Management Console</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8225c-116">Instale o repositório de dados do App-V.</span><span class="sxs-lookup"><span data-stu-id="8225c-116">Install the App-V Data Store.</span></span> <span data-ttu-id="8225c-117">(Opcional ¹)</span><span class="sxs-lookup"><span data-stu-id="8225c-117">(Optional ¹)</span></span></p></td>
<td align="left"><p><a href="how-to-install-a-database.md" data-raw-source="[How to Install a Database](how-to-install-a-database.md)"><span data-ttu-id="8225c-118">Como instalar um banco de dados</span><span class="sxs-lookup"><span data-stu-id="8225c-118">How to Install a Database</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8225c-119">Instale o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="8225c-119">Install the App-V client.</span></span></p></td>
<td align="left"><p><a href="how-to-manually-install-the-application-virtualization-client.md" data-raw-source="[How to Manually Install the Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)"><span data-ttu-id="8225c-120">Como instalar manualmente o Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="8225c-120">How to Manually Install the Application Virtualization Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8225c-121">Instale o sequenciador do App-V.</span><span class="sxs-lookup"><span data-stu-id="8225c-121">Install the App-V Sequencer.</span></span></p></td>
<td align="left"><p><a href="how-to-install-the-application-virtualization-sequencer.md" data-raw-source="[How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)"><span data-ttu-id="8225c-122">Como instalar o Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="8225c-122">How to Install the Application Virtualization Sequencer</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8225c-123">Instale o servidor de streaming do App-V.</span><span class="sxs-lookup"><span data-stu-id="8225c-123">Install the App-V Streaming Server.</span></span> <span data-ttu-id="8225c-124">(Isso é opcional e obrigatório apenas se você estiver instalando o servidor de streaming).</span><span class="sxs-lookup"><span data-stu-id="8225c-124">(This is optional and required only if you are installing the Streaming Server).</span></span></p></td>
<td align="left"><p><a href="how-to-install-the-application-virtualization-streaming-server.md" data-raw-source="[How to Install the Application Virtualization Streaming Server](how-to-install-the-application-virtualization-streaming-server.md)"><span data-ttu-id="8225c-125">Como instalar o Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="8225c-125">How to Install the Application Virtualization Streaming Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8225c-126">Crie diretórios de conteúdo nos servidores que serão usados para transmitir aplicativos para os computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="8225c-126">Create Content directories on the servers that will be used for streaming applications to users’ computers.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="8225c-127">Como configurar os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="8225c-127">How to Configure the Application Virtualization Management Servers</span></span></a></p>
<p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)"><span data-ttu-id="8225c-128">Como configurar os Application Virtualization Streaming Servers</span><span class="sxs-lookup"><span data-stu-id="8225c-128">How to Configure the Application Virtualization Streaming Servers</span></span></a></p>
<p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="8225c-129">Como configurar o servidor para o IIS</span><span class="sxs-lookup"><span data-stu-id="8225c-129">How to Configure the Server for IIS</span></span></a></p>
<p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="8225c-130">Como configurar o Servidor de Arquivos</span><span class="sxs-lookup"><span data-stu-id="8225c-130">How to Configure the File Server</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8225c-131">¹ isso é necessário apenas se você estiver instalando o serviço Web de gerenciamento do App-V, console de gerenciamento ou o repositório de dados em um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="8225c-131">¹ This is required only if you are installing the App-V Management Web Service, Management Console, or the Data Store on a different computer.</span></span>

## <span data-ttu-id="8225c-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8225c-132">Related topics</span></span>


[<span data-ttu-id="8225c-133">Listas de verificação de atualização e implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8225c-133">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

[<span data-ttu-id="8225c-134">Lista de verificação pós-instalação do App-V</span><span class="sxs-lookup"><span data-stu-id="8225c-134">App-V Postinstallation Checklist</span></span>](app-v-postinstallation-checklist.md)

 

 





