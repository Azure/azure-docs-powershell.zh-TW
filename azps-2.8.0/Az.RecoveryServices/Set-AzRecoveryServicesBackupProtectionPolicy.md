---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1f7dcd013bb91b8ba209cf3f7b031a90f7bb49cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792335"
---
# <span data-ttu-id="025f7-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="025f7-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="025f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="025f7-102">SYNOPSIS</span></span>
<span data-ttu-id="025f7-103">修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="025f7-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="025f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="025f7-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="025f7-105">說明</span><span class="sxs-lookup"><span data-stu-id="025f7-105">DESCRIPTION</span></span>
<span data-ttu-id="025f7-106">**AzBackupProtectionPolicy** Cmdlet 會修改現有的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="025f7-106">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="025f7-107">您可以修改備份排程與保留原則的元件。</span><span class="sxs-lookup"><span data-stu-id="025f7-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="025f7-108">您所做的任何變更都會影響與原則相關的專案的備份與保留。</span><span class="sxs-lookup"><span data-stu-id="025f7-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="025f7-109">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="025f7-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="025f7-110">示例</span><span class="sxs-lookup"><span data-stu-id="025f7-110">EXAMPLES</span></span>

### <span data-ttu-id="025f7-111">範例1：修改備份保護原則</span><span class="sxs-lookup"><span data-stu-id="025f7-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="025f7-112">第一個命令會取得基 SchedulePolicy 物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="025f7-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="025f7-113">第二個命令會從 $SchPol 的排程原則中移除所有排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="025f7-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="025f7-114">第三個命令使用 Get-Date Cmdlet 來取得目前的日期和時間，然後將它儲存在 $DT 變數中。</span><span class="sxs-lookup"><span data-stu-id="025f7-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="025f7-115">第四個命令會將 $DT 中的日期和時間新增至排程原則的排程執行時間。</span><span class="sxs-lookup"><span data-stu-id="025f7-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="025f7-116">第五個命令會取得基本保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="025f7-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="025f7-117">第六個命令會將保留期間設定為365天。</span><span class="sxs-lookup"><span data-stu-id="025f7-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="025f7-118">第七個命令會取得名為 NewPolicy 的備份保護原則，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="025f7-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="025f7-119">最後一個命令會在 $Pol 中使用排程 $SchPol 原則，以及 $RetPol 中的保留原則來修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="025f7-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="025f7-120">參數</span><span class="sxs-lookup"><span data-stu-id="025f7-120">PARAMETERS</span></span>

### <span data-ttu-id="025f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025f7-121">-DefaultProfile</span></span>
<span data-ttu-id="025f7-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="025f7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="025f7-123">-原則</span><span class="sxs-lookup"><span data-stu-id="025f7-123">-Policy</span></span>
<span data-ttu-id="025f7-124">指定此 Cmdlet 修改的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="025f7-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="025f7-125">若要取得 **BackupProtectionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="025f7-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="025f7-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="025f7-126">-RetentionPolicy</span></span>
<span data-ttu-id="025f7-127">指定基本保留原則。</span><span class="sxs-lookup"><span data-stu-id="025f7-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="025f7-128">若要取得 **RetentionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupRetentionPolicyObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="025f7-128">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="025f7-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="025f7-129">-SchedulePolicy</span></span>
<span data-ttu-id="025f7-130">指定基本排程原則物件。</span><span class="sxs-lookup"><span data-stu-id="025f7-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="025f7-131">若要取得 **SchedulePolicy** 物件，請使用 Get-AzRecoveryServicesBackupSchedulePolicyObject 物件。</span><span class="sxs-lookup"><span data-stu-id="025f7-131">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="025f7-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="025f7-132">-VaultId</span></span>
<span data-ttu-id="025f7-133">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="025f7-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="025f7-134">-確認</span><span class="sxs-lookup"><span data-stu-id="025f7-134">-Confirm</span></span>
<span data-ttu-id="025f7-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="025f7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="025f7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="025f7-136">-WhatIf</span></span>
<span data-ttu-id="025f7-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="025f7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="025f7-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="025f7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="025f7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025f7-139">CommonParameters</span></span>
<span data-ttu-id="025f7-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="025f7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025f7-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="025f7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025f7-142">輸入</span><span class="sxs-lookup"><span data-stu-id="025f7-142">INPUTS</span></span>

### <span data-ttu-id="025f7-143">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="025f7-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="025f7-144">System.object</span><span class="sxs-lookup"><span data-stu-id="025f7-144">System.String</span></span>

## <span data-ttu-id="025f7-145">輸出</span><span class="sxs-lookup"><span data-stu-id="025f7-145">OUTPUTS</span></span>

### <span data-ttu-id="025f7-146">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="025f7-146">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="025f7-147">筆記</span><span class="sxs-lookup"><span data-stu-id="025f7-147">NOTES</span></span>

## <span data-ttu-id="025f7-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="025f7-148">RELATED LINKS</span></span>

[<span data-ttu-id="025f7-149">AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="025f7-149">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="025f7-150">AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="025f7-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="025f7-151">新-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="025f7-151">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="025f7-152">移除-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="025f7-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


