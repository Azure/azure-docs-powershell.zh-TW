---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 17221e2d4f88e2f59ee13f73fb18132c01f6632e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913021"
---
# <span data-ttu-id="574ae-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="574ae-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="574ae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="574ae-102">SYNOPSIS</span></span>
<span data-ttu-id="574ae-103">更新頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="574ae-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="574ae-104">語法</span><span class="sxs-lookup"><span data-stu-id="574ae-104">SYNTAX</span></span>

### <span data-ttu-id="574ae-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="574ae-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="574ae-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="574ae-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="574ae-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="574ae-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="574ae-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="574ae-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="574ae-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="574ae-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="574ae-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="574ae-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="574ae-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="574ae-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="574ae-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="574ae-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="574ae-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="574ae-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="574ae-114">描述</span><span class="sxs-lookup"><span data-stu-id="574ae-114">DESCRIPTION</span></span>
<span data-ttu-id="574ae-115">**Set-AzStackEdgeBandwidthSchedule** Cmdlet 會更新 Stack Edge 裝置頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="574ae-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="574ae-116">例子</span><span class="sxs-lookup"><span data-stu-id="574ae-116">EXAMPLES</span></span>

### <span data-ttu-id="574ae-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="574ae-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="574ae-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="574ae-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="574ae-119">參數</span><span class="sxs-lookup"><span data-stu-id="574ae-119">PARAMETERS</span></span>

### <span data-ttu-id="574ae-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="574ae-120">-AsJob</span></span>
<span data-ttu-id="574ae-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="574ae-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="574ae-122">-頻寬</span><span class="sxs-lookup"><span data-stu-id="574ae-122">-Bandwidth</span></span>
<span data-ttu-id="574ae-123">以 Mbps 表示的頻寬</span><span class="sxs-lookup"><span data-stu-id="574ae-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="574ae-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="574ae-124">-DaysOfWeek</span></span>
<span data-ttu-id="574ae-125">已排程的 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="574ae-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="574ae-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="574ae-126">-DefaultProfile</span></span>
<span data-ttu-id="574ae-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="574ae-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="574ae-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="574ae-128">-DeviceName</span></span>
<span data-ttu-id="574ae-129">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="574ae-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574ae-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="574ae-130">-InputObject</span></span>
<span data-ttu-id="574ae-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="574ae-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="574ae-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="574ae-132">-Name</span></span>
<span data-ttu-id="574ae-133">資源名稱</span><span class="sxs-lookup"><span data-stu-id="574ae-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="574ae-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="574ae-134">-ResourceGroupName</span></span>
<span data-ttu-id="574ae-135">資源組名</span><span class="sxs-lookup"><span data-stu-id="574ae-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574ae-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="574ae-136">-ResourceId</span></span>
<span data-ttu-id="574ae-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="574ae-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574ae-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="574ae-138">-StartTime</span></span>
<span data-ttu-id="574ae-139">排程開始時間</span><span class="sxs-lookup"><span data-stu-id="574ae-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="574ae-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="574ae-140">-StopTime</span></span>
<span data-ttu-id="574ae-141">排程停止時間</span><span class="sxs-lookup"><span data-stu-id="574ae-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="574ae-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="574ae-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="574ae-143">會設定無限頻寬</span><span class="sxs-lookup"><span data-stu-id="574ae-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="574ae-144">-確認</span><span class="sxs-lookup"><span data-stu-id="574ae-144">-Confirm</span></span>
<span data-ttu-id="574ae-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="574ae-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="574ae-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="574ae-146">-WhatIf</span></span>
<span data-ttu-id="574ae-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="574ae-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="574ae-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="574ae-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="574ae-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574ae-149">CommonParameters</span></span>
<span data-ttu-id="574ae-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="574ae-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574ae-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="574ae-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574ae-152">輸入</span><span class="sxs-lookup"><span data-stu-id="574ae-152">INPUTS</span></span>

### <span data-ttu-id="574ae-153">沒有</span><span class="sxs-lookup"><span data-stu-id="574ae-153">None</span></span>

## <span data-ttu-id="574ae-154">輸出</span><span class="sxs-lookup"><span data-stu-id="574ae-154">OUTPUTS</span></span>

### <span data-ttu-id="574ae-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="574ae-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="574ae-156">筆記</span><span class="sxs-lookup"><span data-stu-id="574ae-156">NOTES</span></span>

## <span data-ttu-id="574ae-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="574ae-157">RELATED LINKS</span></span>
