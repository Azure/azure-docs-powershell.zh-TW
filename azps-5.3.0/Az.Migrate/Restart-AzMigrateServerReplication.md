---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435310"
---
# <span data-ttu-id="c887c-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="c887c-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="c887c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c887c-102">SYNOPSIS</span></span>
<span data-ttu-id="c887c-103">重新開機指定伺服器的複製。</span><span class="sxs-lookup"><span data-stu-id="c887c-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="c887c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c887c-104">SYNTAX</span></span>

### <span data-ttu-id="c887c-105">ByIDVMwareCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="c887c-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c887c-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="c887c-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c887c-107">說明</span><span class="sxs-lookup"><span data-stu-id="c887c-107">DESCRIPTION</span></span>
<span data-ttu-id="c887c-108">Restart-AzMigrateServerReplication Cmdlet 會修復指定伺服器的複製。</span><span class="sxs-lookup"><span data-stu-id="c887c-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="c887c-109">示例</span><span class="sxs-lookup"><span data-stu-id="c887c-109">EXAMPLES</span></span>

### <span data-ttu-id="c887c-110">範例1：依識別碼。</span><span class="sxs-lookup"><span data-stu-id="c887c-110">Example 1: By id.</span></span>
```powershell
PS C:\> Restart-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="c887c-111">依識別碼。</span><span class="sxs-lookup"><span data-stu-id="c887c-111">By id.</span></span>

### <span data-ttu-id="c887c-112">範例2：依輸入物件</span><span class="sxs-lookup"><span data-stu-id="c887c-112">Example 2: By Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> $output = Restart-AzMigrateServerReplication -InputObject $obj
ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="c887c-113">依輸入物件。</span><span class="sxs-lookup"><span data-stu-id="c887c-113">By Input Object.</span></span>

## <span data-ttu-id="c887c-114">參數</span><span class="sxs-lookup"><span data-stu-id="c887c-114">PARAMETERS</span></span>

### <span data-ttu-id="c887c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c887c-115">-DefaultProfile</span></span>
<span data-ttu-id="c887c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c887c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c887c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c887c-117">-InputObject</span></span>
<span data-ttu-id="c887c-118">指定複製伺服器的電腦物件。</span><span class="sxs-lookup"><span data-stu-id="c887c-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="c887c-119">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c887c-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c887c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c887c-120">-SubscriptionId</span></span>
<span data-ttu-id="c887c-121">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="c887c-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c887c-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="c887c-122">-TargetObjectID</span></span>
<span data-ttu-id="c887c-123">指定需要啟動 resync 的 replcating 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c887c-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="c887c-124">您應該使用 Get-AzMigrateServerReplication Cmdlet 來檢索 ID。</span><span class="sxs-lookup"><span data-stu-id="c887c-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c887c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c887c-125">CommonParameters</span></span>
<span data-ttu-id="c887c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c887c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c887c-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c887c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c887c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c887c-128">INPUTS</span></span>

## <span data-ttu-id="c887c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c887c-129">OUTPUTS</span></span>

### <span data-ttu-id="c887c-130">IJob 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="c887c-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="c887c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c887c-131">NOTES</span></span>

<span data-ttu-id="c887c-132">別名</span><span class="sxs-lookup"><span data-stu-id="c887c-132">ALIASES</span></span>

<span data-ttu-id="c887c-133">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c887c-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c887c-134">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c887c-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c887c-135">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c887c-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c887c-136">INPUTOBJECT <IMigrationItem> ：指定複製伺服器的電腦物件。</span><span class="sxs-lookup"><span data-stu-id="c887c-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="c887c-137">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="c887c-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="c887c-138">`[CurrentJobId <String>]`：所執行作業的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="c887c-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="c887c-139">`[CurrentJobName <String>]`：作業名稱。</span><span class="sxs-lookup"><span data-stu-id="c887c-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="c887c-140">`[CurrentJobStartTime <DateTime?>]`：作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="c887c-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="c887c-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：遷移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="c887c-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="c887c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c887c-142">RELATED LINKS</span></span>

