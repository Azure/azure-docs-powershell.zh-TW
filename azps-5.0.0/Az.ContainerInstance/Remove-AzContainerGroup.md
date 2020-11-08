---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140168"
---
# <span data-ttu-id="68579-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="68579-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="68579-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68579-102">SYNOPSIS</span></span>
<span data-ttu-id="68579-103">移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="68579-103">Removes a container group.</span></span>

## <span data-ttu-id="68579-104">句法</span><span class="sxs-lookup"><span data-stu-id="68579-104">SYNTAX</span></span>

### <span data-ttu-id="68579-105">RemoveContainerGroupByResourceGroupAndNameParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="68579-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68579-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="68579-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68579-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="68579-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68579-108">說明</span><span class="sxs-lookup"><span data-stu-id="68579-108">DESCRIPTION</span></span>
<span data-ttu-id="68579-109">**AzContainerGroup** Cmdlet 會移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="68579-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="68579-110">示例</span><span class="sxs-lookup"><span data-stu-id="68579-110">EXAMPLES</span></span>

### <span data-ttu-id="68579-111">範例1：移除容器群組</span><span class="sxs-lookup"><span data-stu-id="68579-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="68579-112">這個命令會移除指定的容器群組。</span><span class="sxs-lookup"><span data-stu-id="68579-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="68579-113">範例2：依管道移除容器群組</span><span class="sxs-lookup"><span data-stu-id="68579-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="68579-114">這個命令會透過 [管道] 移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="68579-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="68579-115">範例3：依資源識別碼移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="68579-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="68579-116">這個命令會依資源識別碼移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="68579-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="68579-117">參數</span><span class="sxs-lookup"><span data-stu-id="68579-117">PARAMETERS</span></span>

### <span data-ttu-id="68579-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68579-118">-DefaultProfile</span></span>
<span data-ttu-id="68579-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68579-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68579-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68579-120">-InputObject</span></span>
<span data-ttu-id="68579-121">要移除的容器群組。</span><span class="sxs-lookup"><span data-stu-id="68579-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68579-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="68579-122">-Name</span></span>
<span data-ttu-id="68579-123">容器組名。</span><span class="sxs-lookup"><span data-stu-id="68579-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68579-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68579-124">-PassThru</span></span>
<span data-ttu-id="68579-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="68579-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="68579-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68579-126">-ResourceGroupName</span></span>
<span data-ttu-id="68579-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68579-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68579-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68579-128">-ResourceId</span></span>
<span data-ttu-id="68579-129">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="68579-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68579-130">-確認</span><span class="sxs-lookup"><span data-stu-id="68579-130">-Confirm</span></span>
<span data-ttu-id="68579-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68579-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68579-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68579-132">-WhatIf</span></span>
<span data-ttu-id="68579-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68579-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68579-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68579-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68579-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68579-135">CommonParameters</span></span>
<span data-ttu-id="68579-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68579-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68579-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68579-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68579-138">輸入</span><span class="sxs-lookup"><span data-stu-id="68579-138">INPUTS</span></span>

### <span data-ttu-id="68579-139">PSContainerGroup 中的 ContainerInstance。</span><span class="sxs-lookup"><span data-stu-id="68579-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="68579-140">System.object</span><span class="sxs-lookup"><span data-stu-id="68579-140">System.String</span></span>

## <span data-ttu-id="68579-141">輸出</span><span class="sxs-lookup"><span data-stu-id="68579-141">OUTPUTS</span></span>

### <span data-ttu-id="68579-142">PSContainerGroup 中的 ContainerInstance。</span><span class="sxs-lookup"><span data-stu-id="68579-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="68579-143">筆記</span><span class="sxs-lookup"><span data-stu-id="68579-143">NOTES</span></span>

## <span data-ttu-id="68579-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="68579-144">RELATED LINKS</span></span>