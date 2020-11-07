---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: fcf5bec22dffc18d6c4f9950d8dfb3e5b37332a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625974"
---
# <span data-ttu-id="a7e91-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="a7e91-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="a7e91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7e91-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e91-103">取得基本排程原則物件。</span><span class="sxs-lookup"><span data-stu-id="a7e91-103">Gets a base schedule policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7e91-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7e91-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7e91-105">說明</span><span class="sxs-lookup"><span data-stu-id="a7e91-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e91-106">**AzureRmRecoveryServicesBackupSchedulePolicyObject** Cmdlet 會取得基 **AzureRMRecoveryServicesSchedulePolicyObject** 。</span><span class="sxs-lookup"><span data-stu-id="a7e91-106">The **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="a7e91-107">這個物件不會在系統中保留。</span><span class="sxs-lookup"><span data-stu-id="a7e91-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="a7e91-108">您可以使用 New-AzureRmRecoveryServicesBackupProtectionPolicy Cmdlet 來處理及使用的暫時物件，以建立新的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="a7e91-108">It is temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="a7e91-109">示例</span><span class="sxs-lookup"><span data-stu-id="a7e91-109">EXAMPLES</span></span>

### <span data-ttu-id="a7e91-110">範例1：將排程頻率設定為每週</span><span class="sxs-lookup"><span data-stu-id="a7e91-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="a7e91-111">第一個命令會取得保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="a7e91-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="a7e91-112">第二個命令會取得排程原則物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="a7e91-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="a7e91-113">第三個命令會將排程原則的頻率變更為 [每週]。</span><span class="sxs-lookup"><span data-stu-id="a7e91-113">The third command changes the frequency for the schedule policy to weekly.</span></span>

<span data-ttu-id="a7e91-114">最後一個命令會建立含更新排程的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="a7e91-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="a7e91-115">範例2：設定備份時間</span><span class="sxs-lookup"><span data-stu-id="a7e91-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="a7e91-116">第一個命令會取得排程原則物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="a7e91-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="a7e91-117">第二個命令會從 $SchPol 移除所有排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="a7e91-117">The second command removes all scheduled run times from $SchPol.</span></span>

<span data-ttu-id="a7e91-118">第三個命令會取得目前的日期和時間，然後將它儲存在 $DT 變數中。</span><span class="sxs-lookup"><span data-stu-id="a7e91-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="a7e91-119">第四個命令會以目前的時間取代排程的執行時間。</span><span class="sxs-lookup"><span data-stu-id="a7e91-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="a7e91-120">您每一天只能進行一次的操作，因此若要重設備份時間，您必須取代原始排程。</span><span class="sxs-lookup"><span data-stu-id="a7e91-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>

<span data-ttu-id="a7e91-121">最後一個命令會使用新排程來建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="a7e91-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="a7e91-122">參數</span><span class="sxs-lookup"><span data-stu-id="a7e91-122">PARAMETERS</span></span>

### <span data-ttu-id="a7e91-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="a7e91-123">-BackupManagementType</span></span>
<span data-ttu-id="a7e91-124">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="a7e91-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="a7e91-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a7e91-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7e91-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a7e91-126">AzureVM</span></span> 
- <span data-ttu-id="a7e91-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="a7e91-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e91-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="a7e91-128">-WorkloadType</span></span>
<span data-ttu-id="a7e91-129">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="a7e91-129">Specifies the workload type.</span></span>
<span data-ttu-id="a7e91-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a7e91-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7e91-131">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a7e91-131">AzureVM</span></span> 
- <span data-ttu-id="a7e91-132">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="a7e91-132">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e91-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e91-133">-DefaultProfile</span></span>
<span data-ttu-id="a7e91-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7e91-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7e91-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e91-135">CommonParameters</span></span>
<span data-ttu-id="a7e91-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7e91-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e91-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7e91-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e91-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a7e91-138">INPUTS</span></span>

## <span data-ttu-id="a7e91-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a7e91-139">OUTPUTS</span></span>

### <span data-ttu-id="a7e91-140">SchedulePolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="a7e91-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="a7e91-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a7e91-141">NOTES</span></span>

## <span data-ttu-id="a7e91-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7e91-142">RELATED LINKS</span></span>

[<span data-ttu-id="a7e91-143">新-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7e91-143">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="a7e91-144">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7e91-144">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


