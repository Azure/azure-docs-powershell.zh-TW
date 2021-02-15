---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131558"
---
# <span data-ttu-id="8d544-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="8d544-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="8d544-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d544-102">SYNOPSIS</span></span>
<span data-ttu-id="8d544-103">針對指定的伺服器啟動複製。</span><span class="sxs-lookup"><span data-stu-id="8d544-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="8d544-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d544-104">SYNTAX</span></span>

### <span data-ttu-id="8d544-105">ByIdDefaultUser (預設) </span><span class="sxs-lookup"><span data-stu-id="8d544-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d544-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="8d544-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d544-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="8d544-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d544-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="8d544-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8d544-109">說明</span><span class="sxs-lookup"><span data-stu-id="8d544-109">DESCRIPTION</span></span>
<span data-ttu-id="8d544-110">New-AzMigrateServerReplication Cmdlet 會針對 Azure 遷移專案中的特定已探索伺服器啟動複製。</span><span class="sxs-lookup"><span data-stu-id="8d544-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="8d544-111">示例</span><span class="sxs-lookup"><span data-stu-id="8d544-111">EXAMPLES</span></span>

### <span data-ttu-id="8d544-112">範例1：只有作業系統磁片時</span><span class="sxs-lookup"><span data-stu-id="8d544-112">Example 1: When there is only OS disk</span></span>
```powershell
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx4/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskType "Standard_LRS" -OSDiskID "6000C299-343d-7bcd-c05e-a94bd63316dd"

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="8d544-113">這適用于案例，在只有一個有必須受到保護的單一磁片時。</span><span class="sxs-lookup"><span data-stu-id="8d544-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="8d544-114">範例2：有多個磁片</span><span class="sxs-lookup"><span data-stu-id="8d544-114">Example 2: When there are multiple disks</span></span>
```powershell
PS C:\> $OSDisk = New-AzMigrateDiskMapping -DiskID '6000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'true'
PS C:\> $DataDisk = New-AzMigrateDiskMapping -DiskID '7000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'false'
PS C:\> $DisksToInclude += $OSDisk
PS C:\> $DisksToInclude += $DataDisk
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskToInclude $DisksToInclude -PerformAutoResync true

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="8d544-115">這適用于在有多個必須受到保護的磁片時的情況。</span><span class="sxs-lookup"><span data-stu-id="8d544-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="8d544-116">參數</span><span class="sxs-lookup"><span data-stu-id="8d544-116">PARAMETERS</span></span>

### <span data-ttu-id="8d544-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d544-117">-DefaultProfile</span></span>
<span data-ttu-id="8d544-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d544-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d544-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="8d544-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="8d544-120">指定要使用的磁片 encyption 集。</span><span class="sxs-lookup"><span data-stu-id="8d544-120">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d544-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="8d544-121">-DiskToInclude</span></span>
<span data-ttu-id="8d544-122">指定要包含在複製中的源伺服器磁片。</span><span class="sxs-lookup"><span data-stu-id="8d544-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="8d544-123">若要建立，請參閱 DISKTOINCLUDE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="8d544-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput[]
Parameter Sets: ByIdPowerUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d544-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="8d544-124">-DiskType</span></span>
<span data-ttu-id="8d544-125">指定要用於 Azure VM 的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="8d544-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d544-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d544-126">-InputObject</span></span>
<span data-ttu-id="8d544-127">指定要遷移的已探索伺服器。</span><span class="sxs-lookup"><span data-stu-id="8d544-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="8d544-128">您可以使用 Get-AzMigrateServer Cmdlet 來檢索 server 物件。</span><span class="sxs-lookup"><span data-stu-id="8d544-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="8d544-129">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8d544-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine
Parameter Sets: ByInputObjectDefaultUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d544-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8d544-130">-LicenseType</span></span>
<span data-ttu-id="8d544-131">指定 Azure 混合式優點是否適用于要遷移的來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="8d544-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.LicenseType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d544-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="8d544-132">-MachineId</span></span>
<span data-ttu-id="8d544-133">指定要遷移的已探索伺服器的電腦 ID。</span><span class="sxs-lookup"><span data-stu-id="8d544-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByIdPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d544-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="8d544-134">-OSDiskID</span></span>
<span data-ttu-id="8d544-135">指定要遷移之來源伺服器的作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="8d544-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d544-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="8d544-136">-PerformAutoResync</span></span>
<span data-ttu-id="8d544-137">指定是否要在 [複製] 下的來源伺服器遺失變更時，自動修復複製。</span><span class="sxs-lookup"><span data-stu-id="8d544-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="8d544-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d544-138">-SubscriptionId</span></span>
<span data-ttu-id="8d544-139">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8d544-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8d544-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8d544-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="8d544-141">指定要用於 VM creationSpecifies 的可用性集，以供建立 VM 時使用。</span><span class="sxs-lookup"><span data-stu-id="8d544-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="8d544-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="8d544-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="8d544-143">指定要用於建立 VM 的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="8d544-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="8d544-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d544-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="8d544-145">指定要用於啟動診斷程式的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="8d544-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="8d544-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="8d544-146">-TargetNetworkId</span></span>
<span data-ttu-id="8d544-147">指定要將伺服器遷移至其中的目的地 Azure 訂閱中的虛擬網路 id。</span><span class="sxs-lookup"><span data-stu-id="8d544-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="8d544-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8d544-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="8d544-149">指定目標 Azure 訂閱中需要遷移伺服器的資源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d544-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="8d544-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="8d544-150">-TargetSubnetName</span></span>
<span data-ttu-id="8d544-151">指定要將伺服器遷移至其中的目的地虛擬 Netowk 內的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="8d544-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="8d544-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="8d544-152">-TargetVMName</span></span>
<span data-ttu-id="8d544-153">指定要建立之 Azure VM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d544-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="8d544-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="8d544-154">-TargetVMSize</span></span>
<span data-ttu-id="8d544-155">指定要建立之 Azure VM 的 SKU。</span><span class="sxs-lookup"><span data-stu-id="8d544-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="8d544-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="8d544-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="8d544-157">[帳戶識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8d544-157">Account id.</span></span>

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

### <span data-ttu-id="8d544-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d544-158">CommonParameters</span></span>
<span data-ttu-id="8d544-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d544-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d544-160">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d544-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d544-161">輸入</span><span class="sxs-lookup"><span data-stu-id="8d544-161">INPUTS</span></span>

## <span data-ttu-id="8d544-162">輸出</span><span class="sxs-lookup"><span data-stu-id="8d544-162">OUTPUTS</span></span>

### <span data-ttu-id="8d544-163">IJob 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="8d544-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="8d544-164">筆記</span><span class="sxs-lookup"><span data-stu-id="8d544-164">NOTES</span></span>

<span data-ttu-id="8d544-165">別名</span><span class="sxs-lookup"><span data-stu-id="8d544-165">ALIASES</span></span>

<span data-ttu-id="8d544-166">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8d544-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d544-167">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8d544-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d544-168">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8d544-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d544-169">DISKTOINCLUDE <IVMwareCbtDiskInput [] >：指定要包含在複製中之來源伺服器上的磁片。</span><span class="sxs-lookup"><span data-stu-id="8d544-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="8d544-170">`DiskId <String>`：磁片 Id。</span><span class="sxs-lookup"><span data-stu-id="8d544-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="8d544-171">`IsOSDisk <String>`：一個值，指出磁片是否為作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="8d544-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="8d544-172">`LogStorageAccountId <String>`：記錄儲存帳戶扶手 Id。</span><span class="sxs-lookup"><span data-stu-id="8d544-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="8d544-173">`LogStorageAccountSasSecretName <String>`：記錄儲存空間帳戶的主要保存庫密碼。</span><span class="sxs-lookup"><span data-stu-id="8d544-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="8d544-174">`[DiskEncryptionSetId <String>]`： DiskEncryptionSet ARM Id。</span><span class="sxs-lookup"><span data-stu-id="8d544-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="8d544-175">`[DiskType <DiskAccountType?>]`：磁片類型。</span><span class="sxs-lookup"><span data-stu-id="8d544-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="8d544-176">INPUTOBJECT <IVMwareMachine> ：指定要遷移的已探索伺服器。</span><span class="sxs-lookup"><span data-stu-id="8d544-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="8d544-177">您可以使用 Get-AzMigrateServer Cmdlet 來檢索 server 物件。</span><span class="sxs-lookup"><span data-stu-id="8d544-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="8d544-178">`[GuestOSDetailOstype <String>]`：作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="8d544-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="8d544-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d544-179">RELATED LINKS</span></span>

