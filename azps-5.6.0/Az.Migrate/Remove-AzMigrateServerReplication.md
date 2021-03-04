---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: 65f9527005b849b9ffbcc8c343b57515b2d437c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916094"
---
# <span data-ttu-id="5a11a-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="5a11a-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="5a11a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a11a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a11a-103">停止移移伺服器的複製。</span><span class="sxs-lookup"><span data-stu-id="5a11a-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="5a11a-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a11a-104">SYNTAX</span></span>

### <span data-ttu-id="5a11a-105">ByIDVCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="5a11a-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5a11a-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="5a11a-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5a11a-107">描述</span><span class="sxs-lookup"><span data-stu-id="5a11a-107">DESCRIPTION</span></span>
<span data-ttu-id="5a11a-108">此Remove-AzMigrateServerReplication Cmdlet 會停止移轉伺服器的複製。</span><span class="sxs-lookup"><span data-stu-id="5a11a-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="5a11a-109">例子</span><span class="sxs-lookup"><span data-stu-id="5a11a-109">EXAMPLES</span></span>

### <span data-ttu-id="5a11a-110">範例 1：移除識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a11a-110">Example 1: Remove by id.</span></span>
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

<span data-ttu-id="5a11a-111">以識別碼重新同步。</span><span class="sxs-lookup"><span data-stu-id="5a11a-111">Resync by id.</span></span>

### <span data-ttu-id="5a11a-112">範例 2：按輸入物件移除</span><span class="sxs-lookup"><span data-stu-id="5a11a-112">Example 2: Remove by Input Object</span></span>
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

<span data-ttu-id="5a11a-113">按名稱。</span><span class="sxs-lookup"><span data-stu-id="5a11a-113">By name.</span></span>

## <span data-ttu-id="5a11a-114">參數</span><span class="sxs-lookup"><span data-stu-id="5a11a-114">PARAMETERS</span></span>

### <span data-ttu-id="5a11a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a11a-115">-DefaultProfile</span></span>
<span data-ttu-id="5a11a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a11a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a11a-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="5a11a-117">-ForceRemove</span></span>
<span data-ttu-id="5a11a-118">指定是否需要強制移除複製。</span><span class="sxs-lookup"><span data-stu-id="5a11a-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="5a11a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a11a-119">-InputObject</span></span>
<span data-ttu-id="5a11a-120">指定複製伺服器的機器物件。</span><span class="sxs-lookup"><span data-stu-id="5a11a-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="5a11a-121">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5a11a-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5a11a-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a11a-122">-SubscriptionId</span></span>
<span data-ttu-id="5a11a-123">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a11a-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5a11a-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="5a11a-124">-TargetObjectID</span></span>
<span data-ttu-id="5a11a-125">指定需要停用複本的重新伺服器。</span><span class="sxs-lookup"><span data-stu-id="5a11a-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="5a11a-126">識別碼應該使用 Cmdlet Get-AzMigrateServerReplication取。</span><span class="sxs-lookup"><span data-stu-id="5a11a-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="5a11a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a11a-127">CommonParameters</span></span>
<span data-ttu-id="5a11a-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a11a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a11a-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a11a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a11a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5a11a-130">INPUTS</span></span>

## <span data-ttu-id="5a11a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5a11a-131">OUTPUTS</span></span>

### <span data-ttu-id="5a11a-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="5a11a-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="5a11a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5a11a-133">NOTES</span></span>

<span data-ttu-id="5a11a-134">別名</span><span class="sxs-lookup"><span data-stu-id="5a11a-134">ALIASES</span></span>

<span data-ttu-id="5a11a-135">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5a11a-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5a11a-136">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5a11a-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a11a-137">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5a11a-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5a11a-138">INPUTOBJECT： <IMigrationItem> 指定複製伺服器的機器物件。</span><span class="sxs-lookup"><span data-stu-id="5a11a-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="5a11a-139">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="5a11a-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="5a11a-140">`[CurrentJobId <String>]`：正在執行之工作的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a11a-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="5a11a-141">`[CurrentJobName <String>]`：工作名稱。</span><span class="sxs-lookup"><span data-stu-id="5a11a-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="5a11a-142">`[CurrentJobStartTime <DateTime?>]`：工作的開始時間。</span><span class="sxs-lookup"><span data-stu-id="5a11a-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="5a11a-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：移移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="5a11a-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="5a11a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a11a-144">RELATED LINKS</span></span>

