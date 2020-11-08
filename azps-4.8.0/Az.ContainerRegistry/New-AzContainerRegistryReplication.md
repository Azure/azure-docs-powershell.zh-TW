---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128337"
---
# <span data-ttu-id="a228e-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a228e-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="a228e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a228e-102">SYNOPSIS</span></span>
<span data-ttu-id="a228e-103">建立容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="a228e-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="a228e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a228e-104">SYNTAX</span></span>

### <span data-ttu-id="a228e-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a228e-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a228e-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a228e-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a228e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a228e-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a228e-108">說明</span><span class="sxs-lookup"><span data-stu-id="a228e-108">DESCRIPTION</span></span>
<span data-ttu-id="a228e-109">New-AzContainerRegistryReplication Cmdlet 會建立新的容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="a228e-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="a228e-110">示例</span><span class="sxs-lookup"><span data-stu-id="a228e-110">EXAMPLES</span></span>

### <span data-ttu-id="a228e-111">範例1：建立新的容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="a228e-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="a228e-112">建立新的容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="a228e-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="a228e-113">參數</span><span class="sxs-lookup"><span data-stu-id="a228e-113">PARAMETERS</span></span>

### <span data-ttu-id="a228e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a228e-114">-DefaultProfile</span></span>
<span data-ttu-id="a228e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a228e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a228e-116">-位置</span><span class="sxs-lookup"><span data-stu-id="a228e-116">-Location</span></span>
<span data-ttu-id="a228e-117">容器登錄位置。</span><span class="sxs-lookup"><span data-stu-id="a228e-117">Container Registry Location.</span></span>
<span data-ttu-id="a228e-118">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="a228e-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a228e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a228e-119">-Name</span></span>
<span data-ttu-id="a228e-120">容器登錄複製名稱。</span><span class="sxs-lookup"><span data-stu-id="a228e-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="a228e-121">預設為位置名稱。</span><span class="sxs-lookup"><span data-stu-id="a228e-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a228e-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="a228e-122">-Registry</span></span>
<span data-ttu-id="a228e-123">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="a228e-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a228e-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="a228e-124">-RegistryName</span></span>
<span data-ttu-id="a228e-125">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="a228e-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a228e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a228e-126">-ResourceGroupName</span></span>
<span data-ttu-id="a228e-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a228e-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a228e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a228e-128">-ResourceId</span></span>
<span data-ttu-id="a228e-129">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a228e-129">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a228e-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a228e-130">-Tag</span></span>
<span data-ttu-id="a228e-131">容器登錄標記。</span><span class="sxs-lookup"><span data-stu-id="a228e-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a228e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a228e-132">-Confirm</span></span>
<span data-ttu-id="a228e-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a228e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a228e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a228e-134">-WhatIf</span></span>
<span data-ttu-id="a228e-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a228e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a228e-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a228e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a228e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a228e-137">CommonParameters</span></span>
<span data-ttu-id="a228e-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a228e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a228e-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a228e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a228e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a228e-140">INPUTS</span></span>

### <span data-ttu-id="a228e-141">System.object</span><span class="sxs-lookup"><span data-stu-id="a228e-141">System.String</span></span>

## <span data-ttu-id="a228e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a228e-142">OUTPUTS</span></span>

### <span data-ttu-id="a228e-143">PSContainerRegistryReplication 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a228e-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="a228e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a228e-144">NOTES</span></span>

## <span data-ttu-id="a228e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a228e-145">RELATED LINKS</span></span>

[<span data-ttu-id="a228e-146">AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a228e-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="a228e-147">移除-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a228e-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)