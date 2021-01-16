---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276988"
---
# <span data-ttu-id="1fb6b-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb6b-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1fb6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fb6b-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb6b-103">將 (ANF) 快照原則的 Azure NetApp 檔案更新為所提供的選擇性修飾符。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="1fb6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fb6b-104">SYNTAX</span></span>

### <span data-ttu-id="1fb6b-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1fb6b-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb6b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fb6b-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb6b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fb6b-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb6b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fb6b-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1fb6b-109">說明</span><span class="sxs-lookup"><span data-stu-id="1fb6b-109">DESCRIPTION</span></span>
<span data-ttu-id="1fb6b-110">**AzNetAppFilesSnapshotPolicy** Cmdlet 會修改 ANF 快照原則。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="1fb6b-111">示例</span><span class="sxs-lookup"><span data-stu-id="1fb6b-111">EXAMPLES</span></span>

### <span data-ttu-id="1fb6b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1fb6b-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="1fb6b-113">這個命令會將 ANF 備份原則 "MySnapshotPolicy" 變更為擁有指定的 HourlySchedule。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="1fb6b-114">參數</span><span class="sxs-lookup"><span data-stu-id="1fb6b-114">PARAMETERS</span></span>

### <span data-ttu-id="1fb6b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1fb6b-115">-AccountName</span></span>
<span data-ttu-id="1fb6b-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="1fb6b-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="1fb6b-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="1fb6b-117">-AccountObject</span></span>
<span data-ttu-id="1fb6b-118">新快照原則物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="1fb6b-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="1fb6b-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="1fb6b-119">-DailySchedule</span></span>
<span data-ttu-id="1fb6b-120">代表每日排程的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="1fb6b-120">A hashtable array which represents the daily Schedule</span></span>

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

### <span data-ttu-id="1fb6b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb6b-121">-DefaultProfile</span></span>
<span data-ttu-id="1fb6b-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb6b-123">-啟用</span><span class="sxs-lookup"><span data-stu-id="1fb6b-123">-Enabled</span></span>
<span data-ttu-id="1fb6b-124">決定已啟用原則的屬性</span><span class="sxs-lookup"><span data-stu-id="1fb6b-124">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="1fb6b-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="1fb6b-125">-HourlySchedule</span></span>
<span data-ttu-id="1fb6b-126">代表每小時排程的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="1fb6b-126">A hashtable array which represents the hourly Schedule</span></span>

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

### <span data-ttu-id="1fb6b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fb6b-127">-InputObject</span></span>
<span data-ttu-id="1fb6b-128">要移除的快照物件</span><span class="sxs-lookup"><span data-stu-id="1fb6b-128">The snapshot object to remove</span></span>

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

### <span data-ttu-id="1fb6b-129">-位置</span><span class="sxs-lookup"><span data-stu-id="1fb6b-129">-Location</span></span>
<span data-ttu-id="1fb6b-130">資源的位置</span><span class="sxs-lookup"><span data-stu-id="1fb6b-130">The location of the resource</span></span>

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

### <span data-ttu-id="1fb6b-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="1fb6b-131">-MonthlySchedule</span></span>
<span data-ttu-id="1fb6b-132">代表 montly 排程的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="1fb6b-132">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="1fb6b-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fb6b-133">-Name</span></span>
<span data-ttu-id="1fb6b-134">ANF 快照原則的名稱</span><span class="sxs-lookup"><span data-stu-id="1fb6b-134">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="1fb6b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb6b-135">-ResourceGroupName</span></span>
<span data-ttu-id="1fb6b-136">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="1fb6b-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1fb6b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fb6b-137">-ResourceId</span></span>
<span data-ttu-id="1fb6b-138">ANF 快照原則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1fb6b-138">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="1fb6b-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="1fb6b-139">-Tag</span></span>
<span data-ttu-id="1fb6b-140">代表資源標記的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="1fb6b-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="1fb6b-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="1fb6b-141">-WeeklySchedule</span></span>
<span data-ttu-id="1fb6b-142">代表 montly 排程的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="1fb6b-142">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="1fb6b-143">-確認</span><span class="sxs-lookup"><span data-stu-id="1fb6b-143">-Confirm</span></span>
<span data-ttu-id="1fb6b-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fb6b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fb6b-145">-WhatIf</span></span>
<span data-ttu-id="1fb6b-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fb6b-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fb6b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb6b-148">CommonParameters</span></span>
<span data-ttu-id="1fb6b-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb6b-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb6b-151">輸入</span><span class="sxs-lookup"><span data-stu-id="1fb6b-151">INPUTS</span></span>

### <span data-ttu-id="1fb6b-152">System.object</span><span class="sxs-lookup"><span data-stu-id="1fb6b-152">System.String</span></span>

### <span data-ttu-id="1fb6b-153">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="1fb6b-154">PSNetAppFilesSnapshotPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1fb6b-155">輸出</span><span class="sxs-lookup"><span data-stu-id="1fb6b-155">OUTPUTS</span></span>

### <span data-ttu-id="1fb6b-156">PSNetAppFilesSnapshotPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="1fb6b-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1fb6b-157">筆記</span><span class="sxs-lookup"><span data-stu-id="1fb6b-157">NOTES</span></span>

## <span data-ttu-id="1fb6b-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fb6b-158">RELATED LINKS</span></span>
