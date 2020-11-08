---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 20daa8d14f77ca4563c072d58d1c2269235cb164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969830"
---
# <span data-ttu-id="3facf-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="3facf-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="3facf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3facf-102">SYNOPSIS</span></span>
<span data-ttu-id="3facf-103">建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="3facf-103">Creates a container group.</span></span>

## <span data-ttu-id="3facf-104">句法</span><span class="sxs-lookup"><span data-stu-id="3facf-104">SYNTAX</span></span>

### <span data-ttu-id="3facf-105">CreateContainerGroupBaseParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3facf-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3facf-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="3facf-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3facf-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="3facf-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3facf-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="3facf-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3facf-109">說明</span><span class="sxs-lookup"><span data-stu-id="3facf-109">DESCRIPTION</span></span>
<span data-ttu-id="3facf-110">**新的-AzContainerGroup** Cmdlet 會建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="3facf-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="3facf-111">示例</span><span class="sxs-lookup"><span data-stu-id="3facf-111">EXAMPLES</span></span>

### <span data-ttu-id="3facf-112">範例1</span><span class="sxs-lookup"><span data-stu-id="3facf-112">Example 1</span></span>
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

<span data-ttu-id="3facf-113">這個命令會使用最新的 nginx 影像建立容器群組，並以開啟埠8000來要求公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3facf-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="3facf-114">範例2</span><span class="sxs-lookup"><span data-stu-id="3facf-114">Example 2</span></span>
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

<span data-ttu-id="3facf-115">這個命令會建立容器群組，並在容器內執行自訂腳本。</span><span class="sxs-lookup"><span data-stu-id="3facf-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="3facf-116">範例3：建立「完成式容器」群組。</span><span class="sxs-lookup"><span data-stu-id="3facf-116">Example 3: Creates a run-to-completion container group.</span></span>
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

<span data-ttu-id="3facf-117">這個命令會建立列印出「hello」的容器群組，並停止。</span><span class="sxs-lookup"><span data-stu-id="3facf-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="3facf-118">範例4：使用 Azure 容器註冊表中的圖像建立容器群組</span><span class="sxs-lookup"><span data-stu-id="3facf-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
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

<span data-ttu-id="3facf-119">這個命令會在 Azure 分枝 Registry 中使用 nginx 影像來建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="3facf-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="3facf-120">範例5：在自訂容器中使用影像建立容器群組影像註冊表</span><span class="sxs-lookup"><span data-stu-id="3facf-120">Example 5: Creates a container group using image in custom container image registry</span></span>
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

<span data-ttu-id="3facf-121">這個命令會使用自訂容器影像註冊表中的自訂影像來建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="3facf-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="3facf-122">範例6：建立裝載 Azure 檔案磁片的容器群組</span><span class="sxs-lookup"><span data-stu-id="3facf-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
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

<span data-ttu-id="3facf-123">這個命令會建立一個容器群組，以將提供的 Azure 檔案共用載入至 `/mnt/azfile` 。</span><span class="sxs-lookup"><span data-stu-id="3facf-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="3facf-124">範例7</span><span class="sxs-lookup"><span data-stu-id="3facf-124">Example 7</span></span>
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

<span data-ttu-id="3facf-125">這個命令會使用最新的 nginx 影像來建立含系統指派身分識別的容器群組，並要求開啟埠8000的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3facf-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="3facf-126">範例8</span><span class="sxs-lookup"><span data-stu-id="3facf-126">Example 8</span></span>
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

<span data-ttu-id="3facf-127">這個命令會使用最新的 nginx 影像，建立具有系統指派和使用者指派身分識別的容器群組，並要求開啟埠8000的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3facf-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="3facf-128">參數</span><span class="sxs-lookup"><span data-stu-id="3facf-128">PARAMETERS</span></span>

### <span data-ttu-id="3facf-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3facf-129">-AssignIdentity</span></span>
<span data-ttu-id="3facf-130">啟用系統指派的身分識別</span><span class="sxs-lookup"><span data-stu-id="3facf-130">Enable system assigned identity</span></span>

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

### <span data-ttu-id="3facf-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3facf-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="3facf-132">要裝入之 Azure 檔案共用的儲存空間帳號憑證，其中的使用者名稱是儲存帳戶名稱，金鑰是儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="3facf-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

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

### <span data-ttu-id="3facf-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="3facf-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="3facf-134">Azure 檔案卷的安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="3facf-134">The mount path for the Azure File volume.</span></span>

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

### <span data-ttu-id="3facf-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="3facf-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="3facf-136">要裝載之 Azure 檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="3facf-136">The name of the Azure File share to mount.</span></span>

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

### <span data-ttu-id="3facf-137">-Command</span><span class="sxs-lookup"><span data-stu-id="3facf-137">-Command</span></span>
<span data-ttu-id="3facf-138">要在容器中執行的命令。</span><span class="sxs-lookup"><span data-stu-id="3facf-138">The command to run in the container.</span></span>

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

### <span data-ttu-id="3facf-139">-Cpu</span><span class="sxs-lookup"><span data-stu-id="3facf-139">-Cpu</span></span>
<span data-ttu-id="3facf-140">所需的 CPU 核心。</span><span class="sxs-lookup"><span data-stu-id="3facf-140">The required CPU cores.</span></span>
<span data-ttu-id="3facf-141">預設值：1</span><span class="sxs-lookup"><span data-stu-id="3facf-141">Default: 1</span></span>

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

### <span data-ttu-id="3facf-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3facf-142">-DefaultProfile</span></span>
<span data-ttu-id="3facf-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3facf-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3facf-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="3facf-144">-DnsNameLabel</span></span>
<span data-ttu-id="3facf-145">IP 位址的 DNS 名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="3facf-145">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="3facf-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="3facf-146">-EnvironmentVariable</span></span>
<span data-ttu-id="3facf-147">容器環境變數。</span><span class="sxs-lookup"><span data-stu-id="3facf-147">The container environment variables.</span></span>

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

### <span data-ttu-id="3facf-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="3facf-148">-IdentityId</span></span>
<span data-ttu-id="3facf-149">指派身分識別識別碼的使用者</span><span class="sxs-lookup"><span data-stu-id="3facf-149">The user assigned identity IDs</span></span>

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

### <span data-ttu-id="3facf-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3facf-150">-IdentityType</span></span>
<span data-ttu-id="3facf-151">受管理的身分識別類型</span><span class="sxs-lookup"><span data-stu-id="3facf-151">The managed identity type</span></span>

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

### <span data-ttu-id="3facf-152">-影像</span><span class="sxs-lookup"><span data-stu-id="3facf-152">-Image</span></span>
<span data-ttu-id="3facf-153">容器影像。</span><span class="sxs-lookup"><span data-stu-id="3facf-153">The container image.</span></span>

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

### <span data-ttu-id="3facf-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="3facf-154">-IpAddressType</span></span>
<span data-ttu-id="3facf-155">IP 位址類型。</span><span class="sxs-lookup"><span data-stu-id="3facf-155">The IP address type.</span></span>

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

### <span data-ttu-id="3facf-156">-位置</span><span class="sxs-lookup"><span data-stu-id="3facf-156">-Location</span></span>
<span data-ttu-id="3facf-157">容器群組位置。</span><span class="sxs-lookup"><span data-stu-id="3facf-157">The container group Location.</span></span>
<span data-ttu-id="3facf-158">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="3facf-158">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="3facf-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="3facf-159">-MemoryInGB</span></span>
<span data-ttu-id="3facf-160">所需的記憶體（GB）。</span><span class="sxs-lookup"><span data-stu-id="3facf-160">The required memory in GB.</span></span>
<span data-ttu-id="3facf-161">預設：1。5</span><span class="sxs-lookup"><span data-stu-id="3facf-161">Default: 1.5</span></span>

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

### <span data-ttu-id="3facf-162">-名稱</span><span class="sxs-lookup"><span data-stu-id="3facf-162">-Name</span></span>
<span data-ttu-id="3facf-163">容器組名。</span><span class="sxs-lookup"><span data-stu-id="3facf-163">The container group name.</span></span>

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

### <span data-ttu-id="3facf-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="3facf-164">-OsType</span></span>
<span data-ttu-id="3facf-165">容器 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="3facf-165">The container OS type.</span></span>
<span data-ttu-id="3facf-166">預設值： Linux</span><span class="sxs-lookup"><span data-stu-id="3facf-166">Default: Linux</span></span>

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

### <span data-ttu-id="3facf-167">-埠</span><span class="sxs-lookup"><span data-stu-id="3facf-167">-Port</span></span>
<span data-ttu-id="3facf-168">) 要開啟的埠 (s。</span><span class="sxs-lookup"><span data-stu-id="3facf-168">The port(s) to open.</span></span> <span data-ttu-id="3facf-169">預設值： [80]</span><span class="sxs-lookup"><span data-stu-id="3facf-169">Default: [80]</span></span>

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

### <span data-ttu-id="3facf-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="3facf-170">-RegistryCredential</span></span>
<span data-ttu-id="3facf-171">自訂容器登錄認證。</span><span class="sxs-lookup"><span data-stu-id="3facf-171">The custom container registry credential.</span></span>

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

### <span data-ttu-id="3facf-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="3facf-172">-RegistryServerDomain</span></span>
<span data-ttu-id="3facf-173">自訂容器登錄伺服器。</span><span class="sxs-lookup"><span data-stu-id="3facf-173">The custom container registry login server.</span></span>

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

### <span data-ttu-id="3facf-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3facf-174">-ResourceGroupName</span></span>
<span data-ttu-id="3facf-175">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3facf-175">The resource group name.</span></span>

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

### <span data-ttu-id="3facf-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="3facf-176">-RestartPolicy</span></span>
<span data-ttu-id="3facf-177">容器重新開機原則。</span><span class="sxs-lookup"><span data-stu-id="3facf-177">The container restart policy.</span></span> <span data-ttu-id="3facf-178">預設： Always</span><span class="sxs-lookup"><span data-stu-id="3facf-178">Default: Always</span></span>

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

### <span data-ttu-id="3facf-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="3facf-179">-Tag</span></span>
<span data-ttu-id="3facf-180">{{Fill 標記描述}}</span><span class="sxs-lookup"><span data-stu-id="3facf-180">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="3facf-181">-確認</span><span class="sxs-lookup"><span data-stu-id="3facf-181">-Confirm</span></span>
<span data-ttu-id="3facf-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3facf-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3facf-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3facf-183">-WhatIf</span></span>
<span data-ttu-id="3facf-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3facf-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3facf-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3facf-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3facf-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3facf-186">CommonParameters</span></span>
<span data-ttu-id="3facf-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3facf-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3facf-188">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3facf-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3facf-189">輸入</span><span class="sxs-lookup"><span data-stu-id="3facf-189">INPUTS</span></span>

### <span data-ttu-id="3facf-190">System.object</span><span class="sxs-lookup"><span data-stu-id="3facf-190">System.String</span></span>

### <span data-ttu-id="3facf-191">System.object []</span><span class="sxs-lookup"><span data-stu-id="3facf-191">System.String[]</span></span>

### <span data-ttu-id="3facf-192">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3facf-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3facf-193">輸出</span><span class="sxs-lookup"><span data-stu-id="3facf-193">OUTPUTS</span></span>

### <span data-ttu-id="3facf-194">PSContainerGroup 中的 ContainerInstance。</span><span class="sxs-lookup"><span data-stu-id="3facf-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="3facf-195">筆記</span><span class="sxs-lookup"><span data-stu-id="3facf-195">NOTES</span></span>

## <span data-ttu-id="3facf-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="3facf-196">RELATED LINKS</span></span>
