---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 6b30f79f7ef1e2819004c8ac7e9d3b6737bfb7d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916198"
---
# <span data-ttu-id="adae2-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="adae2-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="adae2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="adae2-102">SYNOPSIS</span></span>
<span data-ttu-id="adae2-103">移除頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="adae2-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="adae2-104">語法</span><span class="sxs-lookup"><span data-stu-id="adae2-104">SYNTAX</span></span>

### <span data-ttu-id="adae2-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="adae2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adae2-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adae2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adae2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adae2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adae2-108">描述</span><span class="sxs-lookup"><span data-stu-id="adae2-108">DESCRIPTION</span></span>
<span data-ttu-id="adae2-109">**Remove-AzDataBoxEdgeBandwidthSchedule** Cmdlet 會移除 Data Box Edge 裝置頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="adae2-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="adae2-110">例子</span><span class="sxs-lookup"><span data-stu-id="adae2-110">EXAMPLES</span></span>

### <span data-ttu-id="adae2-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="adae2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="adae2-112">參數</span><span class="sxs-lookup"><span data-stu-id="adae2-112">PARAMETERS</span></span>

### <span data-ttu-id="adae2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="adae2-113">-AsJob</span></span>
<span data-ttu-id="adae2-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="adae2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="adae2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adae2-115">-DefaultProfile</span></span>
<span data-ttu-id="adae2-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="adae2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adae2-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="adae2-117">-DeviceName</span></span>
<span data-ttu-id="adae2-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="adae2-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adae2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adae2-119">-InputObject</span></span>
<span data-ttu-id="adae2-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="adae2-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adae2-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="adae2-121">-Name</span></span>
<span data-ttu-id="adae2-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="adae2-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adae2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adae2-123">-PassThru</span></span>
<span data-ttu-id="adae2-124">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="adae2-124">returns true if successful</span></span>

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

### <span data-ttu-id="adae2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adae2-125">-ResourceGroupName</span></span>
<span data-ttu-id="adae2-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="adae2-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adae2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adae2-127">-ResourceId</span></span>
<span data-ttu-id="adae2-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="adae2-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="adae2-129">-確認</span><span class="sxs-lookup"><span data-stu-id="adae2-129">-Confirm</span></span>
<span data-ttu-id="adae2-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="adae2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adae2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adae2-131">-WhatIf</span></span>
<span data-ttu-id="adae2-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="adae2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adae2-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="adae2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adae2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adae2-134">CommonParameters</span></span>
<span data-ttu-id="adae2-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="adae2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adae2-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adae2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adae2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="adae2-137">INPUTS</span></span>

### <span data-ttu-id="adae2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="adae2-138">System.String</span></span>

### <span data-ttu-id="adae2-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="adae2-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="adae2-140">輸出</span><span class="sxs-lookup"><span data-stu-id="adae2-140">OUTPUTS</span></span>

### <span data-ttu-id="adae2-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="adae2-141">System.Boolean</span></span>

## <span data-ttu-id="adae2-142">筆記</span><span class="sxs-lookup"><span data-stu-id="adae2-142">NOTES</span></span>

## <span data-ttu-id="adae2-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="adae2-143">RELATED LINKS</span></span>
