---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 16bb97fdfab6d890f67bef209acaa584b5a67487
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959464"
---
# <span data-ttu-id="ce7d7-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce7d7-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="ce7d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7d7-103">修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="ce7d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce7d7-104">SYNTAX</span></span>

### <span data-ttu-id="ce7d7-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="ce7d7-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce7d7-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="ce7d7-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce7d7-107">說明</span><span class="sxs-lookup"><span data-stu-id="ce7d7-107">DESCRIPTION</span></span>
<span data-ttu-id="ce7d7-108">**AzBackupProtectionPolicy** Cmdlet 會修改現有的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-108">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="ce7d7-109">您可以修改備份排程與保留原則的元件。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="ce7d7-110">您所做的任何變更都會影響與原則相關的專案的備份與保留。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="ce7d7-111">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ce7d7-112">示例</span><span class="sxs-lookup"><span data-stu-id="ce7d7-112">EXAMPLES</span></span>

### <span data-ttu-id="ce7d7-113">範例1：修改備份保護原則</span><span class="sxs-lookup"><span data-stu-id="ce7d7-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> $Pol.AzureBackupRGName = "RG_prefix"
PS C:\> $Pol.AzureBackupRGNameSuffix = "RG_suffix"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="ce7d7-114">第一個命令會取得基 SchedulePolicy 物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="ce7d7-115">第二個命令會從 $SchPol 的排程原則中移除所有排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="ce7d7-116">第三個命令使用 Get-Date Cmdlet 來取得目前的日期和時間，然後將它儲存在 $DT 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="ce7d7-117">第四個命令會將 $DT 中的日期和時間新增至排程原則的排程執行時間。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="ce7d7-118">第五個命令會取得基本保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="ce7d7-119">第六個命令會將保留期間設定為365天。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="ce7d7-120">第七個命令會取得名為 NewPolicy 的備份保護原則，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="ce7d7-121">第八和第九會設定與儲存還原點之原則相關聯的資源群組參數。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="ce7d7-122">最後一個命令會在 $Pol 中使用排程 $SchPol 原則，以及 $RetPol 中的保留原則來修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="ce7d7-123">參數</span><span class="sxs-lookup"><span data-stu-id="ce7d7-123">PARAMETERS</span></span>

### <span data-ttu-id="ce7d7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce7d7-124">-DefaultProfile</span></span>
<span data-ttu-id="ce7d7-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce7d7-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="ce7d7-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="ce7d7-127">指示是否要重試失敗專案原則更新的切換參數。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="ce7d7-128">-原則</span><span class="sxs-lookup"><span data-stu-id="ce7d7-128">-Policy</span></span>
<span data-ttu-id="ce7d7-129">指定此 Cmdlet 修改的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="ce7d7-130">若要取得 **BackupProtectionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="ce7d7-131">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce7d7-131">-RetentionPolicy</span></span>
<span data-ttu-id="ce7d7-132">指定基本保留原則。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="ce7d7-133">若要取得 **RetentionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupRetentionPolicyObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="ce7d7-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="ce7d7-134">-SchedulePolicy</span></span>
<span data-ttu-id="ce7d7-135">指定基本排程原則物件。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="ce7d7-136">若要取得 **SchedulePolicy** 物件，請使用 Get-AzRecoveryServicesBackupSchedulePolicyObject 物件。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="ce7d7-137">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ce7d7-137">-VaultId</span></span>
<span data-ttu-id="ce7d7-138">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ce7d7-139">-確認</span><span class="sxs-lookup"><span data-stu-id="ce7d7-139">-Confirm</span></span>
<span data-ttu-id="ce7d7-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce7d7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce7d7-141">-WhatIf</span></span>
<span data-ttu-id="ce7d7-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce7d7-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce7d7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7d7-144">CommonParameters</span></span>
<span data-ttu-id="ce7d7-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7d7-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ce7d7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7d7-147">輸入</span><span class="sxs-lookup"><span data-stu-id="ce7d7-147">INPUTS</span></span>

### <span data-ttu-id="ce7d7-148">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="ce7d7-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="ce7d7-149">System.object</span><span class="sxs-lookup"><span data-stu-id="ce7d7-149">System.String</span></span>

## <span data-ttu-id="ce7d7-150">輸出</span><span class="sxs-lookup"><span data-stu-id="ce7d7-150">OUTPUTS</span></span>

### <span data-ttu-id="ce7d7-151">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="ce7d7-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ce7d7-152">筆記</span><span class="sxs-lookup"><span data-stu-id="ce7d7-152">NOTES</span></span>

## <span data-ttu-id="ce7d7-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce7d7-153">RELATED LINKS</span></span>

[<span data-ttu-id="ce7d7-154">AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce7d7-154">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ce7d7-155">AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ce7d7-155">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="ce7d7-156">新-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce7d7-156">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ce7d7-157">移除-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce7d7-157">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


