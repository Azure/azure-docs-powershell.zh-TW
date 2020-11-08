---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140067"
---
# <span data-ttu-id="6e367-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="6e367-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="6e367-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e367-102">SYNOPSIS</span></span>
<span data-ttu-id="6e367-103">更新複製伺服器的目標屬性。</span><span class="sxs-lookup"><span data-stu-id="6e367-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="6e367-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e367-104">SYNTAX</span></span>

### <span data-ttu-id="6e367-105">ByIDVMwareCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="6e367-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e367-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="6e367-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6e367-107">說明</span><span class="sxs-lookup"><span data-stu-id="6e367-107">DESCRIPTION</span></span>
<span data-ttu-id="6e367-108">Set-AzMigrateServerReplication Cmdlet 會更新複製伺服器的目標屬性。</span><span class="sxs-lookup"><span data-stu-id="6e367-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="6e367-109">示例</span><span class="sxs-lookup"><span data-stu-id="6e367-109">EXAMPLES</span></span>

### <span data-ttu-id="6e367-110">範例1：依識別碼更新</span><span class="sxs-lookup"><span data-stu-id="6e367-110">Example 1: Update by id</span></span>
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="6e367-111">依識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e367-111">By id.</span></span>

## <span data-ttu-id="6e367-112">參數</span><span class="sxs-lookup"><span data-stu-id="6e367-112">PARAMETERS</span></span>

### <span data-ttu-id="6e367-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e367-113">-DefaultProfile</span></span>
<span data-ttu-id="6e367-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e367-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e367-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e367-115">-InputObject</span></span>
<span data-ttu-id="6e367-116">指定需要更新屬性的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="6e367-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="6e367-117">您可以使用 Get-AzMigrateServerReplication Cmdlet 來檢索 server 物件。</span><span class="sxs-lookup"><span data-stu-id="6e367-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="6e367-118">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6e367-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6e367-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="6e367-119">-NicToUpdate</span></span>
<span data-ttu-id="6e367-120">更新要建立之 Azure VM 的 NIC。</span><span class="sxs-lookup"><span data-stu-id="6e367-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="6e367-121">若要建立，請參閱 NICTOUPDATE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="6e367-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e367-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e367-122">-SubscriptionId</span></span>
<span data-ttu-id="6e367-123">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="6e367-123">The subscription Id.</span></span>

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

### <span data-ttu-id="6e367-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6e367-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="6e367-125">指定要用於建立 VM 的可用性集合。</span><span class="sxs-lookup"><span data-stu-id="6e367-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="6e367-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="6e367-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="6e367-127">指定要用於建立 VM 的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="6e367-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="6e367-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="6e367-128">-TargetNetworkId</span></span>
<span data-ttu-id="6e367-129">更新目標 Azure 訂閱中需要遷移伺服器的虛擬網路 id。</span><span class="sxs-lookup"><span data-stu-id="6e367-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="6e367-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="6e367-130">-TargetObjectID</span></span>
<span data-ttu-id="6e367-131">指定需要更新屬性的 replcating 伺服器。</span><span class="sxs-lookup"><span data-stu-id="6e367-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="6e367-132">您應該使用 Get-AzMigrateServerReplication Cmdlet 來檢索 ID。</span><span class="sxs-lookup"><span data-stu-id="6e367-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="6e367-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="6e367-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="6e367-134">更新目的地 Azure 訂閱中需要遷移伺服器的資源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e367-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="6e367-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="6e367-135">-TargetVMName</span></span>
<span data-ttu-id="6e367-136">指定需要更新屬性的 replcating 伺服器。</span><span class="sxs-lookup"><span data-stu-id="6e367-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="6e367-137">您應該使用 Get-AzMigrateServerReplication Cmdlet 來檢索 ID。</span><span class="sxs-lookup"><span data-stu-id="6e367-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="6e367-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="6e367-138">-TargetVMSize</span></span>
<span data-ttu-id="6e367-139">更新要建立之 Azure VM 的 SKU。</span><span class="sxs-lookup"><span data-stu-id="6e367-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="6e367-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e367-140">CommonParameters</span></span>
<span data-ttu-id="6e367-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e367-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e367-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6e367-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e367-143">輸入</span><span class="sxs-lookup"><span data-stu-id="6e367-143">INPUTS</span></span>

## <span data-ttu-id="6e367-144">輸出</span><span class="sxs-lookup"><span data-stu-id="6e367-144">OUTPUTS</span></span>

### <span data-ttu-id="6e367-145">IJob 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="6e367-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="6e367-146">筆記</span><span class="sxs-lookup"><span data-stu-id="6e367-146">NOTES</span></span>

<span data-ttu-id="6e367-147">別名</span><span class="sxs-lookup"><span data-stu-id="6e367-147">ALIASES</span></span>

<span data-ttu-id="6e367-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6e367-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6e367-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6e367-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e367-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6e367-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6e367-151">INPUTOBJECT <IMigrationItem> ：指定需要更新屬性的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="6e367-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="6e367-152">您可以使用 Get-AzMigrateServerReplication Cmdlet 來檢索 server 物件。</span><span class="sxs-lookup"><span data-stu-id="6e367-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="6e367-153">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="6e367-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="6e367-154">`[CurrentJobId <String>]`：所執行作業的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e367-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="6e367-155">`[CurrentJobName <String>]`：作業名稱。</span><span class="sxs-lookup"><span data-stu-id="6e367-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="6e367-156">`[CurrentJobStartTime <DateTime?>]`：作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="6e367-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="6e367-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：遷移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="6e367-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="6e367-158">NICTOUPDATE <IVMwareCbtNicInput [] >：更新要建立之 Azure VM 的 NIC。</span><span class="sxs-lookup"><span data-stu-id="6e367-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="6e367-159">`IsPrimaryNic <String>`：指示這是否為主要 NIC 的值。</span><span class="sxs-lookup"><span data-stu-id="6e367-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="6e367-160">`NicId <String>`： NIC Id。</span><span class="sxs-lookup"><span data-stu-id="6e367-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="6e367-161">`[IsSelectedForMigration <String>]`：指示是否已選取此 NIC 進行遷移的值。</span><span class="sxs-lookup"><span data-stu-id="6e367-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="6e367-162">`[TargetStaticIPAddress <String>]`：靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6e367-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="6e367-163">`[TargetSubnetName <String>]`：目標子網名稱。</span><span class="sxs-lookup"><span data-stu-id="6e367-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="6e367-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e367-164">RELATED LINKS</span></span>

