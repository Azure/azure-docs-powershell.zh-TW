---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 21c924d02a18ae60f07abd616809358208256039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134674"
---
# <span data-ttu-id="1fc58-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1fc58-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="1fc58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fc58-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc58-103">針對指定的複製受保護專案設定恢復屬性，例如目標網路和虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="1fc58-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="1fc58-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fc58-104">SYNTAX</span></span>

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

## <span data-ttu-id="1fc58-105">說明</span><span class="sxs-lookup"><span data-stu-id="1fc58-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc58-106">**AzRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會為複製受保護的專案設定復原屬性。</span><span class="sxs-lookup"><span data-stu-id="1fc58-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="1fc58-107">示例</span><span class="sxs-lookup"><span data-stu-id="1fc58-107">EXAMPLES</span></span>

### <span data-ttu-id="1fc58-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1fc58-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="1fc58-109">使用指定的參數開始更新複製受保護的專案設定，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="1fc58-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="1fc58-110">範例2</span><span class="sxs-lookup"><span data-stu-id="1fc58-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="1fc58-111">啟動更新受保護的複製專案網路介面卡的操作 (NIC 減少) 設定使用指定的參數，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="1fc58-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="1fc58-112">範例3</span><span class="sxs-lookup"><span data-stu-id="1fc58-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="1fc58-113">開始更新複製受保護的專案主要 NIC (以用於已復原的 vm ) 設定，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="1fc58-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="1fc58-114">範例4</span><span class="sxs-lookup"><span data-stu-id="1fc58-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="1fc58-115">使用指定的參數開始更新複製受保護的專案 NIC () ，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="1fc58-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="1fc58-116">範例5</span><span class="sxs-lookup"><span data-stu-id="1fc58-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="1fc58-117">開始更新已選取 [複製受保護的專案] 的 noc tp 啟用 [Azure 到 Azure 災害復原]) 的 [恢復 VM] 上的加速網路 (。</span><span class="sxs-lookup"><span data-stu-id="1fc58-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="1fc58-118">EnableAcceleratedNetworkingOnRecovery [停用] 以停用加速的網路功能。</span><span class="sxs-lookup"><span data-stu-id="1fc58-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="1fc58-119">範例6</span><span class="sxs-lookup"><span data-stu-id="1fc58-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="1fc58-120">針對指定的加密複製受保護的專案啟動更新作業，以使用針對容錯移轉 VM 提供的加密詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1fc58-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="1fc58-121">範例7</span><span class="sxs-lookup"><span data-stu-id="1fc58-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="1fc58-122">針對指定的複製受保護專案啟動更新作業，以使用針對容錯移轉 VM 提供的鄰近性位置群組。</span><span class="sxs-lookup"><span data-stu-id="1fc58-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>

## <span data-ttu-id="1fc58-123">參數</span><span class="sxs-lookup"><span data-stu-id="1fc58-123">PARAMETERS</span></span>

### <span data-ttu-id="1fc58-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fc58-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="1fc58-125">指定測試容錯移轉與容錯移轉 NIC 配置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1fc58-125">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="1fc58-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fc58-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="1fc58-127">指定要 udpated 受管理磁片 Vm (Azure 到 Azure DR scenrio) 的磁片設定。</span><span class="sxs-lookup"><span data-stu-id="1fc58-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="1fc58-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc58-128">-DefaultProfile</span></span>
<span data-ttu-id="1fc58-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fc58-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1fc58-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="1fc58-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="1fc58-131">指定要在容錯移轉之後用來恢復 VM 之版本 (Azure 磁片加密) 的磁片加密機密 URL。</span><span class="sxs-lookup"><span data-stu-id="1fc58-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="1fc58-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="1fc58-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="1fc58-133">指定要在容錯移轉之後用來恢復 VM 的磁片加密機密金鑰 vault ID (Azure 磁片加密) 。</span><span class="sxs-lookup"><span data-stu-id="1fc58-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="1fc58-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="1fc58-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="1fc58-135">磁片資源識別碼的字典至磁片加密集 ARM Id。</span><span class="sxs-lookup"><span data-stu-id="1fc58-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="1fc58-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="1fc58-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="1fc58-137">在容錯移轉使用加速網路之後，指定恢復 vm 上的指定 NIC。</span><span class="sxs-lookup"><span data-stu-id="1fc58-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="1fc58-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fc58-138">-InputObject</span></span>
<span data-ttu-id="1fc58-139">Cmdlet 的輸入物件：與要更新之受複製受保護的專案對應的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="1fc58-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="1fc58-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="1fc58-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="1fc58-141">指定要在容錯移轉之後用來復原 VM (Azure 磁片加密) 的磁片加密金鑰 URL 版本。</span><span class="sxs-lookup"><span data-stu-id="1fc58-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="1fc58-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="1fc58-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="1fc58-143">指定要在容錯移轉之後用來恢復 VM (Azure 磁片加密) 的磁片加密金鑰 keyVault ID。</span><span class="sxs-lookup"><span data-stu-id="1fc58-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="1fc58-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1fc58-144">-LicenseType</span></span>
<span data-ttu-id="1fc58-145">指定要用於 Windows Server 虛擬機器的授權類型選取專案。</span><span class="sxs-lookup"><span data-stu-id="1fc58-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="1fc58-146">如果您有資格使用 Azure 混合式使用優惠 (中樞) 進行遷移，且想要指定在容錯移轉此受保護的專案時使用中樞設定，請將 [授權類型] 設定為 [WindowsServer]。</span><span class="sxs-lookup"><span data-stu-id="1fc58-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="1fc58-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fc58-147">-Name</span></span>
<span data-ttu-id="1fc58-148">指定將在容錯移轉時建立的恢復虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fc58-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="1fc58-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="1fc58-149">-NicSelectionType</span></span>
<span data-ttu-id="1fc58-150">指定 (NIC 的網路介面卡，) 由使用者設定的屬性或依預設設定的內容。</span><span class="sxs-lookup"><span data-stu-id="1fc58-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="1fc58-151">您可以指定 NotSelected，以回到預設值。</span><span class="sxs-lookup"><span data-stu-id="1fc58-151">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="1fc58-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="1fc58-152">-PrimaryNic</span></span>
<span data-ttu-id="1fc58-153">指定將在容錯移轉之後作為 recvcovery VM 的主要 NIC 使用的 NIC。</span><span class="sxs-lookup"><span data-stu-id="1fc58-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="1fc58-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1fc58-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="1fc58-155">容錯移轉之後，已針對複製受保護的專案進行可用性設定。</span><span class="sxs-lookup"><span data-stu-id="1fc58-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="1fc58-156">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="1fc58-156">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="1fc58-157">在容錯移轉之後，為複製受保護的專案指定可用性區域。</span><span class="sxs-lookup"><span data-stu-id="1fc58-157">Specifies availability zone for replication protected item after failover.</span></span>

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

### <span data-ttu-id="1fc58-158">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1fc58-158">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="1fc58-159">指定用於恢復 azure VM 的啟動診斷的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="1fc58-159">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="1fc58-160">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="1fc58-160">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="1fc58-161">要將此虛擬機器容錯移轉至其中的復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fc58-161">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="1fc58-162">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1fc58-162">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="1fc58-163">指定要與恢復 NIC 相關聯的目標後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="1fc58-163">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="1fc58-164">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="1fc58-164">-RecoveryNetworkId</span></span>
<span data-ttu-id="1fc58-165">指定受保護專案應針對其進行容錯移轉之 Azure 虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fc58-165">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="1fc58-166">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1fc58-166">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="1fc58-167">指定要與恢復 NIC 相關聯之網路安全性群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fc58-167">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="1fc58-168">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="1fc58-168">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="1fc58-169">指定在恢復時應該指派給主要 NIC 的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1fc58-169">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="1fc58-170">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="1fc58-170">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="1fc58-171">指定要在容錯移轉時，將受保護之專案的這個 NIC 連線至之 [復原] Azure 虛擬網路上的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="1fc58-171">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="1fc58-172">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="1fc58-172">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="1fc58-173">指定要將虛擬機器容錯移轉至其中的 [恢復鄰近性] 位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fc58-173">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="1fc58-174">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="1fc58-174">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="1fc58-175">指定要與恢復 NIC 相關聯之公用 IP 位址資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fc58-175">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="1fc58-176">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="1fc58-176">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="1fc58-177">修復區域中的 Azure 資源群組的識別碼，受保護的專案將會在容錯移轉時復原。</span><span class="sxs-lookup"><span data-stu-id="1fc58-177">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="1fc58-178">-大小</span><span class="sxs-lookup"><span data-stu-id="1fc58-178">-Size</span></span>
<span data-ttu-id="1fc58-179">指定復原虛擬電腦大小。</span><span class="sxs-lookup"><span data-stu-id="1fc58-179">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="1fc58-180">此值應該是由 Azure 虛擬機器支援的大小集合所組成。</span><span class="sxs-lookup"><span data-stu-id="1fc58-180">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="1fc58-181">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="1fc58-181">-TfoAzureVMName</span></span>
<span data-ttu-id="1fc58-182">指定測試容錯移轉 VM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fc58-182">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="1fc58-183">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="1fc58-183">-UpdateNic</span></span>
<span data-ttu-id="1fc58-184">指定此 Cmdlet 設定恢復網路屬性需要 udpated 之虛擬機器的 NIC。</span><span class="sxs-lookup"><span data-stu-id="1fc58-184">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="1fc58-185">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1fc58-185">-UseManagedDisk</span></span>
<span data-ttu-id="1fc58-186">指定在容錯移轉中建立的 Azure 虛擬機器是否應使用受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="1fc58-186">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="1fc58-187">-確認</span><span class="sxs-lookup"><span data-stu-id="1fc58-187">-Confirm</span></span>
<span data-ttu-id="1fc58-188">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1fc58-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fc58-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fc58-189">-WhatIf</span></span>
<span data-ttu-id="1fc58-190">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1fc58-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fc58-191">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fc58-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fc58-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc58-192">CommonParameters</span></span>
<span data-ttu-id="1fc58-193">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fc58-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc58-194">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1fc58-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc58-195">輸入</span><span class="sxs-lookup"><span data-stu-id="1fc58-195">INPUTS</span></span>

### <span data-ttu-id="1fc58-196">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1fc58-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1fc58-197">輸出</span><span class="sxs-lookup"><span data-stu-id="1fc58-197">OUTPUTS</span></span>

### <span data-ttu-id="1fc58-198">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1fc58-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1fc58-199">筆記</span><span class="sxs-lookup"><span data-stu-id="1fc58-199">NOTES</span></span>

## <span data-ttu-id="1fc58-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fc58-200">RELATED LINKS</span></span>

[<span data-ttu-id="1fc58-201">AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1fc58-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="1fc58-202">新-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1fc58-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="1fc58-203">移除-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1fc58-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
