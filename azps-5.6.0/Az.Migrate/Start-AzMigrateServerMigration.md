---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 47f87fc2f1f1d4e6186e9caaf4921990122c07fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908405"
---
# <span data-ttu-id="28abe-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="28abe-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="28abe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28abe-102">SYNOPSIS</span></span>
<span data-ttu-id="28abe-103">啟動複製伺服器的移移。</span><span class="sxs-lookup"><span data-stu-id="28abe-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="28abe-104">語法</span><span class="sxs-lookup"><span data-stu-id="28abe-104">SYNTAX</span></span>

### <span data-ttu-id="28abe-105">ByIDVCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="28abe-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="28abe-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="28abe-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="28abe-107">描述</span><span class="sxs-lookup"><span data-stu-id="28abe-107">DESCRIPTION</span></span>
<span data-ttu-id="28abe-108">啟動複製伺服器的移移。</span><span class="sxs-lookup"><span data-stu-id="28abe-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="28abe-109">例子</span><span class="sxs-lookup"><span data-stu-id="28abe-109">EXAMPLES</span></span>

### <span data-ttu-id="28abe-110">範例 1：By id</span><span class="sxs-lookup"><span data-stu-id="28abe-110">Example 1: By id</span></span>
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

<span data-ttu-id="28abe-111">根據識別碼</span><span class="sxs-lookup"><span data-stu-id="28abe-111">By id</span></span>

## <span data-ttu-id="28abe-112">參數</span><span class="sxs-lookup"><span data-stu-id="28abe-112">PARAMETERS</span></span>

### <span data-ttu-id="28abe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28abe-113">-DefaultProfile</span></span>
<span data-ttu-id="28abe-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28abe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28abe-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28abe-115">-InputObject</span></span>
<span data-ttu-id="28abe-116">指定需要啟動移移的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="28abe-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="28abe-117">伺服器物件可以使用 Cmdlet Get-AzMigrateServerReplication取。</span><span class="sxs-lookup"><span data-stu-id="28abe-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="28abe-118">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="28abe-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="28abe-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28abe-119">-SubscriptionId</span></span>
<span data-ttu-id="28abe-120">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="28abe-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="28abe-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="28abe-121">-TargetObjectID</span></span>
<span data-ttu-id="28abe-122">指定需要啟動移移的重新伺服器。</span><span class="sxs-lookup"><span data-stu-id="28abe-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="28abe-123">識別碼應該使用 Cmdlet Get-AzMigrateServerReplication取。</span><span class="sxs-lookup"><span data-stu-id="28abe-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="28abe-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="28abe-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="28abe-125">指定來源伺服器是否應該在移轉後關閉。</span><span class="sxs-lookup"><span data-stu-id="28abe-125">Specifies whether the source server should be turned off post migration.</span></span>

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

### <span data-ttu-id="28abe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28abe-126">CommonParameters</span></span>
<span data-ttu-id="28abe-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28abe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28abe-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28abe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28abe-129">輸入</span><span class="sxs-lookup"><span data-stu-id="28abe-129">INPUTS</span></span>

## <span data-ttu-id="28abe-130">輸出</span><span class="sxs-lookup"><span data-stu-id="28abe-130">OUTPUTS</span></span>

### <span data-ttu-id="28abe-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="28abe-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="28abe-132">筆記</span><span class="sxs-lookup"><span data-stu-id="28abe-132">NOTES</span></span>

<span data-ttu-id="28abe-133">別名</span><span class="sxs-lookup"><span data-stu-id="28abe-133">ALIASES</span></span>

<span data-ttu-id="28abe-134">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="28abe-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28abe-135">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="28abe-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28abe-136">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="28abe-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28abe-137">INPUTOBJECT：指定需要啟動移移 <IMigrationItem> 的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="28abe-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="28abe-138">伺服器物件可以使用 Cmdlet Get-AzMigrateServerReplication取。</span><span class="sxs-lookup"><span data-stu-id="28abe-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="28abe-139">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="28abe-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="28abe-140">`[CurrentJobId <String>]`：正在執行之工作的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="28abe-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="28abe-141">`[CurrentJobName <String>]`：工作名稱。</span><span class="sxs-lookup"><span data-stu-id="28abe-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="28abe-142">`[CurrentJobStartTime <DateTime?>]`：工作的開始時間。</span><span class="sxs-lookup"><span data-stu-id="28abe-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="28abe-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：移移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="28abe-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="28abe-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="28abe-144">RELATED LINKS</span></span>

