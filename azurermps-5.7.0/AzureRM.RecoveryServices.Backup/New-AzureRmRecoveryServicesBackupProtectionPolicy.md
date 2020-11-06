---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9834236a72a68f64cc9b19d6576e56102f96b13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446100"
---
# <span data-ttu-id="38a5c-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38a5c-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="38a5c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="38a5c-103">建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="38a5c-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38a5c-104">句法</span><span class="sxs-lookup"><span data-stu-id="38a5c-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38a5c-105">說明</span><span class="sxs-lookup"><span data-stu-id="38a5c-105">DESCRIPTION</span></span>
<span data-ttu-id="38a5c-106">**新的-AzureRmRecoveryServicesBackupProtectionPolicy** Cmdlet 會在電子倉庫中建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="38a5c-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="38a5c-107">保護原則與至少一個保留原則相關聯。</span><span class="sxs-lookup"><span data-stu-id="38a5c-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="38a5c-108">保留原則定義了在 Azure 備份中保留復原點的時間長度。</span><span class="sxs-lookup"><span data-stu-id="38a5c-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="38a5c-109">您可以使用 Get-AzureRmRecoveryServicesBackupRetentionPolicyObject Cmdlet 來取得預設的保留原則。</span><span class="sxs-lookup"><span data-stu-id="38a5c-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="38a5c-110">您也可以使用 Get-AzureRmRecoveryServicesBackupSchedulePolicyObject Cmdlet 來取得預設的排程原則。</span><span class="sxs-lookup"><span data-stu-id="38a5c-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="38a5c-111">**SchedulePolicy** 和 **RetentionPolicy** 物件是用來做為 **新的 AzureRmRecoveryServicesBackupProtectionPolicy** Cmdlet 的輸入。</span><span class="sxs-lookup"><span data-stu-id="38a5c-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="38a5c-112">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38a5c-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="38a5c-113">示例</span><span class="sxs-lookup"><span data-stu-id="38a5c-113">EXAMPLES</span></span>

### <span data-ttu-id="38a5c-114">範例1：建立備份保護原則</span><span class="sxs-lookup"><span data-stu-id="38a5c-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="38a5c-115">第一個命令會取得基底 **SchedulePolicyObject** ，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="38a5c-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="38a5c-116">第二個命令會從 $SchPol 的排程原則中移除所有排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="38a5c-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="38a5c-117">第三個命令使用 Get-Date Cmdlet 來取得目前的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="38a5c-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="38a5c-118">第四個命令會將目前的日期和時間 $Dt 為排程原則的排程執行時間。</span><span class="sxs-lookup"><span data-stu-id="38a5c-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="38a5c-119">第五個命令會取得基底 **RetentionPolicy** 物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="38a5c-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="38a5c-120">第六個命令會將 [保留期間] 原則設定為365天。</span><span class="sxs-lookup"><span data-stu-id="38a5c-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="38a5c-121">最終命令會根據先前命令建立的排程和保留原則，建立 **BackupProtectionPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="38a5c-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="38a5c-122">參數</span><span class="sxs-lookup"><span data-stu-id="38a5c-122">PARAMETERS</span></span>

### <span data-ttu-id="38a5c-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="38a5c-123">-BackupManagementType</span></span>
<span data-ttu-id="38a5c-124">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="38a5c-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="38a5c-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="38a5c-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="38a5c-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="38a5c-126">AzureVM</span></span> 
- <span data-ttu-id="38a5c-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="38a5c-127">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a5c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a5c-128">-DefaultProfile</span></span>
<span data-ttu-id="38a5c-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38a5c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a5c-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="38a5c-130">-Name</span></span>
<span data-ttu-id="38a5c-131">指定原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="38a5c-131">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a5c-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="38a5c-132">-RetentionPolicy</span></span>
<span data-ttu-id="38a5c-133">指定基底 **RetentionPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="38a5c-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="38a5c-134">您可以使用 Get-AzureRmRecoveryServicesBackupRetentionPolicyObject Cmdlet 來取得 **RetentionPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="38a5c-134">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a5c-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="38a5c-135">-SchedulePolicy</span></span>
<span data-ttu-id="38a5c-136">指定基底 **SchedulePolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="38a5c-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="38a5c-137">您可以使用 Get-AzureRmRecoveryServicesBackupSchedulePolicyObject Cmdlet 來取得 **SchedulePolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="38a5c-137">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a5c-138">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="38a5c-138">-WorkloadType</span></span>
<span data-ttu-id="38a5c-139">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="38a5c-139">Specifies the workload type.</span></span>
<span data-ttu-id="38a5c-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="38a5c-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="38a5c-141">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="38a5c-141">AzureVM</span></span> 
- <span data-ttu-id="38a5c-142">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="38a5c-142">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a5c-143">-確認</span><span class="sxs-lookup"><span data-stu-id="38a5c-143">-Confirm</span></span>
<span data-ttu-id="38a5c-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38a5c-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a5c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a5c-145">-WhatIf</span></span>
<span data-ttu-id="38a5c-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38a5c-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38a5c-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38a5c-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a5c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a5c-148">CommonParameters</span></span>
<span data-ttu-id="38a5c-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38a5c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a5c-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38a5c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a5c-151">輸入</span><span class="sxs-lookup"><span data-stu-id="38a5c-151">INPUTS</span></span>

### <span data-ttu-id="38a5c-152">所有</span><span class="sxs-lookup"><span data-stu-id="38a5c-152">None</span></span>
<span data-ttu-id="38a5c-153">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="38a5c-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38a5c-154">輸出</span><span class="sxs-lookup"><span data-stu-id="38a5c-154">OUTPUTS</span></span>

### <span data-ttu-id="38a5c-155">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="38a5c-155">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="38a5c-156">筆記</span><span class="sxs-lookup"><span data-stu-id="38a5c-156">NOTES</span></span>

## <span data-ttu-id="38a5c-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="38a5c-157">RELATED LINKS</span></span>

[<span data-ttu-id="38a5c-158">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="38a5c-158">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="38a5c-159">AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38a5c-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="38a5c-160">AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="38a5c-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="38a5c-161">AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="38a5c-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="38a5c-162">移除-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38a5c-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="38a5c-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38a5c-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


