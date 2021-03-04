---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: a446fe34ba29789e93e8907d3155af654a93ff21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913257"
---
# <span data-ttu-id="910bd-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="910bd-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="910bd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="910bd-102">SYNOPSIS</span></span>
<span data-ttu-id="910bd-103">建立容器註冊表複製。</span><span class="sxs-lookup"><span data-stu-id="910bd-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="910bd-104">語法</span><span class="sxs-lookup"><span data-stu-id="910bd-104">SYNTAX</span></span>

### <span data-ttu-id="910bd-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="910bd-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="910bd-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="910bd-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="910bd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="910bd-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="910bd-108">描述</span><span class="sxs-lookup"><span data-stu-id="910bd-108">DESCRIPTION</span></span>
<span data-ttu-id="910bd-109">此New-AzContainerRegistryReplication Cmdlet 會建立新的容器註冊表複製。</span><span class="sxs-lookup"><span data-stu-id="910bd-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="910bd-110">例子</span><span class="sxs-lookup"><span data-stu-id="910bd-110">EXAMPLES</span></span>

### <span data-ttu-id="910bd-111">範例 1：建立新容器註冊表複製。</span><span class="sxs-lookup"><span data-stu-id="910bd-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="910bd-112">建立新容器註冊表複製。</span><span class="sxs-lookup"><span data-stu-id="910bd-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="910bd-113">參數</span><span class="sxs-lookup"><span data-stu-id="910bd-113">PARAMETERS</span></span>

### <span data-ttu-id="910bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910bd-114">-DefaultProfile</span></span>
<span data-ttu-id="910bd-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="910bd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="910bd-116">-位置</span><span class="sxs-lookup"><span data-stu-id="910bd-116">-Location</span></span>
<span data-ttu-id="910bd-117">容器註冊表位置。</span><span class="sxs-lookup"><span data-stu-id="910bd-117">Container Registry Location.</span></span>
<span data-ttu-id="910bd-118">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="910bd-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="910bd-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="910bd-119">-Name</span></span>
<span data-ttu-id="910bd-120">容器註冊表複製名稱。</span><span class="sxs-lookup"><span data-stu-id="910bd-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="910bd-121">預設為位置名稱。</span><span class="sxs-lookup"><span data-stu-id="910bd-121">Default to the location name.</span></span>

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

### <span data-ttu-id="910bd-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="910bd-122">-Registry</span></span>
<span data-ttu-id="910bd-123">Container Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="910bd-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="910bd-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="910bd-124">-RegistryName</span></span>
<span data-ttu-id="910bd-125">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="910bd-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="910bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="910bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="910bd-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="910bd-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="910bd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="910bd-128">-ResourceId</span></span>
<span data-ttu-id="910bd-129">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="910bd-129">The container registry resource id</span></span>

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

### <span data-ttu-id="910bd-130">-標記</span><span class="sxs-lookup"><span data-stu-id="910bd-130">-Tag</span></span>
<span data-ttu-id="910bd-131">容器註冊表標記。</span><span class="sxs-lookup"><span data-stu-id="910bd-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="910bd-132">-確認</span><span class="sxs-lookup"><span data-stu-id="910bd-132">-Confirm</span></span>
<span data-ttu-id="910bd-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="910bd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="910bd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="910bd-134">-WhatIf</span></span>
<span data-ttu-id="910bd-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="910bd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="910bd-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="910bd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="910bd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910bd-137">CommonParameters</span></span>
<span data-ttu-id="910bd-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="910bd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910bd-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="910bd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910bd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="910bd-140">INPUTS</span></span>

### <span data-ttu-id="910bd-141">System.String</span><span class="sxs-lookup"><span data-stu-id="910bd-141">System.String</span></span>

## <span data-ttu-id="910bd-142">輸出</span><span class="sxs-lookup"><span data-stu-id="910bd-142">OUTPUTS</span></span>

### <span data-ttu-id="910bd-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="910bd-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="910bd-144">筆記</span><span class="sxs-lookup"><span data-stu-id="910bd-144">NOTES</span></span>

## <span data-ttu-id="910bd-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="910bd-145">RELATED LINKS</span></span>

[<span data-ttu-id="910bd-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="910bd-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="910bd-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="910bd-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)