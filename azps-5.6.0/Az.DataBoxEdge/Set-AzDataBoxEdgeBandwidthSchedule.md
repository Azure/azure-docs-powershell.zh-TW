---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: d0f5d0d71f35df5bb36ea86a1ec20ca009256f67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909718"
---
# <span data-ttu-id="0521b-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0521b-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="0521b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0521b-102">SYNOPSIS</span></span>
<span data-ttu-id="0521b-103">更新頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="0521b-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="0521b-104">語法</span><span class="sxs-lookup"><span data-stu-id="0521b-104">SYNTAX</span></span>

### <span data-ttu-id="0521b-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0521b-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0521b-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0521b-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0521b-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0521b-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0521b-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0521b-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0521b-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0521b-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0521b-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0521b-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0521b-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0521b-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0521b-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0521b-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0521b-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0521b-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0521b-114">描述</span><span class="sxs-lookup"><span data-stu-id="0521b-114">DESCRIPTION</span></span>
<span data-ttu-id="0521b-115">**Set-AzDataBoxEdgeBandwidthSchedule** Cmdlet 會更新 Data Box Edge 裝置頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="0521b-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="0521b-116">例子</span><span class="sxs-lookup"><span data-stu-id="0521b-116">EXAMPLES</span></span>

### <span data-ttu-id="0521b-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="0521b-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="0521b-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="0521b-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="0521b-119">參數</span><span class="sxs-lookup"><span data-stu-id="0521b-119">PARAMETERS</span></span>

### <span data-ttu-id="0521b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0521b-120">-AsJob</span></span>
<span data-ttu-id="0521b-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0521b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0521b-122">-頻寬</span><span class="sxs-lookup"><span data-stu-id="0521b-122">-Bandwidth</span></span>
<span data-ttu-id="0521b-123">以 Mbps 表示的頻寬</span><span class="sxs-lookup"><span data-stu-id="0521b-123">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateByResourceIdParameterBandwidthSet, UpdateByInputObjectParameterBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0521b-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0521b-124">-DaysOfWeek</span></span>
<span data-ttu-id="0521b-125">已排程的 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0521b-125">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0521b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0521b-126">-DefaultProfile</span></span>
<span data-ttu-id="0521b-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0521b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0521b-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0521b-128">-DeviceName</span></span>
<span data-ttu-id="0521b-129">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="0521b-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0521b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0521b-130">-InputObject</span></span>
<span data-ttu-id="0521b-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0521b-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0521b-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="0521b-132">-Name</span></span>
<span data-ttu-id="0521b-133">資源名稱</span><span class="sxs-lookup"><span data-stu-id="0521b-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0521b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0521b-134">-ResourceGroupName</span></span>
<span data-ttu-id="0521b-135">資源組名</span><span class="sxs-lookup"><span data-stu-id="0521b-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0521b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0521b-136">-ResourceId</span></span>
<span data-ttu-id="0521b-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0521b-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0521b-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0521b-138">-StartTime</span></span>
<span data-ttu-id="0521b-139">排程開始時間</span><span class="sxs-lookup"><span data-stu-id="0521b-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="0521b-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="0521b-140">-StopTime</span></span>
<span data-ttu-id="0521b-141">排程停止時間</span><span class="sxs-lookup"><span data-stu-id="0521b-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="0521b-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="0521b-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="0521b-143">會設定無限頻寬</span><span class="sxs-lookup"><span data-stu-id="0521b-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0521b-144">-確認</span><span class="sxs-lookup"><span data-stu-id="0521b-144">-Confirm</span></span>
<span data-ttu-id="0521b-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0521b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0521b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0521b-146">-WhatIf</span></span>
<span data-ttu-id="0521b-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0521b-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0521b-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0521b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0521b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0521b-149">CommonParameters</span></span>
<span data-ttu-id="0521b-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0521b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0521b-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0521b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0521b-152">輸入</span><span class="sxs-lookup"><span data-stu-id="0521b-152">INPUTS</span></span>

### <span data-ttu-id="0521b-153">沒有</span><span class="sxs-lookup"><span data-stu-id="0521b-153">None</span></span>

## <span data-ttu-id="0521b-154">輸出</span><span class="sxs-lookup"><span data-stu-id="0521b-154">OUTPUTS</span></span>

### <span data-ttu-id="0521b-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0521b-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="0521b-156">筆記</span><span class="sxs-lookup"><span data-stu-id="0521b-156">NOTES</span></span>

## <span data-ttu-id="0521b-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="0521b-157">RELATED LINKS</span></span>
