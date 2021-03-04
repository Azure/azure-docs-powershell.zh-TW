---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: d2178e4eaf417ff9db0b7c5b83aa22cc7e131f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902274"
---
# <span data-ttu-id="95594-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95594-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="95594-102">簡介</span><span class="sxs-lookup"><span data-stu-id="95594-102">SYNOPSIS</span></span>
<span data-ttu-id="95594-103">建立複製受保護的專案，為 ASR 受保護的專案啟用複製。</span><span class="sxs-lookup"><span data-stu-id="95594-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="95594-104">語法</span><span class="sxs-lookup"><span data-stu-id="95594-104">SYNTAX</span></span>

### <span data-ttu-id="95594-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="95594-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95594-106">VTypeToAzureWithAzUreWithAzType</span><span class="sxs-lookup"><span data-stu-id="95594-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] -DiskType <String>
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95594-107">VAzToAzure</span><span class="sxs-lookup"><span data-stu-id="95594-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95594-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="95594-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95594-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="95594-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-UseManagedDisk <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95594-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="95594-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95594-111">AzureToAzureWithoutAzDetails</span><span class="sxs-lookup"><span data-stu-id="95594-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95594-112">描述</span><span class="sxs-lookup"><span data-stu-id="95594-112">DESCRIPTION</span></span>
<span data-ttu-id="95594-113">**New-AzRecoveryServicesAsrReplicationProtecedItem** Cmdlet 會建立一個新的複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="95594-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="95594-114">使用此 Cmdlet 啟用 ASR 可保護專案的複製。</span><span class="sxs-lookup"><span data-stu-id="95594-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="95594-115">例子</span><span class="sxs-lookup"><span data-stu-id="95594-115">EXAMPLES</span></span>

### <span data-ttu-id="95594-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="95594-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="95594-117">針對指定的 ASR 可保護專案啟動複製受保護的專案建立作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="95594-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="95594-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="95594-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="95594-119">針對指定的 ASR 可保護專案啟動複製受保護的專案建立作業，並返回用來追蹤作業的 ASR 工作 (vmWare 到 Azure 案例) 。</span><span class="sxs-lookup"><span data-stu-id="95594-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="95594-120">範例 3</span><span class="sxs-lookup"><span data-stu-id="95594-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="95594-121">針對指定的 ASR 可保護專案啟動複製受保護的專案建立作業，並返回用來追蹤作業的 ASR 工作 (Azure 到 Azure 案例) 。</span><span class="sxs-lookup"><span data-stu-id="95594-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="95594-122">範例 4</span><span class="sxs-lookup"><span data-stu-id="95594-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="95594-123">為指定的 VmId 啟動複製受保護的專案建立作業，並返回用來追蹤 Azure (Azure 案例作業的 ASR) 。</span><span class="sxs-lookup"><span data-stu-id="95594-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="95594-124">範例 5</span><span class="sxs-lookup"><span data-stu-id="95594-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="95594-125">針對指定的 ASR 可保護專案啟動複本受保護的專案建立作業，包括選擇性磁片選取，並返回用來追蹤作業 (vmWare 到 Azure 案例的 ASR 工作，) 選取的磁片。</span><span class="sxs-lookup"><span data-stu-id="95594-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="95594-126">範例 6</span><span class="sxs-lookup"><span data-stu-id="95594-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="95594-127">範例 7</span><span class="sxs-lookup"><span data-stu-id="95594-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="95594-128">為指定的 VmId 啟動複製受保護的專案建立作業，並返回用來追蹤 Azure (Azure 案例作業的 ASR) 。針對在 Cmdlet 中傳遞加密的容錯移轉 VM 詳細資料，將會使用。</span><span class="sxs-lookup"><span data-stu-id="95594-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="95594-129">範例 8</span><span class="sxs-lookup"><span data-stu-id="95594-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="95594-130">在鄰近位置群組內啟動虛擬機器的複製受保護的專案建立作業，並返回用來追蹤作業的 ASR 工作 (Azure 到 Azure 案例) 。</span><span class="sxs-lookup"><span data-stu-id="95594-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="95594-131">參數</span><span class="sxs-lookup"><span data-stu-id="95594-131">PARAMETERS</span></span>

### <span data-ttu-id="95594-132">-帳戶</span><span class="sxs-lookup"><span data-stu-id="95594-132">-Account</span></span>
<span data-ttu-id="95594-133">需要時，以帳戶執行以推入安裝行動服務。</span><span class="sxs-lookup"><span data-stu-id="95594-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="95594-134">必須是 ASR 結構中以帳戶執行清單中的帳戶。</span><span class="sxs-lookup"><span data-stu-id="95594-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="95594-135">-AzureToAzure</span></span>
<span data-ttu-id="95594-136">參數參數指定在 Azure 中建立複製的專案至 azure 案例。</span><span class="sxs-lookup"><span data-stu-id="95594-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-137">-AzureToAzureAzlicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="95594-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="95594-138">指定用於 Azure 的 Vm 到 Azure 災害復原案例的磁片組配置。</span><span class="sxs-lookup"><span data-stu-id="95594-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-139">-AzureAzmId</span><span class="sxs-lookup"><span data-stu-id="95594-139">-AzureVmId</span></span>
<span data-ttu-id="95594-140">指定復原地區的災害復原保護 Azure VM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="95594-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95594-141">-DefaultProfile</span></span>
<span data-ttu-id="95594-142">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="95594-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="95594-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="95594-144">指定具有版本 (Azure 磁片加密的磁片加密) 容錯移轉後要用於復原 VM。</span><span class="sxs-lookup"><span data-stu-id="95594-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="95594-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="95594-146">指定磁片加密集的資源識別碼，用來加密受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="95594-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="95594-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="95594-148">指定 Azure 磁片加密的磁片加密 (密碼庫識別碼) 容錯移轉後要用於復原 VM。</span><span class="sxs-lookup"><span data-stu-id="95594-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="95594-149">-DiskType</span></span>
<span data-ttu-id="95594-150">指定修復 VM 管理的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="95594-150">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="95594-151">-HyperVToAzure</span></span>
<span data-ttu-id="95594-152">切換參數以指定複製的專案是正在複製到 Azure 的 Hyper-V 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95594-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-153">-Include隨時隨地使用</span><span class="sxs-lookup"><span data-stu-id="95594-153">-IncludeDiskId</span></span>
<span data-ttu-id="95594-154">要包含複本的磁片清單。</span><span class="sxs-lookup"><span data-stu-id="95594-154">The list of disks to include for replication.</span></span> <span data-ttu-id="95594-155">根據預設，會包含所有磁片。</span><span class="sxs-lookup"><span data-stu-id="95594-155">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-156">-InMageAzureV2AgeInput</span><span class="sxs-lookup"><span data-stu-id="95594-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="95594-157">指定 vMWare 磁片識別碼的磁片組配置輸入，以防範指定的可保護專案。</span><span class="sxs-lookup"><span data-stu-id="95594-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="95594-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="95594-159">指定具有版本 (Azure 磁片加密的磁片加密金鑰 URL，) 容錯移轉後用來做為修復 VM。</span><span class="sxs-lookup"><span data-stu-id="95594-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="95594-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="95594-161">指定 Azure 磁片加密的磁片 (金鑰庫識別碼) 容錯移轉後要用於復原 VM。</span><span class="sxs-lookup"><span data-stu-id="95594-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="95594-162">-LogStorageAccountId</span></span>
<span data-ttu-id="95594-163">指定要用來儲存複製記錄之記錄或緩存儲存帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="95594-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-164">-名稱</span><span class="sxs-lookup"><span data-stu-id="95594-164">-Name</span></span>
<span data-ttu-id="95594-165">指定 ASR 複製受保護專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="95594-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="95594-166">名稱必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="95594-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="95594-167">-OS</span><span class="sxs-lookup"><span data-stu-id="95594-167">-OS</span></span>
<span data-ttu-id="95594-168">指定作業系統系列。</span><span class="sxs-lookup"><span data-stu-id="95594-168">Specifies the operating system family.</span></span>
<span data-ttu-id="95594-169">此參數可接受的值為：Windows 或 Linux。</span><span class="sxs-lookup"><span data-stu-id="95594-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-170">-OSName</span><span class="sxs-lookup"><span data-stu-id="95594-170">-OSDiskName</span></span>
<span data-ttu-id="95594-171">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="95594-171">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="95594-172">-ProcessServer</span></span>
<span data-ttu-id="95594-173">要用於複製此電腦的流程伺服器。</span><span class="sxs-lookup"><span data-stu-id="95594-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="95594-174">使用 ASR 結構中對應至 Configuration 伺服器的流程伺服器清單來指定一個。</span><span class="sxs-lookup"><span data-stu-id="95594-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="95594-175">-ProtectableItem</span></span>
<span data-ttu-id="95594-176">指定啟用複製的 ASR 可保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="95594-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95594-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="95594-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="95594-178">指定對應到要用於複製之複製之複寫原則的 ASR 保護容器對應物件。</span><span class="sxs-lookup"><span data-stu-id="95594-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="95594-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="95594-180">AvailabilitySet 的識別碼，以在容錯移轉時將電腦復原到該電腦。</span><span class="sxs-lookup"><span data-stu-id="95594-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="95594-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="95594-182">指定容錯移轉後的復原 VM 可用性區域。</span><span class="sxs-lookup"><span data-stu-id="95594-182">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="95594-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="95594-184">在容錯移轉時將電腦復原到 Azure 虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="95594-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="95594-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="95594-186">指定要複製到的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="95594-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="95594-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="95594-188">在容錯移轉時，應附加容錯移轉到虛擬機器之復原 Azure 虛擬網路內的子網。</span><span class="sxs-lookup"><span data-stu-id="95594-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="95594-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="95594-190">指定用於修復 Azure VM 之開機診斷的儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="95594-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="95594-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="95594-192">指定要容錯移轉此虛擬機器之復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="95594-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="95594-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="95594-194">指定目標修復區域容錯移轉 Vm 所使用的鄰近位置群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="95594-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="95594-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="95594-196">指定在容錯移轉時建立虛擬機器之資源群組的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="95594-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="95594-197">-RecoveryVmName</span></span>
<span data-ttu-id="95594-198">容錯移轉後所建立復原 Vm 的名稱。</span><span class="sxs-lookup"><span data-stu-id="95594-198">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="95594-199">-ReplicationGroupName</span></span>
<span data-ttu-id="95594-200">指定要用於建立多 VM 一致修復點的複寫組名。</span><span class="sxs-lookup"><span data-stu-id="95594-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="95594-201">根據預設，每個複本受保護的專案都是以一組自己的複本建立，且不會產生多 VM 一致的復原點。</span><span class="sxs-lookup"><span data-stu-id="95594-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="95594-202">只有在您需要保護所有電腦至同一個複本群組，以跨一組機器建立多 VM 一致的修復點時，才使用此選項。</span><span class="sxs-lookup"><span data-stu-id="95594-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-203">-UseManaged可使用</span><span class="sxs-lookup"><span data-stu-id="95594-203">-UseManagedDisk</span></span>
<span data-ttu-id="95594-204">指定在容錯移轉上建立 Azure 虛擬機器時，應該使用受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="95594-204">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span> <span data-ttu-id="95594-205">它接受 True 或 False。</span><span class="sxs-lookup"><span data-stu-id="95594-205">It Accepts either True or False.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-206">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="95594-206">-VmmToVmm</span></span>
<span data-ttu-id="95594-207">切換參數以指定複製的專案是正在 VMM 管理的 Hyper-V 網站之間複製的 Hyper-V 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95594-207">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-208">-VAzToAzure</span><span class="sxs-lookup"><span data-stu-id="95594-208">-VMwareToAzure</span></span>
<span data-ttu-id="95594-209">切換參數以指定複製的專案是 V是否虛擬機器或實體伺服器，會複製到 Azure。</span><span class="sxs-lookup"><span data-stu-id="95594-209">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-210">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="95594-210">-WaitForCompletion</span></span>
<span data-ttu-id="95594-211">指定 Cmdlet 應等候作業完成再返回。</span><span class="sxs-lookup"><span data-stu-id="95594-211">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="95594-212">-確認</span><span class="sxs-lookup"><span data-stu-id="95594-212">-Confirm</span></span>
<span data-ttu-id="95594-213">啟動作業之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="95594-213">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-214">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95594-214">-WhatIf</span></span>
<span data-ttu-id="95594-215">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95594-215">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95594-216">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95594-216">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95594-217">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95594-217">CommonParameters</span></span>
<span data-ttu-id="95594-218">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="95594-218">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95594-219">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95594-219">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95594-220">輸入</span><span class="sxs-lookup"><span data-stu-id="95594-220">INPUTS</span></span>

### <span data-ttu-id="95594-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="95594-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="95594-222">輸出</span><span class="sxs-lookup"><span data-stu-id="95594-222">OUTPUTS</span></span>

### <span data-ttu-id="95594-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="95594-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="95594-224">筆記</span><span class="sxs-lookup"><span data-stu-id="95594-224">NOTES</span></span>

## <span data-ttu-id="95594-225">相關連結</span><span class="sxs-lookup"><span data-stu-id="95594-225">RELATED LINKS</span></span>

[<span data-ttu-id="95594-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95594-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="95594-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95594-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="95594-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95594-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
