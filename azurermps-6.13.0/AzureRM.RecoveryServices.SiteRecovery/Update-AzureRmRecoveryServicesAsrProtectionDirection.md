---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 48647fcc0382dd23f012d64aa70af364355c60e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623541"
---
# <span data-ttu-id="21000-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="21000-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="21000-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21000-102">SYNOPSIS</span></span>
<span data-ttu-id="21000-103">更新指定的複製受保護專案或復原方案的複製方向。</span><span class="sxs-lookup"><span data-stu-id="21000-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="21000-104">用來重新保護/反向複製失敗的複製專案或復原方案。</span><span class="sxs-lookup"><span data-stu-id="21000-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21000-105">句法</span><span class="sxs-lookup"><span data-stu-id="21000-105">SYNTAX</span></span>

### <span data-ttu-id="21000-106">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="21000-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21000-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="21000-107">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21000-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="21000-108">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21000-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="21000-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21000-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="21000-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21000-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="21000-111">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21000-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="21000-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21000-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="21000-113">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21000-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="21000-114">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21000-115">說明</span><span class="sxs-lookup"><span data-stu-id="21000-115">DESCRIPTION</span></span>
<span data-ttu-id="21000-116">**AzureRmRecoveryServicesAsrProtectionDirection** Cmdlet 會在完成認可式容錯移轉作業之後，更新指定 Azure Site Recovery 物件的複製方向。</span><span class="sxs-lookup"><span data-stu-id="21000-116">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="21000-117">示例</span><span class="sxs-lookup"><span data-stu-id="21000-117">EXAMPLES</span></span>

### <span data-ttu-id="21000-118">範例1</span><span class="sxs-lookup"><span data-stu-id="21000-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="21000-119">針對指定的復原方案啟動更新方向作業，並傳回用於追蹤作業的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="21000-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="21000-120">範例2</span><span class="sxs-lookup"><span data-stu-id="21000-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="21000-121">在目標 azure 區域中由保護容器對應所定義的特定複製受保護專案，並在與 VM) 相同地區中使用快取儲存空間 (，啟動更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="21000-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="21000-122">範例3</span><span class="sxs-lookup"><span data-stu-id="21000-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="21000-123">針對由保護容器對應的目標 azure 區域中指定的受保護專案及提供磁碟複製設定，啟動更新方向作業。</span><span class="sxs-lookup"><span data-stu-id="21000-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="21000-124">參數</span><span class="sxs-lookup"><span data-stu-id="21000-124">PARAMETERS</span></span>

### <span data-ttu-id="21000-125">-帳戶</span><span class="sxs-lookup"><span data-stu-id="21000-125">-Account</span></span>
<span data-ttu-id="21000-126">要用來推入行動服務的 [執行方式] 帳戶（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="21000-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="21000-127">必須是在 ASR 結構中的 [作為帳戶執行方式] 清單中的一個。</span><span class="sxs-lookup"><span data-stu-id="21000-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="21000-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="21000-128">-AzureToAzure</span></span>
<span data-ttu-id="21000-129">用於指定在兩個 Azure 區域之間的複製 Azure 虛擬機器更新之複製方向的切換參數。</span><span class="sxs-lookup"><span data-stu-id="21000-129">Switch parameter specifying that the replication direction being updated for replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="21000-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="21000-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="21000-131">指定要複製的虛擬機器磁片清單，以及用來複製磁片的快取儲存空間帳戶和復原儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="21000-131">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

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

### <span data-ttu-id="21000-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="21000-132">-AzureToVMware</span></span>
<span data-ttu-id="21000-133">更新從 Azure 到 Vmware 的複製方向。</span><span class="sxs-lookup"><span data-stu-id="21000-133">Update replication direction from Azure to Vmware.</span></span>

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

### <span data-ttu-id="21000-134">-資料存儲</span><span class="sxs-lookup"><span data-stu-id="21000-134">-DataStore</span></span>
<span data-ttu-id="21000-135">要用於 vmdisk 的 VMware 資料存儲。</span><span class="sxs-lookup"><span data-stu-id="21000-135">The VMware datastore to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="21000-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21000-136">-DefaultProfile</span></span>
<span data-ttu-id="21000-137">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21000-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21000-138">方向</span><span class="sxs-lookup"><span data-stu-id="21000-138">-Direction</span></span>
<span data-ttu-id="21000-139">指定要用於在容錯移轉後進行更新操作的方向。</span><span class="sxs-lookup"><span data-stu-id="21000-139">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="21000-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="21000-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21000-141">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="21000-141">PrimaryToRecovery</span></span>
- <span data-ttu-id="21000-142">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="21000-142">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="21000-143">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="21000-143">-HyperVToAzure</span></span>
<span data-ttu-id="21000-144">在回切之後，重新保護 Hyper-v 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="21000-144">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="21000-145">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="21000-145">-LogStorageAccountId</span></span>
<span data-ttu-id="21000-146">指定儲存空間帳戶識別碼以儲存 Vm 的複製記錄。</span><span class="sxs-lookup"><span data-stu-id="21000-146">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="21000-147">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="21000-147">-MasterTarget</span></span>
<span data-ttu-id="21000-148">主目標伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="21000-148">Master Target Server Details.</span></span>

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

### <span data-ttu-id="21000-149">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="21000-149">-ProcessServer</span></span>
<span data-ttu-id="21000-150">要用於複製的進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="21000-150">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="21000-151">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="21000-151">-ProtectionContainerMapping</span></span>
<span data-ttu-id="21000-152">要用於複製的保護 containerMapping。</span><span class="sxs-lookup"><span data-stu-id="21000-152">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="21000-153">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="21000-153">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="21000-154">應在容錯移轉時建立虛擬機器的可用性集</span><span class="sxs-lookup"><span data-stu-id="21000-154">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="21000-155">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="21000-155">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="21000-156">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="21000-156">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="21000-157">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="21000-157">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="21000-158">指定用於恢復 azure VM 的啟動診斷的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="21000-158">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="21000-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="21000-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="21000-160">要將此虛擬機器容錯移轉至其中的復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="21000-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="21000-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21000-161">-RecoveryPlan</span></span>
<span data-ttu-id="21000-162">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="21000-162">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="21000-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="21000-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="21000-164">受保護的 Vm 的復原 resourceGroup id。</span><span class="sxs-lookup"><span data-stu-id="21000-164">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="21000-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="21000-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="21000-166">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="21000-166">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="21000-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="21000-167">-RetentionVolume</span></span>
<span data-ttu-id="21000-168">要使用的主目標伺服器上的保留音量。</span><span class="sxs-lookup"><span data-stu-id="21000-168">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="21000-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="21000-169">-VmmToVmm</span></span>
<span data-ttu-id="21000-170">針對在兩個 VMM 管理的 Hyper-v 網站之間受保護的 Hyper-v 虛擬機器，更新複製方向。</span><span class="sxs-lookup"><span data-stu-id="21000-170">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="21000-171">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="21000-171">-VMwareToAzure</span></span>
<span data-ttu-id="21000-172">更新從 VMware 到 Azure 的複製方向。</span><span class="sxs-lookup"><span data-stu-id="21000-172">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="21000-173">-確認</span><span class="sxs-lookup"><span data-stu-id="21000-173">-Confirm</span></span>
<span data-ttu-id="21000-174">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21000-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21000-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21000-175">-WhatIf</span></span>
<span data-ttu-id="21000-176">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21000-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21000-177">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21000-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21000-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21000-178">CommonParameters</span></span>
<span data-ttu-id="21000-179">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21000-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21000-180">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21000-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21000-181">輸入</span><span class="sxs-lookup"><span data-stu-id="21000-181">INPUTS</span></span>

### <span data-ttu-id="21000-182">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21000-182">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="21000-183">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="21000-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="21000-184">輸出</span><span class="sxs-lookup"><span data-stu-id="21000-184">OUTPUTS</span></span>

### <span data-ttu-id="21000-185">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="21000-185">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="21000-186">筆記</span><span class="sxs-lookup"><span data-stu-id="21000-186">NOTES</span></span>

## <span data-ttu-id="21000-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="21000-187">RELATED LINKS</span></span>
