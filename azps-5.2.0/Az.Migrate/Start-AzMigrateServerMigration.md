---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282463"
---
# <span data-ttu-id="3d99f-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="3d99f-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="3d99f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d99f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d99f-103">啟動複製伺服器的遷移。</span><span class="sxs-lookup"><span data-stu-id="3d99f-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="3d99f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d99f-104">SYNTAX</span></span>

### <span data-ttu-id="3d99f-105">ByIDVMwareCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="3d99f-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d99f-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="3d99f-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3d99f-107">說明</span><span class="sxs-lookup"><span data-stu-id="3d99f-107">DESCRIPTION</span></span>
<span data-ttu-id="3d99f-108">啟動複製伺服器的遷移。</span><span class="sxs-lookup"><span data-stu-id="3d99f-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="3d99f-109">示例</span><span class="sxs-lookup"><span data-stu-id="3d99f-109">EXAMPLES</span></span>

### <span data-ttu-id="3d99f-110">範例1：依識別碼</span><span class="sxs-lookup"><span data-stu-id="3d99f-110">Example 1: By id</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Start-AzMigrateServerMigration -TargetObjectID "/Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_52f42ee7-8eb3-1aa4-e2d5-1ae83f86b085"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Migrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="3d99f-111">依識別碼</span><span class="sxs-lookup"><span data-stu-id="3d99f-111">By id</span></span>

## <span data-ttu-id="3d99f-112">參數</span><span class="sxs-lookup"><span data-stu-id="3d99f-112">PARAMETERS</span></span>

### <span data-ttu-id="3d99f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d99f-113">-DefaultProfile</span></span>
<span data-ttu-id="3d99f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d99f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d99f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d99f-115">-InputObject</span></span>
<span data-ttu-id="3d99f-116">指定需要啟動遷移的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d99f-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="3d99f-117">您可以使用 Get-AzMigrateServerReplication Cmdlet 來檢索 server 物件。</span><span class="sxs-lookup"><span data-stu-id="3d99f-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="3d99f-118">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3d99f-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3d99f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d99f-119">-SubscriptionId</span></span>
<span data-ttu-id="3d99f-120">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3d99f-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="3d99f-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="3d99f-121">-TargetObjectID</span></span>
<span data-ttu-id="3d99f-122">指定需要啟動遷移的 replcating 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d99f-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="3d99f-123">您應該使用 Get-AzMigrateServerReplication Cmdlet 來檢索 ID。</span><span class="sxs-lookup"><span data-stu-id="3d99f-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="3d99f-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="3d99f-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="3d99f-125">指定是否應關閉遷移後的來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d99f-125">Specifies whether the source server should be turned off post migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d99f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d99f-126">CommonParameters</span></span>
<span data-ttu-id="3d99f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d99f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d99f-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3d99f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d99f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3d99f-129">INPUTS</span></span>

## <span data-ttu-id="3d99f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3d99f-130">OUTPUTS</span></span>

### <span data-ttu-id="3d99f-131">IJob 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="3d99f-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="3d99f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3d99f-132">NOTES</span></span>

<span data-ttu-id="3d99f-133">別名</span><span class="sxs-lookup"><span data-stu-id="3d99f-133">ALIASES</span></span>

<span data-ttu-id="3d99f-134">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3d99f-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d99f-135">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3d99f-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d99f-136">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3d99f-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d99f-137">INPUTOBJECT <IMigrationItem> ：指定需要啟動遷移的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d99f-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="3d99f-138">您可以使用 Get-AzMigrateServerReplication Cmdlet 來檢索 server 物件。</span><span class="sxs-lookup"><span data-stu-id="3d99f-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="3d99f-139">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="3d99f-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="3d99f-140">`[CurrentJobId <String>]`：所執行作業的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d99f-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="3d99f-141">`[CurrentJobName <String>]`：作業名稱。</span><span class="sxs-lookup"><span data-stu-id="3d99f-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="3d99f-142">`[CurrentJobStartTime <DateTime?>]`：作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="3d99f-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="3d99f-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：遷移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="3d99f-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="3d99f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d99f-144">RELATED LINKS</span></span>

