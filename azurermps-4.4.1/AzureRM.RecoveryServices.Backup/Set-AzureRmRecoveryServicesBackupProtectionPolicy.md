---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f17ce0a23c2b91cd00f2a12bb2451c4e235169ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455648"
---
# <span data-ttu-id="31b8d-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="31b8d-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="31b8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="31b8d-103">修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="31b8d-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="31b8d-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b8d-105">說明</span><span class="sxs-lookup"><span data-stu-id="31b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="31b8d-106">**AzureRmBackupProtectionPolicy** Cmdlet 會修改現有的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="31b8d-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="31b8d-107">您可以修改備份排程與保留原則的元件。</span><span class="sxs-lookup"><span data-stu-id="31b8d-107">You can modify the Backup schedule and retention policy components.</span></span>

<span data-ttu-id="31b8d-108">您所做的任何變更都會影響與原則相關的專案的備份與保留。</span><span class="sxs-lookup"><span data-stu-id="31b8d-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>

<span data-ttu-id="31b8d-109">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31b8d-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="31b8d-110">示例</span><span class="sxs-lookup"><span data-stu-id="31b8d-110">EXAMPLES</span></span>

### <span data-ttu-id="31b8d-111">範例1：修改備份保護原則</span><span class="sxs-lookup"><span data-stu-id="31b8d-111">Example 1: Modify a Backup protection policy</span></span>
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

<span data-ttu-id="31b8d-112">第一個命令會取得基 SchedulePolicy 物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="31b8d-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="31b8d-113">第二個命令會從 $SchPol 的排程原則中移除所有排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="31b8d-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="31b8d-114">第三個命令使用 Get-Date Cmdlet 來取得目前的日期和時間，然後將它儲存在 $DT 變數中。</span><span class="sxs-lookup"><span data-stu-id="31b8d-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="31b8d-115">第四個命令會將 $DT 中的日期和時間新增至排程原則的排程執行時間。</span><span class="sxs-lookup"><span data-stu-id="31b8d-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>

<span data-ttu-id="31b8d-116">第五個命令會取得基本保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="31b8d-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="31b8d-117">第六個命令會將保留期間設定為365天。</span><span class="sxs-lookup"><span data-stu-id="31b8d-117">The sixth command sets the retention duration to 365 days.</span></span>

<span data-ttu-id="31b8d-118">第七個命令會取得名為 NewPolicy 的備份保護原則，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="31b8d-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="31b8d-119">最後一個命令會在 $Pol 中使用排程 $SchPol 原則，以及 $RetPol 中的保留原則來修改備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="31b8d-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="31b8d-120">參數</span><span class="sxs-lookup"><span data-stu-id="31b8d-120">PARAMETERS</span></span>

### <span data-ttu-id="31b8d-121">-原則</span><span class="sxs-lookup"><span data-stu-id="31b8d-121">-Policy</span></span>
<span data-ttu-id="31b8d-122">指定此 Cmdlet 修改的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="31b8d-122">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="31b8d-123">若要取得 **BackupProtectionPolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31b8d-123">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="31b8d-124">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="31b8d-124">-RetentionPolicy</span></span>
<span data-ttu-id="31b8d-125">指定基本保留原則。</span><span class="sxs-lookup"><span data-stu-id="31b8d-125">Specifies the base retention policy.</span></span>
<span data-ttu-id="31b8d-126">若要取得 **RetentionPolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupRetentionPolicyObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31b8d-126">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="31b8d-127">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="31b8d-127">-SchedulePolicy</span></span>
<span data-ttu-id="31b8d-128">指定基本排程原則物件。</span><span class="sxs-lookup"><span data-stu-id="31b8d-128">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="31b8d-129">若要取得 **SchedulePolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupSchedulePolicyObject 物件。</span><span class="sxs-lookup"><span data-stu-id="31b8d-129">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="31b8d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b8d-130">-DefaultProfile</span></span>
<span data-ttu-id="31b8d-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31b8d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b8d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b8d-132">CommonParameters</span></span>
<span data-ttu-id="31b8d-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31b8d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b8d-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="31b8d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b8d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="31b8d-135">INPUTS</span></span>

### <span data-ttu-id="31b8d-136">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="31b8d-136">PolicyBase</span></span>
<span data-ttu-id="31b8d-137">形參 "Policy" 接受管線中 "PolicyBase" 類型的值</span><span class="sxs-lookup"><span data-stu-id="31b8d-137">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="31b8d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="31b8d-138">OUTPUTS</span></span>

### <span data-ttu-id="31b8d-139">[System.object]. 清單 ' 1 [JobBase] RecoveryServices..] （）</span><span class="sxs-lookup"><span data-stu-id="31b8d-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="31b8d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="31b8d-140">NOTES</span></span>

## <span data-ttu-id="31b8d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="31b8d-141">RELATED LINKS</span></span>

[<span data-ttu-id="31b8d-142">AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="31b8d-142">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="31b8d-143">AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="31b8d-143">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="31b8d-144">新-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="31b8d-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="31b8d-145">移除-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="31b8d-145">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


