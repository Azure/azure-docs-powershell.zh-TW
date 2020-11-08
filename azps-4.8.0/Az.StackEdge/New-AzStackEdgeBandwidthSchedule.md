---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127217"
---
# <span data-ttu-id="43314-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="43314-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="43314-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43314-102">SYNOPSIS</span></span>
<span data-ttu-id="43314-103">建立新的頻寬排程</span><span class="sxs-lookup"><span data-stu-id="43314-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="43314-104">句法</span><span class="sxs-lookup"><span data-stu-id="43314-104">SYNTAX</span></span>

### <span data-ttu-id="43314-105">UnlimitedBandwidthParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="43314-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43314-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="43314-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43314-107">說明</span><span class="sxs-lookup"><span data-stu-id="43314-107">DESCRIPTION</span></span>
<span data-ttu-id="43314-108">**AzStackEdgeBandwidthSchedule** Cmdlet 會針對堆疊邊緣裝置建立新的頻寬排程，以協助管理頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="43314-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="43314-109">示例</span><span class="sxs-lookup"><span data-stu-id="43314-109">EXAMPLES</span></span>

### <span data-ttu-id="43314-110">範例1</span><span class="sxs-lookup"><span data-stu-id="43314-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="43314-111">範例2</span><span class="sxs-lookup"><span data-stu-id="43314-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="43314-112">參數</span><span class="sxs-lookup"><span data-stu-id="43314-112">PARAMETERS</span></span>

### <span data-ttu-id="43314-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43314-113">-AsJob</span></span>
<span data-ttu-id="43314-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="43314-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43314-115">-頻寬</span><span class="sxs-lookup"><span data-stu-id="43314-115">-Bandwidth</span></span>
<span data-ttu-id="43314-116">頻寬（以 Mbps 為單位）</span><span class="sxs-lookup"><span data-stu-id="43314-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="43314-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="43314-117">-DaysOfWeek</span></span>
<span data-ttu-id="43314-118">排程 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="43314-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="43314-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43314-119">-DefaultProfile</span></span>
<span data-ttu-id="43314-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43314-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43314-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="43314-121">-DeviceName</span></span>
<span data-ttu-id="43314-122">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="43314-122">Device Name</span></span>

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

### <span data-ttu-id="43314-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="43314-123">-Name</span></span>
<span data-ttu-id="43314-124">資源名稱</span><span class="sxs-lookup"><span data-stu-id="43314-124">Resource Name</span></span>

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

### <span data-ttu-id="43314-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43314-125">-ResourceGroupName</span></span>
<span data-ttu-id="43314-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="43314-126">Resource Group Name</span></span>

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

### <span data-ttu-id="43314-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="43314-127">-StartTime</span></span>
<span data-ttu-id="43314-128">排程開始時間</span><span class="sxs-lookup"><span data-stu-id="43314-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="43314-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="43314-129">-StopTime</span></span>
<span data-ttu-id="43314-130">排程停止時間</span><span class="sxs-lookup"><span data-stu-id="43314-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="43314-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="43314-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="43314-132">將頻寬設定為無限制</span><span class="sxs-lookup"><span data-stu-id="43314-132">Will Set Bandwidth as Unlimited</span></span>

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

### <span data-ttu-id="43314-133">-確認</span><span class="sxs-lookup"><span data-stu-id="43314-133">-Confirm</span></span>
<span data-ttu-id="43314-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43314-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43314-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43314-135">-WhatIf</span></span>
<span data-ttu-id="43314-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43314-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43314-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43314-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43314-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43314-138">CommonParameters</span></span>
<span data-ttu-id="43314-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43314-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43314-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43314-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43314-141">輸入</span><span class="sxs-lookup"><span data-stu-id="43314-141">INPUTS</span></span>

### <span data-ttu-id="43314-142">所有</span><span class="sxs-lookup"><span data-stu-id="43314-142">None</span></span>

## <span data-ttu-id="43314-143">輸出</span><span class="sxs-lookup"><span data-stu-id="43314-143">OUTPUTS</span></span>

### <span data-ttu-id="43314-144">PSStackEdgeBandWidthSchedule （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="43314-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="43314-145">筆記</span><span class="sxs-lookup"><span data-stu-id="43314-145">NOTES</span></span>

## <span data-ttu-id="43314-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="43314-146">RELATED LINKS</span></span>
