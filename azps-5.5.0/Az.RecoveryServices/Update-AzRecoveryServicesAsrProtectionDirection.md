---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130946"
---
# <span data-ttu-id="c7863-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="c7863-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="c7863-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7863-102">SYNOPSIS</span></span>
<span data-ttu-id="c7863-103">更新指定的複製受保護專案或復原方案的複製方向。</span><span class="sxs-lookup"><span data-stu-id="c7863-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="c7863-104">用來重新保護/反向複製失敗的複製專案或復原方案。</span><span class="sxs-lookup"><span data-stu-id="c7863-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="c7863-105">句法</span><span class="sxs-lookup"><span data-stu-id="c7863-105">SYNTAX</span></span>

### <span data-ttu-id="c7863-106">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="c7863-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7863-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="c7863-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7863-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="c7863-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7863-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="c7863-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7863-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c7863-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7863-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c7863-111">AzureToAzure</span></span>
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

### <span data-ttu-id="c7863-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7863-112">AzureToAzureWithMultipleStorageAccount</span></span>
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

### <span data-ttu-id="c7863-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c7863-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7863-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="c7863-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7863-115">說明</span><span class="sxs-lookup"><span data-stu-id="c7863-115">DESCRIPTION</span></span>
<span data-ttu-id="c7863-116">**AzRecoveryServicesAsrProtectionDirection** Cmdlet 會在完成認可式容錯移轉作業之後，更新指定 Azure Site Recovery 物件的複製方向。</span><span class="sxs-lookup"><span data-stu-id="c7863-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="c7863-117">示例</span><span class="sxs-lookup"><span data-stu-id="c7863-117">EXAMPLES</span></span>

### <span data-ttu-id="c7863-118">範例1</span><span class="sxs-lookup"><span data-stu-id="c7863-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="c7863-119">針對指定的復原方案啟動更新方向作業，並傳回用於追蹤作業的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="c7863-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="c7863-120">範例2</span><span class="sxs-lookup"><span data-stu-id="c7863-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="c7863-121">在目標 azure 區域中由保護容器對應所定義的特定複製受保護專案，並在與 VM) 相同地區中使用快取儲存空間 (，啟動更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="c7863-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="c7863-122">範例3</span><span class="sxs-lookup"><span data-stu-id="c7863-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="c7863-123">針對由保護容器對應的目標 azure 區域中指定的受保護專案及提供磁碟複製設定，啟動更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="c7863-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="c7863-124">範例4</span><span class="sxs-lookup"><span data-stu-id="c7863-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="c7863-125">針對由保護容器對應的目標 azure 區域中指定的加密複製受保護專案，以及提供磁碟複製設定，啟動更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="c7863-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="c7863-126">範例5</span><span class="sxs-lookup"><span data-stu-id="c7863-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="c7863-127">在目標 azure 區域中由保護容器對應所定義的特定複製受保護專案，以及使用 [快取儲存空間] 與 [VM) 與鄰近性位置] 群組中的 [快取] (，啟動更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="c7863-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="c7863-128">參數</span><span class="sxs-lookup"><span data-stu-id="c7863-128">PARAMETERS</span></span>

### <span data-ttu-id="c7863-129">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c7863-129">-Account</span></span>
<span data-ttu-id="c7863-130">要用來推入行動服務的 [執行方式] 帳戶（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="c7863-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="c7863-131">必須是在 ASR 結構中的 [作為帳戶執行方式] 清單中的一個。</span><span class="sxs-lookup"><span data-stu-id="c7863-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="c7863-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c7863-132">-AzureToAzure</span></span>
<span data-ttu-id="c7863-133">指定 Azure 到 Azure 災害復原。</span><span class="sxs-lookup"><span data-stu-id="c7863-133">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="c7863-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7863-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="c7863-135">指定災害復原的磁片設定。</span><span class="sxs-lookup"><span data-stu-id="c7863-135">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="c7863-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="c7863-136">-AzureToVMware</span></span>
<span data-ttu-id="c7863-137">指定 [從 azure 切換至 vMWare] 案例。</span><span class="sxs-lookup"><span data-stu-id="c7863-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="c7863-138">-資料存儲</span><span class="sxs-lookup"><span data-stu-id="c7863-138">-DataStore</span></span>
<span data-ttu-id="c7863-139">要用於 vmdisk 的 VMware 資料存放區。</span><span class="sxs-lookup"><span data-stu-id="c7863-139">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="c7863-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7863-140">-DefaultProfile</span></span>
<span data-ttu-id="c7863-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7863-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c7863-142">方向</span><span class="sxs-lookup"><span data-stu-id="c7863-142">-Direction</span></span>
<span data-ttu-id="c7863-143">指定要用於在容錯移轉後進行更新操作的方向。</span><span class="sxs-lookup"><span data-stu-id="c7863-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="c7863-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c7863-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7863-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="c7863-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="c7863-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="c7863-146">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="c7863-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="c7863-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="c7863-148">指定要在容錯移轉之後用來恢復 VM 之版本 (Azure 磁片加密) 的磁片加密機密 URL。</span><span class="sxs-lookup"><span data-stu-id="c7863-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="c7863-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="c7863-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="c7863-150">指定要在容錯移轉之後用來恢復 VM 的磁片加密秘密電子倉庫識別碼 (Azure 磁片加密) 。</span><span class="sxs-lookup"><span data-stu-id="c7863-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="c7863-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="c7863-151">-HyperVToAzure</span></span>
<span data-ttu-id="c7863-152">在回切之後，重新保護 Hyper-v 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c7863-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="c7863-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="c7863-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="c7863-154">指定要在容錯移轉之後用來恢復 VM (Azure 磁片加密) 的磁片加密金鑰 URL。</span><span class="sxs-lookup"><span data-stu-id="c7863-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="c7863-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="c7863-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="c7863-156">指定要在容錯移轉之後用來恢復 VM (Azure 磁片加密) 的磁片加密金鑰 keyVault ID。</span><span class="sxs-lookup"><span data-stu-id="c7863-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="c7863-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c7863-157">-LogStorageAccountId</span></span>
<span data-ttu-id="c7863-158">指定儲存空間帳戶識別碼以儲存 Vm 的複製記錄。</span><span class="sxs-lookup"><span data-stu-id="c7863-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="c7863-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="c7863-159">-MasterTarget</span></span>
<span data-ttu-id="c7863-160">主目標伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c7863-160">Master Target Server Details.</span></span>

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

### <span data-ttu-id="c7863-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="c7863-161">-ProcessServer</span></span>
<span data-ttu-id="c7863-162">要用於複製的進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="c7863-162">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="c7863-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c7863-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="c7863-164">要用於複製的保護 containerMapping。</span><span class="sxs-lookup"><span data-stu-id="c7863-164">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="c7863-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="c7863-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="c7863-166">應在容錯移轉時建立虛擬機器的可用性集</span><span class="sxs-lookup"><span data-stu-id="c7863-166">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="c7863-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c7863-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="c7863-168">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="c7863-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="c7863-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c7863-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="c7863-170">指定用於恢復 azure VM 的啟動診斷的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c7863-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="c7863-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="c7863-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="c7863-172">要將此虛擬機器容錯移轉至其中的復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7863-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="c7863-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c7863-173">-RecoveryPlan</span></span>
<span data-ttu-id="c7863-174">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="c7863-174">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="c7863-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="c7863-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="c7863-176">要將此虛擬機器容錯移轉至其中的 [恢復鄰近性] 位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7863-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="c7863-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="c7863-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="c7863-178">受保護的 Vm 的復原 resourceGroup id。</span><span class="sxs-lookup"><span data-stu-id="c7863-178">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="c7863-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c7863-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c7863-180">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="c7863-180">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="c7863-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="c7863-181">-RetentionVolume</span></span>
<span data-ttu-id="c7863-182">要使用的主目標伺服器上的保留音量。</span><span class="sxs-lookup"><span data-stu-id="c7863-182">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="c7863-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="c7863-183">-VmmToVmm</span></span>
<span data-ttu-id="c7863-184">針對在兩個 VMM 管理的 Hyper-v 網站之間受保護的 Hyper-v 虛擬機器，更新複製方向。</span><span class="sxs-lookup"><span data-stu-id="c7863-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="c7863-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="c7863-185">-VMwareToAzure</span></span>
<span data-ttu-id="c7863-186">更新從 VMware 到 Azure 的複製方向。</span><span class="sxs-lookup"><span data-stu-id="c7863-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="c7863-187">-確認</span><span class="sxs-lookup"><span data-stu-id="c7863-187">-Confirm</span></span>
<span data-ttu-id="c7863-188">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7863-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7863-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7863-189">-WhatIf</span></span>
<span data-ttu-id="c7863-190">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7863-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7863-191">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7863-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7863-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7863-192">CommonParameters</span></span>
<span data-ttu-id="c7863-193">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7863-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7863-194">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c7863-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7863-195">輸入</span><span class="sxs-lookup"><span data-stu-id="c7863-195">INPUTS</span></span>

### <span data-ttu-id="c7863-196">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c7863-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="c7863-197">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c7863-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c7863-198">輸出</span><span class="sxs-lookup"><span data-stu-id="c7863-198">OUTPUTS</span></span>

### <span data-ttu-id="c7863-199">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c7863-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c7863-200">筆記</span><span class="sxs-lookup"><span data-stu-id="c7863-200">NOTES</span></span>

## <span data-ttu-id="c7863-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7863-201">RELATED LINKS</span></span>
