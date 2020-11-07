---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fab7fa9f02f70b5afa1c4c5ffcbd07a8e1706998
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625007"
---
# <span data-ttu-id="5e164-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5e164-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="5e164-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e164-102">SYNOPSIS</span></span>
<span data-ttu-id="5e164-103">透過建立受禁止複製的專案，為 ASR 可保護的專案啟用複製。</span><span class="sxs-lookup"><span data-stu-id="5e164-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e164-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e164-104">SYNTAX</span></span>

### <span data-ttu-id="5e164-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="5e164-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e164-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="5e164-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e164-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="5e164-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e164-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="5e164-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e164-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="5e164-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e164-110">說明</span><span class="sxs-lookup"><span data-stu-id="5e164-110">DESCRIPTION</span></span>
<span data-ttu-id="5e164-111">**新的-AzureRmRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會建立新的受保護的複製專案。</span><span class="sxs-lookup"><span data-stu-id="5e164-111">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="5e164-112">使用此 Cmdlet 來啟用 ASR 可保護專案的複製。</span><span class="sxs-lookup"><span data-stu-id="5e164-112">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="5e164-113">示例</span><span class="sxs-lookup"><span data-stu-id="5e164-113">EXAMPLES</span></span>

### <span data-ttu-id="5e164-114">範例1</span><span class="sxs-lookup"><span data-stu-id="5e164-114">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="5e164-115">針對指定的 ASR 可保護專案啟動複製受保護的專案建立作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="5e164-115">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="5e164-116">範例2</span><span class="sxs-lookup"><span data-stu-id="5e164-116">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="5e164-117">針對指定的 ASR 可傳送專案啟動複製受保護的專案建立作業，並傳回用來追蹤作業 (vmWare 至 Azure 案例) 的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="5e164-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="5e164-118">範例3</span><span class="sxs-lookup"><span data-stu-id="5e164-118">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="5e164-119">針對指定的 ASR 可傳送專案啟動複製受保護的專案建立作業，並傳回用來追蹤作業的 ASR 作業， (Azure 到 Azure 案例) 。</span><span class="sxs-lookup"><span data-stu-id="5e164-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="5e164-120">範例4</span><span class="sxs-lookup"><span data-stu-id="5e164-120">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="5e164-121">針對指定的 VmId 啟動複製受保護的專案建立作業，並傳回用於追蹤作業 (Azure 到 Azure 案例) 的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="5e164-121">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="5e164-122">參數</span><span class="sxs-lookup"><span data-stu-id="5e164-122">PARAMETERS</span></span>

### <span data-ttu-id="5e164-123">-帳戶</span><span class="sxs-lookup"><span data-stu-id="5e164-123">-Account</span></span>
<span data-ttu-id="5e164-124">要用來推入行動服務的 [執行方式] 帳戶（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="5e164-124">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="5e164-125">必須是在 ASR 結構中的 [作為帳戶執行方式] 清單中的一個。</span><span class="sxs-lookup"><span data-stu-id="5e164-125">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="5e164-126">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="5e164-126">-AzureToAzure</span></span>
<span data-ttu-id="5e164-127">切換參數以指定複製的專案是 Azure 虛擬機器複製到復原 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="5e164-127">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-128">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e164-128">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="5e164-129">指定要複製的虛擬機器磁片清單，以及用來複製磁片的快取儲存空間帳戶和復原儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="5e164-129">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-130">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="5e164-130">-AzureVmId</span></span>
<span data-ttu-id="5e164-131">指定要複製的 azure vm id。</span><span class="sxs-lookup"><span data-stu-id="5e164-131">Specifies the azure vm id to be replicated.</span></span>

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

### <span data-ttu-id="5e164-132">-確認</span><span class="sxs-lookup"><span data-stu-id="5e164-132">-Confirm</span></span>
<span data-ttu-id="5e164-133">啟動作業前提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5e164-133">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="5e164-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e164-134">-DefaultProfile</span></span>
<span data-ttu-id="5e164-135">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e164-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="5e164-136">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="5e164-136">-HyperVToAzure</span></span>
<span data-ttu-id="5e164-137">切換參數以指定複製的專案是要複製到 Azure 的 Hyper-v 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5e164-137">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-138">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="5e164-138">-IncludeDiskId</span></span>
<span data-ttu-id="5e164-139">要納入複製的磁片清單。</span><span class="sxs-lookup"><span data-stu-id="5e164-139">The list of disks to include for replication.</span></span> <span data-ttu-id="5e164-140">根據預設，會包含所有磁片。</span><span class="sxs-lookup"><span data-stu-id="5e164-140">By default all disks are included.</span></span>

```yaml
Type: String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-141">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5e164-141">-LogStorageAccountId</span></span>
<span data-ttu-id="5e164-142">指定要用來儲存複製記錄的記錄或快取儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e164-142">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e164-143">-Name</span></span>
<span data-ttu-id="5e164-144">指定 ASR 複製受保護的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="5e164-144">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="5e164-145">該名稱在保存庫中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="5e164-145">The name must be unique within the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-146">-OS</span><span class="sxs-lookup"><span data-stu-id="5e164-146">-OS</span></span>
<span data-ttu-id="5e164-147">指定作業系統系列。</span><span class="sxs-lookup"><span data-stu-id="5e164-147">Specifies the operating system family.</span></span>
<span data-ttu-id="5e164-148">此參數可接受的值為： Windows 或 Linux。</span><span class="sxs-lookup"><span data-stu-id="5e164-148">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-149">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="5e164-149">-OSDiskName</span></span>
<span data-ttu-id="5e164-150">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e164-150">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="5e164-151">-ProcessServer</span></span>
<span data-ttu-id="5e164-152">要用來複製此電腦的進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="5e164-152">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="5e164-153">使用與佈建服務器相對應的 ASR 結構中的進程伺服器清單來指定它。</span><span class="sxs-lookup"><span data-stu-id="5e164-153">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-154">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5e164-154">-ProtectableItem</span></span>
<span data-ttu-id="5e164-155">指定要啟用複製的 ASR 可保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="5e164-155">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-156">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5e164-156">-ProtectionContainerMapping</span></span>
<span data-ttu-id="5e164-157">指定要用於複製之複製原則對應的 ASR 保護容器對應物件。</span><span class="sxs-lookup"><span data-stu-id="5e164-157">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-158">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="5e164-158">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="5e164-159">在發生容錯移轉時，要將電腦復原至其中的 AvailabilitySet 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e164-159">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-160">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="5e164-160">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="5e164-161">在容錯移轉事件時，要將電腦復原至其中的 Azure 虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e164-161">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-162">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5e164-162">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="5e164-163">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="5e164-163">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-164">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="5e164-164">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="5e164-165">在容錯移轉時，容錯移轉虛擬機器應附加到的復原 Azure 虛擬網路中的子網。</span><span class="sxs-lookup"><span data-stu-id="5e164-165">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-166">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="5e164-166">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="5e164-167">指定要將此虛擬機器容錯移轉至其中的復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e164-167">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-168">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="5e164-168">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="5e164-169">指定在容錯移轉事件中，將建立虛擬機器之資源群組的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e164-169">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-170">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="5e164-170">-RecoveryVmName</span></span>
<span data-ttu-id="5e164-171">在容錯移轉之後建立的復原 Vm 名稱。</span><span class="sxs-lookup"><span data-stu-id="5e164-171">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-172">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="5e164-172">-ReplicationGroupName</span></span>
<span data-ttu-id="5e164-173">指定要用來建立多 VM 一致復原點的複製組名。</span><span class="sxs-lookup"><span data-stu-id="5e164-173">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="5e164-174">根據預設，每個複製受保護的專案都會在自己的群組中建立，且不會產生多重 VM 一致的復原點。</span><span class="sxs-lookup"><span data-stu-id="5e164-174">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="5e164-175">只有在您需要將所有電腦保護到相同的複製群組時，才能使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="5e164-175">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-176">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="5e164-176">-VMwareToAzure</span></span>
<span data-ttu-id="5e164-177">切換參數以指定複製的專案是將會複製到 Azure 的 VMware 虛擬機器或物理伺服器。</span><span class="sxs-lookup"><span data-stu-id="5e164-177">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="5e164-178">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="5e164-178">-VmmToVmm</span></span>
<span data-ttu-id="5e164-179">切換參數以指定複製的專案是要在 VMM 管理的 Hyper-v 網站之間複製的 Hyper-v 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5e164-179">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-180">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5e164-180">-WaitForCompletion</span></span>
<span data-ttu-id="5e164-181">指定在傳回前，該指令應等待完成操作。</span><span class="sxs-lookup"><span data-stu-id="5e164-181">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e164-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e164-182">-WhatIf</span></span>
<span data-ttu-id="5e164-183">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e164-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e164-184">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e164-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e164-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e164-185">CommonParameters</span></span>
<span data-ttu-id="5e164-186">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e164-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e164-187">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e164-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e164-188">輸入</span><span class="sxs-lookup"><span data-stu-id="5e164-188">INPUTS</span></span>

### <span data-ttu-id="5e164-189">RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5e164-189">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="5e164-190">輸出</span><span class="sxs-lookup"><span data-stu-id="5e164-190">OUTPUTS</span></span>

### <span data-ttu-id="5e164-191">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5e164-191">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5e164-192">筆記</span><span class="sxs-lookup"><span data-stu-id="5e164-192">NOTES</span></span>

## <span data-ttu-id="5e164-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e164-193">RELATED LINKS</span></span>

[<span data-ttu-id="5e164-194">AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5e164-194">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="5e164-195">移除-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5e164-195">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="5e164-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5e164-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
