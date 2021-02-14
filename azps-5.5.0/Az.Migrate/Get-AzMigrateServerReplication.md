---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateServerReplication.md
ms.openlocfilehash: 2ba6f3252dc3ac1a16609c3d4a82f0bf76ce8a48
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140691"
---
# <span data-ttu-id="0b3da-101">Get-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="0b3da-101">Get-AzMigrateServerReplication</span></span>

## <span data-ttu-id="0b3da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b3da-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3da-103">檢索複製伺服器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0b3da-103">Retrieves the details of the replicating server.</span></span>

## <span data-ttu-id="0b3da-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b3da-104">SYNTAX</span></span>

### <span data-ttu-id="0b3da-105">ListByName (預設) </span><span class="sxs-lookup"><span data-stu-id="0b3da-105">ListByName (Default)</span></span>
```
Get-AzMigrateServerReplication -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-SkipToken <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b3da-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b3da-106">GetByInputObject</span></span>
```
Get-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b3da-107">GetByMachineName</span><span class="sxs-lookup"><span data-stu-id="0b3da-107">GetByMachineName</span></span>
```
Get-AzMigrateServerReplication -MachineName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b3da-108">GetBySDSID</span><span class="sxs-lookup"><span data-stu-id="0b3da-108">GetBySDSID</span></span>
```
Get-AzMigrateServerReplication -DiscoveredMachineId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b3da-109">GetBySRSID</span><span class="sxs-lookup"><span data-stu-id="0b3da-109">GetBySRSID</span></span>
```
Get-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b3da-110">ListById</span><span class="sxs-lookup"><span data-stu-id="0b3da-110">ListById</span></span>
```
Get-AzMigrateServerReplication -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>]
 [-Filter <String>] [-SkipToken <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0b3da-111">說明</span><span class="sxs-lookup"><span data-stu-id="0b3da-111">DESCRIPTION</span></span>
<span data-ttu-id="0b3da-112">Get-AzMigrateServerReplication Cmdlet 會檢索複製伺服器的物件。</span><span class="sxs-lookup"><span data-stu-id="0b3da-112">The Get-AzMigrateServerReplication cmdlet retrieves the object for the replicating server.</span></span>

## <span data-ttu-id="0b3da-113">示例</span><span class="sxs-lookup"><span data-stu-id="0b3da-113">EXAMPLES</span></span>

### <span data-ttu-id="0b3da-114">範例1：依識別碼取得詳細資料</span><span class="sxs-lookup"><span data-stu-id="0b3da-114">Example 1: Get details by id</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="0b3da-115">[依 id 取得]。</span><span class="sxs-lookup"><span data-stu-id="0b3da-115">Get by id.</span></span>

### <span data-ttu-id="0b3da-116">範例2：依識別碼列出專案中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="0b3da-116">Example 2: List all in project by id.</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -ResourceGroupID /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020 -ProjectID "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Migrate/MigrateProjects/AzMigrateTestProjectPWSH"

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : 57b59212-6a2f-4333-8882-461647bb05f9
Health                      : Normal
HealthError                 : {593b735d-2a34-53b2-b8ed-e33da5650703}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : rb-w2k12r2-1
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="0b3da-117">[全部列出]。</span><span class="sxs-lookup"><span data-stu-id="0b3da-117">List all.</span></span>

### <span data-ttu-id="0b3da-118">範例2：依名稱列出專案中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="0b3da-118">Example 2: List all in project by name.</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -ResourceGroupName azmigratepwshtestasr13072020 -ProjectName AzMigrateTestProjectPWSH

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : 57b59212-6a2f-4333-8882-461647bb05f9
Health                      : Normal
HealthError                 : {593b735d-2a34-53b2-b8ed-e33da5650703}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : rb-w2k12r2-1
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="0b3da-119">[全部列出]。</span><span class="sxs-lookup"><span data-stu-id="0b3da-119">List all.</span></span>

## <span data-ttu-id="0b3da-120">參數</span><span class="sxs-lookup"><span data-stu-id="0b3da-120">PARAMETERS</span></span>

### <span data-ttu-id="0b3da-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3da-121">-DefaultProfile</span></span>
<span data-ttu-id="0b3da-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b3da-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b3da-123">-DiscoveredMachineId</span><span class="sxs-lookup"><span data-stu-id="0b3da-123">-DiscoveredMachineId</span></span>
<span data-ttu-id="0b3da-124">指定已探索伺服器的電腦 ID。</span><span class="sxs-lookup"><span data-stu-id="0b3da-124">Specifies the machine ID of the discovered server.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySDSID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3da-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="0b3da-125">-Filter</span></span>
<span data-ttu-id="0b3da-126">OData 篩選選項。</span><span class="sxs-lookup"><span data-stu-id="0b3da-126">OData filter options.</span></span>

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

### <span data-ttu-id="0b3da-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b3da-127">-InputObject</span></span>
<span data-ttu-id="0b3da-128">指定複製伺服器的電腦物件。</span><span class="sxs-lookup"><span data-stu-id="0b3da-128">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="0b3da-129">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0b3da-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3da-130">-MachineName</span><span class="sxs-lookup"><span data-stu-id="0b3da-130">-MachineName</span></span>
<span data-ttu-id="0b3da-131">指定複製電腦的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0b3da-131">Specifies the display name of the replicating machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByMachineName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3da-132">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="0b3da-132">-ProjectID</span></span>
<span data-ttu-id="0b3da-133">指定要在其中複製伺服器的 Azure 遷移專案。</span><span class="sxs-lookup"><span data-stu-id="0b3da-133">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

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

### <span data-ttu-id="0b3da-134">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="0b3da-134">-ProjectName</span></span>
<span data-ttu-id="0b3da-135">指定目前訂閱中的 Azure 遷移專案。</span><span class="sxs-lookup"><span data-stu-id="0b3da-135">Specifies the Azure Migrate project  in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByMachineName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3da-136">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="0b3da-136">-ResourceGroupID</span></span>
<span data-ttu-id="0b3da-137">指定目前訂閱中 Azure 遷移專案的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0b3da-137">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="0b3da-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b3da-138">-ResourceGroupName</span></span>
<span data-ttu-id="0b3da-139">指定目前訂閱中 Azure 遷移專案的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0b3da-139">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByMachineName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3da-140">-SkipToken</span><span class="sxs-lookup"><span data-stu-id="0b3da-140">-SkipToken</span></span>
<span data-ttu-id="0b3da-141">分頁標記。</span><span class="sxs-lookup"><span data-stu-id="0b3da-141">The pagination token.</span></span>

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

### <span data-ttu-id="0b3da-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b3da-142">-SubscriptionId</span></span>
<span data-ttu-id="0b3da-143">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="0b3da-143">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0b3da-144">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="0b3da-144">-TargetObjectID</span></span>
<span data-ttu-id="0b3da-145">指定複製的伺服器。</span><span class="sxs-lookup"><span data-stu-id="0b3da-145">Specifies the replicating server.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySRSID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3da-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3da-146">CommonParameters</span></span>
<span data-ttu-id="0b3da-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b3da-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3da-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b3da-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3da-149">輸入</span><span class="sxs-lookup"><span data-stu-id="0b3da-149">INPUTS</span></span>

## <span data-ttu-id="0b3da-150">輸出</span><span class="sxs-lookup"><span data-stu-id="0b3da-150">OUTPUTS</span></span>

### <span data-ttu-id="0b3da-151">IMigrationItem 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="0b3da-151">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem</span></span>

## <span data-ttu-id="0b3da-152">筆記</span><span class="sxs-lookup"><span data-stu-id="0b3da-152">NOTES</span></span>

<span data-ttu-id="0b3da-153">別名</span><span class="sxs-lookup"><span data-stu-id="0b3da-153">ALIASES</span></span>

<span data-ttu-id="0b3da-154">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="0b3da-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b3da-155">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="0b3da-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b3da-156">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0b3da-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b3da-157">INPUTOBJECT <IMigrationItem> ：指定複製伺服器的電腦物件。</span><span class="sxs-lookup"><span data-stu-id="0b3da-157">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="0b3da-158">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="0b3da-158">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="0b3da-159">`[CurrentJobId <String>]`：所執行作業的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b3da-159">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="0b3da-160">`[CurrentJobName <String>]`：作業名稱。</span><span class="sxs-lookup"><span data-stu-id="0b3da-160">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="0b3da-161">`[CurrentJobStartTime <DateTime?>]`：作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="0b3da-161">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="0b3da-162">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：遷移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="0b3da-162">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="0b3da-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b3da-163">RELATED LINKS</span></span>

