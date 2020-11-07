---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 1bf16226f65cebd6003631bc8adbcb1ebbc7b93d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966167"
---
# <span data-ttu-id="5336d-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="5336d-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="5336d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5336d-102">SYNOPSIS</span></span>
<span data-ttu-id="5336d-103">取得基本排程原則物件。</span><span class="sxs-lookup"><span data-stu-id="5336d-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="5336d-104">句法</span><span class="sxs-lookup"><span data-stu-id="5336d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5336d-105">說明</span><span class="sxs-lookup"><span data-stu-id="5336d-105">DESCRIPTION</span></span>
<span data-ttu-id="5336d-106">**AzRecoveryServicesBackupSchedulePolicyObject** Cmdlet 會取得基 **AzureRMRecoveryServicesSchedulePolicyObject** 。</span><span class="sxs-lookup"><span data-stu-id="5336d-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="5336d-107">這個物件不會在系統中保留。</span><span class="sxs-lookup"><span data-stu-id="5336d-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="5336d-108">您可以使用 New-AzRecoveryServicesBackupProtectionPolicy Cmdlet 來處理及使用的暫時物件，以建立新的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="5336d-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="5336d-109">示例</span><span class="sxs-lookup"><span data-stu-id="5336d-109">EXAMPLES</span></span>

### <span data-ttu-id="5336d-110">範例1：將排程頻率設定為每週</span><span class="sxs-lookup"><span data-stu-id="5336d-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="5336d-111">第一個命令會取得保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="5336d-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="5336d-112">第二個命令會取得排程原則物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="5336d-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="5336d-113">第三個命令會將排程原則的頻率變更為 [每週]。</span><span class="sxs-lookup"><span data-stu-id="5336d-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="5336d-114">最後一個命令會建立含更新排程的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="5336d-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="5336d-115">範例2：設定備份時間</span><span class="sxs-lookup"><span data-stu-id="5336d-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="5336d-116">第一個命令會取得排程原則物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="5336d-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="5336d-117">第二個命令會從 $SchPol 移除所有排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="5336d-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="5336d-118">第三個命令會取得目前的日期和時間，然後將它儲存在 $DT 變數中。</span><span class="sxs-lookup"><span data-stu-id="5336d-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="5336d-119">第四個命令會以目前的時間取代排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="5336d-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="5336d-120">您每一天只能進行一次的操作，因此若要重設備份時間，您必須取代原始排程。</span><span class="sxs-lookup"><span data-stu-id="5336d-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="5336d-121">最後一個命令會使用新排程來建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="5336d-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="5336d-122">參數</span><span class="sxs-lookup"><span data-stu-id="5336d-122">PARAMETERS</span></span>

### <span data-ttu-id="5336d-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="5336d-123">-BackupManagementType</span></span>
<span data-ttu-id="5336d-124">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="5336d-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="5336d-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5336d-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5336d-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="5336d-126">AzureVM</span></span> 
- <span data-ttu-id="5336d-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="5336d-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="5336d-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="5336d-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5336d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5336d-129">-DefaultProfile</span></span>
<span data-ttu-id="5336d-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5336d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5336d-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="5336d-131">-WorkloadType</span></span>
<span data-ttu-id="5336d-132">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="5336d-132">Specifies the workload type.</span></span>
<span data-ttu-id="5336d-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5336d-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5336d-134">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="5336d-134">AzureVM</span></span> 
- <span data-ttu-id="5336d-135">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="5336d-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="5336d-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="5336d-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5336d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5336d-137">CommonParameters</span></span>
<span data-ttu-id="5336d-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5336d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5336d-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5336d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5336d-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5336d-140">INPUTS</span></span>

### <span data-ttu-id="5336d-141">所有</span><span class="sxs-lookup"><span data-stu-id="5336d-141">None</span></span>

## <span data-ttu-id="5336d-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5336d-142">OUTPUTS</span></span>

### <span data-ttu-id="5336d-143">SchedulePolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="5336d-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="5336d-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5336d-144">NOTES</span></span>

## <span data-ttu-id="5336d-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5336d-145">RELATED LINKS</span></span>

[<span data-ttu-id="5336d-146">新-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5336d-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="5336d-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5336d-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


