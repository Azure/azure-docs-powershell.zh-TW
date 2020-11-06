---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 717e1ecd7b2242ee5643ca80883e472f5ea4a3c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613059"
---
# <span data-ttu-id="ae13a-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ae13a-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="ae13a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae13a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae13a-103">移除容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="ae13a-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="ae13a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae13a-104">SYNTAX</span></span>

### <span data-ttu-id="ae13a-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ae13a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae13a-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae13a-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae13a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae13a-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae13a-108">說明</span><span class="sxs-lookup"><span data-stu-id="ae13a-108">DESCRIPTION</span></span>
<span data-ttu-id="ae13a-109">Remove-AzContainerRegistryReplication Cmdlet 會移除容器註冊複本。</span><span class="sxs-lookup"><span data-stu-id="ae13a-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="ae13a-110">示例</span><span class="sxs-lookup"><span data-stu-id="ae13a-110">EXAMPLES</span></span>

### <span data-ttu-id="ae13a-111">範例1：移除容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="ae13a-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="ae13a-112">移除容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="ae13a-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="ae13a-113">參數</span><span class="sxs-lookup"><span data-stu-id="ae13a-113">PARAMETERS</span></span>

### <span data-ttu-id="ae13a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae13a-114">-DefaultProfile</span></span>
<span data-ttu-id="ae13a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae13a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae13a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae13a-116">-Name</span></span>
<span data-ttu-id="ae13a-117">容器登錄複製名稱。</span><span class="sxs-lookup"><span data-stu-id="ae13a-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="ae13a-118">預設為位置名稱。</span><span class="sxs-lookup"><span data-stu-id="ae13a-118">Default to the location name.</span></span>

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

### <span data-ttu-id="ae13a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae13a-119">-PassThru</span></span>
<span data-ttu-id="ae13a-120">表示如果移除成功，此 Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="ae13a-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="ae13a-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ae13a-121">-RegistryName</span></span>
<span data-ttu-id="ae13a-122">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="ae13a-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="ae13a-123">-複製</span><span class="sxs-lookup"><span data-stu-id="ae13a-123">-Replication</span></span>
<span data-ttu-id="ae13a-124">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="ae13a-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="ae13a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae13a-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae13a-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ae13a-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="ae13a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae13a-127">-ResourceId</span></span>
<span data-ttu-id="ae13a-128">容器登錄複製資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ae13a-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="ae13a-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ae13a-129">-Confirm</span></span>
<span data-ttu-id="ae13a-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae13a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae13a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae13a-131">-WhatIf</span></span>
<span data-ttu-id="ae13a-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae13a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae13a-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae13a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae13a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae13a-134">CommonParameters</span></span>
<span data-ttu-id="ae13a-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae13a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae13a-136">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ae13a-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae13a-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ae13a-137">INPUTS</span></span>

### <span data-ttu-id="ae13a-138">PSContainerRegistryReplication 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae13a-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="ae13a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="ae13a-139">System.String</span></span>

## <span data-ttu-id="ae13a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ae13a-140">OUTPUTS</span></span>

### <span data-ttu-id="ae13a-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ae13a-141">System.Boolean</span></span>

## <span data-ttu-id="ae13a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ae13a-142">NOTES</span></span>

## <span data-ttu-id="ae13a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae13a-143">RELATED LINKS</span></span>

[<span data-ttu-id="ae13a-144">新-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ae13a-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="ae13a-145">AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ae13a-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

