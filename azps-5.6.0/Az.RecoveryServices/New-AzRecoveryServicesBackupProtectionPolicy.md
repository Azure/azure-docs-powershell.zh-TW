---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 65bda3a4829971ce3d073c672b578099130fae6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902250"
---
# <span data-ttu-id="8894d-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8894d-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="8894d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8894d-102">SYNOPSIS</span></span>
<span data-ttu-id="8894d-103">建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="8894d-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="8894d-104">語法</span><span class="sxs-lookup"><span data-stu-id="8894d-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8894d-105">描述</span><span class="sxs-lookup"><span data-stu-id="8894d-105">DESCRIPTION</span></span>
<span data-ttu-id="8894d-106">**New-AzRecoveryServicesBackupProtectionPolicy** Cmdlet 在儲存庫中建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="8894d-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="8894d-107">保護原則至少與一個保留原則相關聯。</span><span class="sxs-lookup"><span data-stu-id="8894d-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="8894d-108">保留原則會定義復原點與 Azure 備份的保留時間。</span><span class="sxs-lookup"><span data-stu-id="8894d-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="8894d-109">您可以使用 Cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject取得預設的保留原則。</span><span class="sxs-lookup"><span data-stu-id="8894d-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="8894d-110">您也可以使用 Get-AzRecoveryServicesBackupSchedulePolicyObject Cmdlet 取得預設的排程策略。</span><span class="sxs-lookup"><span data-stu-id="8894d-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="8894d-111">**SchedulePolicy 和** **RetentionPolicy** 物件會做為 **New-AzRecoveryServicesBackupProtectionPolicy** Cmdlet 的輸入。</span><span class="sxs-lookup"><span data-stu-id="8894d-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="8894d-112">使用目前的 Cmdlet 之前，使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定庫內容。</span><span class="sxs-lookup"><span data-stu-id="8894d-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8894d-113">例子</span><span class="sxs-lookup"><span data-stu-id="8894d-113">EXAMPLES</span></span>

### <span data-ttu-id="8894d-114">範例 1：建立備份保護原則</span><span class="sxs-lookup"><span data-stu-id="8894d-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="8894d-115">第一個命令會獲得一個 **基準 SchedulePolicyObject，** 然後將它儲存在$SchPol變數中。</span><span class="sxs-lookup"><span data-stu-id="8894d-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="8894d-116">第二個命令會從任務中的排程策略移除所有$SchPol。</span><span class="sxs-lookup"><span data-stu-id="8894d-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="8894d-117">第三個命令使用 Get-Date Cmdlet 取得目前的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8894d-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="8894d-118">第四個命令會將目前的日期與時間$Dt排程策略的執行時間。</span><span class="sxs-lookup"><span data-stu-id="8894d-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="8894d-119">第五個命令會獲得一個基礎 **的 RetentionPolicy** 物件，然後將它儲存在$RetPol變數中。</span><span class="sxs-lookup"><span data-stu-id="8894d-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="8894d-120">第六個命令將保留持續時間規則設定為 365 天。</span><span class="sxs-lookup"><span data-stu-id="8894d-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="8894d-121">最後一個命令會根據先前命令所建立排程和保留原則，建立 **BackupProtectionPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="8894d-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="8894d-122">範例 2</span><span class="sxs-lookup"><span data-stu-id="8894d-122">Example 2</span></span>

<span data-ttu-id="8894d-123">建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="8894d-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="8894d-124"> (自動) </span><span class="sxs-lookup"><span data-stu-id="8894d-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="8894d-125">參數</span><span class="sxs-lookup"><span data-stu-id="8894d-125">PARAMETERS</span></span>

### <span data-ttu-id="8894d-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="8894d-126">-BackupManagementType</span></span>
<span data-ttu-id="8894d-127">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="8894d-127">The class of resources being protected.</span></span> <span data-ttu-id="8894d-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8894d-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8894d-129">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="8894d-129">AzureVM</span></span> 
- <span data-ttu-id="8894d-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="8894d-130">AzureStorage</span></span>
- <span data-ttu-id="8894d-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="8894d-131">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8894d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8894d-132">-DefaultProfile</span></span>
<span data-ttu-id="8894d-133">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8894d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8894d-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="8894d-134">-Name</span></span>
<span data-ttu-id="8894d-135">指定該策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="8894d-135">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8894d-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8894d-136">-RetentionPolicy</span></span>
<span data-ttu-id="8894d-137">指定基礎的 **RetentionPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="8894d-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="8894d-138">您可以使用 Get-AzRecoveryServicesBackupRetentionPolicyObject 取得 **RetentionPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="8894d-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8894d-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="8894d-139">-SchedulePolicy</span></span>
<span data-ttu-id="8894d-140">指定基準 **SchedulePolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="8894d-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="8894d-141">您可以使用 Get-AzRecoveryServicesBackupSchedulePolicyObject Cmdlet 取得 **SchedulePolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="8894d-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8894d-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8894d-142">-VaultId</span></span>
<span data-ttu-id="8894d-143">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="8894d-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8894d-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="8894d-144">-WorkloadType</span></span>
<span data-ttu-id="8894d-145">資源的工作量類型。</span><span class="sxs-lookup"><span data-stu-id="8894d-145">Workload type of the resource.</span></span> <span data-ttu-id="8894d-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8894d-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8894d-147">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="8894d-147">AzureVM</span></span> 
- <span data-ttu-id="8894d-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="8894d-148">AzureFiles</span></span>
- <span data-ttu-id="8894d-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="8894d-149">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8894d-150">-確認</span><span class="sxs-lookup"><span data-stu-id="8894d-150">-Confirm</span></span>
<span data-ttu-id="8894d-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8894d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8894d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8894d-152">-WhatIf</span></span>
<span data-ttu-id="8894d-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8894d-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="8894d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8894d-154">CommonParameters</span></span>
<span data-ttu-id="8894d-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8894d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8894d-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8894d-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8894d-157">輸入</span><span class="sxs-lookup"><span data-stu-id="8894d-157">INPUTS</span></span>

### <span data-ttu-id="8894d-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.WorkloadType</span><span class="sxs-lookup"><span data-stu-id="8894d-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="8894d-159">System.Nullable'1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8894d-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8894d-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="8894d-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="8894d-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="8894d-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="8894d-162">System.String</span><span class="sxs-lookup"><span data-stu-id="8894d-162">System.String</span></span>

## <span data-ttu-id="8894d-163">輸出</span><span class="sxs-lookup"><span data-stu-id="8894d-163">OUTPUTS</span></span>

### <span data-ttu-id="8894d-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="8894d-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="8894d-165">筆記</span><span class="sxs-lookup"><span data-stu-id="8894d-165">NOTES</span></span>

## <span data-ttu-id="8894d-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="8894d-166">RELATED LINKS</span></span>

[<span data-ttu-id="8894d-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="8894d-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="8894d-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8894d-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="8894d-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8894d-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="8894d-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="8894d-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="8894d-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8894d-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="8894d-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8894d-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


