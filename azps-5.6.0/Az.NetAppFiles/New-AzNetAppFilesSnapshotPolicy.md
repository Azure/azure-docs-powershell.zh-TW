---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 1f8b68ac04a563dbec44b0ed43bca0a54015154d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906030"
---
# <span data-ttu-id="1627d-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="1627d-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1627d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1627d-102">SYNOPSIS</span></span>
<span data-ttu-id="1627d-103">在 ANF 帳戶的 anF (快照) 建立新 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="1627d-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="1627d-104">語法</span><span class="sxs-lookup"><span data-stu-id="1627d-104">SYNTAX</span></span>

### <span data-ttu-id="1627d-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1627d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1627d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1627d-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1627d-107">描述</span><span class="sxs-lookup"><span data-stu-id="1627d-107">DESCRIPTION</span></span>
<span data-ttu-id="1627d-108">**New-AzNetAppFilesActiveDirectory Cmdlet** 會為 ANF 帳戶建立新的快照策略。</span><span class="sxs-lookup"><span data-stu-id="1627d-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="1627d-109">例子</span><span class="sxs-lookup"><span data-stu-id="1627d-109">EXAMPLES</span></span>

### <span data-ttu-id="1627d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="1627d-110">Example 1</span></span>
```powershell
$hourlySchedule = @{        
        Minute = 2
        SnapshotsToKeep = 6
    }
    $dailySchedule = @{
        Hour = 1
        Minute = 2
        SnapshotsToKeep = 6
    }
    $weeklySchedule = @{
        Minute = 2    
        Hour = 1                
        Day = "Sunday,Monday"
        SnapshotsToKeep = 6
    }
    $monthlySchedule = @{
        Minute = 2    
        Hour = 1        
        DaysOfMonth = "2,11,21"
        SnapshotsToKeep = 6
    }
PS C:\> New-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MySnapshotPolicy" -Enabled -HourlySchedule $hourlySchedule -DailySchedule $dailySchedule -WeeklySchedule $weeklySchedule -MonthlySchedule $monthlySchedule
```

<span data-ttu-id="1627d-111">此命令會為名為「MyAccount」的帳戶之 ANF 帳戶建立新的 ANF 快照快照策略。</span><span class="sxs-lookup"><span data-stu-id="1627d-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="1627d-112">參數</span><span class="sxs-lookup"><span data-stu-id="1627d-112">PARAMETERS</span></span>

### <span data-ttu-id="1627d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1627d-113">-AccountName</span></span>
<span data-ttu-id="1627d-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="1627d-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1627d-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="1627d-115">-AccountObject</span></span>
<span data-ttu-id="1627d-116">新快照策略物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="1627d-116">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1627d-117">-每日排版</span><span class="sxs-lookup"><span data-stu-id="1627d-117">-DailySchedule</span></span>
<span data-ttu-id="1627d-118">代表每日排程的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="1627d-118">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1627d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1627d-119">-DefaultProfile</span></span>
<span data-ttu-id="1627d-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1627d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1627d-121">-已啟用</span><span class="sxs-lookup"><span data-stu-id="1627d-121">-Enabled</span></span>
<span data-ttu-id="1627d-122">決定是否已啟用策略的屬性</span><span class="sxs-lookup"><span data-stu-id="1627d-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="1627d-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="1627d-123">-HourlySchedule</span></span>
<span data-ttu-id="1627d-124">代表小時排程的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="1627d-124">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1627d-125">-位置</span><span class="sxs-lookup"><span data-stu-id="1627d-125">-Location</span></span>
<span data-ttu-id="1627d-126">資源的位置</span><span class="sxs-lookup"><span data-stu-id="1627d-126">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1627d-127">-每月排期</span><span class="sxs-lookup"><span data-stu-id="1627d-127">-MonthlySchedule</span></span>
<span data-ttu-id="1627d-128">代表 Montly Schedule 的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="1627d-128">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1627d-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="1627d-129">-Name</span></span>
<span data-ttu-id="1627d-130">ANF 快照策略的名稱</span><span class="sxs-lookup"><span data-stu-id="1627d-130">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1627d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1627d-131">-ResourceGroupName</span></span>
<span data-ttu-id="1627d-132">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="1627d-132">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1627d-133">-標記</span><span class="sxs-lookup"><span data-stu-id="1627d-133">-Tag</span></span>
<span data-ttu-id="1627d-134">代表資源標記的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="1627d-134">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1627d-135">-每週排班</span><span class="sxs-lookup"><span data-stu-id="1627d-135">-WeeklySchedule</span></span>
<span data-ttu-id="1627d-136">代表 Montly Schedule 的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="1627d-136">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1627d-137">-確認</span><span class="sxs-lookup"><span data-stu-id="1627d-137">-Confirm</span></span>
<span data-ttu-id="1627d-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1627d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1627d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1627d-139">-WhatIf</span></span>
<span data-ttu-id="1627d-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1627d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1627d-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1627d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1627d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1627d-142">CommonParameters</span></span>
<span data-ttu-id="1627d-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1627d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1627d-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1627d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1627d-145">輸入</span><span class="sxs-lookup"><span data-stu-id="1627d-145">INPUTS</span></span>

### <span data-ttu-id="1627d-146">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1627d-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="1627d-147">輸出</span><span class="sxs-lookup"><span data-stu-id="1627d-147">OUTPUTS</span></span>

### <span data-ttu-id="1627d-148">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilessnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="1627d-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1627d-149">筆記</span><span class="sxs-lookup"><span data-stu-id="1627d-149">NOTES</span></span>

## <span data-ttu-id="1627d-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="1627d-150">RELATED LINKS</span></span>
