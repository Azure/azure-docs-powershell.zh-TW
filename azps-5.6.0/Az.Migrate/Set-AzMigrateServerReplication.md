---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: b87e541266c3ce555c0fc11910c9541914b14738
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916624"
---
# <span data-ttu-id="c9f5e-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="c9f5e-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="c9f5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c9f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f5e-103">更新複製伺服器的目標屬性。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="c9f5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="c9f5e-104">SYNTAX</span></span>

### <span data-ttu-id="c9f5e-105">ByIDVCbt (預設) </span><span class="sxs-lookup"><span data-stu-id="c9f5e-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9f5e-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="c9f5e-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9f5e-107">描述</span><span class="sxs-lookup"><span data-stu-id="c9f5e-107">DESCRIPTION</span></span>
<span data-ttu-id="c9f5e-108">Cmdlet Set-AzMigrateServerReplication更新複製伺服器的目標屬性。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="c9f5e-109">例子</span><span class="sxs-lookup"><span data-stu-id="c9f5e-109">EXAMPLES</span></span>

### <span data-ttu-id="c9f5e-110">範例 1：以識別碼更新</span><span class="sxs-lookup"><span data-stu-id="c9f5e-110">Example 1: Update by id</span></span>
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

<span data-ttu-id="c9f5e-111">按識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-111">By id.</span></span>

## <span data-ttu-id="c9f5e-112">參數</span><span class="sxs-lookup"><span data-stu-id="c9f5e-112">PARAMETERS</span></span>

### <span data-ttu-id="c9f5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f5e-113">-DefaultProfile</span></span>
<span data-ttu-id="c9f5e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9f5e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9f5e-115">-InputObject</span></span>
<span data-ttu-id="c9f5e-116">指定需要更新屬性的複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c9f5e-117">伺服器物件可以使用 Cmdlet Get-AzMigrateServerReplication取。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="c9f5e-118">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9f5e-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="c9f5e-119">-NicToUpdate</span></span>
<span data-ttu-id="c9f5e-120">更新要建立 Azure VM 的 NIC。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="c9f5e-121">若要建構，請參閱 NICTOUPDATE 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9f5e-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9f5e-122">-SubscriptionId</span></span>
<span data-ttu-id="c9f5e-123">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-123">The subscription Id.</span></span>

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

### <span data-ttu-id="c9f5e-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c9f5e-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="c9f5e-125">指定建立 VM 時所使用的可用性集。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="c9f5e-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="c9f5e-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="c9f5e-127">指定建立 VM 時所使用的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="c9f5e-128">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9f5e-128">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="c9f5e-129">指定要用於開機診斷的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-129">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="c9f5e-130">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="c9f5e-130">-TargetNetworkId</span></span>
<span data-ttu-id="c9f5e-131">補救伺服器需要移移的目標 Azure 訂閱中的虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-131">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="c9f5e-132">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="c9f5e-132">-TargetObjectID</span></span>
<span data-ttu-id="c9f5e-133">指定需要更新屬性的重新發佈伺服器。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-133">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c9f5e-134">識別碼應該使用 Cmdlet Get-AzMigrateServerReplication取。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-134">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="c9f5e-135">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="c9f5e-135">-TargetResourceGroupID</span></span>
<span data-ttu-id="c9f5e-136">補救伺服器需要移移的目標 Azure 訂閱中的資源組識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-136">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="c9f5e-137">-TargetMSNAME</span><span class="sxs-lookup"><span data-stu-id="c9f5e-137">-TargetVMName</span></span>
<span data-ttu-id="c9f5e-138">指定需要更新屬性的重新發佈伺服器。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-138">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c9f5e-139">識別碼應該使用 Cmdlet Get-AzMigrateServerReplication取。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-139">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="c9f5e-140">-TargetMSMSize</span><span class="sxs-lookup"><span data-stu-id="c9f5e-140">-TargetVMSize</span></span>
<span data-ttu-id="c9f5e-141">更新要建立之 Azure VM 的 SKU。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-141">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="c9f5e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f5e-142">CommonParameters</span></span>
<span data-ttu-id="c9f5e-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f5e-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9f5e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f5e-145">輸入</span><span class="sxs-lookup"><span data-stu-id="c9f5e-145">INPUTS</span></span>

## <span data-ttu-id="c9f5e-146">輸出</span><span class="sxs-lookup"><span data-stu-id="c9f5e-146">OUTPUTS</span></span>

### <span data-ttu-id="c9f5e-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="c9f5e-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="c9f5e-148">筆記</span><span class="sxs-lookup"><span data-stu-id="c9f5e-148">NOTES</span></span>

<span data-ttu-id="c9f5e-149">別名</span><span class="sxs-lookup"><span data-stu-id="c9f5e-149">ALIASES</span></span>

<span data-ttu-id="c9f5e-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c9f5e-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9f5e-151">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9f5e-152">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9f5e-153">INPUTOBJECT：指定需要更新其屬性的 <IMigrationItem> 複製伺服器。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-153">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="c9f5e-154">伺服器物件可以使用 Cmdlet Get-AzMigrateServerReplication取。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-154">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="c9f5e-155">`[Location <String>]`：資源位置</span><span class="sxs-lookup"><span data-stu-id="c9f5e-155">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="c9f5e-156">`[CurrentJobId <String>]`：正在執行之工作的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-156">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="c9f5e-157">`[CurrentJobName <String>]`：工作名稱。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-157">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="c9f5e-158">`[CurrentJobStartTime <DateTime?>]`：工作的開始時間。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-158">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="c9f5e-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`：移移提供者自訂設定。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="c9f5e-160">NICTOUPDATE <IVCbtNicInput[]>：更新要建立 Azure VM 的 NIC。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-160">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="c9f5e-161">`IsPrimaryNic <String>`：指出這是否為主要 NIC 的值。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-161">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="c9f5e-162">`NicId <String>`：NIC 識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-162">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="c9f5e-163">`[IsSelectedForMigration <String>]`：指出是否已選取此 NIC 進行移移的值。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-163">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="c9f5e-164">`[TargetStaticIPAddress <String>]`：靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-164">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="c9f5e-165">`[TargetSubnetName <String>]`：目標子網名稱。</span><span class="sxs-lookup"><span data-stu-id="c9f5e-165">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="c9f5e-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9f5e-166">RELATED LINKS</span></span>

