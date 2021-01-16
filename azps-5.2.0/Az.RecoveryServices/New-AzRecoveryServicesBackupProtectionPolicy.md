---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281149"
---
# <span data-ttu-id="d0fd5-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0fd5-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="d0fd5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d0fd5-103">建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="d0fd5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0fd5-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0fd5-105">說明</span><span class="sxs-lookup"><span data-stu-id="d0fd5-105">DESCRIPTION</span></span>
<span data-ttu-id="d0fd5-106">**新的-AzRecoveryServicesBackupProtectionPolicy** Cmdlet 會在電子倉庫中建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="d0fd5-107">保護原則與至少一個保留原則相關聯。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="d0fd5-108">保留原則定義了在 Azure 備份中保留復原點的時間長度。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="d0fd5-109">您可以使用 Get-AzRecoveryServicesBackupRetentionPolicyObject Cmdlet 來取得預設的保留原則。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="d0fd5-110">您也可以使用 Get-AzRecoveryServicesBackupSchedulePolicyObject Cmdlet 來取得預設的排程原則。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="d0fd5-111">**SchedulePolicy** 和 **RetentionPolicy** 物件是用來做為 **新的 AzRecoveryServicesBackupProtectionPolicy** Cmdlet 的輸入。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="d0fd5-112">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d0fd5-113">示例</span><span class="sxs-lookup"><span data-stu-id="d0fd5-113">EXAMPLES</span></span>

### <span data-ttu-id="d0fd5-114">範例1：建立備份保護原則</span><span class="sxs-lookup"><span data-stu-id="d0fd5-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="d0fd5-115">第一個命令會取得基底 **SchedulePolicyObject**，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="d0fd5-116">第二個命令會從 $SchPol 的排程原則中移除所有排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="d0fd5-117">第三個命令使用 Get-Date Cmdlet 來取得目前的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="d0fd5-118">第四個命令會將目前的日期和時間 $Dt 為排程原則的排程執行時間。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="d0fd5-119">第五個命令會取得基底 **RetentionPolicy** 物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="d0fd5-120">第六個命令會將 [保留期間] 原則設定為365天。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="d0fd5-121">最終命令會根據先前命令建立的排程和保留原則，建立 **BackupProtectionPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="d0fd5-122">範例2</span><span class="sxs-lookup"><span data-stu-id="d0fd5-122">Example 2</span></span>

<span data-ttu-id="d0fd5-123">建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="d0fd5-124"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="d0fd5-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="d0fd5-125">參數</span><span class="sxs-lookup"><span data-stu-id="d0fd5-125">PARAMETERS</span></span>

### <span data-ttu-id="d0fd5-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d0fd5-126">-BackupManagementType</span></span>
<span data-ttu-id="d0fd5-127">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-127">The class of resources being protected.</span></span> <span data-ttu-id="d0fd5-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d0fd5-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d0fd5-129">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d0fd5-129">AzureVM</span></span> 
- <span data-ttu-id="d0fd5-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="d0fd5-130">AzureStorage</span></span>
- <span data-ttu-id="d0fd5-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="d0fd5-131">AzureWorkload</span></span>

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

### <span data-ttu-id="d0fd5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0fd5-132">-DefaultProfile</span></span>
<span data-ttu-id="d0fd5-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0fd5-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0fd5-134">-Name</span></span>
<span data-ttu-id="d0fd5-135">指定原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="d0fd5-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0fd5-136">-RetentionPolicy</span></span>
<span data-ttu-id="d0fd5-137">指定基底 **RetentionPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="d0fd5-138">您可以使用 Get-AzRecoveryServicesBackupRetentionPolicyObject Cmdlet 來取得 **RetentionPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="d0fd5-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="d0fd5-139">-SchedulePolicy</span></span>
<span data-ttu-id="d0fd5-140">指定基底 **SchedulePolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="d0fd5-141">您可以使用 Get-AzRecoveryServicesBackupSchedulePolicyObject Cmdlet 來取得 **SchedulePolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="d0fd5-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d0fd5-142">-VaultId</span></span>
<span data-ttu-id="d0fd5-143">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d0fd5-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d0fd5-144">-WorkloadType</span></span>
<span data-ttu-id="d0fd5-145">資源的工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-145">Workload type of the resource.</span></span> <span data-ttu-id="d0fd5-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d0fd5-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d0fd5-147">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d0fd5-147">AzureVM</span></span> 
- <span data-ttu-id="d0fd5-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="d0fd5-148">AzureFiles</span></span>
- <span data-ttu-id="d0fd5-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="d0fd5-149">MSSQL</span></span>

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

### <span data-ttu-id="d0fd5-150">-確認</span><span class="sxs-lookup"><span data-stu-id="d0fd5-150">-Confirm</span></span>
<span data-ttu-id="d0fd5-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0fd5-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0fd5-152">-WhatIf</span></span>
<span data-ttu-id="d0fd5-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="d0fd5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0fd5-154">CommonParameters</span></span>
<span data-ttu-id="d0fd5-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0fd5-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d0fd5-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0fd5-157">輸入</span><span class="sxs-lookup"><span data-stu-id="d0fd5-157">INPUTS</span></span>

### <span data-ttu-id="d0fd5-158">WorkloadType 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="d0fd5-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="d0fd5-159">RecoveryServices 為 Nullable "1 [BackupManagementType，RecoveryServices... 模型、版本 = 1.0.0.0、Culture = 中性、PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="d0fd5-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d0fd5-160">RetentionPolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="d0fd5-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="d0fd5-161">SchedulePolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="d0fd5-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="d0fd5-162">System.object</span><span class="sxs-lookup"><span data-stu-id="d0fd5-162">System.String</span></span>

## <span data-ttu-id="d0fd5-163">輸出</span><span class="sxs-lookup"><span data-stu-id="d0fd5-163">OUTPUTS</span></span>

### <span data-ttu-id="d0fd5-164">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="d0fd5-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="d0fd5-165">筆記</span><span class="sxs-lookup"><span data-stu-id="d0fd5-165">NOTES</span></span>

## <span data-ttu-id="d0fd5-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0fd5-166">RELATED LINKS</span></span>

[<span data-ttu-id="d0fd5-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d0fd5-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="d0fd5-168">AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0fd5-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d0fd5-169">AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d0fd5-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="d0fd5-170">AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="d0fd5-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="d0fd5-171">移除-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0fd5-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d0fd5-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0fd5-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


