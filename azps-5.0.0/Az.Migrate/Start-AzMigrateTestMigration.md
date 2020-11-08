---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140066"
---
# <span data-ttu-id="0a725-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="0a725-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="0a725-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a725-102">SYNOPSIS</span></span>
<span data-ttu-id="0a725-103">啟動複製伺服器的測試遷移。</span><span class="sxs-lookup"><span data-stu-id="0a725-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="0a725-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a725-104">SYNTAX</span></span>

### <span data-ttu-id="0a725-105">ByIDVMwareCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="0a725-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0a725-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="0a725-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0a725-107">說明</span><span class="sxs-lookup"><span data-stu-id="0a725-107">DESCRIPTION</span></span>
<span data-ttu-id="0a725-108">Start-AzMigrateTestMigration Cmdlet 會啟動複製伺服器的測試遷移。</span><span class="sxs-lookup"><span data-stu-id="0a725-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="0a725-109">示例</span><span class="sxs-lookup"><span data-stu-id="0a725-109">EXAMPLES</span></span>

### <span data-ttu-id="0a725-110">範例1：依機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a725-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigration -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f' -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxxresourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="0a725-111">依 [電腦識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0a725-111">By machine id.</span></span>

### <span data-ttu-id="0a725-112">範例2：依輸入物件</span><span class="sxs-lookup"><span data-stu-id="0a725-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigration -InputObject $obj -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="0a725-113">依輸入物件。</span><span class="sxs-lookup"><span data-stu-id="0a725-113">By input object.</span></span>

## <span data-ttu-id="0a725-114">參數</span><span class="sxs-lookup"><span data-stu-id="0a725-114">PARAMETERS</span></span>

### <span data-ttu-id="0a725-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a725-115">-DefaultProfile</span></span>
<span data-ttu-id="0a725-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a725-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a725-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a725-117">-InputObject</span></span>
<span data-ttu-id="0a725-118">指定需要啟動測試遷移的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="0a725-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="0a725-119">您可以使用 Get-AzMigrateServerReplication Cmdlet 來檢索 server 物件。</span><span class="sxs-lookup"><span data-stu-id="0a725-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="0a725-120">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0a725-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0a725-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a725-121">-SubscriptionId</span></span>
<span data-ttu-id="0a725-122">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="0a725-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0a725-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="0a725-123">-TargetObjectID</span></span>
<span data-ttu-id="0a725-124">指定需要啟動測試遷移的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="0a725-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="0a725-125">您應該使用 Get-AzMigrateServerReplication Cmdlet 來檢索 ID。</span><span class="sxs-lookup"><span data-stu-id="0a725-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="0a725-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="0a725-126">-TestNetworkID</span></span>
<span data-ttu-id="0a725-127">更新目的地 Azure 訂閱中要用於測試遷移的虛擬網路 id。</span><span class="sxs-lookup"><span data-stu-id="0a725-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a725-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a725-128">CommonParameters</span></span>
<span data-ttu-id="0a725-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a725-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a725-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0a725-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a725-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0a725-131">INPUTS</span></span>

## <span data-ttu-id="0a725-132">輸出</span><span class="sxs-lookup"><span data-stu-id="0a725-132">OUTPUTS</span></span>

### <span data-ttu-id="0a725-133">IJob 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="0a725-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="0a725-134">筆記</span><span class="sxs-lookup"><span data-stu-id="0a725-134">NOTES</span></span>

<span data-ttu-id="0a725-135">別名</span><span class="sxs-lookup"><span data-stu-id="0a725-135">ALIASES</span></span>

<span data-ttu-id="0a725-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="0a725-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a725-137">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="0a725-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a725-138">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0a725-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a725-139">INPUTOBJECT <IMigrationItem> ：指定需要啟動測試遷移的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="0a725-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="0a725-140">您可以使用 Get-AzMigrateServerReplication Cmdlet 來檢索 server 物件。</span><span class="sxs-lookup"><span data-stu-id="0a725-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="0a725-141">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="0a725-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="0a725-142">`[CurrentJobId <String>]`：所執行作業的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a725-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="0a725-143">`[CurrentJobName <String>]`：作業名稱。</span><span class="sxs-lookup"><span data-stu-id="0a725-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="0a725-144">`[CurrentJobStartTime <DateTime?>]`：作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="0a725-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="0a725-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：遷移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="0a725-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="0a725-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a725-146">RELATED LINKS</span></span>

