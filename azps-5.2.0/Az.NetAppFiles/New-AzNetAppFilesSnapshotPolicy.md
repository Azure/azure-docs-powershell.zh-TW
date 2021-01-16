---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cfa7fc38fa8c7b66347ae3632b6d1ea94ca07c86
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281759"
---
# <span data-ttu-id="2fa51-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="2fa51-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="2fa51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2fa51-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa51-103"> () ANF ANF 帳戶的快照原則中，建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="2fa51-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="2fa51-104">句法</span><span class="sxs-lookup"><span data-stu-id="2fa51-104">SYNTAX</span></span>

### <span data-ttu-id="2fa51-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2fa51-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa51-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fa51-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa51-107">說明</span><span class="sxs-lookup"><span data-stu-id="2fa51-107">DESCRIPTION</span></span>
<span data-ttu-id="2fa51-108">**新的-AzNetAppFilesActiveDirectory** Cmdlet 會為 ANF 帳戶建立新的快照原則。</span><span class="sxs-lookup"><span data-stu-id="2fa51-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="2fa51-109">示例</span><span class="sxs-lookup"><span data-stu-id="2fa51-109">EXAMPLES</span></span>

### <span data-ttu-id="2fa51-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2fa51-110">Example 1</span></span>
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

<span data-ttu-id="2fa51-111">這個命令會為名為「我的帳戶」的 ANF 帳戶建立新的 ANF 快照原則。</span><span class="sxs-lookup"><span data-stu-id="2fa51-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="2fa51-112">參數</span><span class="sxs-lookup"><span data-stu-id="2fa51-112">PARAMETERS</span></span>

### <span data-ttu-id="2fa51-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2fa51-113">-AccountName</span></span>
<span data-ttu-id="2fa51-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="2fa51-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="2fa51-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="2fa51-115">-AccountObject</span></span>
<span data-ttu-id="2fa51-116">新快照原則物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="2fa51-116">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="2fa51-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="2fa51-117">-DailySchedule</span></span>
<span data-ttu-id="2fa51-118">代表每日排程的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="2fa51-118">A hashtable array which represents the daily Schedule</span></span>

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

### <span data-ttu-id="2fa51-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa51-119">-DefaultProfile</span></span>
<span data-ttu-id="2fa51-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2fa51-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fa51-121">-啟用</span><span class="sxs-lookup"><span data-stu-id="2fa51-121">-Enabled</span></span>
<span data-ttu-id="2fa51-122">決定已啟用原則的屬性</span><span class="sxs-lookup"><span data-stu-id="2fa51-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="2fa51-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="2fa51-123">-HourlySchedule</span></span>
<span data-ttu-id="2fa51-124">代表每小時排程的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="2fa51-124">A hashtable array which represents the hourly Schedule</span></span>

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

### <span data-ttu-id="2fa51-125">-位置</span><span class="sxs-lookup"><span data-stu-id="2fa51-125">-Location</span></span>
<span data-ttu-id="2fa51-126">資源的位置</span><span class="sxs-lookup"><span data-stu-id="2fa51-126">The location of the resource</span></span>

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

### <span data-ttu-id="2fa51-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="2fa51-127">-MonthlySchedule</span></span>
<span data-ttu-id="2fa51-128">代表 montly 排程的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="2fa51-128">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="2fa51-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="2fa51-129">-Name</span></span>
<span data-ttu-id="2fa51-130">ANF 快照原則的名稱</span><span class="sxs-lookup"><span data-stu-id="2fa51-130">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="2fa51-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fa51-131">-ResourceGroupName</span></span>
<span data-ttu-id="2fa51-132">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="2fa51-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="2fa51-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="2fa51-133">-Tag</span></span>
<span data-ttu-id="2fa51-134">代表資源標記的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="2fa51-134">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="2fa51-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="2fa51-135">-WeeklySchedule</span></span>
<span data-ttu-id="2fa51-136">代表 montly 排程的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="2fa51-136">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="2fa51-137">-確認</span><span class="sxs-lookup"><span data-stu-id="2fa51-137">-Confirm</span></span>
<span data-ttu-id="2fa51-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2fa51-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa51-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa51-139">-WhatIf</span></span>
<span data-ttu-id="2fa51-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2fa51-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa51-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2fa51-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fa51-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa51-142">CommonParameters</span></span>
<span data-ttu-id="2fa51-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2fa51-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa51-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2fa51-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa51-145">輸入</span><span class="sxs-lookup"><span data-stu-id="2fa51-145">INPUTS</span></span>

### <span data-ttu-id="2fa51-146">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="2fa51-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="2fa51-147">輸出</span><span class="sxs-lookup"><span data-stu-id="2fa51-147">OUTPUTS</span></span>

### <span data-ttu-id="2fa51-148">PSNetAppFilesSnapshotPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="2fa51-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="2fa51-149">筆記</span><span class="sxs-lookup"><span data-stu-id="2fa51-149">NOTES</span></span>

## <span data-ttu-id="2fa51-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fa51-150">RELATED LINKS</span></span>
