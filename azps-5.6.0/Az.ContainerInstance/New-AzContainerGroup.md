---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 43f8144d22632d100e818bebcfb7f9247130035f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915585"
---
# <span data-ttu-id="ba31c-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ba31c-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="ba31c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ba31c-102">SYNOPSIS</span></span>
<span data-ttu-id="ba31c-103">建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="ba31c-103">Creates a container group.</span></span>

## <span data-ttu-id="ba31c-104">語法</span><span class="sxs-lookup"><span data-stu-id="ba31c-104">SYNTAX</span></span>

### <span data-ttu-id="ba31c-105">CreateContainerGroupBaseParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ba31c-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba31c-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="ba31c-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba31c-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="ba31c-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba31c-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba31c-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba31c-109">描述</span><span class="sxs-lookup"><span data-stu-id="ba31c-109">DESCRIPTION</span></span>
<span data-ttu-id="ba31c-110">**New-AzContainerGroup** Cmdlet 會建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="ba31c-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="ba31c-111">例子</span><span class="sxs-lookup"><span data-stu-id="ba31c-111">EXAMPLES</span></span>

### <span data-ttu-id="ba31c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="ba31c-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="ba31c-113">這個命令會使用最新的 nginx 影像建立容器群組，並要求開啟埠 8000 的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ba31c-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="ba31c-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="ba31c-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="ba31c-115">這個命令會建立容器群組，並在此容器內執行自訂腳本。</span><span class="sxs-lookup"><span data-stu-id="ba31c-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="ba31c-116">範例 3：建立執行到完成容器群組。</span><span class="sxs-lookup"><span data-stu-id="ba31c-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="ba31c-117">這個命令會建立一個容器群組，該群組會列印出"hello"並停止。</span><span class="sxs-lookup"><span data-stu-id="ba31c-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="ba31c-118">範例 4：使用 Azure Container Registry 中的圖像建立容器群組</span><span class="sxs-lookup"><span data-stu-id="ba31c-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="ba31c-119">這個命令會使用 Azure Container Registry 中的 nginx 圖像建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="ba31c-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="ba31c-120">範例 5：使用自訂容器圖像註冊表中的圖像建立容器群組</span><span class="sxs-lookup"><span data-stu-id="ba31c-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="ba31c-121">這個命令會使用自訂容器圖像註冊表中的自訂圖像來建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="ba31c-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="ba31c-122">範例 6：建立安裝 Azure 檔案音量的容器群組</span><span class="sxs-lookup"><span data-stu-id="ba31c-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name mycontainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountCredential $mycred -AzureFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="ba31c-123">這個命令會建立容器群組，將提供的 Azure 檔案共用安裝至 `/mnt/azfile` 。</span><span class="sxs-lookup"><span data-stu-id="ba31c-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="ba31c-124">範例 7</span><span class="sxs-lookup"><span data-stu-id="ba31c-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="ba31c-125">這個命令會建立一個容器群組，其系統會使用最新的 nginx 影像指派身分識別，並要求開啟埠 8000 的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ba31c-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="ba31c-126">範例 8</span><span class="sxs-lookup"><span data-stu-id="ba31c-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="ba31c-127">這個命令會建立一個容器群組，其系統已指派，且使用者已使用最新的 nginx 影像指派身分識別，並要求開啟埠 8000 的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ba31c-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="ba31c-128">參數</span><span class="sxs-lookup"><span data-stu-id="ba31c-128">PARAMETERS</span></span>

### <span data-ttu-id="ba31c-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ba31c-129">-AssignIdentity</span></span>
<span data-ttu-id="ba31c-130">啟用系統指派的身分識別</span><span class="sxs-lookup"><span data-stu-id="ba31c-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="ba31c-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="ba31c-132">要安裝的 Azure 檔案共用儲存帳號憑證，使用者名稱是儲存帳戶名稱，而金鑰是儲存帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="ba31c-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="ba31c-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="ba31c-134">Azure 檔案音量的安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="ba31c-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="ba31c-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="ba31c-136">要安裝的 Azure 檔案共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="ba31c-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-137">-命令</span><span class="sxs-lookup"><span data-stu-id="ba31c-137">-Command</span></span>
<span data-ttu-id="ba31c-138">在容器中執行的命令。</span><span class="sxs-lookup"><span data-stu-id="ba31c-138">The command to run in the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-139">-Cpu</span><span class="sxs-lookup"><span data-stu-id="ba31c-139">-Cpu</span></span>
<span data-ttu-id="ba31c-140">必要的 CPU 核心。</span><span class="sxs-lookup"><span data-stu-id="ba31c-140">The required CPU cores.</span></span>
<span data-ttu-id="ba31c-141">預設值：1</span><span class="sxs-lookup"><span data-stu-id="ba31c-141">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba31c-142">-DefaultProfile</span></span>
<span data-ttu-id="ba31c-143">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba31c-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="ba31c-144">-DnsNameLabel</span></span>
<span data-ttu-id="ba31c-145">IP 位址的 DNS 名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="ba31c-145">The DNS name label for the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="ba31c-146">-EnvironmentVariable</span></span>
<span data-ttu-id="ba31c-147">容器環境變數。</span><span class="sxs-lookup"><span data-stu-id="ba31c-147">The container environment variables.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ba31c-148">-IdentityId</span></span>
<span data-ttu-id="ba31c-149">使用者已指派身分識別 ID</span><span class="sxs-lookup"><span data-stu-id="ba31c-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ba31c-150">-IdentityType</span></span>
<span data-ttu-id="ba31c-151">受管理的身分識別類型</span><span class="sxs-lookup"><span data-stu-id="ba31c-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-152">-影像</span><span class="sxs-lookup"><span data-stu-id="ba31c-152">-Image</span></span>
<span data-ttu-id="ba31c-153">容器圖像。</span><span class="sxs-lookup"><span data-stu-id="ba31c-153">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="ba31c-154">-IpAddressType</span></span>
<span data-ttu-id="ba31c-155">IP 位址類型。</span><span class="sxs-lookup"><span data-stu-id="ba31c-155">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-156">-位置</span><span class="sxs-lookup"><span data-stu-id="ba31c-156">-Location</span></span>
<span data-ttu-id="ba31c-157">容器群組位置。</span><span class="sxs-lookup"><span data-stu-id="ba31c-157">The container group Location.</span></span>
<span data-ttu-id="ba31c-158">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="ba31c-158">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="ba31c-159">-MemoryInGB</span></span>
<span data-ttu-id="ba31c-160">所需的記憶體 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="ba31c-160">The required memory in GB.</span></span>
<span data-ttu-id="ba31c-161">預設值：1.5</span><span class="sxs-lookup"><span data-stu-id="ba31c-161">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-162">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba31c-162">-Name</span></span>
<span data-ttu-id="ba31c-163">容器組名。</span><span class="sxs-lookup"><span data-stu-id="ba31c-163">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="ba31c-164">-OsType</span></span>
<span data-ttu-id="ba31c-165">容器作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="ba31c-165">The container OS type.</span></span>
<span data-ttu-id="ba31c-166">預設：Linux</span><span class="sxs-lookup"><span data-stu-id="ba31c-166">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-167">-埠</span><span class="sxs-lookup"><span data-stu-id="ba31c-167">-Port</span></span>
<span data-ttu-id="ba31c-168">埠 () 開啟。</span><span class="sxs-lookup"><span data-stu-id="ba31c-168">The port(s) to open.</span></span> <span data-ttu-id="ba31c-169">預設值：[80]</span><span class="sxs-lookup"><span data-stu-id="ba31c-169">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ba31c-170">-RegistryCredential</span></span>
<span data-ttu-id="ba31c-171">自訂容器登錄認證。</span><span class="sxs-lookup"><span data-stu-id="ba31c-171">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="ba31c-172">-RegistryServerDomain</span></span>
<span data-ttu-id="ba31c-173">自訂容器登錄登入伺服器。</span><span class="sxs-lookup"><span data-stu-id="ba31c-173">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba31c-174">-ResourceGroupName</span></span>
<span data-ttu-id="ba31c-175">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ba31c-175">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="ba31c-176">-RestartPolicy</span></span>
<span data-ttu-id="ba31c-177">容器重新開機政策。</span><span class="sxs-lookup"><span data-stu-id="ba31c-177">The container restart policy.</span></span> <span data-ttu-id="ba31c-178">預設：永遠</span><span class="sxs-lookup"><span data-stu-id="ba31c-178">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-179">-標記</span><span class="sxs-lookup"><span data-stu-id="ba31c-179">-Tag</span></span>
<span data-ttu-id="ba31c-180">{{Fill Tag Description}}</span><span class="sxs-lookup"><span data-stu-id="ba31c-180">{{Fill Tag Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-181">-確認</span><span class="sxs-lookup"><span data-stu-id="ba31c-181">-Confirm</span></span>
<span data-ttu-id="ba31c-182">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ba31c-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba31c-183">-WhatIf</span></span>
<span data-ttu-id="ba31c-184">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba31c-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba31c-185">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba31c-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba31c-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba31c-186">CommonParameters</span></span>
<span data-ttu-id="ba31c-187">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ba31c-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba31c-188">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ba31c-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba31c-189">輸入</span><span class="sxs-lookup"><span data-stu-id="ba31c-189">INPUTS</span></span>

### <span data-ttu-id="ba31c-190">System.String</span><span class="sxs-lookup"><span data-stu-id="ba31c-190">System.String</span></span>

### <span data-ttu-id="ba31c-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ba31c-191">System.String[]</span></span>

### <span data-ttu-id="ba31c-192">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ba31c-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ba31c-193">輸出</span><span class="sxs-lookup"><span data-stu-id="ba31c-193">OUTPUTS</span></span>

### <span data-ttu-id="ba31c-194">Microsoft.Azure.Commands.ContainerInstance.models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ba31c-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="ba31c-195">筆記</span><span class="sxs-lookup"><span data-stu-id="ba31c-195">NOTES</span></span>

## <span data-ttu-id="ba31c-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba31c-196">RELATED LINKS</span></span>
