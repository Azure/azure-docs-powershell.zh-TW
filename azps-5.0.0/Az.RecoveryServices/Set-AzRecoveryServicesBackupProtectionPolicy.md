---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f9cd7064c1949639526f2e7b84f01fb6355b584f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137148"
---
# <span data-ttu-id="be01b-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="be01b-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="be01b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be01b-102">SYNOPSIS</span></span>
<span data-ttu-id="be01b-103">修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="be01b-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="be01b-104">句法</span><span class="sxs-lookup"><span data-stu-id="be01b-104">SYNTAX</span></span>

### <span data-ttu-id="be01b-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="be01b-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be01b-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="be01b-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be01b-107">說明</span><span class="sxs-lookup"><span data-stu-id="be01b-107">DESCRIPTION</span></span>
<span data-ttu-id="be01b-108">**AzRecoveryServicesBackupProtectionPolicy** Cmdlet 會修改現有的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="be01b-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="be01b-109">您可以修改備份排程與保留原則的元件。</span><span class="sxs-lookup"><span data-stu-id="be01b-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="be01b-110">您所做的任何變更都會影響與原則相關的專案的備份與保留。</span><span class="sxs-lookup"><span data-stu-id="be01b-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="be01b-111">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be01b-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="be01b-112">示例</span><span class="sxs-lookup"><span data-stu-id="be01b-112">EXAMPLES</span></span>

### <span data-ttu-id="be01b-113">範例1：修改備份保護原則</span><span class="sxs-lookup"><span data-stu-id="be01b-113">Example 1: Modify a Backup protection policy</span></span>
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

<span data-ttu-id="be01b-114">第一個命令會取得基 SchedulePolicy 物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="be01b-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="be01b-115">第二個命令會從 $SchPol 的排程原則中移除所有排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="be01b-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="be01b-116">第三個命令使用 Get-Date Cmdlet 來取得目前的日期和時間，然後將它儲存在 $DT 變數中。</span><span class="sxs-lookup"><span data-stu-id="be01b-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="be01b-117">第四個命令會將 $DT 中的日期和時間新增至排程原則的排程執行時間。</span><span class="sxs-lookup"><span data-stu-id="be01b-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="be01b-118">第五個命令會取得基本保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="be01b-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="be01b-119">第六個命令會將保留期間設定為365天。</span><span class="sxs-lookup"><span data-stu-id="be01b-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="be01b-120">第七個命令會取得名為 NewPolicy 的備份保護原則，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="be01b-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="be01b-121">第八和第九會設定與儲存還原點之原則相關聯的資源群組參數。</span><span class="sxs-lookup"><span data-stu-id="be01b-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="be01b-122">最後一個命令會在 $Pol 中使用排程 $SchPol 原則，以及 $RetPol 中的保留原則來修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="be01b-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="be01b-123">參數</span><span class="sxs-lookup"><span data-stu-id="be01b-123">PARAMETERS</span></span>

### <span data-ttu-id="be01b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be01b-124">-DefaultProfile</span></span>
<span data-ttu-id="be01b-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be01b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be01b-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="be01b-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="be01b-127">指示是否要重試失敗專案原則更新的切換參數。</span><span class="sxs-lookup"><span data-stu-id="be01b-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="be01b-128">-原則</span><span class="sxs-lookup"><span data-stu-id="be01b-128">-Policy</span></span>
<span data-ttu-id="be01b-129">指定此 Cmdlet 修改的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="be01b-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="be01b-130">若要取得 **BackupProtectionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be01b-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="be01b-131">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="be01b-131">-RetentionPolicy</span></span>
<span data-ttu-id="be01b-132">指定基本保留原則。</span><span class="sxs-lookup"><span data-stu-id="be01b-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="be01b-133">若要取得 **RetentionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupRetentionPolicyObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be01b-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="be01b-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="be01b-134">-SchedulePolicy</span></span>
<span data-ttu-id="be01b-135">指定基本排程原則物件。</span><span class="sxs-lookup"><span data-stu-id="be01b-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="be01b-136">若要取得 **SchedulePolicy** 物件，請使用 Get-AzRecoveryServicesBackupSchedulePolicyObject 物件。</span><span class="sxs-lookup"><span data-stu-id="be01b-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="be01b-137">-VaultId</span><span class="sxs-lookup"><span data-stu-id="be01b-137">-VaultId</span></span>
<span data-ttu-id="be01b-138">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="be01b-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="be01b-139">-確認</span><span class="sxs-lookup"><span data-stu-id="be01b-139">-Confirm</span></span>
<span data-ttu-id="be01b-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="be01b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be01b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be01b-141">-WhatIf</span></span>
<span data-ttu-id="be01b-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be01b-142">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="be01b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be01b-143">CommonParameters</span></span>
<span data-ttu-id="be01b-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be01b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be01b-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="be01b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be01b-146">輸入</span><span class="sxs-lookup"><span data-stu-id="be01b-146">INPUTS</span></span>

### <span data-ttu-id="be01b-147">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="be01b-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="be01b-148">System.object</span><span class="sxs-lookup"><span data-stu-id="be01b-148">System.String</span></span>

## <span data-ttu-id="be01b-149">輸出</span><span class="sxs-lookup"><span data-stu-id="be01b-149">OUTPUTS</span></span>

### <span data-ttu-id="be01b-150">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="be01b-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="be01b-151">筆記</span><span class="sxs-lookup"><span data-stu-id="be01b-151">NOTES</span></span>

## <span data-ttu-id="be01b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="be01b-152">RELATED LINKS</span></span>

[<span data-ttu-id="be01b-153">AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="be01b-153">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="be01b-154">AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="be01b-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="be01b-155">新-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="be01b-155">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="be01b-156">移除-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="be01b-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


