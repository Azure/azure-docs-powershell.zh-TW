---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: fb0373e97d719535c87c01c0a4b53b029cc2a878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451799"
---
# <span data-ttu-id="24940-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="24940-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="24940-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24940-102">SYNOPSIS</span></span>
<span data-ttu-id="24940-103">修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="24940-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24940-104">句法</span><span class="sxs-lookup"><span data-stu-id="24940-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24940-105">說明</span><span class="sxs-lookup"><span data-stu-id="24940-105">DESCRIPTION</span></span>
<span data-ttu-id="24940-106">**AzureRmBackupProtectionPolicy** Cmdlet 會修改現有的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="24940-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="24940-107">您可以修改備份排程與保留原則的元件。</span><span class="sxs-lookup"><span data-stu-id="24940-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="24940-108">您所做的任何變更都會影響與原則相關的專案的備份與保留。</span><span class="sxs-lookup"><span data-stu-id="24940-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="24940-109">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24940-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="24940-110">示例</span><span class="sxs-lookup"><span data-stu-id="24940-110">EXAMPLES</span></span>

### <span data-ttu-id="24940-111">範例1：修改備份保護原則</span><span class="sxs-lookup"><span data-stu-id="24940-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="24940-112">第一個命令會取得基 SchedulePolicy 物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="24940-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="24940-113">第二個命令會從 $SchPol 的排程原則中移除所有排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="24940-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="24940-114">第三個命令使用 Get-Date Cmdlet 來取得目前的日期和時間，然後將它儲存在 $DT 變數中。</span><span class="sxs-lookup"><span data-stu-id="24940-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="24940-115">第四個命令會將 $DT 中的日期和時間新增至排程原則的排程執行時間。</span><span class="sxs-lookup"><span data-stu-id="24940-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="24940-116">第五個命令會取得基本保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="24940-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="24940-117">第六個命令會將保留期間設定為365天。</span><span class="sxs-lookup"><span data-stu-id="24940-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="24940-118">第七個命令會取得名為 NewPolicy 的備份保護原則，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="24940-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="24940-119">最後一個命令會在 $Pol 中使用排程 $SchPol 原則，以及 $RetPol 中的保留原則來修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="24940-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="24940-120">參數</span><span class="sxs-lookup"><span data-stu-id="24940-120">PARAMETERS</span></span>

### <span data-ttu-id="24940-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24940-121">-DefaultProfile</span></span>
<span data-ttu-id="24940-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24940-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24940-123">-原則</span><span class="sxs-lookup"><span data-stu-id="24940-123">-Policy</span></span>
<span data-ttu-id="24940-124">指定此 Cmdlet 修改的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="24940-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="24940-125">若要取得 **BackupProtectionPolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24940-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="24940-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="24940-126">-RetentionPolicy</span></span>
<span data-ttu-id="24940-127">指定基本保留原則。</span><span class="sxs-lookup"><span data-stu-id="24940-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="24940-128">若要取得 **RetentionPolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupRetentionPolicyObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24940-128">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24940-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="24940-129">-SchedulePolicy</span></span>
<span data-ttu-id="24940-130">指定基本排程原則物件。</span><span class="sxs-lookup"><span data-stu-id="24940-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="24940-131">若要取得 **SchedulePolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupSchedulePolicyObject 物件。</span><span class="sxs-lookup"><span data-stu-id="24940-131">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24940-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="24940-132">-VaultId</span></span>
<span data-ttu-id="24940-133">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="24940-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="24940-134">-確認</span><span class="sxs-lookup"><span data-stu-id="24940-134">-Confirm</span></span>
<span data-ttu-id="24940-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24940-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24940-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24940-136">-WhatIf</span></span>
<span data-ttu-id="24940-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24940-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24940-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24940-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24940-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24940-139">CommonParameters</span></span>
<span data-ttu-id="24940-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24940-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24940-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24940-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24940-142">輸入</span><span class="sxs-lookup"><span data-stu-id="24940-142">INPUTS</span></span>

### <span data-ttu-id="24940-143">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="24940-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>
<span data-ttu-id="24940-144">參數：原則 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="24940-144">Parameters: Policy (ByValue)</span></span>

### <span data-ttu-id="24940-145">System.object</span><span class="sxs-lookup"><span data-stu-id="24940-145">System.String</span></span>
<span data-ttu-id="24940-146">參數： VaultId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="24940-146">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="24940-147">輸出</span><span class="sxs-lookup"><span data-stu-id="24940-147">OUTPUTS</span></span>

### <span data-ttu-id="24940-148">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="24940-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="24940-149">筆記</span><span class="sxs-lookup"><span data-stu-id="24940-149">NOTES</span></span>

## <span data-ttu-id="24940-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="24940-150">RELATED LINKS</span></span>

[<span data-ttu-id="24940-151">AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="24940-151">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="24940-152">AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="24940-152">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="24940-153">新-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="24940-153">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="24940-154">移除-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="24940-154">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


