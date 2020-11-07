---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: f761a84fe994f0da68b4d3a86b513ba333b06573
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794807"
---
# <span data-ttu-id="ecfd2-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ecfd2-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="ecfd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecfd2-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfd2-103">更新頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="ecfd2-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="ecfd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecfd2-104">SYNTAX</span></span>

### <span data-ttu-id="ecfd2-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ecfd2-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfd2-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecfd2-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecfd2-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="ecfd2-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfd2-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="ecfd2-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfd2-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecfd2-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfd2-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="ecfd2-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfd2-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="ecfd2-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfd2-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="ecfd2-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfd2-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="ecfd2-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecfd2-114">說明</span><span class="sxs-lookup"><span data-stu-id="ecfd2-114">DESCRIPTION</span></span>
<span data-ttu-id="ecfd2-115">**AzDataBoxEdgeBandwidthSchedule** Cmdlet 會更新資料編輯方塊邊緣裝置的頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="ecfd2-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="ecfd2-116">示例</span><span class="sxs-lookup"><span data-stu-id="ecfd2-116">EXAMPLES</span></span>

### <span data-ttu-id="ecfd2-117">範例1</span><span class="sxs-lookup"><span data-stu-id="ecfd2-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="ecfd2-118">範例2</span><span class="sxs-lookup"><span data-stu-id="ecfd2-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="ecfd2-119">參數</span><span class="sxs-lookup"><span data-stu-id="ecfd2-119">PARAMETERS</span></span>

### <span data-ttu-id="ecfd2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecfd2-120">-AsJob</span></span>
<span data-ttu-id="ecfd2-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ecfd2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecfd2-122">-頻寬</span><span class="sxs-lookup"><span data-stu-id="ecfd2-122">-Bandwidth</span></span>
<span data-ttu-id="ecfd2-123">頻寬（以 Mbps 為單位）</span><span class="sxs-lookup"><span data-stu-id="ecfd2-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="ecfd2-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="ecfd2-124">-DaysOfWeek</span></span>
<span data-ttu-id="ecfd2-125">排程 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="ecfd2-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="ecfd2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfd2-126">-DefaultProfile</span></span>
<span data-ttu-id="ecfd2-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecfd2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecfd2-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ecfd2-128">-DeviceName</span></span>
<span data-ttu-id="ecfd2-129">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="ecfd2-129">Device Name</span></span>

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

### <span data-ttu-id="ecfd2-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecfd2-130">-InputObject</span></span>
<span data-ttu-id="ecfd2-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecfd2-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="ecfd2-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="ecfd2-132">-Name</span></span>
<span data-ttu-id="ecfd2-133">資源名稱</span><span class="sxs-lookup"><span data-stu-id="ecfd2-133">Resource Name</span></span>

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

### <span data-ttu-id="ecfd2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfd2-134">-ResourceGroupName</span></span>
<span data-ttu-id="ecfd2-135">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ecfd2-135">Resource Group Name</span></span>

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

### <span data-ttu-id="ecfd2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecfd2-136">-ResourceId</span></span>
<span data-ttu-id="ecfd2-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecfd2-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="ecfd2-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ecfd2-138">-StartTime</span></span>
<span data-ttu-id="ecfd2-139">排程開始時間</span><span class="sxs-lookup"><span data-stu-id="ecfd2-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="ecfd2-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="ecfd2-140">-StopTime</span></span>
<span data-ttu-id="ecfd2-141">排程停止時間</span><span class="sxs-lookup"><span data-stu-id="ecfd2-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="ecfd2-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="ecfd2-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="ecfd2-143">會設定無限制的頻寬</span><span class="sxs-lookup"><span data-stu-id="ecfd2-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="ecfd2-144">-確認</span><span class="sxs-lookup"><span data-stu-id="ecfd2-144">-Confirm</span></span>
<span data-ttu-id="ecfd2-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ecfd2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecfd2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecfd2-146">-WhatIf</span></span>
<span data-ttu-id="ecfd2-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ecfd2-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecfd2-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ecfd2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecfd2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfd2-149">CommonParameters</span></span>
<span data-ttu-id="ecfd2-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecfd2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfd2-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ecfd2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfd2-152">輸入</span><span class="sxs-lookup"><span data-stu-id="ecfd2-152">INPUTS</span></span>

### <span data-ttu-id="ecfd2-153">所有</span><span class="sxs-lookup"><span data-stu-id="ecfd2-153">None</span></span>

## <span data-ttu-id="ecfd2-154">輸出</span><span class="sxs-lookup"><span data-stu-id="ecfd2-154">OUTPUTS</span></span>

### <span data-ttu-id="ecfd2-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ecfd2-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="ecfd2-156">筆記</span><span class="sxs-lookup"><span data-stu-id="ecfd2-156">NOTES</span></span>

## <span data-ttu-id="ecfd2-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecfd2-157">RELATED LINKS</span></span>
