---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 1f63238fede4c3a280cd4eb631c33e97db8f73ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911641"
---
# <span data-ttu-id="0dd6c-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="0dd6c-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="0dd6c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0dd6c-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd6c-103">重新開機指定伺服器的複製。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="0dd6c-104">語法</span><span class="sxs-lookup"><span data-stu-id="0dd6c-104">SYNTAX</span></span>

### <span data-ttu-id="0dd6c-105">ByIDVCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="0dd6c-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0dd6c-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="0dd6c-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0dd6c-107">描述</span><span class="sxs-lookup"><span data-stu-id="0dd6c-107">DESCRIPTION</span></span>
<span data-ttu-id="0dd6c-108">Cmdlet Restart-AzMigrateServerReplication修復指定伺服器的複製。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="0dd6c-109">例子</span><span class="sxs-lookup"><span data-stu-id="0dd6c-109">EXAMPLES</span></span>

### <span data-ttu-id="0dd6c-110">範例 1：By id。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-110">Example 1: By id.</span></span>
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

<span data-ttu-id="0dd6c-111">按識別碼。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-111">By id.</span></span>

### <span data-ttu-id="0dd6c-112">範例 2：按輸入物件</span><span class="sxs-lookup"><span data-stu-id="0dd6c-112">Example 2: By Input Object</span></span>
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

<span data-ttu-id="0dd6c-113">按輸入物件。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-113">By Input Object.</span></span>

## <span data-ttu-id="0dd6c-114">參數</span><span class="sxs-lookup"><span data-stu-id="0dd6c-114">PARAMETERS</span></span>

### <span data-ttu-id="0dd6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd6c-115">-DefaultProfile</span></span>
<span data-ttu-id="0dd6c-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dd6c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0dd6c-117">-InputObject</span></span>
<span data-ttu-id="0dd6c-118">指定複製伺服器的機器物件。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="0dd6c-119">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0dd6c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0dd6c-120">-SubscriptionId</span></span>
<span data-ttu-id="0dd6c-121">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0dd6c-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="0dd6c-122">-TargetObjectID</span></span>
<span data-ttu-id="0dd6c-123">指定需要初始化重新同步的重新同步處理伺服器。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="0dd6c-124">識別碼應該使用 Cmdlet Get-AzMigrateServerReplication取。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="0dd6c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd6c-125">CommonParameters</span></span>
<span data-ttu-id="0dd6c-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd6c-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dd6c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd6c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0dd6c-128">INPUTS</span></span>

## <span data-ttu-id="0dd6c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0dd6c-129">OUTPUTS</span></span>

### <span data-ttu-id="0dd6c-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="0dd6c-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="0dd6c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0dd6c-131">NOTES</span></span>

<span data-ttu-id="0dd6c-132">別名</span><span class="sxs-lookup"><span data-stu-id="0dd6c-132">ALIASES</span></span>

<span data-ttu-id="0dd6c-133">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="0dd6c-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0dd6c-134">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0dd6c-135">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0dd6c-136">INPUTOBJECT： <IMigrationItem> 指定複製伺服器的機器物件。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="0dd6c-137">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="0dd6c-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="0dd6c-138">`[CurrentJobId <String>]`：正在執行之工作的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="0dd6c-139">`[CurrentJobName <String>]`：工作名稱。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="0dd6c-140">`[CurrentJobStartTime <DateTime?>]`：工作的開始時間。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="0dd6c-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：移移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="0dd6c-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="0dd6c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dd6c-142">RELATED LINKS</span></span>

