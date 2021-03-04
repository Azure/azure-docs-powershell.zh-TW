---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 5bf91aafffb1c6fd650b5fd88f343897afc6c5d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908781"
---
# <span data-ttu-id="7e7dc-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="7e7dc-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="7e7dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7e7dc-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7dc-103">獲得基本排程策略物件。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="7e7dc-104">語法</span><span class="sxs-lookup"><span data-stu-id="7e7dc-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e7dc-105">描述</span><span class="sxs-lookup"><span data-stu-id="7e7dc-105">DESCRIPTION</span></span>
<span data-ttu-id="7e7dc-106">**Get-AzRecoveryServicesBackupSchedulePolicyObject** Cmdlet 會取得基礎 **AzureRMRecoveryServicesSchedulePolicyObject。**</span><span class="sxs-lookup"><span data-stu-id="7e7dc-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="7e7dc-107">此物件不會持續存在系統中。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="7e7dc-108">這是您可以操作並用於 Cmdlet 的暫New-AzRecoveryServicesBackupProtectionPolicy物件，以建立新的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="7e7dc-109">例子</span><span class="sxs-lookup"><span data-stu-id="7e7dc-109">EXAMPLES</span></span>

### <span data-ttu-id="7e7dc-110">範例 1：將排程頻率設定為每週</span><span class="sxs-lookup"><span data-stu-id="7e7dc-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="7e7dc-111">第一個命令會獲得保留原則物件，然後將它儲存在$RetPol變數中。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="7e7dc-112">第二個命令會獲得排程策略物件，然後將它儲存在$SchPol變數中。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="7e7dc-113">第三個命令將排程策略的頻率變更為每週。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="7e7dc-114">最後一個命令會使用更新的排程建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="7e7dc-115">範例 2：設定備份時間</span><span class="sxs-lookup"><span data-stu-id="7e7dc-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="7e7dc-116">第一個命令會獲得排程策略物件，然後將它儲存在$SchPol變數中。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="7e7dc-117">第二個命令會移除所有排定的執行時間$SchPol。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="7e7dc-118">第三個命令會獲得目前的日期和時間，然後將它儲存在$DT變數中。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="7e7dc-119">第四個命令會以目前的時間取代排定的執行時間。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="7e7dc-120">您每天只能備份 Azure%。若要重設備份時間，您必須取代原本的排程。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="7e7dc-121">最後一個命令會使用新排程建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="7e7dc-122">參數</span><span class="sxs-lookup"><span data-stu-id="7e7dc-122">PARAMETERS</span></span>

### <span data-ttu-id="7e7dc-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7e7dc-123">-BackupManagementType</span></span>
<span data-ttu-id="7e7dc-124">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-124">The class of resources being protected.</span></span> <span data-ttu-id="7e7dc-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7e7dc-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7e7dc-126">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="7e7dc-126">AzureVM</span></span> 
- <span data-ttu-id="7e7dc-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="7e7dc-127">AzureStorage</span></span>
- <span data-ttu-id="7e7dc-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="7e7dc-128">AzureWorkload</span></span>

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

### <span data-ttu-id="7e7dc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7dc-129">-DefaultProfile</span></span>
<span data-ttu-id="7e7dc-130">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e7dc-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="7e7dc-131">-WorkloadType</span></span>
<span data-ttu-id="7e7dc-132">資源的工作量類型。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-132">Workload type of the resource.</span></span> <span data-ttu-id="7e7dc-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7e7dc-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7e7dc-134">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="7e7dc-134">AzureVM</span></span> 
- <span data-ttu-id="7e7dc-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="7e7dc-135">AzureFiles</span></span>
- <span data-ttu-id="7e7dc-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="7e7dc-136">MSSQL</span></span>


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

### <span data-ttu-id="7e7dc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7dc-137">CommonParameters</span></span>
<span data-ttu-id="7e7dc-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7dc-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e7dc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7dc-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7e7dc-140">INPUTS</span></span>

### <span data-ttu-id="7e7dc-141">沒有</span><span class="sxs-lookup"><span data-stu-id="7e7dc-141">None</span></span>

## <span data-ttu-id="7e7dc-142">輸出</span><span class="sxs-lookup"><span data-stu-id="7e7dc-142">OUTPUTS</span></span>

### <span data-ttu-id="7e7dc-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="7e7dc-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="7e7dc-144">筆記</span><span class="sxs-lookup"><span data-stu-id="7e7dc-144">NOTES</span></span>

## <span data-ttu-id="7e7dc-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e7dc-145">RELATED LINKS</span></span>

[<span data-ttu-id="7e7dc-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e7dc-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="7e7dc-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e7dc-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


