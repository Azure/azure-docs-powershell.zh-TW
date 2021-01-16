---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435308"
---
# <span data-ttu-id="04836-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="04836-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="04836-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04836-102">SYNOPSIS</span></span>
<span data-ttu-id="04836-103">停止對已遷移伺服器的複製。</span><span class="sxs-lookup"><span data-stu-id="04836-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="04836-104">句法</span><span class="sxs-lookup"><span data-stu-id="04836-104">SYNTAX</span></span>

### <span data-ttu-id="04836-105">ByIDVMwareCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="04836-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="04836-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="04836-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="04836-107">說明</span><span class="sxs-lookup"><span data-stu-id="04836-107">DESCRIPTION</span></span>
<span data-ttu-id="04836-108">Remove-AzMigrateServerReplication Cmdlet 會停止對已遷移伺服器的複製。</span><span class="sxs-lookup"><span data-stu-id="04836-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="04836-109">示例</span><span class="sxs-lookup"><span data-stu-id="04836-109">EXAMPLES</span></span>

### <span data-ttu-id="04836-110">範例1：依識別碼移除。</span><span class="sxs-lookup"><span data-stu-id="04836-110">Example 1: Remove by id.</span></span>
```powershell
PS C:\> Remove-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="04836-111">依識別碼重新同步。</span><span class="sxs-lookup"><span data-stu-id="04836-111">Resync by id.</span></span>

### <span data-ttu-id="04836-112">範例2：移除輸入物件</span><span class="sxs-lookup"><span data-stu-id="04836-112">Example 2: Remove by Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> Remove-AzMigrateServerReplication -InputObject $obj


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="04836-113">依名稱。</span><span class="sxs-lookup"><span data-stu-id="04836-113">By name.</span></span>

## <span data-ttu-id="04836-114">參數</span><span class="sxs-lookup"><span data-stu-id="04836-114">PARAMETERS</span></span>

### <span data-ttu-id="04836-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04836-115">-DefaultProfile</span></span>
<span data-ttu-id="04836-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04836-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04836-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="04836-117">-ForceRemove</span></span>
<span data-ttu-id="04836-118">指定是否需要強制移除複製。</span><span class="sxs-lookup"><span data-stu-id="04836-118">Specifies whether the replication needs to be force removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04836-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04836-119">-InputObject</span></span>
<span data-ttu-id="04836-120">指定複製伺服器的電腦物件。</span><span class="sxs-lookup"><span data-stu-id="04836-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="04836-121">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="04836-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="04836-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04836-122">-SubscriptionId</span></span>
<span data-ttu-id="04836-123">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="04836-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="04836-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="04836-124">-TargetObjectID</span></span>
<span data-ttu-id="04836-125">指定 replicatio 需要停用的 replcating 伺服器。</span><span class="sxs-lookup"><span data-stu-id="04836-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="04836-126">您應該使用 Get-AzMigrateServerReplication Cmdlet 來檢索 ID。</span><span class="sxs-lookup"><span data-stu-id="04836-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="04836-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04836-127">CommonParameters</span></span>
<span data-ttu-id="04836-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04836-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04836-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04836-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04836-130">輸入</span><span class="sxs-lookup"><span data-stu-id="04836-130">INPUTS</span></span>

## <span data-ttu-id="04836-131">輸出</span><span class="sxs-lookup"><span data-stu-id="04836-131">OUTPUTS</span></span>

### <span data-ttu-id="04836-132">IJob 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="04836-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="04836-133">筆記</span><span class="sxs-lookup"><span data-stu-id="04836-133">NOTES</span></span>

<span data-ttu-id="04836-134">別名</span><span class="sxs-lookup"><span data-stu-id="04836-134">ALIASES</span></span>

<span data-ttu-id="04836-135">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="04836-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="04836-136">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="04836-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04836-137">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="04836-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="04836-138">INPUTOBJECT <IMigrationItem> ：指定複製伺服器的電腦物件。</span><span class="sxs-lookup"><span data-stu-id="04836-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="04836-139">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="04836-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="04836-140">`[CurrentJobId <String>]`：所執行作業的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="04836-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="04836-141">`[CurrentJobName <String>]`：作業名稱。</span><span class="sxs-lookup"><span data-stu-id="04836-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="04836-142">`[CurrentJobStartTime <DateTime?>]`：作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="04836-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="04836-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：遷移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="04836-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="04836-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="04836-144">RELATED LINKS</span></span>

