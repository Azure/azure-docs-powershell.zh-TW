---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281401"
---
# <span data-ttu-id="12897-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="12897-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="12897-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12897-102">SYNOPSIS</span></span>
<span data-ttu-id="12897-103">修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="12897-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="12897-104">句法</span><span class="sxs-lookup"><span data-stu-id="12897-104">SYNTAX</span></span>

### <span data-ttu-id="12897-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="12897-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12897-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="12897-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12897-107">說明</span><span class="sxs-lookup"><span data-stu-id="12897-107">DESCRIPTION</span></span>
<span data-ttu-id="12897-108">**AzRecoveryServicesBackupProtectionPolicy** Cmdlet 會修改現有的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="12897-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="12897-109">您可以修改備份排程與保留原則的元件。</span><span class="sxs-lookup"><span data-stu-id="12897-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="12897-110">您所做的任何變更都會影響與原則相關的專案的備份與保留。</span><span class="sxs-lookup"><span data-stu-id="12897-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="12897-111">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12897-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="12897-112">示例</span><span class="sxs-lookup"><span data-stu-id="12897-112">EXAMPLES</span></span>

### <span data-ttu-id="12897-113">範例1：修改備份保護原則</span><span class="sxs-lookup"><span data-stu-id="12897-113">Example 1: Modify a Backup protection policy</span></span>
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

<span data-ttu-id="12897-114">以下是修改保護原則所遵循之步驟的高層描述：</span><span class="sxs-lookup"><span data-stu-id="12897-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="12897-115">取得基本 SchedulePolicyObject 和基 RetentionPolicyObject。</span><span class="sxs-lookup"><span data-stu-id="12897-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="12897-116">將它們儲存在一些變數中。</span><span class="sxs-lookup"><span data-stu-id="12897-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="12897-117">根據您的需求，設定排程與保留原則物件的不同參數。</span><span class="sxs-lookup"><span data-stu-id="12897-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="12897-118">例如，在上述範例腳本中，我們嘗試設定每週保護原則。</span><span class="sxs-lookup"><span data-stu-id="12897-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="12897-119">因此，我們將排程頻率變更為 [每週]，並且也更新排程執行時間。</span><span class="sxs-lookup"><span data-stu-id="12897-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="12897-120">在 [保留原則] 物件中，我們會更新每週保留期間，並設定正確的「每週排程已啟用」標誌。</span><span class="sxs-lookup"><span data-stu-id="12897-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="12897-121">如果您想要設定每日原則，請將「已啟用每日排程」標誌設定為 true，並為其他物件參數指派適當的值。</span><span class="sxs-lookup"><span data-stu-id="12897-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="12897-122">取得您要修改的備份保護原則，並將它儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="12897-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="12897-123">在上述範例中，我們檢索了要修改之名稱為 "TestPolicy" 的備份原則。</span><span class="sxs-lookup"><span data-stu-id="12897-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="12897-124">使用已修改的排程原則物件和保留原則物件來修改在步驟3中檢索到的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="12897-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="12897-125">參數</span><span class="sxs-lookup"><span data-stu-id="12897-125">PARAMETERS</span></span>

### <span data-ttu-id="12897-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12897-126">-DefaultProfile</span></span>
<span data-ttu-id="12897-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12897-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12897-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="12897-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="12897-129">指示是否要重試失敗專案原則更新的切換參數。</span><span class="sxs-lookup"><span data-stu-id="12897-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="12897-130">-原則</span><span class="sxs-lookup"><span data-stu-id="12897-130">-Policy</span></span>
<span data-ttu-id="12897-131">指定此 Cmdlet 修改的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="12897-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="12897-132">若要取得 **BackupProtectionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12897-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="12897-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="12897-133">-RetentionPolicy</span></span>
<span data-ttu-id="12897-134">指定基本保留原則。</span><span class="sxs-lookup"><span data-stu-id="12897-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="12897-135">若要取得 **RetentionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupRetentionPolicyObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12897-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="12897-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="12897-136">-SchedulePolicy</span></span>
<span data-ttu-id="12897-137">指定基本排程原則物件。</span><span class="sxs-lookup"><span data-stu-id="12897-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="12897-138">若要取得 **SchedulePolicy** 物件，請使用 Get-AzRecoveryServicesBackupSchedulePolicyObject 物件。</span><span class="sxs-lookup"><span data-stu-id="12897-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="12897-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="12897-139">-VaultId</span></span>
<span data-ttu-id="12897-140">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="12897-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="12897-141">-確認</span><span class="sxs-lookup"><span data-stu-id="12897-141">-Confirm</span></span>
<span data-ttu-id="12897-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12897-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12897-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12897-143">-WhatIf</span></span>
<span data-ttu-id="12897-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12897-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="12897-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12897-145">CommonParameters</span></span>
<span data-ttu-id="12897-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12897-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12897-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="12897-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12897-148">輸入</span><span class="sxs-lookup"><span data-stu-id="12897-148">INPUTS</span></span>

### <span data-ttu-id="12897-149">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="12897-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="12897-150">System.object</span><span class="sxs-lookup"><span data-stu-id="12897-150">System.String</span></span>

## <span data-ttu-id="12897-151">輸出</span><span class="sxs-lookup"><span data-stu-id="12897-151">OUTPUTS</span></span>

### <span data-ttu-id="12897-152">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="12897-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="12897-153">筆記</span><span class="sxs-lookup"><span data-stu-id="12897-153">NOTES</span></span>

## <span data-ttu-id="12897-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="12897-154">RELATED LINKS</span></span>

[<span data-ttu-id="12897-155">AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="12897-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="12897-156">AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="12897-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="12897-157">新-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="12897-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="12897-158">移除-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="12897-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


