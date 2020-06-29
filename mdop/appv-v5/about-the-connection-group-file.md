---
title: Sobre o arquivo do grupo de conexão
description: Sobre o arquivo do grupo de conexão
author: dansimp
ms.assetid: bfeb6013-a7ca-4e36-9fe3-229702e83f0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5cb93326ce182d71de0f0f89cc569823d6154e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796623"
---
# <span data-ttu-id="e8ca5-103">Sobre o arquivo do grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-103">About the Connection Group File</span></span>


**<span data-ttu-id="e8ca5-104">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="e8ca5-104">In this topic:</span></span>**

-   [<span data-ttu-id="e8ca5-105">Finalidade e local do arquivo de grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-105">Connection group file purpose and location</span></span>](#bkmk-cg-purpose-loc)

-   [<span data-ttu-id="e8ca5-106">Estrutura do arquivo XML do grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="e8ca5-106">Structure of the connection group XML file</span></span>](#bkmk-define-cg-5-0sp3)

-   [<span data-ttu-id="e8ca5-107">Configurar a prioridade dos pacotes em um grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-107">Configuring the priority of packages in a connection group</span></span>](#bkmk-config-pkg-priority-incg)

-   [<span data-ttu-id="e8ca5-108">Configurações de conexão de aplicativo virtual com suporte</span><span class="sxs-lookup"><span data-stu-id="e8ca5-108">Supported virtual application connection configurations</span></span>](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a><span data-ttu-id="e8ca5-109">Finalidade e local do arquivo de grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-109">Connection group file purpose and location</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8ca5-110">Finalidade do grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-110">Connection group purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-111">Um grupo de conexão é um recurso App-V que permite agrupar pacotes para criar um ambiente virtual no qual os aplicativos desses pacotes podem interagir uns com os outros.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-111">A connection group is an App-V feature that enables you to group packages together to create a virtual environment in which the applications in those packages can interact with each other.</span></span></p>
<p><span data-ttu-id="e8ca5-112">Exemplo: você deseja usar plug-ins com o Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-112">Example: You want to use plug-ins with Microsoft Office.</span></span> <span data-ttu-id="e8ca5-113">Você pode criar um pacote que contém os plug-ins e criar outro pacote que contém o Office e, em seguida, adicionar os dois pacotes a um grupo de conexão para permitir que o Office Use esses plug-ins.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-113">You can create a package that contains the plug-ins, and create another package that contains Office, and then add both packages to a connection group to enable Office to use those plug-ins.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8ca5-114">Como funciona o arquivo de grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-114">How the connection group file works</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-115">Quando você aplica um arquivo de grupo de conexão do Application Virtualization 5,0, os pacotes enumerados no arquivo serão combinados em tempo de execução em um único ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-115">When you apply an Application Virtualization 5.0 connection group file, the packages that are enumerated in the file will be combined at runtime into a single virtual environment.</span></span> <span data-ttu-id="e8ca5-116">Use o arquivo de grupo de conexão do 5,0 do Microsoft Application Virtualization (App-V) para configurar grupos de conexão do aplicativo virtual 5,0 existentes.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-116">Use the Microsoft Application Virtualization (App-V) 5.0 connection group file to configure existing Application Virtualization 5.0 connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8ca5-117">Caminho de arquivo de exemplo</span><span class="sxs-lookup"><span data-stu-id="e8ca5-117">Example file path</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups{6CCC7575-162E-4152-9407-ED411DA138F4}{4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a><span data-ttu-id="e8ca5-119">Estrutura do arquivo XML do grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="e8ca5-119">Structure of the connection group XML file</span></span>


**<span data-ttu-id="e8ca5-120">Nesta seção:</span><span class="sxs-lookup"><span data-stu-id="e8ca5-120">In this section:</span></span>**

-   [<span data-ttu-id="e8ca5-121">Parâmetros que definem o grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-121">Parameters that define the connection group</span></span>](#bkmk-params-define-cg)

-   [<span data-ttu-id="e8ca5-122">Parâmetros que definem os pacotes no grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="e8ca5-122">Parameters that define the packages in the connection group</span></span>](#bkmk-params-define-pkgs-incg)

-   [<span data-ttu-id="e8ca5-123">App-V 5,0 SP3 exemplo de arquivo XML do grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="e8ca5-123">App-V 5.0 SP3 example connection group XML file</span></span>](#bkmk-50sp3-exp-cg-xml)

-   [<span data-ttu-id="e8ca5-124">Exemplo do App-V 5,0 a App-V 5,0 SP2-arquivo XML do grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="e8ca5-124">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a><span data-ttu-id="e8ca5-125">Parâmetros que definem o grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-125">Parameters that define the connection group</span></span>

<span data-ttu-id="e8ca5-126">A tabela a seguir descreve os parâmetros no arquivo XML que definem o grupo de conexão propriamente dito, e não os pacotes.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-126">The following table describes the parameters in the XML file that define the connection group itself, not the packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8ca5-127">Campo</span><span class="sxs-lookup"><span data-stu-id="e8ca5-127">Field</span></span></th>
<th align="left"><span data-ttu-id="e8ca5-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8ca5-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8ca5-129">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="e8ca5-129">Schema name</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-130">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-130">Name of the schema.</span></span></p>
<p><strong><span data-ttu-id="e8ca5-131">Aplicável a partir do App-V 5,0 SP3 </strong> : se você quiser usar os novos recursos "pacotes opcionais" e "usar qualquer versão" descritos nesta tabela, você deve especificar o seguinte esquema no arquivo XML:</span><span class="sxs-lookup"><span data-stu-id="e8ca5-131">Applicable starting in App-V 5.0 SP3</strong>: If you want to use the new “optional packages” and “use any version” features that are described in this table, you must specify the following schema in the XML file:</span></span></p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8ca5-132">AppConnectionGroupId</span><span class="sxs-lookup"><span data-stu-id="e8ca5-132">AppConnectionGroupId</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-133">Identificador de GUID exclusivo para esse grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-133">Unique GUID identifier for this connection group.</span></span> <span data-ttu-id="e8ca5-134">O estado do grupo de conexão é associado a esse identificador.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-134">The connection group state is associated with this identifier.</span></span> <span data-ttu-id="e8ca5-135">Especifique esse identificador somente quando criar o grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-135">Specify this identifier only when you create the connection group.</span></span></p>
<p><span data-ttu-id="e8ca5-136">Você pode criar um novo GUID digitando: <strong>[Guid]::NewGuid()</strong> .</span><span class="sxs-lookup"><span data-stu-id="e8ca5-136">You can create a new GUID by typing: <strong>[Guid]::NewGuid()</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8ca5-137">VersionId</span><span class="sxs-lookup"><span data-stu-id="e8ca5-137">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-138">Identificador de GUID de versão para esta versão do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-138">Version GUID identifier for this version of the connection group.</span></span></p>
<p><span data-ttu-id="e8ca5-139">Ao atualizar um grupo de conexão (por exemplo, ao adicionar ou atualizar um novo pacote), você deve atualizar o GUID de versão para refletir a nova versão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-139">When you update a connection group (for example, by adding or updating a new package), you must update the version GUID to reflect the new version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8ca5-140">DisplayName</span><span class="sxs-lookup"><span data-stu-id="e8ca5-140">DisplayName</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-141">Nome para exibição do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-141">Display name of the connection group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8ca5-142">Prioridade</span><span class="sxs-lookup"><span data-stu-id="e8ca5-142">Priority</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-143">Campo prioridade opcional para o grupo conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-143">Optional priority field for the connection group.</span></span></p>
<p><strong><span data-ttu-id="e8ca5-144">"0" </strong> - indica a prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-144">“0”</strong> - indicates the highest priority.</span></span></p>
<p><span data-ttu-id="e8ca5-145">Se for necessária uma prioridade, mas não tiver sido configurada, o pacote falhará porque o grupo de conexões correto a ser usado não pode ser determinado.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-145">If a priority is required, but has not been configured, the package will fail because the correct connection group to use cannot be determined.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a><span data-ttu-id="e8ca5-146">Parâmetros que definem os pacotes no grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="e8ca5-146">Parameters that define the packages in the connection group</span></span>

<span data-ttu-id="e8ca5-147">Na &lt; seção pacotes &gt; do arquivo XML do grupo de conexão, você lista os pacotes de membros no grupo conexão especificando cada identificador de pacote exclusivo e identificador de versão do pacote, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-147">In the &lt;Packages&gt; section of the connection group XML file, you list the member packages in the connection group by specifying each package’s unique package identifier and version identifier, as described in the following table.</span></span> <span data-ttu-id="e8ca5-148">O primeiro pacote na lista tem a precedência mais alta.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-148">The first package in the list has the highest precedence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8ca5-149">Campo</span><span class="sxs-lookup"><span data-stu-id="e8ca5-149">Field</span></span></th>
<th align="left"><span data-ttu-id="e8ca5-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8ca5-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8ca5-151">PackageID</span><span class="sxs-lookup"><span data-stu-id="e8ca5-151">PackageId</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-152">Identificador de GUID exclusivo para este pacote.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-152">Unique GUID identifier for this package.</span></span> <span data-ttu-id="e8ca5-153">Esse GUID não é alterado quando novas versões do pacote são publicadas.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-153">This GUID doesn’t change when newer versions of the package are published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8ca5-154">VersionId</span><span class="sxs-lookup"><span data-stu-id="e8ca5-154">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-155">Identificador de GUID exclusivo para a versão do pacote.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-155">Unique GUID identifier for the version of the package.</span></span></p>
<p><strong><span data-ttu-id="e8ca5-156">Aplicável a partir do App-V 5,0 SP3 </strong> : se você especificar <strong> "\*" </strong> para a versão do pacote, o GUID da versão do pacote mais recente disponível será inserido dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-156">Applicable starting in App-V 5.0 SP3</strong>: If you specify <strong>“\*”</strong> for the package version, the GUID of the latest available package version is dynamically inserted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8ca5-157">IsOptional</span><span class="sxs-lookup"><span data-stu-id="e8ca5-157">IsOptional</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="e8ca5-158">Aplicável a partir do App-V 5,0 SP3 </strong> : parâmetro que permite que você crie um pacote opcional dentro do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-158">Applicable starting in App-V 5.0 SP3</strong>: Parameter that enables you to make a package optional within the connection group.</span></span> <span data-ttu-id="e8ca5-159">As entradas válidas são:</span><span class="sxs-lookup"><span data-stu-id="e8ca5-159">Valid entries are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="e8ca5-160">"verdadeiro" </strong> – o pacote é opcional no grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-160">“true”</strong> – package is optional in the connection group</span></span></p></li>
<li><p><strong><span data-ttu-id="e8ca5-161">"falso" </strong> – o pacote é necessário no grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-161">“false”</strong> – package is required in the connection group</span></span></p></li>
</ul>
<p><span data-ttu-id="e8ca5-162">Veja <a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)"> como usar pacotes opcionais em grupos de conexão </a> .</span><span class="sxs-lookup"><span data-stu-id="e8ca5-162">See <a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)">How to Use Optional Packages in Connection Groups</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a><span data-ttu-id="e8ca5-163">App-V 5,0 SP3 exemplo de arquivo XML do grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="e8ca5-163">App-V 5.0 SP3 example connection group XML file</span></span>

<span data-ttu-id="e8ca5-164">O exemplo de arquivo XML do grupo de conexão a seguir mostra exemplos dos campos nas tabelas anteriores e realça os itens que são novos para o App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-164">The following example connection group XML file shows examples of the fields in the previous tables and highlights the items that are new for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup 
   xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"  
   Priority="0"  
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="*"
         IsOptional=”true”
      />    
     <appv:Package
        PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
        VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
        IsOptional="false"
     />  
   </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a><span data-ttu-id="e8ca5-165">Exemplo do App-V 5,0 a App-V 5,0 SP2-arquivo XML do grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="e8ca5-165">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>

<span data-ttu-id="e8ca5-166">O exemplo de arquivo XML do grupo de conexão de exemplo a seguir aplica-se ao App-V 5,0 a App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-166">The following example connection group XML file applies to App-V 5.0 through App-V 5.0 SP2.</span></span> <span data-ttu-id="e8ca5-167">Ele mostra exemplos dos campos na tabela anterior, mas exclui as alterações descritas acima para o App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-167">It shows examples of the fields in the previous table, but it excludes the changes described above for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup
   xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
   Priority="0"
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package``      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
      />
      <appv:Package
         PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
         VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      />
   </appv:Packages>
</appv:AppConnectionGroup
 ```

## <a href="" id="bkmk-config-pkg-priority-incg"></a><span data-ttu-id="e8ca5-168">Configurar a prioridade dos pacotes em um grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-168">Configuring the priority of packages in a connection group</span></span>


<span data-ttu-id="e8ca5-169">A precedência do pacote é configurada usando a ordem da lista do pacote.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-169">Package precedence is configured using the package list order.</span></span> <span data-ttu-id="e8ca5-170">O primeiro pacote no documento tem a precedência mais alta.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-170">The first package in the document has the highest precedence.</span></span> <span data-ttu-id="e8ca5-171">Os pacotes subsequentes na lista têm prioridade decrescente.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-171">Subsequent packages in the list have descending priority.</span></span>

<span data-ttu-id="e8ca5-172">A precedência do pacote é a resolução para colisões de recursos inevitávels durante a inicialização do ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-172">Package precedence is the resolution for otherwise inevitable resource collisions during virtual environment initialization.</span></span> <span data-ttu-id="e8ca5-173">Por exemplo, se dois pacotes que estão sendo abertos no mesmo ambiente virtual definirem o mesmo valor DWORD do registro, o pacote com a precedência mais alta determinará o valor definido.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-173">For example, if two packages that are opening in the same virtual environment define the same registry DWORD value, the package with the highest precedence determines the value that is set.</span></span>

<span data-ttu-id="e8ca5-174">Você pode usar o arquivo de grupo de conexão para configurar cada grupo de conexão usando os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="e8ca5-174">You can use the connection group file to configure each connection group by using the following methods:</span></span>

-   <span data-ttu-id="e8ca5-175">Especifique as prioridades do tempo de execução para grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-175">Specify runtime priorities for connection groups.</span></span>

    <span data-ttu-id="e8ca5-176">**Observação**  A prioridade só será necessária se o pacote estiver associado a mais de um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-176">**Note** Priority is required only if the package is associated with more than one connection group.</span></span>

     

-   <span data-ttu-id="e8ca5-177">Especifique a precedência do pacote dentro do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-177">Specify package precedence within the connection group.</span></span>

<span data-ttu-id="e8ca5-178">O campo Priority é necessário quando um aplicativo virtual em execução é iniciado a partir de uma solicitação de aplicativo nativo, por exemplo, o Microsoft Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-178">The priority field is required when a running virtual application initiates from a native application request, for example, Microsoft Windows Explorer.</span></span> <span data-ttu-id="e8ca5-179">O cliente App-V usa a prioridade para determinar em qual ambiente virtual de grupo de conexão o aplicativo deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-179">The App-V client uses the priority to determine which connection group virtual environment the application should run in.</span></span> <span data-ttu-id="e8ca5-180">Essa situação ocorre se um aplicativo virtual fizer parte de vários grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-180">This situation occurs if a virtual application is part of multiple connection groups.</span></span>

<span data-ttu-id="e8ca5-181">Se um aplicativo virtual for aberto usando outro aplicativo virtual, o ambiente virtual do aplicativo virtual original será usado.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-181">If a virtual application is opened using another virtual application the virtual environment of the original virtual application will be used.</span></span> <span data-ttu-id="e8ca5-182">Nesse caso, o campo Priority não é usado.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-182">The priority field is not used in this case.</span></span>

**<span data-ttu-id="e8ca5-183">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="e8ca5-183">Example:</span></span>**

<span data-ttu-id="e8ca5-184">O aplicativo virtual que o Microsoft Outlook está em execução no ambiente virtual **XYZ**.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-184">The virtual application Microsoft Outlook is running in virtual environment **XYZ**.</span></span> <span data-ttu-id="e8ca5-185">Quando você abre um documento do Microsoft Word anexado, uma versão virtualizada do Microsoft Word abre no ambiente virtual **XYZ**, independentemente dos grupos de conexão associados do Microsoft Word ou das prioridades do tempo de execução da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-185">When you open an attached Microsoft Word document, a virtualized version Microsoft Word opens in the virtual environment **XYZ**, regardless of the virtualized Microsoft Word’s associated connection groups or runtime priorities.</span></span>

## <a href="" id="bkmk-va-conn-configs"></a><span data-ttu-id="e8ca5-186">Configurações de conexão de aplicativo virtual com suporte</span><span class="sxs-lookup"><span data-stu-id="e8ca5-186">Supported virtual application connection configurations</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8ca5-187">Configuração</span><span class="sxs-lookup"><span data-stu-id="e8ca5-187">Configuration</span></span></th>
<th align="left"><span data-ttu-id="e8ca5-188">Cenário de exemplo</span><span class="sxs-lookup"><span data-stu-id="e8ca5-188">Example scenario</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8ca5-189">A.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-189">An.</span></span> <span data-ttu-id="e8ca5-190">plug-in e arquivo exe (. dll)</span><span class="sxs-lookup"><span data-stu-id="e8ca5-190">exe file and plug-in (.dll)</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e8ca5-191">Você deseja distribuir o Microsoft Office para todos os usuários, mas distribuir um plug-in do Microsoft Excel para apenas um subconjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-191">You want to distribute Microsoft Office to all users, but distribute a Microsoft Excel plug-in to only a subset of users.</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-192">Habilite o grupo de conexão para os usuários apropriados.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-192">Enable the connection group for the appropriate users.</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-193">Atualize cada pacote individualmente, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-193">Update each package individually as required.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8ca5-194">A.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-194">An.</span></span> <span data-ttu-id="e8ca5-195">arquivo exe e um aplicativo de middleware</span><span class="sxs-lookup"><span data-stu-id="e8ca5-195">exe file and a middleware application</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e8ca5-196">Você tem um aplicativo exige um aplicativo de middleware ou vários aplicativos que dependem da mesma versão de tempo de execução de middleware.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-196">You have an application requires a middleware application, or several applications that all depend on the same middleware runtime version.</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-197">Todos os computadores que exigem um ou mais aplicativos recebem os grupos de conexão com o aplicativo de tempo de execução do aplicativo e middleware.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-197">All computers that require one or more of the applications receive the connection groups with the application and middleware application runtime.</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-198">Opcionalmente, você pode combinar vários aplicativos middleware em um único grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-198">You can optionally combine multiple middleware applications into a single connection group.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8ca5-199">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e8ca5-199">Example</span></span></th>
<th align="left"><span data-ttu-id="e8ca5-200">Exemplo de descrição</span><span class="sxs-lookup"><span data-stu-id="e8ca5-200">Example description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8ca5-201">Grupo de conexão de aplicativo virtual para a divisão financeira</span><span class="sxs-lookup"><span data-stu-id="e8ca5-201">Virtual application connection group for the financial division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e8ca5-202">Aplicativo middleware 1</span><span class="sxs-lookup"><span data-stu-id="e8ca5-202">Middleware application 1</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-203">Aplicativo Middleware 2</span><span class="sxs-lookup"><span data-stu-id="e8ca5-203">Middleware application 2</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-204">Aplicativo middleware 3</span><span class="sxs-lookup"><span data-stu-id="e8ca5-204">Middleware application 3</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-205">Tempo de execução do aplicativo middleware</span><span class="sxs-lookup"><span data-stu-id="e8ca5-205">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8ca5-206">Grupo de conexão de aplicativo virtual para divisão de RH</span><span class="sxs-lookup"><span data-stu-id="e8ca5-206">Virtual application connection group for HR division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e8ca5-207">Aplicativo middleware 5</span><span class="sxs-lookup"><span data-stu-id="e8ca5-207">Middleware application 5</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-208">Aplicativo middleware 6</span><span class="sxs-lookup"><span data-stu-id="e8ca5-208">Middleware application 6</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-209">Tempo de execução do aplicativo middleware</span><span class="sxs-lookup"><span data-stu-id="e8ca5-209">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8ca5-210">A.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-210">An.</span></span> <span data-ttu-id="e8ca5-211">arquivo exe e um arquivo. exe</span><span class="sxs-lookup"><span data-stu-id="e8ca5-211">exe file and an .exe file</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8ca5-212">Você tem um aplicativo que depende de outro aplicativo e deseja manter os pacotes separados para desempenho operacional, restrições de licenciamento ou linhas do tempo de distribuição.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-212">You have an application that relies on another application, and you want to keep the packages separate for operational efficiencies, licensing restrictions, or rollout timelines.</span></span></p>
<p><strong><span data-ttu-id="e8ca5-213">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="e8ca5-213">Example:</span></span></strong></p>
<p><span data-ttu-id="e8ca5-214">Se você estiver implantando o Microsoft Lync 2010, poderá usar três pacotes:</span><span class="sxs-lookup"><span data-stu-id="e8ca5-214">If you are deploying Microsoft Lync 2010, you can use three packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="e8ca5-215">Microsoft office2010</span><span class="sxs-lookup"><span data-stu-id="e8ca5-215">Microsoft Office2010</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-216">Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="e8ca5-216">Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-217">Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="e8ca5-217">Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="e8ca5-218">Você pode gerenciar a implantação usando os seguintes grupos de conexão:</span><span class="sxs-lookup"><span data-stu-id="e8ca5-218">You can manage the deployment using the following connection groups:</span></span></p>
<ul>
<li><p><span data-ttu-id="e8ca5-219">Microsoft office2010 e Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="e8ca5-219">Microsoft Office2010 and Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="e8ca5-220">Microsoft office2010 e Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="e8ca5-220">Microsoft Office2010 and Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="e8ca5-221">Quando a implantação for concluída, você poderá criar um único novo pacote Microsoft office2010 + Microsoft Lync2010 ou mantê-los e mantê-los como pacotes separados e implantá-los usando um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="e8ca5-221">When the deployment has completed, you can either create a single new Microsoft Office2010 + Microsoft Lync2010 package, or keep and maintain them as separate packages and deploy them by using a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="e8ca5-222">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8ca5-222">Related topics</span></span>


[<span data-ttu-id="e8ca5-223">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="e8ca5-223">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 




