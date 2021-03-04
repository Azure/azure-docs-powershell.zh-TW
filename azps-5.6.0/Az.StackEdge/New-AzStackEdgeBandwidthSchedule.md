---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: a9a49f89301da627fcafa285915d0331240f75b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909422"
---
# <span data-ttu-id="737d1-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="737d1-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="737d1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="737d1-102">SYNOPSIS</span></span>
<span data-ttu-id="737d1-103">建立新的頻寬排程</span><span class="sxs-lookup"><span data-stu-id="737d1-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="737d1-104">語法</span><span class="sxs-lookup"><span data-stu-id="737d1-104">SYNTAX</span></span>

### <span data-ttu-id="737d1-105">UnlimitedBandwidthParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="737d1-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="737d1-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="737d1-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="737d1-107">描述</span><span class="sxs-lookup"><span data-stu-id="737d1-107">DESCRIPTION</span></span>
<span data-ttu-id="737d1-108">**New-AzStackEdgeBandwidthSchedule** Cmdlet 為 Stack Edge 裝置建立新的頻寬排程，協助管理頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="737d1-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="737d1-109">例子</span><span class="sxs-lookup"><span data-stu-id="737d1-109">EXAMPLES</span></span>

### <span data-ttu-id="737d1-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="737d1-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="737d1-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="737d1-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="737d1-112">參數</span><span class="sxs-lookup"><span data-stu-id="737d1-112">PARAMETERS</span></span>

### <span data-ttu-id="737d1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="737d1-113">-AsJob</span></span>
<span data-ttu-id="737d1-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="737d1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="737d1-115">-頻寬</span><span class="sxs-lookup"><span data-stu-id="737d1-115">-Bandwidth</span></span>
<span data-ttu-id="737d1-116">以 Mbps 表示的頻寬</span><span class="sxs-lookup"><span data-stu-id="737d1-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="737d1-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="737d1-117">-DaysOfWeek</span></span>
<span data-ttu-id="737d1-118">已排程的 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="737d1-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="737d1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737d1-119">-DefaultProfile</span></span>
<span data-ttu-id="737d1-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="737d1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737d1-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="737d1-121">-DeviceName</span></span>
<span data-ttu-id="737d1-122">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="737d1-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737d1-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="737d1-123">-Name</span></span>
<span data-ttu-id="737d1-124">資源名稱</span><span class="sxs-lookup"><span data-stu-id="737d1-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737d1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737d1-125">-ResourceGroupName</span></span>
<span data-ttu-id="737d1-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="737d1-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737d1-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="737d1-127">-StartTime</span></span>
<span data-ttu-id="737d1-128">排程開始時間</span><span class="sxs-lookup"><span data-stu-id="737d1-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="737d1-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="737d1-129">-StopTime</span></span>
<span data-ttu-id="737d1-130">排程停止時間</span><span class="sxs-lookup"><span data-stu-id="737d1-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="737d1-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="737d1-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="737d1-132">將頻寬設為無限制</span><span class="sxs-lookup"><span data-stu-id="737d1-132">Will Set Bandwidth as Unlimited</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737d1-133">-確認</span><span class="sxs-lookup"><span data-stu-id="737d1-133">-Confirm</span></span>
<span data-ttu-id="737d1-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="737d1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="737d1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="737d1-135">-WhatIf</span></span>
<span data-ttu-id="737d1-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="737d1-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="737d1-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="737d1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="737d1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737d1-138">CommonParameters</span></span>
<span data-ttu-id="737d1-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="737d1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737d1-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="737d1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737d1-141">輸入</span><span class="sxs-lookup"><span data-stu-id="737d1-141">INPUTS</span></span>

### <span data-ttu-id="737d1-142">沒有</span><span class="sxs-lookup"><span data-stu-id="737d1-142">None</span></span>

## <span data-ttu-id="737d1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="737d1-143">OUTPUTS</span></span>

### <span data-ttu-id="737d1-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="737d1-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="737d1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="737d1-145">NOTES</span></span>

## <span data-ttu-id="737d1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="737d1-146">RELATED LINKS</span></span>
