---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 716beafc05c4746d0cfe76dce70109226b1f8f26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915745"
---
# <span data-ttu-id="7deed-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="7deed-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="7deed-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7deed-102">SYNOPSIS</span></span>
<span data-ttu-id="7deed-103">移除裝置的順序。</span><span class="sxs-lookup"><span data-stu-id="7deed-103">Removes the order for a device.</span></span>

## <span data-ttu-id="7deed-104">語法</span><span class="sxs-lookup"><span data-stu-id="7deed-104">SYNTAX</span></span>

### <span data-ttu-id="7deed-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7deed-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7deed-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7deed-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7deed-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7deed-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7deed-108">描述</span><span class="sxs-lookup"><span data-stu-id="7deed-108">DESCRIPTION</span></span>
<span data-ttu-id="7deed-109">**Remove-AzStackEdgeOrder** Cmdlet 會刪除 Stack Edge 裝置的現有訂單。</span><span class="sxs-lookup"><span data-stu-id="7deed-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="7deed-110">例子</span><span class="sxs-lookup"><span data-stu-id="7deed-110">EXAMPLES</span></span>

### <span data-ttu-id="7deed-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="7deed-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="7deed-112">參數</span><span class="sxs-lookup"><span data-stu-id="7deed-112">PARAMETERS</span></span>

### <span data-ttu-id="7deed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7deed-113">-AsJob</span></span>
<span data-ttu-id="7deed-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7deed-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7deed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7deed-115">-DefaultProfile</span></span>
<span data-ttu-id="7deed-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7deed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7deed-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7deed-117">-DeviceName</span></span>
<span data-ttu-id="7deed-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="7deed-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7deed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7deed-119">-InputObject</span></span>
<span data-ttu-id="7deed-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="7deed-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7deed-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7deed-121">-PassThru</span></span>
<span data-ttu-id="7deed-122">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="7deed-122">returns true if successful</span></span>

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

### <span data-ttu-id="7deed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7deed-123">-ResourceGroupName</span></span>
<span data-ttu-id="7deed-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="7deed-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7deed-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7deed-125">-ResourceId</span></span>
<span data-ttu-id="7deed-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7deed-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7deed-127">-確認</span><span class="sxs-lookup"><span data-stu-id="7deed-127">-Confirm</span></span>
<span data-ttu-id="7deed-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7deed-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7deed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7deed-129">-WhatIf</span></span>
<span data-ttu-id="7deed-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7deed-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7deed-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7deed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7deed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7deed-132">CommonParameters</span></span>
<span data-ttu-id="7deed-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7deed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7deed-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7deed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7deed-135">輸入</span><span class="sxs-lookup"><span data-stu-id="7deed-135">INPUTS</span></span>

### <span data-ttu-id="7deed-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7deed-136">System.String</span></span>

### <span data-ttu-id="7deed-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="7deed-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="7deed-138">輸出</span><span class="sxs-lookup"><span data-stu-id="7deed-138">OUTPUTS</span></span>

### <span data-ttu-id="7deed-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="7deed-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="7deed-140">筆記</span><span class="sxs-lookup"><span data-stu-id="7deed-140">NOTES</span></span>

## <span data-ttu-id="7deed-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="7deed-141">RELATED LINKS</span></span>
