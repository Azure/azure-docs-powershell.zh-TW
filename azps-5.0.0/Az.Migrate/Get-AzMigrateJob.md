---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141519"
---
# <span data-ttu-id="91197-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="91197-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="91197-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91197-102">SYNOPSIS</span></span>
<span data-ttu-id="91197-103">檢索 Azure 遷移工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="91197-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="91197-104">句法</span><span class="sxs-lookup"><span data-stu-id="91197-104">SYNTAX</span></span>

### <span data-ttu-id="91197-105">ListByName (預設) </span><span class="sxs-lookup"><span data-stu-id="91197-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91197-106">GetById</span><span class="sxs-lookup"><span data-stu-id="91197-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91197-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="91197-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="91197-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="91197-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91197-109">ListById</span><span class="sxs-lookup"><span data-stu-id="91197-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="91197-110">說明</span><span class="sxs-lookup"><span data-stu-id="91197-110">DESCRIPTION</span></span>
<span data-ttu-id="91197-111">Get-AzMigrateJob Cmdlet 會 retrives Azure 遷移作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="91197-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="91197-112">示例</span><span class="sxs-lookup"><span data-stu-id="91197-112">EXAMPLES</span></span>

### <span data-ttu-id="91197-113">範例1：根據作業 Id 取得</span><span class="sxs-lookup"><span data-stu-id="91197-113">Example 1: Get By Job Id</span></span>
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="91197-114">這會透過其識別碼來檢索作業。</span><span class="sxs-lookup"><span data-stu-id="91197-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="91197-115">範例2：依資源群組和專案列出清單</span><span class="sxs-lookup"><span data-stu-id="91197-115">Example 2: List by resource group and project</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="91197-116">這會取得專案中的所有作業。</span><span class="sxs-lookup"><span data-stu-id="91197-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="91197-117">範例3：依資源群組、專案與工作名稱取得</span><span class="sxs-lookup"><span data-stu-id="91197-117">Example 3: Get by resource group, project and job name</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="91197-118">這會取得特定作業。</span><span class="sxs-lookup"><span data-stu-id="91197-118">This gets a specific job.</span></span>

## <span data-ttu-id="91197-119">參數</span><span class="sxs-lookup"><span data-stu-id="91197-119">PARAMETERS</span></span>

### <span data-ttu-id="91197-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91197-120">-DefaultProfile</span></span>
<span data-ttu-id="91197-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91197-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91197-122">-篩選</span><span class="sxs-lookup"><span data-stu-id="91197-122">-Filter</span></span>
<span data-ttu-id="91197-123">OData 篩選選項。</span><span class="sxs-lookup"><span data-stu-id="91197-123">OData filter options.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91197-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91197-124">-InputObject</span></span>
<span data-ttu-id="91197-125">指定複製伺服器的工作物件。</span><span class="sxs-lookup"><span data-stu-id="91197-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="91197-126">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="91197-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91197-127">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="91197-127">-JobID</span></span>
<span data-ttu-id="91197-128">指定需要檢索其詳細資料的作業 id。</span><span class="sxs-lookup"><span data-stu-id="91197-128">Specifies the job id for which the details needs to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91197-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="91197-129">-JobName</span></span>
<span data-ttu-id="91197-130">作業識別碼</span><span class="sxs-lookup"><span data-stu-id="91197-130">Job identifier</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91197-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="91197-131">-ProjectID</span></span>
<span data-ttu-id="91197-132">指定要在其中複製伺服器的 Azure 遷移專案。</span><span class="sxs-lookup"><span data-stu-id="91197-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91197-133">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="91197-133">-ProjectName</span></span>
<span data-ttu-id="91197-134">[遷移專案] 的名稱。</span><span class="sxs-lookup"><span data-stu-id="91197-134">The name of the migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91197-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="91197-135">-ResourceGroupID</span></span>
<span data-ttu-id="91197-136">指定目前訂閱中 Azure 遷移專案的資源群組。</span><span class="sxs-lookup"><span data-stu-id="91197-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91197-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91197-137">-ResourceGroupName</span></span>
<span data-ttu-id="91197-138">[恢復服務] 電子倉庫所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91197-138">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91197-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91197-139">-SubscriptionId</span></span>
<span data-ttu-id="91197-140">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="91197-140">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91197-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91197-141">CommonParameters</span></span>
<span data-ttu-id="91197-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91197-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91197-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="91197-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91197-144">輸入</span><span class="sxs-lookup"><span data-stu-id="91197-144">INPUTS</span></span>

## <span data-ttu-id="91197-145">輸出</span><span class="sxs-lookup"><span data-stu-id="91197-145">OUTPUTS</span></span>

### <span data-ttu-id="91197-146">IJob 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="91197-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="91197-147">筆記</span><span class="sxs-lookup"><span data-stu-id="91197-147">NOTES</span></span>

<span data-ttu-id="91197-148">別名</span><span class="sxs-lookup"><span data-stu-id="91197-148">ALIASES</span></span>

<span data-ttu-id="91197-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="91197-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91197-150">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="91197-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91197-151">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="91197-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91197-152">INPUTOBJECT <IJob> ：指定複製伺服器的工作物件。</span><span class="sxs-lookup"><span data-stu-id="91197-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="91197-153">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="91197-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="91197-154">`[ActivityId <String>]`：活動識別碼。</span><span class="sxs-lookup"><span data-stu-id="91197-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="91197-155">`[AllowedAction <String[]>]`：允許對作業執行的動作。</span><span class="sxs-lookup"><span data-stu-id="91197-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="91197-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`：受影響的物件屬性（例如來源伺服器、來源雲端、目標伺服器、目標雲端等）都是以工作流程物件詳細資料為基礎。</span><span class="sxs-lookup"><span data-stu-id="91197-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="91197-157">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="91197-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="91197-158">`[EndTime <DateTime?>]`：結束時間。</span><span class="sxs-lookup"><span data-stu-id="91197-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="91197-159">`[Error <IJobErrorDetails[]>]`：錯誤。</span><span class="sxs-lookup"><span data-stu-id="91197-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="91197-160">`[CreationTime <DateTime?>]`：作業錯誤的建立時間。</span><span class="sxs-lookup"><span data-stu-id="91197-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="91197-161">`[ErrorLevel <String>]`：錯誤等級錯誤。</span><span class="sxs-lookup"><span data-stu-id="91197-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="91197-162">`[ProviderErrorDetailErrorCode <Int32?>]`：錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="91197-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="91197-163">`[ProviderErrorDetailErrorId <String>]`：提供者錯誤 Id。</span><span class="sxs-lookup"><span data-stu-id="91197-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="91197-164">`[ProviderErrorDetailErrorMessage <String>]`：錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="91197-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="91197-165">`[ProviderErrorDetailPossibleCaus <String>]`：錯誤的可能原因。</span><span class="sxs-lookup"><span data-stu-id="91197-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="91197-166">`[ProviderErrorDetailRecommendedAction <String>]`：解決錯誤的建議動作。</span><span class="sxs-lookup"><span data-stu-id="91197-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="91197-167">`[ServiceErrorDetailActivityId <String>]`： [活動識別碼]。</span><span class="sxs-lookup"><span data-stu-id="91197-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="91197-168">`[ServiceErrorDetailCode <String>]`：錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="91197-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="91197-169">`[ServiceErrorDetailMessage <String>]`：錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="91197-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="91197-170">`[ServiceErrorDetailPossibleCaus <String>]`：錯誤的可能原因。</span><span class="sxs-lookup"><span data-stu-id="91197-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="91197-171">`[ServiceErrorDetailRecommendedAction <String>]`：解決錯誤的建議動作。</span><span class="sxs-lookup"><span data-stu-id="91197-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="91197-172">`[TaskId <String>]`：任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="91197-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="91197-173">`[FriendlyName <String>]`： DisplayName。</span><span class="sxs-lookup"><span data-stu-id="91197-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="91197-174">`[ScenarioName <String>]`： ScenarioName。</span><span class="sxs-lookup"><span data-stu-id="91197-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="91197-175">`[StartTime <DateTime?>]`：開始時間。</span><span class="sxs-lookup"><span data-stu-id="91197-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="91197-176">`[State <String>]`：工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="91197-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="91197-177">它是下列其中一個值，例如 NotStarted、InProgress、成功、失敗、取消、暫停或其他。</span><span class="sxs-lookup"><span data-stu-id="91197-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="91197-178">`[StateDescription <String>]`：作業狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="91197-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="91197-179">例如，對於 [成功] 狀態，說明可以是已完成、PartiallySucceeded、CompletedWithInformation 或略過。</span><span class="sxs-lookup"><span data-stu-id="91197-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="91197-180">`[TargetInstanceType <String>]`：受影響之物件的類型，屬於 {Microsoft.Azure.SiteRecovery.V2015_11_10 AffectedObjectType} 類別。</span><span class="sxs-lookup"><span data-stu-id="91197-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="91197-181">`[TargetObjectId <String>]`：受影響的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="91197-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="91197-182">`[TargetObjectName <String>]`：受影響物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="91197-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="91197-183">`[Task <IAsrTask[]>]`： [任務]。</span><span class="sxs-lookup"><span data-stu-id="91197-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="91197-184">`[AllowedAction <String[]>]`：適用于此任務的狀態/動作。</span><span class="sxs-lookup"><span data-stu-id="91197-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="91197-185">`[CustomDetailInstanceType <String>]`：任務詳細資料的類型。</span><span class="sxs-lookup"><span data-stu-id="91197-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="91197-186">`[EndTime <DateTime?>]`：結束時間。</span><span class="sxs-lookup"><span data-stu-id="91197-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="91197-187">`[Error <IJobErrorDetails[]>]`：任務錯誤詳細資料。</span><span class="sxs-lookup"><span data-stu-id="91197-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="91197-188">`[FriendlyName <String>]`：名稱。</span><span class="sxs-lookup"><span data-stu-id="91197-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="91197-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`：子任務。</span><span class="sxs-lookup"><span data-stu-id="91197-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="91197-190">`[GroupTaskCustomDetailInstanceType <String>]`：任務詳細資料的類型。</span><span class="sxs-lookup"><span data-stu-id="91197-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="91197-191">`[Name <String>]`：唯一任務名稱。</span><span class="sxs-lookup"><span data-stu-id="91197-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="91197-192">`[StartTime <DateTime?>]`：開始時間。</span><span class="sxs-lookup"><span data-stu-id="91197-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="91197-193">`[State <String>]`： [狀態]。</span><span class="sxs-lookup"><span data-stu-id="91197-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="91197-194">它是下列其中一個值，例如 NotStarted、InProgress、成功、失敗、取消、暫停或其他。</span><span class="sxs-lookup"><span data-stu-id="91197-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="91197-195">`[StateDescription <String>]`：任務狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="91197-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="91197-196">例如，如果成功的狀態，說明可以是已完成、PartiallySucceeded、CompletedWithInformation 或略過。</span><span class="sxs-lookup"><span data-stu-id="91197-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="91197-197">`[TaskId <String>]`：識別碼。</span><span class="sxs-lookup"><span data-stu-id="91197-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="91197-198">`[TaskType <String>]`：任務類型。</span><span class="sxs-lookup"><span data-stu-id="91197-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="91197-199">CustomDetails 屬性中的詳細資料視這種類型而定。</span><span class="sxs-lookup"><span data-stu-id="91197-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="91197-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="91197-200">RELATED LINKS</span></span>

