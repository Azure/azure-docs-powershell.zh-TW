---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437304"
---
# <span data-ttu-id="f14d1-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f14d1-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="f14d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f14d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f14d1-103">透過建立受禁止複製的專案，為 ASR 可保護的專案啟用複製。</span><span class="sxs-lookup"><span data-stu-id="f14d1-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="f14d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f14d1-104">SYNTAX</span></span>

### <span data-ttu-id="f14d1-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="f14d1-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f14d1-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="f14d1-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f14d1-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="f14d1-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f14d1-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="f14d1-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f14d1-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="f14d1-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f14d1-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f14d1-110">AzureToAzure</span></span>
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

### <span data-ttu-id="f14d1-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="f14d1-111">AzureToAzureWithoutDiskDetails</span></span>
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

## <span data-ttu-id="f14d1-112">說明</span><span class="sxs-lookup"><span data-stu-id="f14d1-112">DESCRIPTION</span></span>
<span data-ttu-id="f14d1-113">**新的-AzRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會建立新的受保護的複製專案。</span><span class="sxs-lookup"><span data-stu-id="f14d1-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="f14d1-114">使用此 Cmdlet 來啟用 ASR 可保護專案的複製。</span><span class="sxs-lookup"><span data-stu-id="f14d1-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="f14d1-115">示例</span><span class="sxs-lookup"><span data-stu-id="f14d1-115">EXAMPLES</span></span>

### <span data-ttu-id="f14d1-116">範例1</span><span class="sxs-lookup"><span data-stu-id="f14d1-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="f14d1-117">針對指定的 ASR 可保護專案啟動複製受保護的專案建立作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f14d1-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f14d1-118">範例2</span><span class="sxs-lookup"><span data-stu-id="f14d1-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="f14d1-119">針對指定的 ASR 可傳送專案啟動複製受保護的專案建立作業，並傳回用來追蹤作業 (vmWare 至 Azure 案例) 的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f14d1-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="f14d1-120">範例3</span><span class="sxs-lookup"><span data-stu-id="f14d1-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="f14d1-121">針對指定的 ASR 可傳送專案啟動複製受保護的專案建立作業，並傳回用來追蹤作業的 ASR 作業， (Azure 到 Azure 案例) 。</span><span class="sxs-lookup"><span data-stu-id="f14d1-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="f14d1-122">範例4</span><span class="sxs-lookup"><span data-stu-id="f14d1-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="f14d1-123">針對指定的 VmId 啟動複製受保護的專案建立作業，並傳回用於追蹤作業 (Azure 到 Azure 案例) 的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f14d1-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="f14d1-124">範例5</span><span class="sxs-lookup"><span data-stu-id="f14d1-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="f14d1-125">針對指定的 ASR 可傳送專案（包括選擇性磁片）啟動複製受保護的專案建立作業，並傳回用來追蹤作業 (vmWare 至 Azure 案例的 ASR 作業) 選取的磁片。</span><span class="sxs-lookup"><span data-stu-id="f14d1-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="f14d1-126">範例6</span><span class="sxs-lookup"><span data-stu-id="f14d1-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="f14d1-127">範例7</span><span class="sxs-lookup"><span data-stu-id="f14d1-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="f14d1-128">針對指定的 VmId 啟動複製受保護的專案建立作業，並傳回用於追蹤作業 (Azure 到 Azure 案例) 的 ASR 作業。針對以 Cmdlet 傳遞的容錯移轉 VM 詳細資料，將會使用。</span><span class="sxs-lookup"><span data-stu-id="f14d1-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="f14d1-129">範例8</span><span class="sxs-lookup"><span data-stu-id="f14d1-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="f14d1-130">在鄰近性位置群組內啟動虛擬機器的複製受保護專案建立作業，並傳回用來追蹤作業 (Azure 到 Azure 案例) 的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f14d1-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="f14d1-131">參數</span><span class="sxs-lookup"><span data-stu-id="f14d1-131">PARAMETERS</span></span>

### <span data-ttu-id="f14d1-132">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f14d1-132">-Account</span></span>
<span data-ttu-id="f14d1-133">要用來推入行動服務的 [執行方式] 帳戶（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="f14d1-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="f14d1-134">必須是在 ASR 結構中的 [作為帳戶執行方式] 清單中的一個。</span><span class="sxs-lookup"><span data-stu-id="f14d1-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="f14d1-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f14d1-135">-AzureToAzure</span></span>
<span data-ttu-id="f14d1-136">Switch 參數指定在 azure 中建立複製的專案至 azure 案例。</span><span class="sxs-lookup"><span data-stu-id="f14d1-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

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

### <span data-ttu-id="f14d1-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="f14d1-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="f14d1-138">針對 Azure 災害復原案例指定要使用 Vm 的磁片設定。</span><span class="sxs-lookup"><span data-stu-id="f14d1-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="f14d1-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="f14d1-139">-AzureVmId</span></span>
<span data-ttu-id="f14d1-140">針對復原區域中的災害復原保護指定 Azure VM id。</span><span class="sxs-lookup"><span data-stu-id="f14d1-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

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

### <span data-ttu-id="f14d1-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14d1-141">-DefaultProfile</span></span>
<span data-ttu-id="f14d1-142">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f14d1-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f14d1-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="f14d1-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="f14d1-144">指定要在容錯移轉之後用來恢復 VM 之版本 (Azure 磁片加密) 的磁片加密機密 URL。</span><span class="sxs-lookup"><span data-stu-id="f14d1-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="f14d1-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="f14d1-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="f14d1-146">指定磁片加密集的資源識別碼，以用於加密受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="f14d1-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="f14d1-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="f14d1-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="f14d1-148">指定要在容錯移轉之後用來恢復 VM 的磁片加密秘密電子倉庫識別碼 (Azure 磁片加密) 。</span><span class="sxs-lookup"><span data-stu-id="f14d1-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="f14d1-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="f14d1-149">-DiskType</span></span>
<span data-ttu-id="f14d1-150">指定復原 VM 管理的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="f14d1-150">Specifies the Recovery VM managed disk type.</span></span>

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

### <span data-ttu-id="f14d1-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="f14d1-151">-HyperVToAzure</span></span>
<span data-ttu-id="f14d1-152">切換參數以指定複製的專案是要複製到 Azure 的 Hyper-v 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f14d1-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="f14d1-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="f14d1-153">-IncludeDiskId</span></span>
<span data-ttu-id="f14d1-154">要納入複製的磁片清單。</span><span class="sxs-lookup"><span data-stu-id="f14d1-154">The list of disks to include for replication.</span></span> <span data-ttu-id="f14d1-155">根據預設，會包含所有磁片。</span><span class="sxs-lookup"><span data-stu-id="f14d1-155">By default all disks are included.</span></span>

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

### <span data-ttu-id="f14d1-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="f14d1-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="f14d1-157">指定 vMWare 磁片 id 的磁片設定輸入，以便從指定的可保護專案中受到保護。</span><span class="sxs-lookup"><span data-stu-id="f14d1-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

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

### <span data-ttu-id="f14d1-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="f14d1-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="f14d1-159">指定要在容錯移轉之後用來恢復 VM 之版本 (Azure 磁片加密) 的磁片加密金鑰 URL。</span><span class="sxs-lookup"><span data-stu-id="f14d1-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="f14d1-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="f14d1-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="f14d1-161">指定要在容錯移轉之後用來恢復 VM 的磁片加密金鑰-vault 識別碼 (Azure 磁片加密) 。</span><span class="sxs-lookup"><span data-stu-id="f14d1-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="f14d1-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f14d1-162">-LogStorageAccountId</span></span>
<span data-ttu-id="f14d1-163">指定要用來儲存複製記錄的記錄或快取儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="f14d1-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="f14d1-164">-名稱</span><span class="sxs-lookup"><span data-stu-id="f14d1-164">-Name</span></span>
<span data-ttu-id="f14d1-165">指定 ASR 複製受保護的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="f14d1-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="f14d1-166">該名稱在保存庫中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="f14d1-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="f14d1-167">-OS</span><span class="sxs-lookup"><span data-stu-id="f14d1-167">-OS</span></span>
<span data-ttu-id="f14d1-168">指定作業系統系列。</span><span class="sxs-lookup"><span data-stu-id="f14d1-168">Specifies the operating system family.</span></span>
<span data-ttu-id="f14d1-169">此參數可接受的值為： Windows 或 Linux。</span><span class="sxs-lookup"><span data-stu-id="f14d1-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="f14d1-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="f14d1-170">-OSDiskName</span></span>
<span data-ttu-id="f14d1-171">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="f14d1-171">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="f14d1-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="f14d1-172">-ProcessServer</span></span>
<span data-ttu-id="f14d1-173">要用來複製此電腦的進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="f14d1-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="f14d1-174">使用與佈建服務器相對應的 ASR 結構中的進程伺服器清單來指定它。</span><span class="sxs-lookup"><span data-stu-id="f14d1-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

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

### <span data-ttu-id="f14d1-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f14d1-175">-ProtectableItem</span></span>
<span data-ttu-id="f14d1-176">指定要啟用複製的 ASR 可保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="f14d1-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="f14d1-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f14d1-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="f14d1-178">指定要用於複製之複製原則對應的 ASR 保護容器對應物件。</span><span class="sxs-lookup"><span data-stu-id="f14d1-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="f14d1-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="f14d1-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="f14d1-180">在發生容錯移轉時，要將電腦復原至其中的 AvailabilitySet 識別碼。</span><span class="sxs-lookup"><span data-stu-id="f14d1-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="f14d1-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="f14d1-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="f14d1-182">指定容錯移轉後的 [恢復 VM 可用性區域]。</span><span class="sxs-lookup"><span data-stu-id="f14d1-182">Specifies the recovery VM availability zone after failover.</span></span>


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

### <span data-ttu-id="f14d1-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="f14d1-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="f14d1-184">在容錯移轉事件時，要將電腦復原至其中的 Azure 虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="f14d1-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="f14d1-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f14d1-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f14d1-186">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="f14d1-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="f14d1-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="f14d1-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="f14d1-188">在容錯移轉時，容錯移轉虛擬機器應附加到的復原 Azure 虛擬網路中的子網。</span><span class="sxs-lookup"><span data-stu-id="f14d1-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

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

### <span data-ttu-id="f14d1-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f14d1-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="f14d1-190">指定用於恢復 azure VM 的啟動診斷的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f14d1-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="f14d1-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="f14d1-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="f14d1-192">指定要將此虛擬機器容錯移轉至其中的復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f14d1-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="f14d1-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="f14d1-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="f14d1-194">指定 [目標復原區域] 中容錯移轉 Vm 所使用的鄰近性位置群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="f14d1-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

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

### <span data-ttu-id="f14d1-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="f14d1-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="f14d1-196">指定在容錯移轉事件中，將建立虛擬機器之資源群組的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="f14d1-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="f14d1-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="f14d1-197">-RecoveryVmName</span></span>
<span data-ttu-id="f14d1-198">在容錯移轉之後建立的復原 Vm 名稱。</span><span class="sxs-lookup"><span data-stu-id="f14d1-198">Name of the recovery Vm created after failover.</span></span>

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

### <span data-ttu-id="f14d1-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="f14d1-199">-ReplicationGroupName</span></span>
<span data-ttu-id="f14d1-200">指定要用來建立多 VM 一致復原點的複製組名。</span><span class="sxs-lookup"><span data-stu-id="f14d1-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="f14d1-201">根據預設，每個複製受保護的專案都會在自己的群組中建立，且不會產生多重 VM 一致的復原點。</span><span class="sxs-lookup"><span data-stu-id="f14d1-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="f14d1-202">只有在您需要將所有電腦保護到相同的複製群組時，才能使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="f14d1-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

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

### <span data-ttu-id="f14d1-203">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="f14d1-203">-VmmToVmm</span></span>
<span data-ttu-id="f14d1-204">切換參數以指定複製的專案是要在 VMM 管理的 Hyper-v 網站之間複製的 Hyper-v 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f14d1-204">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="f14d1-205">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="f14d1-205">-VMwareToAzure</span></span>
<span data-ttu-id="f14d1-206">切換參數以指定複製的專案是將會複製到 Azure 的 VMware 虛擬機器或物理伺服器。</span><span class="sxs-lookup"><span data-stu-id="f14d1-206">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="f14d1-207">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f14d1-207">-WaitForCompletion</span></span>
<span data-ttu-id="f14d1-208">指定在傳回前，該指令應等待完成操作。</span><span class="sxs-lookup"><span data-stu-id="f14d1-208">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="f14d1-209">-確認</span><span class="sxs-lookup"><span data-stu-id="f14d1-209">-Confirm</span></span>
<span data-ttu-id="f14d1-210">啟動作業前提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f14d1-210">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="f14d1-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f14d1-211">-WhatIf</span></span>
<span data-ttu-id="f14d1-212">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f14d1-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f14d1-213">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f14d1-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f14d1-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14d1-214">CommonParameters</span></span>
<span data-ttu-id="f14d1-215">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f14d1-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14d1-216">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f14d1-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14d1-217">輸入</span><span class="sxs-lookup"><span data-stu-id="f14d1-217">INPUTS</span></span>

### <span data-ttu-id="f14d1-218">RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f14d1-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="f14d1-219">輸出</span><span class="sxs-lookup"><span data-stu-id="f14d1-219">OUTPUTS</span></span>

### <span data-ttu-id="f14d1-220">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f14d1-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f14d1-221">筆記</span><span class="sxs-lookup"><span data-stu-id="f14d1-221">NOTES</span></span>

## <span data-ttu-id="f14d1-222">相關連結</span><span class="sxs-lookup"><span data-stu-id="f14d1-222">RELATED LINKS</span></span>

[<span data-ttu-id="f14d1-223">AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f14d1-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f14d1-224">移除-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f14d1-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f14d1-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f14d1-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
