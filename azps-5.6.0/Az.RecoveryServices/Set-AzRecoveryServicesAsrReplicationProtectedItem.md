---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: ad3f2c07d358819917706253df05bfd899c3b53e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913754"
---
# <span data-ttu-id="9bb00-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bb00-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="9bb00-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9bb00-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb00-103">針對指定的複本受保護專案設定復原屬性，例如目標網路和虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="9bb00-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="9bb00-104">語法</span><span class="sxs-lookup"><span data-stu-id="9bb00-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bb00-105">描述</span><span class="sxs-lookup"><span data-stu-id="9bb00-105">DESCRIPTION</span></span>
<span data-ttu-id="9bb00-106">**Set-AzRecoveryServicesAsrReplicationProtecedItem** Cmdlet 會設定複寫受保護的專案的復原屬性。</span><span class="sxs-lookup"><span data-stu-id="9bb00-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="9bb00-107">例子</span><span class="sxs-lookup"><span data-stu-id="9bb00-107">EXAMPLES</span></span>

### <span data-ttu-id="9bb00-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9bb00-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="9bb00-109">使用指定的參數開始更新複製受保護的專案設定，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="9bb00-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="9bb00-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="9bb00-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="9bb00-111">開始使用指定的參數更新複製受保護的專案網路介面卡片 (NIC 減少) 設定，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="9bb00-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="9bb00-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="9bb00-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="9bb00-113">啟動使用指定參數更新複本受保護專案主要 NIC (的作業，以用於復原的 vm ) 設定，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="9bb00-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="9bb00-114">範例 4</span><span class="sxs-lookup"><span data-stu-id="9bb00-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="9bb00-115">啟動使用指定參數更新複本受保護專案 NIC (的作業，以用於復原的 vm ) 設定，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="9bb00-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="9bb00-116">範例 5</span><span class="sxs-lookup"><span data-stu-id="9bb00-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="9bb00-117">開始執行更新複本受保護專案的操作，選取 noc tp 啟用 Azure 的復原 VM (加速網路，) 。</span><span class="sxs-lookup"><span data-stu-id="9bb00-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="9bb00-118">請勿傳遞 -EnableAcceworkNetworkingOnRecovery 以停用加速網路。</span><span class="sxs-lookup"><span data-stu-id="9bb00-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="9bb00-119">範例 6</span><span class="sxs-lookup"><span data-stu-id="9bb00-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="9bb00-120">針對指定的加密複製受保護專案啟動更新作業，以針對容錯移轉 VM 使用提供的加密詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9bb00-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="9bb00-121">範例 7</span><span class="sxs-lookup"><span data-stu-id="9bb00-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="9bb00-122">針對指定的複製受保護專案啟動更新作業，以針對容錯移轉 VM 使用提供的鄰近位置群組。</span><span class="sxs-lookup"><span data-stu-id="9bb00-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>

## <span data-ttu-id="9bb00-123">參數</span><span class="sxs-lookup"><span data-stu-id="9bb00-123">PARAMETERS</span></span>

### <span data-ttu-id="9bb00-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bb00-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="9bb00-125">指定測試容錯移轉和容錯移轉 NIC 組組詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9bb00-125">Specifies the test failover and failover NIC configuration details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb00-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bb00-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="9bb00-127">指定將受管理磁片 Vm 的磁片組 (Azure DR scenrio) 。</span><span class="sxs-lookup"><span data-stu-id="9bb00-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb00-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb00-128">-DefaultProfile</span></span>
<span data-ttu-id="9bb00-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9bb00-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9bb00-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="9bb00-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="9bb00-131">指定具有版本 (Azure 磁片加密的磁片加密) 容錯移轉後要用於復原 VM。</span><span class="sxs-lookup"><span data-stu-id="9bb00-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="9bb00-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="9bb00-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="9bb00-133">指定 Azure 磁片加密的磁片加密 (金鑰庫識別碼) 容錯移轉後要用於復原 VM。</span><span class="sxs-lookup"><span data-stu-id="9bb00-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="9bb00-134">-DiskIdToCryptEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="9bb00-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="9bb00-135">磁片資源識別碼到磁片加密集 ARM Id 的字典。</span><span class="sxs-lookup"><span data-stu-id="9bb00-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb00-136">-EnableAccenetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="9bb00-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="9bb00-137">在容錯移轉使用加速網路之後，指定修復 vm 上指定的 NIC。</span><span class="sxs-lookup"><span data-stu-id="9bb00-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="9bb00-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bb00-138">-InputObject</span></span>
<span data-ttu-id="9bb00-139">Cmdlet 的輸入物件：對應到要更新之複製受保護專案的 ASR 複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="9bb00-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb00-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="9bb00-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="9bb00-141">指定 Azure 磁片加密的磁片 (URL 版本，) 容錯移轉後用來做為修復 VM。</span><span class="sxs-lookup"><span data-stu-id="9bb00-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="9bb00-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="9bb00-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="9bb00-143">指定 Azure 磁片加密的磁片 (金鑰金鑰 Vault 識別碼) 容錯移轉後要用於復原 VM。</span><span class="sxs-lookup"><span data-stu-id="9bb00-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="9bb00-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9bb00-144">-LicenseType</span></span>
<span data-ttu-id="9bb00-145">指定 Windows Server 虛擬機器所使用之授權類型選項。</span><span class="sxs-lookup"><span data-stu-id="9bb00-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="9bb00-146">如果您有權使用 Azure 混合式使用權益 (HUB) 進行移移，並想指定在超過此受保護的專案時，使用 HUB 設定，將授權類型設為 WindowsServer。</span><span class="sxs-lookup"><span data-stu-id="9bb00-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb00-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="9bb00-147">-Name</span></span>
<span data-ttu-id="9bb00-148">指定容錯移轉時要建立復原虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bb00-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="9bb00-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="9bb00-149">-NicSelectionType</span></span>
<span data-ttu-id="9bb00-150">指定網路介面配接器 (NIC) 使用者設定或預設設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="9bb00-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="9bb00-151">您可以指定 NotSelected 以回到預設值。</span><span class="sxs-lookup"><span data-stu-id="9bb00-151">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb00-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="9bb00-152">-PrimaryNic</span></span>
<span data-ttu-id="9bb00-153">指定 NIC，該 NIC 在容錯移轉之後會做為 revbcovery VM 的主要 NIC。</span><span class="sxs-lookup"><span data-stu-id="9bb00-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="9bb00-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9bb00-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="9bb00-155">容錯移轉後複製受保護專案的可用性集。</span><span class="sxs-lookup"><span data-stu-id="9bb00-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="9bb00-156">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="9bb00-156">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="9bb00-157">指定容錯移轉後受禁止複製專案的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="9bb00-157">Specifies availability zone for replication protected item after failover.</span></span>

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

### <span data-ttu-id="9bb00-158">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9bb00-158">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="9bb00-159">指定用於修復 Azure VM 之開機診斷的儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="9bb00-159">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="9bb00-160">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="9bb00-160">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="9bb00-161">要容錯移轉到此虛擬機器之復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9bb00-161">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="9bb00-162">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9bb00-162">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="9bb00-163">指定要與復原 NIC 相關聯的目標後端位址資料庫。</span><span class="sxs-lookup"><span data-stu-id="9bb00-163">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb00-164">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="9bb00-164">-RecoveryNetworkId</span></span>
<span data-ttu-id="9bb00-165">指定受保護專案應失敗之 Azure 虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9bb00-165">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="9bb00-166">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9bb00-166">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="9bb00-167">指定要與復原 NIC 相關聯的網路安全性群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="9bb00-167">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="9bb00-168">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="9bb00-168">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="9bb00-169">指定復原時應指派給主要 NIC 的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9bb00-169">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="9bb00-170">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="9bb00-170">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="9bb00-171">指定復原 Azure 虛擬網路上的子網名稱，此受保護專案的 NIC 應該于容錯移轉時連接到該子網。</span><span class="sxs-lookup"><span data-stu-id="9bb00-171">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="9bb00-172">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="9bb00-172">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="9bb00-173">指定要容錯移轉虛擬機器之復原鄰近位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9bb00-173">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="9bb00-174">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="9bb00-174">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="9bb00-175">指定要與復原 NIC 關聯的公用 IP 位址資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9bb00-175">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="9bb00-176">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="9bb00-176">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="9bb00-177">復原區域 Azure 資源群組的識別碼，其中受保護的專案將在容錯移轉時復原。</span><span class="sxs-lookup"><span data-stu-id="9bb00-177">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="9bb00-178">-大小</span><span class="sxs-lookup"><span data-stu-id="9bb00-178">-Size</span></span>
<span data-ttu-id="9bb00-179">指定復原虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="9bb00-179">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="9bb00-180">該值應來自 Azure 虛擬機器支援的大小集。</span><span class="sxs-lookup"><span data-stu-id="9bb00-180">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="9bb00-181">-TfoAzureUFNAME</span><span class="sxs-lookup"><span data-stu-id="9bb00-181">-TfoAzureVMName</span></span>
<span data-ttu-id="9bb00-182">指定測試容錯移轉 VM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bb00-182">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="9bb00-183">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="9bb00-183">-UpdateNic</span></span>
<span data-ttu-id="9bb00-184">指定此 Cmdlet 設定復原網路屬性需要 udpated 之虛擬機器的 NIC。</span><span class="sxs-lookup"><span data-stu-id="9bb00-184">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="9bb00-185">-UseManaged可使用</span><span class="sxs-lookup"><span data-stu-id="9bb00-185">-UseManagedDisk</span></span>
<span data-ttu-id="9bb00-186">指定在容錯移轉上建立 Azure 虛擬機器時，應該使用受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="9bb00-186">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="9bb00-187">-確認</span><span class="sxs-lookup"><span data-stu-id="9bb00-187">-Confirm</span></span>
<span data-ttu-id="9bb00-188">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9bb00-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb00-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bb00-189">-WhatIf</span></span>
<span data-ttu-id="9bb00-190">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9bb00-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bb00-191">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9bb00-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bb00-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb00-192">CommonParameters</span></span>
<span data-ttu-id="9bb00-193">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9bb00-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb00-194">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bb00-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb00-195">輸入</span><span class="sxs-lookup"><span data-stu-id="9bb00-195">INPUTS</span></span>

### <span data-ttu-id="9bb00-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bb00-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9bb00-197">輸出</span><span class="sxs-lookup"><span data-stu-id="9bb00-197">OUTPUTS</span></span>

### <span data-ttu-id="9bb00-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="9bb00-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9bb00-199">筆記</span><span class="sxs-lookup"><span data-stu-id="9bb00-199">NOTES</span></span>

## <span data-ttu-id="9bb00-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="9bb00-200">RELATED LINKS</span></span>

[<span data-ttu-id="9bb00-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bb00-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9bb00-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bb00-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9bb00-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bb00-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
