---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: 534728e98d913a3de7f7b02628451433b252ded9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916619"
---
# <span data-ttu-id="b568d-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="b568d-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="b568d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b568d-102">SYNOPSIS</span></span>
<span data-ttu-id="b568d-103">清理複製伺服器的測試移移。</span><span class="sxs-lookup"><span data-stu-id="b568d-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="b568d-104">語法</span><span class="sxs-lookup"><span data-stu-id="b568d-104">SYNTAX</span></span>

### <span data-ttu-id="b568d-105">ByIDVCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="b568d-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b568d-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="b568d-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b568d-107">描述</span><span class="sxs-lookup"><span data-stu-id="b568d-107">DESCRIPTION</span></span>
<span data-ttu-id="b568d-108">此Start-AzMigrateTestMigrationCleanup Cmdlet 會啟動複製伺服器測試移轉的清理。</span><span class="sxs-lookup"><span data-stu-id="b568d-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="b568d-109">例子</span><span class="sxs-lookup"><span data-stu-id="b568d-109">EXAMPLES</span></span>

### <span data-ttu-id="b568d-110">範例 1：根據電腦識別碼。</span><span class="sxs-lookup"><span data-stu-id="b568d-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigrationCleanup -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="b568d-111">根據電腦識別碼。</span><span class="sxs-lookup"><span data-stu-id="b568d-111">By machine id.</span></span>

### <span data-ttu-id="b568d-112">範例 2：按輸入物件</span><span class="sxs-lookup"><span data-stu-id="b568d-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigrationCleanup -InputObject $ob


AllowedOperation            : {DisableMigration, TestMigrate, Migrate}

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="b568d-113">按輸入物件。</span><span class="sxs-lookup"><span data-stu-id="b568d-113">By input object.</span></span>

## <span data-ttu-id="b568d-114">參數</span><span class="sxs-lookup"><span data-stu-id="b568d-114">PARAMETERS</span></span>

### <span data-ttu-id="b568d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b568d-115">-DefaultProfile</span></span>
<span data-ttu-id="b568d-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b568d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b568d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b568d-117">-InputObject</span></span>
<span data-ttu-id="b568d-118">指定需要啟動測試移移清理的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="b568d-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="b568d-119">伺服器物件可以使用 Cmdlet Get-AzMigrateServerReplication結構來取取，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b568d-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b568d-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b568d-120">-SubscriptionId</span></span>
<span data-ttu-id="b568d-121">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b568d-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b568d-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="b568d-122">-TargetObjectID</span></span>
<span data-ttu-id="b568d-123">指定需要啟動測試移移清理的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="b568d-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="b568d-124">識別碼應該使用 Cmdlet Get-AzMigrateServerReplication取。</span><span class="sxs-lookup"><span data-stu-id="b568d-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="b568d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b568d-125">CommonParameters</span></span>
<span data-ttu-id="b568d-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b568d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b568d-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b568d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b568d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b568d-128">INPUTS</span></span>

## <span data-ttu-id="b568d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b568d-129">OUTPUTS</span></span>

### <span data-ttu-id="b568d-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="b568d-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="b568d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b568d-131">NOTES</span></span>

<span data-ttu-id="b568d-132">別名</span><span class="sxs-lookup"><span data-stu-id="b568d-132">ALIASES</span></span>

<span data-ttu-id="b568d-133">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b568d-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b568d-134">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b568d-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b568d-135">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b568d-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b568d-136">INPUTOBJECT：指定需要啟動測試移移清理的複製 <IMigrationItem> 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b568d-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="b568d-137">伺服器物件可以使用 Cmdlet Get-AzMigrateServerReplication取</span><span class="sxs-lookup"><span data-stu-id="b568d-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="b568d-138">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="b568d-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="b568d-139">`[CurrentJobId <String>]`：正在執行之工作的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="b568d-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="b568d-140">`[CurrentJobName <String>]`：工作名稱。</span><span class="sxs-lookup"><span data-stu-id="b568d-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="b568d-141">`[CurrentJobStartTime <DateTime?>]`：工作的開始時間。</span><span class="sxs-lookup"><span data-stu-id="b568d-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="b568d-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：移移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="b568d-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="b568d-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b568d-143">RELATED LINKS</span></span>

