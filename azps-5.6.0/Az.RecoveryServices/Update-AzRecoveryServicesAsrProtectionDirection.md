---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: c6e25b9b8ec7fe22f76ccec954312914af8dd53e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911865"
---
# <span data-ttu-id="32816-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="32816-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="32816-102">簡介</span><span class="sxs-lookup"><span data-stu-id="32816-102">SYNOPSIS</span></span>
<span data-ttu-id="32816-103">更新指定複本受保護的專案或復原計畫的複本方向。</span><span class="sxs-lookup"><span data-stu-id="32816-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="32816-104">用來重新保護/反向複製已複製的專案或復原計畫失敗。</span><span class="sxs-lookup"><span data-stu-id="32816-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="32816-105">語法</span><span class="sxs-lookup"><span data-stu-id="32816-105">SYNTAX</span></span>

### <span data-ttu-id="32816-106">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="32816-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32816-107">AzureToVPv</span><span class="sxs-lookup"><span data-stu-id="32816-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32816-108">VAzToAzure</span><span class="sxs-lookup"><span data-stu-id="32816-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32816-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="32816-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32816-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="32816-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32816-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="32816-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32816-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="32816-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32816-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="32816-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32816-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="32816-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32816-115">描述</span><span class="sxs-lookup"><span data-stu-id="32816-115">DESCRIPTION</span></span>
<span data-ttu-id="32816-116">完成 **提交容錯移轉作業後，Update-AzRecoveryServicesrProtectionDirection** Cmdlet 會更新指定 Azure 網站修復物件的複本方向。</span><span class="sxs-lookup"><span data-stu-id="32816-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="32816-117">例子</span><span class="sxs-lookup"><span data-stu-id="32816-117">EXAMPLES</span></span>

### <span data-ttu-id="32816-118">範例 1</span><span class="sxs-lookup"><span data-stu-id="32816-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="32816-119">為指定的復原計畫啟動更新方向作業，並返回用來追蹤作業的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="32816-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="32816-120">範例 2</span><span class="sxs-lookup"><span data-stu-id="32816-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="32816-121">在目標 Azure 地區中，針對保護容器的映射和使用與 VM (相同的區域使用快 (定義的指定複製受保護的專案，開始更新方向) 。</span><span class="sxs-lookup"><span data-stu-id="32816-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="32816-122">範例 3</span><span class="sxs-lookup"><span data-stu-id="32816-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="32816-123">針對由保護容器映射和提供的磁碟複製組定所定義之目標 Azure 區域指定複製受保護的專案，開始更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="32816-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="32816-124">範例 4</span><span class="sxs-lookup"><span data-stu-id="32816-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="32816-125">針對由保護容器地圖和提供的磁碟複製組定所定義之目標 Azure 區域指定的加密複製受保護的專案，開始更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="32816-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="32816-126">範例 5</span><span class="sxs-lookup"><span data-stu-id="32816-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="32816-127">在目標 Azure 區域，針對由保護容器映射和使用快件儲存空間 (在與 VM) 和鄰近位置群組相同的地區中定義之指定複製受保護的專案，開始更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="32816-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="32816-128">參數</span><span class="sxs-lookup"><span data-stu-id="32816-128">PARAMETERS</span></span>

### <span data-ttu-id="32816-129">-帳戶</span><span class="sxs-lookup"><span data-stu-id="32816-129">-Account</span></span>
<span data-ttu-id="32816-130">需要時，以帳戶執行以推入安裝行動服務。</span><span class="sxs-lookup"><span data-stu-id="32816-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="32816-131">必須是 ASR 結構中以帳戶執行清單中的帳戶。</span><span class="sxs-lookup"><span data-stu-id="32816-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="32816-132">-AzureToAzure</span></span>
<span data-ttu-id="32816-133">指定 Azure 到 Azure 的災害復原。</span><span class="sxs-lookup"><span data-stu-id="32816-133">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-134">-AzureToAzureAzlicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="32816-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="32816-135">指定復原的磁片組。</span><span class="sxs-lookup"><span data-stu-id="32816-135">Specifies the disk configuration for disaster recovery.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-136">-AzureToVPv</span><span class="sxs-lookup"><span data-stu-id="32816-136">-AzureToVMware</span></span>
<span data-ttu-id="32816-137">指定 Azure 切換到 vMWare 案例。</span><span class="sxs-lookup"><span data-stu-id="32816-137">Specifies the switch azure to vMWare scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="32816-138">-DataStore</span></span>
<span data-ttu-id="32816-139">要用於 vm一代的 V市資料存放區。</span><span class="sxs-lookup"><span data-stu-id="32816-139">The VMware data-store to be used for the vmdisk's.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32816-140">-DefaultProfile</span></span>
<span data-ttu-id="32816-141">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="32816-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="32816-142">-方向</span><span class="sxs-lookup"><span data-stu-id="32816-142">-Direction</span></span>
<span data-ttu-id="32816-143">指定容錯移轉後更新作業使用的方向。</span><span class="sxs-lookup"><span data-stu-id="32816-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="32816-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="32816-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="32816-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="32816-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="32816-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="32816-146">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="32816-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="32816-148">指定具有版本 (Azure 磁片加密的磁片加密) 容錯移轉後要用於復原 VM。</span><span class="sxs-lookup"><span data-stu-id="32816-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="32816-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="32816-150">指定 Azure 磁片加密的磁片加密 (密碼庫識別碼) 容錯移轉後要用於復原 VM。</span><span class="sxs-lookup"><span data-stu-id="32816-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="32816-151">-HyperVToAzure</span></span>
<span data-ttu-id="32816-152">在容錯移轉之後重新保護 Hyper-V 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="32816-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="32816-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="32816-154">指定 Azure 磁片加密 (的磁片加密金鑰 URL，) 容錯移轉後用來做為修復 VM。</span><span class="sxs-lookup"><span data-stu-id="32816-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="32816-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="32816-156">指定 Azure 磁片加密的磁片 (金鑰金鑰 Vault 識別碼) 容錯移轉後要用於復原 VM。</span><span class="sxs-lookup"><span data-stu-id="32816-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="32816-157">-LogStorageAccountId</span></span>
<span data-ttu-id="32816-158">指定儲存帳戶識別碼以儲存虛擬機器的複製記錄。</span><span class="sxs-lookup"><span data-stu-id="32816-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="32816-159">-MasterTarget</span></span>
<span data-ttu-id="32816-160">主目標伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="32816-160">Master Target Server Details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="32816-161">-ProcessServer</span></span>
<span data-ttu-id="32816-162">要用於複製的 Process Server。</span><span class="sxs-lookup"><span data-stu-id="32816-162">Process Server to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="32816-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="32816-164">要用於複製的保護容器Mapping。</span><span class="sxs-lookup"><span data-stu-id="32816-164">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="32816-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="32816-166">容錯移轉時應建立虛擬機器的可用性集</span><span class="sxs-lookup"><span data-stu-id="32816-166">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="32816-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="32816-168">指定要複製到的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="32816-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="32816-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="32816-170">指定用於修復 Azure VM 之開機診斷的儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="32816-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="32816-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="32816-172">要容錯移轉到此虛擬機器之復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="32816-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="32816-173">-RecoveryPlan</span></span>
<span data-ttu-id="32816-174">指定 ASR 復原計畫物件。</span><span class="sxs-lookup"><span data-stu-id="32816-174">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32816-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="32816-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="32816-176">要容錯移轉此虛擬機器之復原鄰近位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="32816-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="32816-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="32816-178">受保護 Vm 的復原資源組識別碼。</span><span class="sxs-lookup"><span data-stu-id="32816-178">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="32816-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="32816-180">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="32816-180">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32816-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="32816-181">-RetentionVolume</span></span>
<span data-ttu-id="32816-182">要使用的主目標伺服器的保留音量。</span><span class="sxs-lookup"><span data-stu-id="32816-182">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="32816-183">-VmmToVmm</span></span>
<span data-ttu-id="32816-184">在兩個 VMM 受管理的 Hyper-V 網站之間保護的 Hyper-V 虛擬機器上失敗的更新複製方向。</span><span class="sxs-lookup"><span data-stu-id="32816-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-185">-VAzToAzure</span><span class="sxs-lookup"><span data-stu-id="32816-185">-VMwareToAzure</span></span>
<span data-ttu-id="32816-186">將 VAz 的複製方向更新為 Azure。</span><span class="sxs-lookup"><span data-stu-id="32816-186">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32816-187">-確認</span><span class="sxs-lookup"><span data-stu-id="32816-187">-Confirm</span></span>
<span data-ttu-id="32816-188">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="32816-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32816-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32816-189">-WhatIf</span></span>
<span data-ttu-id="32816-190">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32816-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32816-191">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32816-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32816-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32816-192">CommonParameters</span></span>
<span data-ttu-id="32816-193">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="32816-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32816-194">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32816-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32816-195">輸入</span><span class="sxs-lookup"><span data-stu-id="32816-195">INPUTS</span></span>

### <span data-ttu-id="32816-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="32816-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="32816-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="32816-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="32816-198">輸出</span><span class="sxs-lookup"><span data-stu-id="32816-198">OUTPUTS</span></span>

### <span data-ttu-id="32816-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="32816-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="32816-200">筆記</span><span class="sxs-lookup"><span data-stu-id="32816-200">NOTES</span></span>

## <span data-ttu-id="32816-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="32816-201">RELATED LINKS</span></span>
