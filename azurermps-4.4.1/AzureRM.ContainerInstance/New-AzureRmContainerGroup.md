---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 63c54c5f1bb17af82e353b70e757bf91b1208958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453572"
---
# <span data-ttu-id="d72dd-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="d72dd-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="d72dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d72dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d72dd-103">建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="d72dd-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d72dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="d72dd-104">SYNTAX</span></span>

### <span data-ttu-id="d72dd-105">CreateContainerGroupBaseParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d72dd-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d72dd-106">CreateContainerGroupWithRegistryParamSet</span><span class="sxs-lookup"><span data-stu-id="d72dd-106">CreateContainerGroupWithRegistryParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>]
 -RegistryCredential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d72dd-107">說明</span><span class="sxs-lookup"><span data-stu-id="d72dd-107">DESCRIPTION</span></span>
<span data-ttu-id="d72dd-108">**新的-AzureRmContainerGroup** Cmdlet 會建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="d72dd-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="d72dd-109">示例</span><span class="sxs-lookup"><span data-stu-id="d72dd-109">EXAMPLES</span></span>

### <span data-ttu-id="d72dd-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d72dd-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port 8000

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
```

<span data-ttu-id="d72dd-111">這個命令會使用最新的 nginx 影像建立容器群組，並以開啟埠8000來要求公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d72dd-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="d72dd-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d72dd-112">Example 2</span></span>
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
```

<span data-ttu-id="d72dd-113">這個命令會建立容器群組，並在容器內執行自訂腳本。</span><span class="sxs-lookup"><span data-stu-id="d72dd-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="d72dd-114">範例3：使用 Azure 容器註冊表中的圖像建立容器群組</span><span class="sxs-lookup"><span data-stu-id="d72dd-114">Example 3: Creates a container group using image in Azure Container Registry</span></span>
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
```

<span data-ttu-id="d72dd-115">這個命令會在 Azure 分枝 Registry 中使用 nginx 影像來建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="d72dd-115">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="d72dd-116">範例4：在自訂容器中使用影像建立容器群組影像註冊表</span><span class="sxs-lookup"><span data-stu-id="d72dd-116">Example 4: Creates a container group using image in custom container image registry</span></span>
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
```

<span data-ttu-id="d72dd-117">這個命令會使用自訂容器影像註冊表中的自訂影像來建立容器群組。</span><span class="sxs-lookup"><span data-stu-id="d72dd-117">This commands creates a container group using a custom image from a custom container image registry.</span></span>

## <span data-ttu-id="d72dd-118">參數</span><span class="sxs-lookup"><span data-stu-id="d72dd-118">PARAMETERS</span></span>

### <span data-ttu-id="d72dd-119">-Command</span><span class="sxs-lookup"><span data-stu-id="d72dd-119">-Command</span></span>
<span data-ttu-id="d72dd-120">要在容器中執行的命令。</span><span class="sxs-lookup"><span data-stu-id="d72dd-120">The command to run in the container.</span></span>

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

### <span data-ttu-id="d72dd-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d72dd-121">-Confirm</span></span>
<span data-ttu-id="d72dd-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d72dd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d72dd-123">-Cpu</span><span class="sxs-lookup"><span data-stu-id="d72dd-123">-Cpu</span></span>
<span data-ttu-id="d72dd-124">所需的 CPU 核心。</span><span class="sxs-lookup"><span data-stu-id="d72dd-124">The required CPU cores.</span></span>
<span data-ttu-id="d72dd-125">預設值：1</span><span class="sxs-lookup"><span data-stu-id="d72dd-125">Default: 1</span></span>

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

### <span data-ttu-id="d72dd-126">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="d72dd-126">-EnvironmentVariable</span></span>
<span data-ttu-id="d72dd-127">容器環境變數。</span><span class="sxs-lookup"><span data-stu-id="d72dd-127">The container environment variables.</span></span>

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

### <span data-ttu-id="d72dd-128">-影像</span><span class="sxs-lookup"><span data-stu-id="d72dd-128">-Image</span></span>
<span data-ttu-id="d72dd-129">容器影像。</span><span class="sxs-lookup"><span data-stu-id="d72dd-129">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72dd-130">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="d72dd-130">-IpAddressType</span></span>
<span data-ttu-id="d72dd-131">IP 位址類型。</span><span class="sxs-lookup"><span data-stu-id="d72dd-131">The IP address type.</span></span>

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

### <span data-ttu-id="d72dd-132">-位置</span><span class="sxs-lookup"><span data-stu-id="d72dd-132">-Location</span></span>
<span data-ttu-id="d72dd-133">容器群組位置。</span><span class="sxs-lookup"><span data-stu-id="d72dd-133">The container group Location.</span></span>
<span data-ttu-id="d72dd-134">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="d72dd-134">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="d72dd-135">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="d72dd-135">-MemoryInGB</span></span>
<span data-ttu-id="d72dd-136">所需的記憶體（GB）。</span><span class="sxs-lookup"><span data-stu-id="d72dd-136">The required memory in GB.</span></span>
<span data-ttu-id="d72dd-137">預設：1。5</span><span class="sxs-lookup"><span data-stu-id="d72dd-137">Default: 1.5</span></span>

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

### <span data-ttu-id="d72dd-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="d72dd-138">-Name</span></span>
<span data-ttu-id="d72dd-139">容器組名。</span><span class="sxs-lookup"><span data-stu-id="d72dd-139">The container group name.</span></span>

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

### <span data-ttu-id="d72dd-140">-OsType</span><span class="sxs-lookup"><span data-stu-id="d72dd-140">-OsType</span></span>
<span data-ttu-id="d72dd-141">容器 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="d72dd-141">The container OS type.</span></span>
<span data-ttu-id="d72dd-142">預設值： Linux</span><span class="sxs-lookup"><span data-stu-id="d72dd-142">Default: Linux</span></span>

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

### <span data-ttu-id="d72dd-143">-埠</span><span class="sxs-lookup"><span data-stu-id="d72dd-143">-Port</span></span>
<span data-ttu-id="d72dd-144">要開啟的埠。</span><span class="sxs-lookup"><span data-stu-id="d72dd-144">The port to open.</span></span>
<span data-ttu-id="d72dd-145">預設：80</span><span class="sxs-lookup"><span data-stu-id="d72dd-145">Default: 80</span></span>

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

### <span data-ttu-id="d72dd-146">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="d72dd-146">-RegistryCredential</span></span>
<span data-ttu-id="d72dd-147">自訂容器登錄認證。</span><span class="sxs-lookup"><span data-stu-id="d72dd-147">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72dd-148">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="d72dd-148">-RegistryServerDomain</span></span>
<span data-ttu-id="d72dd-149">自訂容器登錄伺服器。</span><span class="sxs-lookup"><span data-stu-id="d72dd-149">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72dd-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72dd-150">-ResourceGroupName</span></span>
<span data-ttu-id="d72dd-151">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d72dd-151">The resource group name.</span></span>

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

### <span data-ttu-id="d72dd-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="d72dd-152">-Tag</span></span>
<span data-ttu-id="d72dd-153">{{Fill 標記描述}}</span><span class="sxs-lookup"><span data-stu-id="d72dd-153">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="d72dd-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72dd-154">-WhatIf</span></span>
<span data-ttu-id="d72dd-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d72dd-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72dd-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d72dd-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d72dd-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72dd-157">-DefaultProfile</span></span>
<span data-ttu-id="d72dd-158">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d72dd-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d72dd-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72dd-159">CommonParameters</span></span>
<span data-ttu-id="d72dd-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d72dd-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72dd-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d72dd-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72dd-162">輸入</span><span class="sxs-lookup"><span data-stu-id="d72dd-162">INPUTS</span></span>

### <span data-ttu-id="d72dd-163">System.object</span><span class="sxs-lookup"><span data-stu-id="d72dd-163">System.String</span></span>
<span data-ttu-id="d72dd-164">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d72dd-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d72dd-165">輸出</span><span class="sxs-lookup"><span data-stu-id="d72dd-165">OUTPUTS</span></span>

### <span data-ttu-id="d72dd-166">PSContainerGroup 中的 ContainerInstance。</span><span class="sxs-lookup"><span data-stu-id="d72dd-166">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="d72dd-167">筆記</span><span class="sxs-lookup"><span data-stu-id="d72dd-167">NOTES</span></span>

## <span data-ttu-id="d72dd-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="d72dd-168">RELATED LINKS</span></span>

