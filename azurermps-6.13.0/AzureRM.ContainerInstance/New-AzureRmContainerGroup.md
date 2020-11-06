---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 1823759b72bdb3162164068732f3a8201fcfb589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445640"
---
# <span data-ttu-id="25640-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="25640-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="25640-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25640-102">SYNOPSIS</span></span>
<span data-ttu-id="25640-103">建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="25640-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25640-104">句法</span><span class="sxs-lookup"><span data-stu-id="25640-104">SYNTAX</span></span>

### <span data-ttu-id="25640-105">CreateContainerGroupBaseParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="25640-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25640-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="25640-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25640-107">說明</span><span class="sxs-lookup"><span data-stu-id="25640-107">DESCRIPTION</span></span>
<span data-ttu-id="25640-108">**新的-AzureRmContainerGroup** Cmdlet 會建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="25640-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="25640-109">示例</span><span class="sxs-lookup"><span data-stu-id="25640-109">EXAMPLES</span></span>

### <span data-ttu-id="25640-110">範例1</span><span class="sxs-lookup"><span data-stu-id="25640-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

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

<span data-ttu-id="25640-111">這個命令會使用最新的 nginx 影像建立容器群組，並以開啟埠8000來要求公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="25640-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="25640-112">範例2</span><span class="sxs-lookup"><span data-stu-id="25640-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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

<span data-ttu-id="25640-113">這個命令會建立容器群組，並在容器內執行自訂腳本。</span><span class="sxs-lookup"><span data-stu-id="25640-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="25640-114">範例3：建立「完成式容器」群組。</span><span class="sxs-lookup"><span data-stu-id="25640-114">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

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

<span data-ttu-id="25640-115">這個命令會建立列印出「hello」的容器群組，並停止。</span><span class="sxs-lookup"><span data-stu-id="25640-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="25640-116">範例4：使用 Azure 容器註冊表中的圖像建立容器群組</span><span class="sxs-lookup"><span data-stu-id="25640-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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

<span data-ttu-id="25640-117">這個命令會在 Azure 分枝 Registry 中使用 nginx 影像來建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="25640-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="25640-118">範例5：在自訂容器中使用影像建立容器群組影像註冊表</span><span class="sxs-lookup"><span data-stu-id="25640-118">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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

<span data-ttu-id="25640-119">這個命令會使用自訂容器影像註冊表中的自訂影像來建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="25640-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="25640-120">範例6：建立裝載 Azure 檔案磁片的容器群組</span><span class="sxs-lookup"><span data-stu-id="25640-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountKey $mycred -AzureFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="25640-121">這個命令會建立一個容器群組，以將提供的 Azure 檔案共用載入至 `/mnt/azfile` 。</span><span class="sxs-lookup"><span data-stu-id="25640-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="25640-122">參數</span><span class="sxs-lookup"><span data-stu-id="25640-122">PARAMETERS</span></span>

### <span data-ttu-id="25640-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="25640-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="25640-124">要裝入之 Azure 檔案共用的儲存空間帳號憑證，其中的使用者名稱是儲存帳戶名稱，金鑰是儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="25640-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25640-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="25640-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="25640-126">Azure 檔案卷的安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="25640-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25640-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="25640-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="25640-128">要裝載之 Azure 檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="25640-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25640-129">-Command</span><span class="sxs-lookup"><span data-stu-id="25640-129">-Command</span></span>
<span data-ttu-id="25640-130">要在容器中執行的命令。</span><span class="sxs-lookup"><span data-stu-id="25640-130">The command to run in the container.</span></span>

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

### <span data-ttu-id="25640-131">-Cpu</span><span class="sxs-lookup"><span data-stu-id="25640-131">-Cpu</span></span>
<span data-ttu-id="25640-132">所需的 CPU 核心。</span><span class="sxs-lookup"><span data-stu-id="25640-132">The required CPU cores.</span></span>
<span data-ttu-id="25640-133">預設值：1</span><span class="sxs-lookup"><span data-stu-id="25640-133">Default: 1</span></span>

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

### <span data-ttu-id="25640-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25640-134">-DefaultProfile</span></span>
<span data-ttu-id="25640-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25640-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25640-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="25640-136">-DnsNameLabel</span></span>
<span data-ttu-id="25640-137">IP 位址的 DNS 名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="25640-137">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="25640-138">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="25640-138">-EnvironmentVariable</span></span>
<span data-ttu-id="25640-139">容器環境變數。</span><span class="sxs-lookup"><span data-stu-id="25640-139">The container environment variables.</span></span>

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

### <span data-ttu-id="25640-140">-影像</span><span class="sxs-lookup"><span data-stu-id="25640-140">-Image</span></span>
<span data-ttu-id="25640-141">容器影像。</span><span class="sxs-lookup"><span data-stu-id="25640-141">The container image.</span></span>

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

### <span data-ttu-id="25640-142">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="25640-142">-IpAddressType</span></span>
<span data-ttu-id="25640-143">IP 位址類型。</span><span class="sxs-lookup"><span data-stu-id="25640-143">The IP address type.</span></span>

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

### <span data-ttu-id="25640-144">-位置</span><span class="sxs-lookup"><span data-stu-id="25640-144">-Location</span></span>
<span data-ttu-id="25640-145">容器群組位置。</span><span class="sxs-lookup"><span data-stu-id="25640-145">The container group Location.</span></span>
<span data-ttu-id="25640-146">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="25640-146">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="25640-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="25640-147">-MemoryInGB</span></span>
<span data-ttu-id="25640-148">所需的記憶體（GB）。</span><span class="sxs-lookup"><span data-stu-id="25640-148">The required memory in GB.</span></span>
<span data-ttu-id="25640-149">預設：1。5</span><span class="sxs-lookup"><span data-stu-id="25640-149">Default: 1.5</span></span>

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

### <span data-ttu-id="25640-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="25640-150">-Name</span></span>
<span data-ttu-id="25640-151">容器組名。</span><span class="sxs-lookup"><span data-stu-id="25640-151">The container group name.</span></span>

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

### <span data-ttu-id="25640-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="25640-152">-OsType</span></span>
<span data-ttu-id="25640-153">容器 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="25640-153">The container OS type.</span></span>
<span data-ttu-id="25640-154">預設值： Linux</span><span class="sxs-lookup"><span data-stu-id="25640-154">Default: Linux</span></span>

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

### <span data-ttu-id="25640-155">-埠</span><span class="sxs-lookup"><span data-stu-id="25640-155">-Port</span></span>
<span data-ttu-id="25640-156">) 要開啟的埠 (s。</span><span class="sxs-lookup"><span data-stu-id="25640-156">The port(s) to open.</span></span> <span data-ttu-id="25640-157">預設值： [80]</span><span class="sxs-lookup"><span data-stu-id="25640-157">Default: [80]</span></span>

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

### <span data-ttu-id="25640-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="25640-158">-RegistryCredential</span></span>
<span data-ttu-id="25640-159">自訂容器登錄認證。</span><span class="sxs-lookup"><span data-stu-id="25640-159">The custom container registry credential.</span></span>

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

### <span data-ttu-id="25640-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="25640-160">-RegistryServerDomain</span></span>
<span data-ttu-id="25640-161">自訂容器登錄伺服器。</span><span class="sxs-lookup"><span data-stu-id="25640-161">The custom container registry login server.</span></span>

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

### <span data-ttu-id="25640-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25640-162">-ResourceGroupName</span></span>
<span data-ttu-id="25640-163">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25640-163">The resource group name.</span></span>

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

### <span data-ttu-id="25640-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="25640-164">-RestartPolicy</span></span>
<span data-ttu-id="25640-165">容器重新開機原則。</span><span class="sxs-lookup"><span data-stu-id="25640-165">The container restart policy.</span></span> <span data-ttu-id="25640-166">預設： Always</span><span class="sxs-lookup"><span data-stu-id="25640-166">Default: Always</span></span>

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

### <span data-ttu-id="25640-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="25640-167">-Tag</span></span>
<span data-ttu-id="25640-168">{{Fill 標記描述}}</span><span class="sxs-lookup"><span data-stu-id="25640-168">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="25640-169">-確認</span><span class="sxs-lookup"><span data-stu-id="25640-169">-Confirm</span></span>
<span data-ttu-id="25640-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25640-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25640-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25640-171">-WhatIf</span></span>
<span data-ttu-id="25640-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25640-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25640-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25640-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25640-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25640-174">CommonParameters</span></span>
<span data-ttu-id="25640-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25640-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25640-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25640-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25640-177">輸入</span><span class="sxs-lookup"><span data-stu-id="25640-177">INPUTS</span></span>

### <span data-ttu-id="25640-178">System.object</span><span class="sxs-lookup"><span data-stu-id="25640-178">System.String</span></span>

### <span data-ttu-id="25640-179">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="25640-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="25640-180">輸出</span><span class="sxs-lookup"><span data-stu-id="25640-180">OUTPUTS</span></span>

### <span data-ttu-id="25640-181">PSContainerGroup 中的 ContainerInstance。</span><span class="sxs-lookup"><span data-stu-id="25640-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="25640-182">筆記</span><span class="sxs-lookup"><span data-stu-id="25640-182">NOTES</span></span>

## <span data-ttu-id="25640-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="25640-183">RELATED LINKS</span></span>
