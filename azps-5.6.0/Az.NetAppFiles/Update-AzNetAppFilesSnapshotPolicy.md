---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cf099afe95eec37e070cc2b09d30b7f4b2766b8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905942"
---
# <span data-ttu-id="19aa7-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="19aa7-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="19aa7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="19aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="19aa7-103">將 Azure NetApp 檔案 (ANF) 快照快照策略更新為提供的選擇性修改程式。</span><span class="sxs-lookup"><span data-stu-id="19aa7-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="19aa7-104">語法</span><span class="sxs-lookup"><span data-stu-id="19aa7-104">SYNTAX</span></span>

### <span data-ttu-id="19aa7-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="19aa7-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19aa7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19aa7-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19aa7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19aa7-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19aa7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19aa7-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19aa7-109">描述</span><span class="sxs-lookup"><span data-stu-id="19aa7-109">DESCRIPTION</span></span>
<span data-ttu-id="19aa7-110">**Update-AzNetAppFilesnapshotPolicy** Cmdlet 會修改 ANF 快照策略。</span><span class="sxs-lookup"><span data-stu-id="19aa7-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="19aa7-111">例子</span><span class="sxs-lookup"><span data-stu-id="19aa7-111">EXAMPLES</span></span>

### <span data-ttu-id="19aa7-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="19aa7-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="19aa7-113">此命令會變更 ANF 備份策略 「MySnapshotPolicy」，讓系統提供 HourlySchedule。</span><span class="sxs-lookup"><span data-stu-id="19aa7-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="19aa7-114">參數</span><span class="sxs-lookup"><span data-stu-id="19aa7-114">PARAMETERS</span></span>

### <span data-ttu-id="19aa7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="19aa7-115">-AccountName</span></span>
<span data-ttu-id="19aa7-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="19aa7-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="19aa7-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="19aa7-117">-AccountObject</span></span>
<span data-ttu-id="19aa7-118">新快照策略物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="19aa7-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="19aa7-119">-每日排版</span><span class="sxs-lookup"><span data-stu-id="19aa7-119">-DailySchedule</span></span>
<span data-ttu-id="19aa7-120">代表每日排程的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="19aa7-120">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19aa7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19aa7-121">-DefaultProfile</span></span>
<span data-ttu-id="19aa7-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="19aa7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19aa7-123">-已啟用</span><span class="sxs-lookup"><span data-stu-id="19aa7-123">-Enabled</span></span>
<span data-ttu-id="19aa7-124">決定是否已啟用策略的屬性</span><span class="sxs-lookup"><span data-stu-id="19aa7-124">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19aa7-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="19aa7-125">-HourlySchedule</span></span>
<span data-ttu-id="19aa7-126">代表小時排程的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="19aa7-126">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19aa7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19aa7-127">-InputObject</span></span>
<span data-ttu-id="19aa7-128">要移除的快照物件</span><span class="sxs-lookup"><span data-stu-id="19aa7-128">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19aa7-129">-位置</span><span class="sxs-lookup"><span data-stu-id="19aa7-129">-Location</span></span>
<span data-ttu-id="19aa7-130">資源的位置</span><span class="sxs-lookup"><span data-stu-id="19aa7-130">The location of the resource</span></span>

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

### <span data-ttu-id="19aa7-131">-每月排期</span><span class="sxs-lookup"><span data-stu-id="19aa7-131">-MonthlySchedule</span></span>
<span data-ttu-id="19aa7-132">代表 Montly Schedule 的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="19aa7-132">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19aa7-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="19aa7-133">-Name</span></span>
<span data-ttu-id="19aa7-134">ANF 快照策略的名稱</span><span class="sxs-lookup"><span data-stu-id="19aa7-134">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19aa7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19aa7-135">-ResourceGroupName</span></span>
<span data-ttu-id="19aa7-136">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="19aa7-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="19aa7-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19aa7-137">-ResourceId</span></span>
<span data-ttu-id="19aa7-138">ANF 快照策略的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="19aa7-138">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19aa7-139">-標記</span><span class="sxs-lookup"><span data-stu-id="19aa7-139">-Tag</span></span>
<span data-ttu-id="19aa7-140">代表資源標記的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="19aa7-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="19aa7-141">-每週排班</span><span class="sxs-lookup"><span data-stu-id="19aa7-141">-WeeklySchedule</span></span>
<span data-ttu-id="19aa7-142">代表 Montly Schedule 的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="19aa7-142">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19aa7-143">-確認</span><span class="sxs-lookup"><span data-stu-id="19aa7-143">-Confirm</span></span>
<span data-ttu-id="19aa7-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="19aa7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19aa7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19aa7-145">-WhatIf</span></span>
<span data-ttu-id="19aa7-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="19aa7-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19aa7-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="19aa7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19aa7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19aa7-148">CommonParameters</span></span>
<span data-ttu-id="19aa7-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="19aa7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19aa7-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19aa7-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19aa7-151">輸入</span><span class="sxs-lookup"><span data-stu-id="19aa7-151">INPUTS</span></span>

### <span data-ttu-id="19aa7-152">System.String</span><span class="sxs-lookup"><span data-stu-id="19aa7-152">System.String</span></span>

### <span data-ttu-id="19aa7-153">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="19aa7-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="19aa7-154">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilessnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="19aa7-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="19aa7-155">輸出</span><span class="sxs-lookup"><span data-stu-id="19aa7-155">OUTPUTS</span></span>

### <span data-ttu-id="19aa7-156">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilessnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="19aa7-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="19aa7-157">筆記</span><span class="sxs-lookup"><span data-stu-id="19aa7-157">NOTES</span></span>

## <span data-ttu-id="19aa7-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="19aa7-158">RELATED LINKS</span></span>
