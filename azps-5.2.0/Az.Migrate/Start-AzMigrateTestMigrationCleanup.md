---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: df4eac2c6380c36dcd07c906ccbbee4d2a93f27b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282459"
---
# <span data-ttu-id="2adc9-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="2adc9-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="2adc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2adc9-102">SYNOPSIS</span></span>
<span data-ttu-id="2adc9-103">清除複製伺服器的測試遷移。</span><span class="sxs-lookup"><span data-stu-id="2adc9-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="2adc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="2adc9-104">SYNTAX</span></span>

### <span data-ttu-id="2adc9-105">ByIDVMwareCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="2adc9-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2adc9-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="2adc9-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2adc9-107">說明</span><span class="sxs-lookup"><span data-stu-id="2adc9-107">DESCRIPTION</span></span>
<span data-ttu-id="2adc9-108">Start-AzMigrateTestMigrationCleanup Cmdlet 會針對複製伺服器的測試遷移啟動清理。</span><span class="sxs-lookup"><span data-stu-id="2adc9-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="2adc9-109">示例</span><span class="sxs-lookup"><span data-stu-id="2adc9-109">EXAMPLES</span></span>

### <span data-ttu-id="2adc9-110">範例1：依機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="2adc9-110">Example 1: By machine id.</span></span>
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

<span data-ttu-id="2adc9-111">依 [電腦識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2adc9-111">By machine id.</span></span>

### <span data-ttu-id="2adc9-112">範例2：依輸入物件</span><span class="sxs-lookup"><span data-stu-id="2adc9-112">Example 2: By input object</span></span>
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

<span data-ttu-id="2adc9-113">依輸入物件。</span><span class="sxs-lookup"><span data-stu-id="2adc9-113">By input object.</span></span>

## <span data-ttu-id="2adc9-114">參數</span><span class="sxs-lookup"><span data-stu-id="2adc9-114">PARAMETERS</span></span>

### <span data-ttu-id="2adc9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2adc9-115">-DefaultProfile</span></span>
<span data-ttu-id="2adc9-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2adc9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2adc9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2adc9-117">-InputObject</span></span>
<span data-ttu-id="2adc9-118">指定需要啟動測試遷移清除的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="2adc9-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="2adc9-119">您可以使用 Get-AzMigrateServerReplication Cmdlet 來檢索 server 物件，請參閱適用于 INPUTOBJECT 屬性的記事區段，並建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2adc9-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2adc9-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2adc9-120">-SubscriptionId</span></span>
<span data-ttu-id="2adc9-121">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="2adc9-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="2adc9-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="2adc9-122">-TargetObjectID</span></span>
<span data-ttu-id="2adc9-123">指定需要啟動測試遷移清除的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="2adc9-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="2adc9-124">您應該使用 Get-AzMigrateServerReplication Cmdlet 來檢索 ID。</span><span class="sxs-lookup"><span data-stu-id="2adc9-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="2adc9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2adc9-125">CommonParameters</span></span>
<span data-ttu-id="2adc9-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2adc9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2adc9-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2adc9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2adc9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2adc9-128">INPUTS</span></span>

## <span data-ttu-id="2adc9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2adc9-129">OUTPUTS</span></span>

### <span data-ttu-id="2adc9-130">IJob 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="2adc9-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="2adc9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2adc9-131">NOTES</span></span>

<span data-ttu-id="2adc9-132">別名</span><span class="sxs-lookup"><span data-stu-id="2adc9-132">ALIASES</span></span>

<span data-ttu-id="2adc9-133">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2adc9-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2adc9-134">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2adc9-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2adc9-135">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2adc9-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2adc9-136">INPUTOBJECT <IMigrationItem> ：指定需要啟動測試遷移清除的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="2adc9-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="2adc9-137">可以使用 Get-AzMigrateServerReplication Cmdlet 來檢索 server 物件</span><span class="sxs-lookup"><span data-stu-id="2adc9-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="2adc9-138">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="2adc9-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="2adc9-139">`[CurrentJobId <String>]`：所執行作業的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="2adc9-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="2adc9-140">`[CurrentJobName <String>]`：作業名稱。</span><span class="sxs-lookup"><span data-stu-id="2adc9-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="2adc9-141">`[CurrentJobStartTime <DateTime?>]`：作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="2adc9-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="2adc9-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：遷移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="2adc9-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="2adc9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="2adc9-143">RELATED LINKS</span></span>

