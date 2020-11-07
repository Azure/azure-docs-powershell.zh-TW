---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 494edd4f399855512cd7b0a847f261e711bb01cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959473"
---
# <span data-ttu-id="8ba10-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ba10-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="8ba10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ba10-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba10-103">針對指定的複製受保護專案設定恢復屬性，例如目標網路和虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="8ba10-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="8ba10-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ba10-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-EnableAcceleratedNetworkingOnRecovery]
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

## <span data-ttu-id="8ba10-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ba10-105">DESCRIPTION</span></span>
<span data-ttu-id="8ba10-106">**AzRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會為複製受保護的專案設定復原屬性。</span><span class="sxs-lookup"><span data-stu-id="8ba10-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="8ba10-107">示例</span><span class="sxs-lookup"><span data-stu-id="8ba10-107">EXAMPLES</span></span>

### <span data-ttu-id="8ba10-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8ba10-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="8ba10-109">使用指定的參數開始更新複製受保護的專案設定，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="8ba10-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8ba10-110">範例2</span><span class="sxs-lookup"><span data-stu-id="8ba10-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="8ba10-111">啟動更新受保護的複製專案網路介面卡的操作 (NIC 減少) 設定使用指定的參數，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="8ba10-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8ba10-112">範例3</span><span class="sxs-lookup"><span data-stu-id="8ba10-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="8ba10-113">開始更新複製受保護的專案主要 NIC (以用於已復原的 vm ) 設定，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="8ba10-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8ba10-114">範例4</span><span class="sxs-lookup"><span data-stu-id="8ba10-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="8ba10-115">使用指定的參數開始更新複製受保護的專案 NIC () ，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="8ba10-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8ba10-116">範例5</span><span class="sxs-lookup"><span data-stu-id="8ba10-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="8ba10-117">開始更新已選取 [複製受保護的專案] 的 noc tp 啟用 [Azure 到 Azure 災害復原]) 的 [恢復 VM] 上的加速網路 (。</span><span class="sxs-lookup"><span data-stu-id="8ba10-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="8ba10-118">EnableAcceleratedNetworkingOnRecovery [停用] 以停用加速的網路功能。</span><span class="sxs-lookup"><span data-stu-id="8ba10-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="8ba10-119">範例6</span><span class="sxs-lookup"><span data-stu-id="8ba10-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="8ba10-120">針對指定的加密複製受保護的專案啟動更新作業，以使用針對容錯移轉 VM 提供的加密詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8ba10-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

## <span data-ttu-id="8ba10-121">參數</span><span class="sxs-lookup"><span data-stu-id="8ba10-121">PARAMETERS</span></span>

### <span data-ttu-id="8ba10-122">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ba10-122">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="8ba10-123">指定測試容錯移轉與容錯移轉 NIC 配置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8ba10-123">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="8ba10-124">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ba10-124">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="8ba10-125">指定要 udpated 受管理磁片 Vm (Azure 到 Azure DR scenrio) 的磁片設定。</span><span class="sxs-lookup"><span data-stu-id="8ba10-125">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="8ba10-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba10-126">-DefaultProfile</span></span>
<span data-ttu-id="8ba10-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ba10-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8ba10-128">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="8ba10-128">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="8ba10-129">指定要在容錯移轉之後用來恢復 VM 之版本 (Azure 磁片加密) 的磁片加密機密 URL。</span><span class="sxs-lookup"><span data-stu-id="8ba10-129">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8ba10-130">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8ba10-130">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="8ba10-131">指定要在容錯移轉之後用來恢復 VM 的磁片加密機密金鑰 vault ID (Azure 磁片加密) 。</span><span class="sxs-lookup"><span data-stu-id="8ba10-131">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8ba10-132">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="8ba10-132">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="8ba10-133">磁片資源識別碼的字典至磁片加密集 ARM Id。</span><span class="sxs-lookup"><span data-stu-id="8ba10-133">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="8ba10-134">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="8ba10-134">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="8ba10-135">在容錯移轉使用加速網路之後，指定恢復 vm 上的指定 NIC。</span><span class="sxs-lookup"><span data-stu-id="8ba10-135">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="8ba10-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ba10-136">-InputObject</span></span>
<span data-ttu-id="8ba10-137">Cmdlet 的輸入物件：與要更新之受複製受保護的專案對應的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="8ba10-137">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="8ba10-138">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="8ba10-138">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="8ba10-139">指定要在容錯移轉之後用來復原 VM (Azure 磁片加密) 的磁片加密金鑰 URL 版本。</span><span class="sxs-lookup"><span data-stu-id="8ba10-139">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8ba10-140">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8ba10-140">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="8ba10-141">指定要在容錯移轉之後用來恢復 VM (Azure 磁片加密) 的磁片加密金鑰 keyVault ID。</span><span class="sxs-lookup"><span data-stu-id="8ba10-141">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="8ba10-142">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8ba10-142">-LicenseType</span></span>
<span data-ttu-id="8ba10-143">指定要用於 Windows Server 虛擬機器的授權類型選取專案。</span><span class="sxs-lookup"><span data-stu-id="8ba10-143">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="8ba10-144">如果您有資格使用 Azure 混合式使用優惠 (中樞) 進行遷移，且想要指定在容錯移轉此受保護的專案時使用中樞設定，請將 [授權類型] 設定為 [WindowsServer]。</span><span class="sxs-lookup"><span data-stu-id="8ba10-144">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="8ba10-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ba10-145">-Name</span></span>
<span data-ttu-id="8ba10-146">指定將在容錯移轉時建立的恢復虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ba10-146">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="8ba10-147">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="8ba10-147">-NicSelectionType</span></span>
<span data-ttu-id="8ba10-148">指定 (NIC 的網路介面卡，) 由使用者設定的屬性或依預設設定的內容。</span><span class="sxs-lookup"><span data-stu-id="8ba10-148">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="8ba10-149">您可以指定 NotSelected，以回到預設值。</span><span class="sxs-lookup"><span data-stu-id="8ba10-149">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="8ba10-150">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="8ba10-150">-PrimaryNic</span></span>
<span data-ttu-id="8ba10-151">指定將在容錯移轉之後作為 recvcovery VM 的主要 NIC 使用的 NIC。</span><span class="sxs-lookup"><span data-stu-id="8ba10-151">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="8ba10-152">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8ba10-152">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="8ba10-153">容錯移轉之後，已針對複製受保護的專案進行可用性設定。</span><span class="sxs-lookup"><span data-stu-id="8ba10-153">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="8ba10-154">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8ba10-154">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="8ba10-155">指定用於恢復 azure VM 的啟動診斷的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="8ba10-155">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="8ba10-156">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="8ba10-156">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="8ba10-157">要將此虛擬機器容錯移轉至其中的復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ba10-157">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="8ba10-158">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8ba10-158">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="8ba10-159">指定要與恢復 NIC 相關聯的目標後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="8ba10-159">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="8ba10-160">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="8ba10-160">-RecoveryNetworkId</span></span>
<span data-ttu-id="8ba10-161">指定受保護專案應針對其進行容錯移轉之 Azure 虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ba10-161">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="8ba10-162">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8ba10-162">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="8ba10-163">指定要與恢復 NIC 相關聯之網路安全性群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ba10-163">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="8ba10-164">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="8ba10-164">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="8ba10-165">指定在恢復時應該指派給主要 NIC 的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8ba10-165">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="8ba10-166">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="8ba10-166">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="8ba10-167">指定要在容錯移轉時，將受保護之專案的這個 NIC 連線至之 [復原] Azure 虛擬網路上的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="8ba10-167">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="8ba10-168">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="8ba10-168">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="8ba10-169">指定要與恢復 NIC 相關聯之公用 IP 位址資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ba10-169">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="8ba10-170">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8ba10-170">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="8ba10-171">修復區域中的 Azure 資源群組的識別碼，受保護的專案將會在容錯移轉時復原。</span><span class="sxs-lookup"><span data-stu-id="8ba10-171">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="8ba10-172">-大小</span><span class="sxs-lookup"><span data-stu-id="8ba10-172">-Size</span></span>
<span data-ttu-id="8ba10-173">指定復原虛擬電腦大小。</span><span class="sxs-lookup"><span data-stu-id="8ba10-173">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="8ba10-174">此值應該是由 Azure 虛擬機器支援的大小集合所組成。</span><span class="sxs-lookup"><span data-stu-id="8ba10-174">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="8ba10-175">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="8ba10-175">-TfoAzureVMName</span></span>
<span data-ttu-id="8ba10-176">指定測試容錯移轉 VM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ba10-176">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="8ba10-177">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="8ba10-177">-UpdateNic</span></span>
<span data-ttu-id="8ba10-178">指定此 Cmdlet 設定恢復網路屬性需要 udpated 之虛擬機器的 NIC。</span><span class="sxs-lookup"><span data-stu-id="8ba10-178">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="8ba10-179">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8ba10-179">-UseManagedDisk</span></span>
<span data-ttu-id="8ba10-180">指定在容錯移轉中建立的 Azure 虛擬機器是否應使用受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="8ba10-180">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="8ba10-181">-確認</span><span class="sxs-lookup"><span data-stu-id="8ba10-181">-Confirm</span></span>
<span data-ttu-id="8ba10-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ba10-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba10-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba10-183">-WhatIf</span></span>
<span data-ttu-id="8ba10-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ba10-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ba10-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ba10-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba10-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba10-186">CommonParameters</span></span>
<span data-ttu-id="8ba10-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ba10-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba10-188">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8ba10-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba10-189">輸入</span><span class="sxs-lookup"><span data-stu-id="8ba10-189">INPUTS</span></span>

### <span data-ttu-id="8ba10-190">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ba10-190">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8ba10-191">輸出</span><span class="sxs-lookup"><span data-stu-id="8ba10-191">OUTPUTS</span></span>

### <span data-ttu-id="8ba10-192">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8ba10-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8ba10-193">筆記</span><span class="sxs-lookup"><span data-stu-id="8ba10-193">NOTES</span></span>

## <span data-ttu-id="8ba10-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ba10-194">RELATED LINKS</span></span>

[<span data-ttu-id="8ba10-195">AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ba10-195">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="8ba10-196">新-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ba10-196">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="8ba10-197">移除-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ba10-197">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
