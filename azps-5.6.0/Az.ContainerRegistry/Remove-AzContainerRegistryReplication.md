---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 3fff7a0952f4ace41f76237a8fbf226e9bb58128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917766"
---
# <span data-ttu-id="462d3-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="462d3-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="462d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="462d3-102">SYNOPSIS</span></span>
<span data-ttu-id="462d3-103">移除容器註冊表複製。</span><span class="sxs-lookup"><span data-stu-id="462d3-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="462d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="462d3-104">SYNTAX</span></span>

### <span data-ttu-id="462d3-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="462d3-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="462d3-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="462d3-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="462d3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="462d3-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="462d3-108">描述</span><span class="sxs-lookup"><span data-stu-id="462d3-108">DESCRIPTION</span></span>
<span data-ttu-id="462d3-109">Cmdlet Remove-AzContainerRegistryReplication移除容器註冊表複製。</span><span class="sxs-lookup"><span data-stu-id="462d3-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="462d3-110">例子</span><span class="sxs-lookup"><span data-stu-id="462d3-110">EXAMPLES</span></span>

### <span data-ttu-id="462d3-111">範例 1：移除容器註冊表複製。</span><span class="sxs-lookup"><span data-stu-id="462d3-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="462d3-112">移除容器註冊表複製。</span><span class="sxs-lookup"><span data-stu-id="462d3-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="462d3-113">參數</span><span class="sxs-lookup"><span data-stu-id="462d3-113">PARAMETERS</span></span>

### <span data-ttu-id="462d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462d3-114">-DefaultProfile</span></span>
<span data-ttu-id="462d3-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="462d3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="462d3-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="462d3-116">-Name</span></span>
<span data-ttu-id="462d3-117">容器註冊表複製名稱。</span><span class="sxs-lookup"><span data-stu-id="462d3-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="462d3-118">預設為位置名稱。</span><span class="sxs-lookup"><span data-stu-id="462d3-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462d3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="462d3-119">-PassThru</span></span>
<span data-ttu-id="462d3-120">表示移除成功時，此 Cmdlet 會返回 True。</span><span class="sxs-lookup"><span data-stu-id="462d3-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462d3-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="462d3-121">-RegistryName</span></span>
<span data-ttu-id="462d3-122">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="462d3-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462d3-123">-複製</span><span class="sxs-lookup"><span data-stu-id="462d3-123">-Replication</span></span>
<span data-ttu-id="462d3-124">Container Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="462d3-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="462d3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="462d3-125">-ResourceGroupName</span></span>
<span data-ttu-id="462d3-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="462d3-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462d3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="462d3-127">-ResourceId</span></span>
<span data-ttu-id="462d3-128">容器登錄複製資源識別碼</span><span class="sxs-lookup"><span data-stu-id="462d3-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="462d3-129">-確認</span><span class="sxs-lookup"><span data-stu-id="462d3-129">-Confirm</span></span>
<span data-ttu-id="462d3-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="462d3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="462d3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="462d3-131">-WhatIf</span></span>
<span data-ttu-id="462d3-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="462d3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="462d3-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="462d3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="462d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462d3-134">CommonParameters</span></span>
<span data-ttu-id="462d3-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="462d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462d3-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="462d3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462d3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="462d3-137">INPUTS</span></span>

### <span data-ttu-id="462d3-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="462d3-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="462d3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="462d3-139">System.String</span></span>

## <span data-ttu-id="462d3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="462d3-140">OUTPUTS</span></span>

### <span data-ttu-id="462d3-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="462d3-141">System.Boolean</span></span>

## <span data-ttu-id="462d3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="462d3-142">NOTES</span></span>

## <span data-ttu-id="462d3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="462d3-143">RELATED LINKS</span></span>

[<span data-ttu-id="462d3-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="462d3-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="462d3-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="462d3-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

