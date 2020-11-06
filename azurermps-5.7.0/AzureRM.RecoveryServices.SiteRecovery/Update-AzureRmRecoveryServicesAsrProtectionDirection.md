---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 13d1829326695e2860caf99bf002dcf5da31caac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446055"
---
# <span data-ttu-id="ccaca-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="ccaca-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="ccaca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ccaca-102">SYNOPSIS</span></span>
<span data-ttu-id="ccaca-103">更新指定的複製受保護專案或復原方案的複製方向。</span><span class="sxs-lookup"><span data-stu-id="ccaca-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="ccaca-104">用來重新保護/反向複製失敗的複製專案或復原方案。</span><span class="sxs-lookup"><span data-stu-id="ccaca-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccaca-105">句法</span><span class="sxs-lookup"><span data-stu-id="ccaca-105">SYNTAX</span></span>

### <span data-ttu-id="ccaca-106">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="ccaca-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaca-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="ccaca-107">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccaca-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="ccaca-108">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaca-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="ccaca-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaca-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ccaca-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaca-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="ccaca-111">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaca-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ccaca-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaca-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ccaca-113">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaca-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="ccaca-114">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccaca-115">說明</span><span class="sxs-lookup"><span data-stu-id="ccaca-115">DESCRIPTION</span></span>
<span data-ttu-id="ccaca-116">**AzureRmRecoveryServicesAsrProtectionDirection** Cmdlet 會在完成認可式容錯移轉作業之後，更新指定 Azure Site Recovery 物件的複製方向。</span><span class="sxs-lookup"><span data-stu-id="ccaca-116">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="ccaca-117">示例</span><span class="sxs-lookup"><span data-stu-id="ccaca-117">EXAMPLES</span></span>

### <span data-ttu-id="ccaca-118">範例1</span><span class="sxs-lookup"><span data-stu-id="ccaca-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="ccaca-119">針對指定的復原方案啟動更新方向作業，並傳回用於追蹤作業的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="ccaca-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="ccaca-120">範例2</span><span class="sxs-lookup"><span data-stu-id="ccaca-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="ccaca-121">在目標 azure 區域中由保護容器對應所定義的特定複製受保護專案，並在與 VM) 相同地區中使用快取儲存空間 (，啟動更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="ccaca-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="ccaca-122">範例3</span><span class="sxs-lookup"><span data-stu-id="ccaca-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="ccaca-123">針對由保護容器對應的目標 azure 區域中指定的受保護專案及提供磁碟複製設定，啟動更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="ccaca-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="ccaca-124">參數</span><span class="sxs-lookup"><span data-stu-id="ccaca-124">PARAMETERS</span></span>

### <span data-ttu-id="ccaca-125">-帳戶</span><span class="sxs-lookup"><span data-stu-id="ccaca-125">-Account</span></span>
<span data-ttu-id="ccaca-126">要用來推入行動服務的 [執行方式] 帳戶（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="ccaca-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="ccaca-127">必須是在 ASR 結構中的 [作為帳戶執行方式] 清單中的一個。</span><span class="sxs-lookup"><span data-stu-id="ccaca-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="ccaca-128">-AzureToAzure</span></span>
<span data-ttu-id="ccaca-129">用於指定在兩個 Azure 區域之間的複製 Azure 虛擬機器更新之複製方向的切換參數。</span><span class="sxs-lookup"><span data-stu-id="ccaca-129">Switch parameter specifying that the replication direction being updated for replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="ccaca-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="ccaca-131">指定要複製的虛擬機器磁片清單，以及用來複製磁片的快取儲存空間帳戶和復原儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ccaca-131">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="ccaca-132">-AzureToVMware</span></span>
<span data-ttu-id="ccaca-133">更新從 Azure 到 Vmware 的複製方向。</span><span class="sxs-lookup"><span data-stu-id="ccaca-133">Update replication direction from Azure to Vmware.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-134">-確認</span><span class="sxs-lookup"><span data-stu-id="ccaca-134">-Confirm</span></span>
<span data-ttu-id="ccaca-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ccaca-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-136">-資料存儲</span><span class="sxs-lookup"><span data-stu-id="ccaca-136">-DataStore</span></span>
<span data-ttu-id="ccaca-137">要用於 vmdisk 的 VMware 資料存儲。</span><span class="sxs-lookup"><span data-stu-id="ccaca-137">The VMware datastore to be used for the vmdisk's.</span></span>

```yaml
Type: ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccaca-138">-DefaultProfile</span></span>
<span data-ttu-id="ccaca-139">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ccaca-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-140">方向</span><span class="sxs-lookup"><span data-stu-id="ccaca-140">-Direction</span></span>
<span data-ttu-id="ccaca-141">指定要用於在容錯移轉後進行更新操作的方向。</span><span class="sxs-lookup"><span data-stu-id="ccaca-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="ccaca-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ccaca-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ccaca-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ccaca-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="ccaca-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ccaca-144">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-145">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="ccaca-145">-HyperVToAzure</span></span>
<span data-ttu-id="ccaca-146">在回切之後，重新保護 Hyper-v 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ccaca-146">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-147">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ccaca-147">-LogStorageAccountId</span></span>
<span data-ttu-id="ccaca-148">指定儲存空間帳戶識別碼以儲存 Vm 的複製記錄。</span><span class="sxs-lookup"><span data-stu-id="ccaca-148">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-149">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="ccaca-149">-MasterTarget</span></span>
<span data-ttu-id="ccaca-150">主目標伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ccaca-150">Master Target Server Details.</span></span>

```yaml
Type: ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="ccaca-151">-ProcessServer</span></span>
<span data-ttu-id="ccaca-152">要用於複製的進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="ccaca-152">Process Server to be used for replication.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-153">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ccaca-153">-ProtectionContainerMapping</span></span>
<span data-ttu-id="ccaca-154">要用於複製的保護 containerMapping。</span><span class="sxs-lookup"><span data-stu-id="ccaca-154">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-155">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="ccaca-155">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="ccaca-156">應在容錯移轉時建立虛擬機器的可用性集</span><span class="sxs-lookup"><span data-stu-id="ccaca-156">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-157">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ccaca-157">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="ccaca-158">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="ccaca-158">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="ccaca-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="ccaca-160">要將此虛擬機器容錯移轉至其中的復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ccaca-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ccaca-161">-RecoveryPlan</span></span>
<span data-ttu-id="ccaca-162">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="ccaca-162">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="ccaca-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="ccaca-164">受保護的 Vm 的復原 resourceGroup id。</span><span class="sxs-lookup"><span data-stu-id="ccaca-164">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ccaca-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ccaca-166">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="ccaca-166">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="ccaca-167">-RetentionVolume</span></span>
<span data-ttu-id="ccaca-168">要使用的主目標伺服器上的保留音量。</span><span class="sxs-lookup"><span data-stu-id="ccaca-168">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-169">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="ccaca-169">-VMwareToAzure</span></span>
<span data-ttu-id="ccaca-170">更新從 VMware 到 Azure 的複製方向。</span><span class="sxs-lookup"><span data-stu-id="ccaca-170">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="ccaca-171">-VmmToVmm</span></span>
<span data-ttu-id="ccaca-172">針對在兩個 VMM 管理的 Hyper-v 網站之間受保護的 Hyper-v 虛擬機器，更新複製方向。</span><span class="sxs-lookup"><span data-stu-id="ccaca-172">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccaca-173">-WhatIf</span></span>
<span data-ttu-id="ccaca-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ccaca-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccaca-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccaca-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaca-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccaca-176">CommonParameters</span></span>
<span data-ttu-id="ccaca-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ccaca-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccaca-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ccaca-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccaca-179">輸入</span><span class="sxs-lookup"><span data-stu-id="ccaca-179">INPUTS</span></span>

### <span data-ttu-id="ccaca-180">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ccaca-180">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="ccaca-181">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ccaca-181">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ccaca-182">輸出</span><span class="sxs-lookup"><span data-stu-id="ccaca-182">OUTPUTS</span></span>

### <span data-ttu-id="ccaca-183">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ccaca-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ccaca-184">筆記</span><span class="sxs-lookup"><span data-stu-id="ccaca-184">NOTES</span></span>

## <span data-ttu-id="ccaca-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccaca-185">RELATED LINKS</span></span>
