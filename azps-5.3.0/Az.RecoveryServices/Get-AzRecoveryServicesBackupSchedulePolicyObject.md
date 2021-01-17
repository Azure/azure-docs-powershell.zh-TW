---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439075"
---
# <span data-ttu-id="0d070-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="0d070-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="0d070-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d070-102">SYNOPSIS</span></span>
<span data-ttu-id="0d070-103">取得基本排程原則物件。</span><span class="sxs-lookup"><span data-stu-id="0d070-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="0d070-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d070-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d070-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d070-105">DESCRIPTION</span></span>
<span data-ttu-id="0d070-106">**AzRecoveryServicesBackupSchedulePolicyObject** Cmdlet 會取得基 **AzureRMRecoveryServicesSchedulePolicyObject**。</span><span class="sxs-lookup"><span data-stu-id="0d070-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="0d070-107">這個物件不會在系統中保留。</span><span class="sxs-lookup"><span data-stu-id="0d070-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="0d070-108">您可以使用 New-AzRecoveryServicesBackupProtectionPolicy Cmdlet 來處理及使用的暫時物件，以建立新的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="0d070-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="0d070-109">示例</span><span class="sxs-lookup"><span data-stu-id="0d070-109">EXAMPLES</span></span>

### <span data-ttu-id="0d070-110">範例1：將排程頻率設定為每週</span><span class="sxs-lookup"><span data-stu-id="0d070-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="0d070-111">第一個命令會取得保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="0d070-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="0d070-112">第二個命令會取得排程原則物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="0d070-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="0d070-113">第三個命令會將排程原則的頻率變更為 [每週]。</span><span class="sxs-lookup"><span data-stu-id="0d070-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="0d070-114">最後一個命令會建立含更新排程的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="0d070-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="0d070-115">範例2：設定備份時間</span><span class="sxs-lookup"><span data-stu-id="0d070-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="0d070-116">第一個命令會取得排程原則物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="0d070-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="0d070-117">第二個命令會從 $SchPol 移除所有排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="0d070-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="0d070-118">第三個命令會取得目前的日期和時間，然後將它儲存在 $DT 變數中。</span><span class="sxs-lookup"><span data-stu-id="0d070-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="0d070-119">第四個命令會以目前的時間取代排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="0d070-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="0d070-120">您每一天只能進行一次的操作，因此若要重設備份時間，您必須取代原始排程。</span><span class="sxs-lookup"><span data-stu-id="0d070-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="0d070-121">最後一個命令會使用新排程來建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="0d070-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="0d070-122">參數</span><span class="sxs-lookup"><span data-stu-id="0d070-122">PARAMETERS</span></span>

### <span data-ttu-id="0d070-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0d070-123">-BackupManagementType</span></span>
<span data-ttu-id="0d070-124">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="0d070-124">The class of resources being protected.</span></span> <span data-ttu-id="0d070-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0d070-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0d070-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0d070-126">AzureVM</span></span> 
- <span data-ttu-id="0d070-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="0d070-127">AzureStorage</span></span>
- <span data-ttu-id="0d070-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="0d070-128">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d070-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d070-129">-DefaultProfile</span></span>
<span data-ttu-id="0d070-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d070-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d070-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="0d070-131">-WorkloadType</span></span>
<span data-ttu-id="0d070-132">資源的工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="0d070-132">Workload type of the resource.</span></span> <span data-ttu-id="0d070-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0d070-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0d070-134">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0d070-134">AzureVM</span></span> 
- <span data-ttu-id="0d070-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="0d070-135">AzureFiles</span></span>
- <span data-ttu-id="0d070-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="0d070-136">MSSQL</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d070-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d070-137">CommonParameters</span></span>
<span data-ttu-id="0d070-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d070-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d070-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d070-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d070-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0d070-140">INPUTS</span></span>

### <span data-ttu-id="0d070-141">所有</span><span class="sxs-lookup"><span data-stu-id="0d070-141">None</span></span>

## <span data-ttu-id="0d070-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0d070-142">OUTPUTS</span></span>

### <span data-ttu-id="0d070-143">SchedulePolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="0d070-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="0d070-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0d070-144">NOTES</span></span>

## <span data-ttu-id="0d070-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d070-145">RELATED LINKS</span></span>

[<span data-ttu-id="0d070-146">新-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0d070-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="0d070-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0d070-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


