---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c71dcc24947070a6d57aa617d121c1b5fcc3e923
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913741"
---
# <span data-ttu-id="6549a-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6549a-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="6549a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6549a-102">SYNOPSIS</span></span>
<span data-ttu-id="6549a-103">修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="6549a-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="6549a-104">語法</span><span class="sxs-lookup"><span data-stu-id="6549a-104">SYNTAX</span></span>

### <span data-ttu-id="6549a-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="6549a-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6549a-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="6549a-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6549a-107">描述</span><span class="sxs-lookup"><span data-stu-id="6549a-107">DESCRIPTION</span></span>
<span data-ttu-id="6549a-108">**Set-AzRecoveryServicesBackupProtectionPolicy** Cmdlet 會修改現有的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="6549a-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="6549a-109">您可以修改備份排程和保留原則元件。</span><span class="sxs-lookup"><span data-stu-id="6549a-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="6549a-110">您進行的任何變更都會影響與策略關聯的專案的備份和保留。</span><span class="sxs-lookup"><span data-stu-id="6549a-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="6549a-111">使用目前的 Cmdlet 之前，使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定庫內容。</span><span class="sxs-lookup"><span data-stu-id="6549a-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6549a-112">例子</span><span class="sxs-lookup"><span data-stu-id="6549a-112">EXAMPLES</span></span>

### <span data-ttu-id="6549a-113">範例 1：修改備份保護原則</span><span class="sxs-lookup"><span data-stu-id="6549a-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Time = Get-Date
PS C:\> $Time1 = Get-Date -Year $Time.Year -Month $Time.Month -Day $Time.Day -Hour $Time.Hour -Minute 0 -Second 0 -Millisecond 0
PS C:\> $Time1 = $Time1.ToUniversalTime()
PS C:\> $SchPol.ScheduleRunTimes.Add($Time1)
PS C:\> $SchPol.ScheduleRunFrequency.Clear
PS C:\> $SchPol.ScheduleRunDays.Add("Monday")
PS C:\> $SchPol.ScheduleRunFrequency="Weekly"
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.IsDailyScheduleEnabled=$false
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 0
PS C:\> $RetPol.IsWeeklyScheduleEnabled=$true 
PS C:\> $RetPol.WeeklySchedule.DaysOfTheWeek.Add("Monday")
PS C:\> $RetPol.WeeklySchedule.DurationCountInWeeks = 365
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "azurefiles" -Name "azurefilesvault"
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "TestPolicy" -VaultId $vault.ID
PS C:\> $Pol.SnapshotRetentionInDays=5
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="6549a-114">以下是修改保護政策時要遵循之步驟的高層級描述：</span><span class="sxs-lookup"><span data-stu-id="6549a-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="6549a-115">取得基準 SchedulePolicyObject 和 Base RetentionPolicyObject。</span><span class="sxs-lookup"><span data-stu-id="6549a-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="6549a-116">將它們儲存在一些變數中。</span><span class="sxs-lookup"><span data-stu-id="6549a-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="6549a-117">根據需求設定排程和保留原則物件的不同參數。</span><span class="sxs-lookup"><span data-stu-id="6549a-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="6549a-118">例如，在上述範例腳本中，我們嘗試設定每週保護政策。</span><span class="sxs-lookup"><span data-stu-id="6549a-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="6549a-119">因此，我們將排程頻率變更為「每週」，並更新排程執行時間。</span><span class="sxs-lookup"><span data-stu-id="6549a-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="6549a-120">在保留原則物件中，我們已更新每週保留持續時間，並設定正確的「啟用每週排程」標標。</span><span class="sxs-lookup"><span data-stu-id="6549a-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="6549a-121">若要設定每日策略，請設定 「啟用每日排程」標號為 True，並指派適當的值給其他物件參數。</span><span class="sxs-lookup"><span data-stu-id="6549a-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="6549a-122">取得您想要修改的備份保護原則，並儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="6549a-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="6549a-123">在上例中，我們取了一個名稱為 "TestPolicy" 的備份策略，而我們想要修改該名稱。</span><span class="sxs-lookup"><span data-stu-id="6549a-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="6549a-124">使用修改的排程策略物件和保留原則物件修改步驟 3 中所取回的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="6549a-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="6549a-125">參數</span><span class="sxs-lookup"><span data-stu-id="6549a-125">PARAMETERS</span></span>

### <span data-ttu-id="6549a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6549a-126">-DefaultProfile</span></span>
<span data-ttu-id="6549a-127">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6549a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6549a-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="6549a-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="6549a-129">切換參數，指出是否要重試失敗專案的 Policy Update。</span><span class="sxs-lookup"><span data-stu-id="6549a-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6549a-130">-策略</span><span class="sxs-lookup"><span data-stu-id="6549a-130">-Policy</span></span>
<span data-ttu-id="6549a-131">指定此 Cmdlet 修改的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="6549a-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="6549a-132">若要取得 **BackupProtectionPolicy 物件** ，請使用 Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6549a-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6549a-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6549a-133">-RetentionPolicy</span></span>
<span data-ttu-id="6549a-134">指定基本保留原則。</span><span class="sxs-lookup"><span data-stu-id="6549a-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="6549a-135">若要取得 **RetentionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupRetentionPolicyObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6549a-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6549a-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="6549a-136">-SchedulePolicy</span></span>
<span data-ttu-id="6549a-137">指定基準排程策略物件。</span><span class="sxs-lookup"><span data-stu-id="6549a-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="6549a-138">若要取得 **SchedulePolicy 物件** ，請使用Get-AzRecoveryServicesBackupSchedulePolicyObject物件。</span><span class="sxs-lookup"><span data-stu-id="6549a-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6549a-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6549a-139">-VaultId</span></span>
<span data-ttu-id="6549a-140">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6549a-140">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6549a-141">-確認</span><span class="sxs-lookup"><span data-stu-id="6549a-141">-Confirm</span></span>
<span data-ttu-id="6549a-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6549a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6549a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6549a-143">-WhatIf</span></span>
<span data-ttu-id="6549a-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6549a-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="6549a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6549a-145">CommonParameters</span></span>
<span data-ttu-id="6549a-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6549a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6549a-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6549a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6549a-148">輸入</span><span class="sxs-lookup"><span data-stu-id="6549a-148">INPUTS</span></span>

### <span data-ttu-id="6549a-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="6549a-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="6549a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="6549a-150">System.String</span></span>

## <span data-ttu-id="6549a-151">輸出</span><span class="sxs-lookup"><span data-stu-id="6549a-151">OUTPUTS</span></span>

### <span data-ttu-id="6549a-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.JobBase</span><span class="sxs-lookup"><span data-stu-id="6549a-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6549a-153">筆記</span><span class="sxs-lookup"><span data-stu-id="6549a-153">NOTES</span></span>

## <span data-ttu-id="6549a-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="6549a-154">RELATED LINKS</span></span>

[<span data-ttu-id="6549a-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6549a-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6549a-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6549a-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="6549a-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6549a-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6549a-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6549a-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


