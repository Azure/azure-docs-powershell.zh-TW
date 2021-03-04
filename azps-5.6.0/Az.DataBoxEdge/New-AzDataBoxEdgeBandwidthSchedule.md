---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 2c83773ba08c2fefe9404fa69861518d00d4d936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913925"
---
# <span data-ttu-id="a2dd8-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a2dd8-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a2dd8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="a2dd8-103">建立新的頻寬排程</span><span class="sxs-lookup"><span data-stu-id="a2dd8-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="a2dd8-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2dd8-104">SYNTAX</span></span>

### <span data-ttu-id="a2dd8-105">BandwidthParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a2dd8-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2dd8-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2dd8-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2dd8-107">描述</span><span class="sxs-lookup"><span data-stu-id="a2dd8-107">DESCRIPTION</span></span>
<span data-ttu-id="a2dd8-108">**New-AzDataBoxEdgeBandwidthSchedule** Cmdlet 為 Data Box Edge 裝置建立新的頻寬排程，協助管理頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="a2dd8-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="a2dd8-109">例子</span><span class="sxs-lookup"><span data-stu-id="a2dd8-109">EXAMPLES</span></span>

### <span data-ttu-id="a2dd8-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a2dd8-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="a2dd8-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="a2dd8-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="a2dd8-112">參數</span><span class="sxs-lookup"><span data-stu-id="a2dd8-112">PARAMETERS</span></span>

### <span data-ttu-id="a2dd8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2dd8-113">-AsJob</span></span>
<span data-ttu-id="a2dd8-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a2dd8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2dd8-115">-頻寬</span><span class="sxs-lookup"><span data-stu-id="a2dd8-115">-Bandwidth</span></span>
<span data-ttu-id="a2dd8-116">以 Mbps 表示的頻寬</span><span class="sxs-lookup"><span data-stu-id="a2dd8-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2dd8-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a2dd8-117">-DaysOfWeek</span></span>
<span data-ttu-id="a2dd8-118">已排程的 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a2dd8-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2dd8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2dd8-119">-DefaultProfile</span></span>
<span data-ttu-id="a2dd8-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2dd8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2dd8-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a2dd8-121">-DeviceName</span></span>
<span data-ttu-id="a2dd8-122">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="a2dd8-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2dd8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2dd8-123">-Name</span></span>
<span data-ttu-id="a2dd8-124">資源名稱</span><span class="sxs-lookup"><span data-stu-id="a2dd8-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2dd8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2dd8-125">-ResourceGroupName</span></span>
<span data-ttu-id="a2dd8-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="a2dd8-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2dd8-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a2dd8-127">-StartTime</span></span>
<span data-ttu-id="a2dd8-128">排程開始時間</span><span class="sxs-lookup"><span data-stu-id="a2dd8-128">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2dd8-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="a2dd8-129">-StopTime</span></span>
<span data-ttu-id="a2dd8-130">排程停止時間</span><span class="sxs-lookup"><span data-stu-id="a2dd8-130">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2dd8-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="a2dd8-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="a2dd8-132">將設定無限頻寬，如果設為 False，預設值會設為 20 Mbps</span><span class="sxs-lookup"><span data-stu-id="a2dd8-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2dd8-133">-確認</span><span class="sxs-lookup"><span data-stu-id="a2dd8-133">-Confirm</span></span>
<span data-ttu-id="a2dd8-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a2dd8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2dd8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2dd8-135">-WhatIf</span></span>
<span data-ttu-id="a2dd8-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2dd8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2dd8-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2dd8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2dd8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2dd8-138">CommonParameters</span></span>
<span data-ttu-id="a2dd8-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2dd8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2dd8-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2dd8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2dd8-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a2dd8-141">INPUTS</span></span>

### <span data-ttu-id="a2dd8-142">沒有</span><span class="sxs-lookup"><span data-stu-id="a2dd8-142">None</span></span>

## <span data-ttu-id="a2dd8-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a2dd8-143">OUTPUTS</span></span>

### <span data-ttu-id="a2dd8-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a2dd8-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a2dd8-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a2dd8-145">NOTES</span></span>

## <span data-ttu-id="a2dd8-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2dd8-146">RELATED LINKS</span></span>
