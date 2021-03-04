---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: cf6b87b8d03855ae79fc0cea62a3bd126f8342a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907854"
---
# <span data-ttu-id="8776a-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="8776a-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="8776a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8776a-102">SYNOPSIS</span></span>
<span data-ttu-id="8776a-103">啟動指定伺服器的複製。</span><span class="sxs-lookup"><span data-stu-id="8776a-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="8776a-104">語法</span><span class="sxs-lookup"><span data-stu-id="8776a-104">SYNTAX</span></span>

### <span data-ttu-id="8776a-105">ByIdDefaultUser (預設) </span><span class="sxs-lookup"><span data-stu-id="8776a-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -LicenseType <String> -MachineId <String> -OSDiskID <String>
 -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String> -TargetVMName <String>
 [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8776a-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="8776a-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <String>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8776a-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="8776a-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -InputObject <IVMwareMachine> -LicenseType <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8776a-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="8776a-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8776a-109">描述</span><span class="sxs-lookup"><span data-stu-id="8776a-109">DESCRIPTION</span></span>
<span data-ttu-id="8776a-110">Cmdlet New-AzMigrateServerReplication Azure Migrate 專案中所發現的特定伺服器開始複製。</span><span class="sxs-lookup"><span data-stu-id="8776a-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="8776a-111">例子</span><span class="sxs-lookup"><span data-stu-id="8776a-111">EXAMPLES</span></span>

### <span data-ttu-id="8776a-112">範例 1：當只有作業系統磁片時</span><span class="sxs-lookup"><span data-stu-id="8776a-112">Example 1: When there is only OS disk</span></span>
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

<span data-ttu-id="8776a-113">這是針對只有一個必須受到保護的單一磁片的情況。</span><span class="sxs-lookup"><span data-stu-id="8776a-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="8776a-114">範例 2：當有多個磁片時</span><span class="sxs-lookup"><span data-stu-id="8776a-114">Example 2: When there are multiple disks</span></span>
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

<span data-ttu-id="8776a-115">這是針對需要保護的多個磁片的情況。</span><span class="sxs-lookup"><span data-stu-id="8776a-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="8776a-116">參數</span><span class="sxs-lookup"><span data-stu-id="8776a-116">PARAMETERS</span></span>

### <span data-ttu-id="8776a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8776a-117">-DefaultProfile</span></span>
<span data-ttu-id="8776a-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8776a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8776a-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="8776a-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="8776a-120">指定要使用的磁片 encyption 集。</span><span class="sxs-lookup"><span data-stu-id="8776a-120">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="8776a-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="8776a-121">-DiskToInclude</span></span>
<span data-ttu-id="8776a-122">指定要包含在來源伺服器上用於複本的磁片。</span><span class="sxs-lookup"><span data-stu-id="8776a-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="8776a-123">若要建構，請參閱 DISKTOINCLUDE 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8776a-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="8776a-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="8776a-124">-DiskType</span></span>
<span data-ttu-id="8776a-125">指定 Azure VM 使用的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="8776a-125">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="8776a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8776a-126">-InputObject</span></span>
<span data-ttu-id="8776a-127">指定要移移的已發現伺服器。</span><span class="sxs-lookup"><span data-stu-id="8776a-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="8776a-128">伺服器物件可以使用 Cmdlet Get-AzMigrateServer取。</span><span class="sxs-lookup"><span data-stu-id="8776a-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="8776a-129">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8776a-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8776a-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8776a-130">-LicenseType</span></span>
<span data-ttu-id="8776a-131">指定 Azure 混合式權益是否適用于要移移的來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="8776a-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

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

### <span data-ttu-id="8776a-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="8776a-132">-MachineId</span></span>
<span data-ttu-id="8776a-133">指定要移移之所發現伺服器的機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="8776a-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="8776a-134">-OS也Id</span><span class="sxs-lookup"><span data-stu-id="8776a-134">-OSDiskID</span></span>
<span data-ttu-id="8776a-135">指定要移移來源伺服器的作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="8776a-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

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

### <span data-ttu-id="8776a-136">-執行AutoResync</span><span class="sxs-lookup"><span data-stu-id="8776a-136">-PerformAutoResync</span></span>
<span data-ttu-id="8776a-137">指定如果複製時來源伺服器遺失追蹤變更，是否可自動修復複製。</span><span class="sxs-lookup"><span data-stu-id="8776a-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="8776a-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8776a-138">-SubscriptionId</span></span>
<span data-ttu-id="8776a-139">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8776a-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8776a-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8776a-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="8776a-141">指定要用於 VM 建立的可用性集S指定要用於建立 VM 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="8776a-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="8776a-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="8776a-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="8776a-143">指定建立 VM 時所使用的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="8776a-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="8776a-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8776a-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="8776a-145">指定要用於開機診斷的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="8776a-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="8776a-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="8776a-146">-TargetNetworkId</span></span>
<span data-ttu-id="8776a-147">指定伺服器需要移移的目標 Azure 訂閱內的虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="8776a-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="8776a-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8776a-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="8776a-149">指定伺服器需要移移的目標 Azure 訂閱內的資源組識別碼。</span><span class="sxs-lookup"><span data-stu-id="8776a-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="8776a-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="8776a-150">-TargetSubnetName</span></span>
<span data-ttu-id="8776a-151">指定目的地 Virtual Netowk 中伺服器需要移移的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="8776a-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="8776a-152">-TargetMSNAME</span><span class="sxs-lookup"><span data-stu-id="8776a-152">-TargetVMName</span></span>
<span data-ttu-id="8776a-153">指定要建立之 Azure VM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8776a-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="8776a-154">-TargetMSMSize</span><span class="sxs-lookup"><span data-stu-id="8776a-154">-TargetVMSize</span></span>
<span data-ttu-id="8776a-155">指定要建立之 Azure VM 的 SKU。</span><span class="sxs-lookup"><span data-stu-id="8776a-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="8776a-156">-VMWareWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="8776a-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="8776a-157">帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="8776a-157">Account id.</span></span>

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

### <span data-ttu-id="8776a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8776a-158">CommonParameters</span></span>
<span data-ttu-id="8776a-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8776a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8776a-160">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8776a-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8776a-161">輸入</span><span class="sxs-lookup"><span data-stu-id="8776a-161">INPUTS</span></span>

## <span data-ttu-id="8776a-162">輸出</span><span class="sxs-lookup"><span data-stu-id="8776a-162">OUTPUTS</span></span>

### <span data-ttu-id="8776a-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="8776a-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="8776a-164">筆記</span><span class="sxs-lookup"><span data-stu-id="8776a-164">NOTES</span></span>

<span data-ttu-id="8776a-165">別名</span><span class="sxs-lookup"><span data-stu-id="8776a-165">ALIASES</span></span>

<span data-ttu-id="8776a-166">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8776a-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8776a-167">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8776a-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8776a-168">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8776a-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8776a-169">DISKTOINCLUDE <IVCbt一文[]>：指定要包含在來源伺服器上用於複本的磁片。</span><span class="sxs-lookup"><span data-stu-id="8776a-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="8776a-170">`DiskId <String>`：磁片識別碼。</span><span class="sxs-lookup"><span data-stu-id="8776a-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="8776a-171">`IsOSDisk <String>`：指出磁片是否為作業系統磁片的值。</span><span class="sxs-lookup"><span data-stu-id="8776a-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="8776a-172">`LogStorageAccountId <String>`：記錄儲存空間帳戶 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="8776a-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="8776a-173">`LogStorageAccountSasSecretName <String>`：記錄儲存帳戶的金鑰保存庫密碼。</span><span class="sxs-lookup"><span data-stu-id="8776a-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="8776a-174">`[DiskEncryptionSetId <String>]`：DiskEncryptionSet ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="8776a-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="8776a-175">`[DiskType <DiskAccountType?>]`：磁片類型。</span><span class="sxs-lookup"><span data-stu-id="8776a-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="8776a-176">INPUTOBJECT： <IVMwareMachine> 指定要移移的已發現伺服器。</span><span class="sxs-lookup"><span data-stu-id="8776a-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="8776a-177">伺服器物件可以使用 Cmdlet Get-AzMigrateServer取。</span><span class="sxs-lookup"><span data-stu-id="8776a-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="8776a-178">`[GuestOSDetailOstype <String>]`：作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="8776a-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="8776a-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="8776a-179">RELATED LINKS</span></span>

