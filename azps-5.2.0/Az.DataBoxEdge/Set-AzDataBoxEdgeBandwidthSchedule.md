---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283159"
---
# <span data-ttu-id="48c86-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="48c86-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="48c86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48c86-102">SYNOPSIS</span></span>
<span data-ttu-id="48c86-103">更新頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="48c86-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="48c86-104">句法</span><span class="sxs-lookup"><span data-stu-id="48c86-104">SYNTAX</span></span>

### <span data-ttu-id="48c86-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="48c86-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c86-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48c86-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48c86-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="48c86-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c86-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="48c86-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c86-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48c86-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c86-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="48c86-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c86-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="48c86-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c86-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="48c86-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c86-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="48c86-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48c86-114">說明</span><span class="sxs-lookup"><span data-stu-id="48c86-114">DESCRIPTION</span></span>
<span data-ttu-id="48c86-115">**AzDataBoxEdgeBandwidthSchedule** Cmdlet 會更新資料編輯方塊邊緣裝置的頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="48c86-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="48c86-116">示例</span><span class="sxs-lookup"><span data-stu-id="48c86-116">EXAMPLES</span></span>

### <span data-ttu-id="48c86-117">範例1</span><span class="sxs-lookup"><span data-stu-id="48c86-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="48c86-118">範例2</span><span class="sxs-lookup"><span data-stu-id="48c86-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="48c86-119">參數</span><span class="sxs-lookup"><span data-stu-id="48c86-119">PARAMETERS</span></span>

### <span data-ttu-id="48c86-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48c86-120">-AsJob</span></span>
<span data-ttu-id="48c86-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="48c86-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48c86-122">-頻寬</span><span class="sxs-lookup"><span data-stu-id="48c86-122">-Bandwidth</span></span>
<span data-ttu-id="48c86-123">頻寬（以 Mbps 為單位）</span><span class="sxs-lookup"><span data-stu-id="48c86-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="48c86-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="48c86-124">-DaysOfWeek</span></span>
<span data-ttu-id="48c86-125">排程 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="48c86-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="48c86-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c86-126">-DefaultProfile</span></span>
<span data-ttu-id="48c86-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48c86-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48c86-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="48c86-128">-DeviceName</span></span>
<span data-ttu-id="48c86-129">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="48c86-129">Device Name</span></span>

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

### <span data-ttu-id="48c86-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48c86-130">-InputObject</span></span>
<span data-ttu-id="48c86-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="48c86-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="48c86-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="48c86-132">-Name</span></span>
<span data-ttu-id="48c86-133">資源名稱</span><span class="sxs-lookup"><span data-stu-id="48c86-133">Resource Name</span></span>

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

### <span data-ttu-id="48c86-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48c86-134">-ResourceGroupName</span></span>
<span data-ttu-id="48c86-135">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="48c86-135">Resource Group Name</span></span>

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

### <span data-ttu-id="48c86-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48c86-136">-ResourceId</span></span>
<span data-ttu-id="48c86-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="48c86-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="48c86-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="48c86-138">-StartTime</span></span>
<span data-ttu-id="48c86-139">排程開始時間</span><span class="sxs-lookup"><span data-stu-id="48c86-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="48c86-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="48c86-140">-StopTime</span></span>
<span data-ttu-id="48c86-141">排程停止時間</span><span class="sxs-lookup"><span data-stu-id="48c86-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="48c86-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="48c86-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="48c86-143">會設定無限制的頻寬</span><span class="sxs-lookup"><span data-stu-id="48c86-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="48c86-144">-確認</span><span class="sxs-lookup"><span data-stu-id="48c86-144">-Confirm</span></span>
<span data-ttu-id="48c86-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48c86-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48c86-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48c86-146">-WhatIf</span></span>
<span data-ttu-id="48c86-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48c86-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48c86-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48c86-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48c86-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c86-149">CommonParameters</span></span>
<span data-ttu-id="48c86-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48c86-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c86-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48c86-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c86-152">輸入</span><span class="sxs-lookup"><span data-stu-id="48c86-152">INPUTS</span></span>

### <span data-ttu-id="48c86-153">所有</span><span class="sxs-lookup"><span data-stu-id="48c86-153">None</span></span>

## <span data-ttu-id="48c86-154">輸出</span><span class="sxs-lookup"><span data-stu-id="48c86-154">OUTPUTS</span></span>

### <span data-ttu-id="48c86-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="48c86-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="48c86-156">筆記</span><span class="sxs-lookup"><span data-stu-id="48c86-156">NOTES</span></span>

## <span data-ttu-id="48c86-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="48c86-157">RELATED LINKS</span></span>
