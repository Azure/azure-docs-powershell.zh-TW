---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: e7659c6437e9566a4793e12518a30067aa73297a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915722"
---
# <span data-ttu-id="fb1b5-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="fb1b5-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="fb1b5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb1b5-102">SYNOPSIS</span></span>
<span data-ttu-id="fb1b5-103">移除裝置上現有的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fb1b5-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="fb1b5-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb1b5-104">SYNTAX</span></span>

### <span data-ttu-id="fb1b5-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fb1b5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb1b5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb1b5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb1b5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb1b5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb1b5-108">描述</span><span class="sxs-lookup"><span data-stu-id="fb1b5-108">DESCRIPTION</span></span>
<span data-ttu-id="fb1b5-109">**Remove-AzStackEdgeTrigger Cmdlet** 會移除 Stack Edge 裝置上現有的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fb1b5-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="fb1b5-110">例子</span><span class="sxs-lookup"><span data-stu-id="fb1b5-110">EXAMPLES</span></span>

### <span data-ttu-id="fb1b5-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="fb1b5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="fb1b5-112">參數</span><span class="sxs-lookup"><span data-stu-id="fb1b5-112">PARAMETERS</span></span>

### <span data-ttu-id="fb1b5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb1b5-113">-AsJob</span></span>
<span data-ttu-id="fb1b5-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb1b5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb1b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb1b5-115">-DefaultProfile</span></span>
<span data-ttu-id="fb1b5-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb1b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb1b5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fb1b5-117">-DeviceName</span></span>
<span data-ttu-id="fb1b5-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="fb1b5-118">Device Name</span></span>

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

### <span data-ttu-id="fb1b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb1b5-119">-InputObject</span></span>
<span data-ttu-id="fb1b5-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="fb1b5-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb1b5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb1b5-121">-Name</span></span>
<span data-ttu-id="fb1b5-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="fb1b5-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb1b5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb1b5-123">-PassThru</span></span>
<span data-ttu-id="fb1b5-124">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="fb1b5-124">returns true if successful</span></span>

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

### <span data-ttu-id="fb1b5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb1b5-125">-ResourceGroupName</span></span>
<span data-ttu-id="fb1b5-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="fb1b5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fb1b5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb1b5-127">-ResourceId</span></span>
<span data-ttu-id="fb1b5-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb1b5-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb1b5-129">-確認</span><span class="sxs-lookup"><span data-stu-id="fb1b5-129">-Confirm</span></span>
<span data-ttu-id="fb1b5-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fb1b5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb1b5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb1b5-131">-WhatIf</span></span>
<span data-ttu-id="fb1b5-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb1b5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb1b5-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb1b5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb1b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb1b5-134">CommonParameters</span></span>
<span data-ttu-id="fb1b5-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb1b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb1b5-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb1b5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb1b5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="fb1b5-137">INPUTS</span></span>

### <span data-ttu-id="fb1b5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fb1b5-138">System.String</span></span>

### <span data-ttu-id="fb1b5-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeTrirr</span><span class="sxs-lookup"><span data-stu-id="fb1b5-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="fb1b5-140">輸出</span><span class="sxs-lookup"><span data-stu-id="fb1b5-140">OUTPUTS</span></span>

### <span data-ttu-id="fb1b5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb1b5-141">System.Boolean</span></span>

## <span data-ttu-id="fb1b5-142">筆記</span><span class="sxs-lookup"><span data-stu-id="fb1b5-142">NOTES</span></span>

## <span data-ttu-id="fb1b5-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb1b5-143">RELATED LINKS</span></span>
