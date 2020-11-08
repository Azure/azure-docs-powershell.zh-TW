---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129145"
---
# <span data-ttu-id="16345-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="16345-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="16345-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16345-102">SYNOPSIS</span></span>
<span data-ttu-id="16345-103">更新頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="16345-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="16345-104">句法</span><span class="sxs-lookup"><span data-stu-id="16345-104">SYNTAX</span></span>

### <span data-ttu-id="16345-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="16345-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16345-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16345-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16345-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="16345-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16345-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="16345-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16345-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16345-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16345-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="16345-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16345-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="16345-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16345-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="16345-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16345-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="16345-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16345-114">說明</span><span class="sxs-lookup"><span data-stu-id="16345-114">DESCRIPTION</span></span>
<span data-ttu-id="16345-115">**AzStackEdgeBandwidthSchedule** Cmdlet 會更新堆疊邊緣裝置的頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="16345-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="16345-116">示例</span><span class="sxs-lookup"><span data-stu-id="16345-116">EXAMPLES</span></span>

### <span data-ttu-id="16345-117">範例1</span><span class="sxs-lookup"><span data-stu-id="16345-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="16345-118">範例2</span><span class="sxs-lookup"><span data-stu-id="16345-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="16345-119">參數</span><span class="sxs-lookup"><span data-stu-id="16345-119">PARAMETERS</span></span>

### <span data-ttu-id="16345-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16345-120">-AsJob</span></span>
<span data-ttu-id="16345-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="16345-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16345-122">-頻寬</span><span class="sxs-lookup"><span data-stu-id="16345-122">-Bandwidth</span></span>
<span data-ttu-id="16345-123">頻寬（以 Mbps 為單位）</span><span class="sxs-lookup"><span data-stu-id="16345-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="16345-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="16345-124">-DaysOfWeek</span></span>
<span data-ttu-id="16345-125">排程 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="16345-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="16345-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16345-126">-DefaultProfile</span></span>
<span data-ttu-id="16345-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16345-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16345-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="16345-128">-DeviceName</span></span>
<span data-ttu-id="16345-129">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="16345-129">Device Name</span></span>

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

### <span data-ttu-id="16345-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16345-130">-InputObject</span></span>
<span data-ttu-id="16345-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="16345-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="16345-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="16345-132">-Name</span></span>
<span data-ttu-id="16345-133">資源名稱</span><span class="sxs-lookup"><span data-stu-id="16345-133">Resource Name</span></span>

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

### <span data-ttu-id="16345-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16345-134">-ResourceGroupName</span></span>
<span data-ttu-id="16345-135">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="16345-135">Resource Group Name</span></span>

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

### <span data-ttu-id="16345-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16345-136">-ResourceId</span></span>
<span data-ttu-id="16345-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="16345-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="16345-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="16345-138">-StartTime</span></span>
<span data-ttu-id="16345-139">排程開始時間</span><span class="sxs-lookup"><span data-stu-id="16345-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="16345-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="16345-140">-StopTime</span></span>
<span data-ttu-id="16345-141">排程停止時間</span><span class="sxs-lookup"><span data-stu-id="16345-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="16345-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="16345-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="16345-143">會設定無限制的頻寬</span><span class="sxs-lookup"><span data-stu-id="16345-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="16345-144">-確認</span><span class="sxs-lookup"><span data-stu-id="16345-144">-Confirm</span></span>
<span data-ttu-id="16345-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16345-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16345-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16345-146">-WhatIf</span></span>
<span data-ttu-id="16345-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16345-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16345-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16345-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16345-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16345-149">CommonParameters</span></span>
<span data-ttu-id="16345-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16345-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16345-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="16345-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16345-152">輸入</span><span class="sxs-lookup"><span data-stu-id="16345-152">INPUTS</span></span>

### <span data-ttu-id="16345-153">所有</span><span class="sxs-lookup"><span data-stu-id="16345-153">None</span></span>

## <span data-ttu-id="16345-154">輸出</span><span class="sxs-lookup"><span data-stu-id="16345-154">OUTPUTS</span></span>

### <span data-ttu-id="16345-155">PSStackEdgeBandWidthSchedule （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="16345-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="16345-156">筆記</span><span class="sxs-lookup"><span data-stu-id="16345-156">NOTES</span></span>

## <span data-ttu-id="16345-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="16345-157">RELATED LINKS</span></span>
