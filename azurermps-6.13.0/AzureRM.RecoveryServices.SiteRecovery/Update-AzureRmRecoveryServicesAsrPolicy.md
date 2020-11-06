---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 805e421aedbb06b6f9a821b3f575b8a5035c86d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445523"
---
# <span data-ttu-id="da1d4-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="da1d4-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="da1d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da1d4-102">SYNOPSIS</span></span>
<span data-ttu-id="da1d4-103">更新 Azure 網站恢復複製原則。</span><span class="sxs-lookup"><span data-stu-id="da1d4-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da1d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="da1d4-104">SYNTAX</span></span>

### <span data-ttu-id="da1d4-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="da1d4-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1d4-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="da1d4-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1d4-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="da1d4-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da1d4-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="da1d4-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1d4-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="da1d4-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1d4-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="da1d4-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da1d4-111">說明</span><span class="sxs-lookup"><span data-stu-id="da1d4-111">DESCRIPTION</span></span>
<span data-ttu-id="da1d4-112">**AzureRmRecoveryServicesAsrPolicy** Cmdlet 會更新指定的 Azure Site Recovery 複製原則。</span><span class="sxs-lookup"><span data-stu-id="da1d4-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="da1d4-113">示例</span><span class="sxs-lookup"><span data-stu-id="da1d4-113">EXAMPLES</span></span>

### <span data-ttu-id="da1d4-114">範例1</span><span class="sxs-lookup"><span data-stu-id="da1d4-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="da1d4-115">使用指定的參數啟動更新複製原則作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="da1d4-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="da1d4-116">範例2</span><span class="sxs-lookup"><span data-stu-id="da1d4-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="da1d4-117">使用指定的參數開始將 azure to azure 複製原則作業更新，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="da1d4-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="da1d4-118">範例3</span><span class="sxs-lookup"><span data-stu-id="da1d4-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="da1d4-119">使用指定的參數開始將 azure 更新到 azure 複製原則，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="da1d4-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="da1d4-120">參數</span><span class="sxs-lookup"><span data-stu-id="da1d4-120">PARAMETERS</span></span>

### <span data-ttu-id="da1d4-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="da1d4-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="da1d4-122">指定要建立應用程式一致復原點的頻率 (，單位為小時) 。</span><span class="sxs-lookup"><span data-stu-id="da1d4-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-123">-驗證</span><span class="sxs-lookup"><span data-stu-id="da1d4-123">-Authentication</span></span>
<span data-ttu-id="da1d4-124">指定所使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="da1d4-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="da1d4-125">-AzureToAzure</span></span>
<span data-ttu-id="da1d4-126">[切換參數] 指定用於在兩個 Azure 區域之間複製 Azure 虛擬機器的複製原則將會更新。</span><span class="sxs-lookup"><span data-stu-id="da1d4-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="da1d4-127">-AzureToVMware</span></span>
<span data-ttu-id="da1d4-128">[切換] 參數指出所代表的原則是用來將在 Azure 中執行的虛擬機器複製容錯移轉回內部部署的 VMware 網站。</span><span class="sxs-lookup"><span data-stu-id="da1d4-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="da1d4-129">壓縮</span><span class="sxs-lookup"><span data-stu-id="da1d4-129">-Compression</span></span>
<span data-ttu-id="da1d4-130">指定是否應啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="da1d4-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da1d4-131">-DefaultProfile</span></span>
<span data-ttu-id="da1d4-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da1d4-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="da1d4-133">-加密</span><span class="sxs-lookup"><span data-stu-id="da1d4-133">-Encryption</span></span>
<span data-ttu-id="da1d4-134">{{Fill 加密描述}}</span><span class="sxs-lookup"><span data-stu-id="da1d4-134">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="da1d4-135">-HyperVToAzure</span></span>
<span data-ttu-id="da1d4-136">[切換] 參數指出已使用預先指明的原則，將 Hyper-v 虛擬機器複製到 Azure。</span><span class="sxs-lookup"><span data-stu-id="da1d4-136">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="da1d4-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da1d4-137">-InputObject</span></span>
<span data-ttu-id="da1d4-138">Cmdlet 的輸入物件：指定對應到要更新之複製原則的 ASR 複製原則物件。</span><span class="sxs-lookup"><span data-stu-id="da1d4-138">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="da1d4-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="da1d4-140">指定原則的 multiVm 同步處理狀態。</span><span class="sxs-lookup"><span data-stu-id="da1d4-140">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-141">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="da1d4-141">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="da1d4-142">指定要保留的復原點數。</span><span class="sxs-lookup"><span data-stu-id="da1d4-142">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-143">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="da1d4-143">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="da1d4-144">指定複製目標的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="da1d4-144">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="da1d4-145">如果您在使用 New-AzureRmRecoveryServicesASRReplicationProtectedItem Cmdlet 啟用複製時未提供備用，就會將它當作複製的目標儲存空間帳戶使用。</span><span class="sxs-lookup"><span data-stu-id="da1d4-145">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-146">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="da1d4-146">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="da1d4-147">在建立之後保留復原點的時間（小時）。</span><span class="sxs-lookup"><span data-stu-id="da1d4-147">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-148">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="da1d4-148">-ReplicaDeletion</span></span>
<span data-ttu-id="da1d4-149">指定在停用從 VMM 管理的網站到另一個網站的複製時，是否應該刪除複本虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="da1d4-149">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-150">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="da1d4-150">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="da1d4-151">指定複製頻率間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="da1d4-151">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="da1d4-152">有效值為：</span><span class="sxs-lookup"><span data-stu-id="da1d4-152">Valid values are:</span></span>

- <span data-ttu-id="da1d4-153">為期</span><span class="sxs-lookup"><span data-stu-id="da1d4-153">30</span></span>
- <span data-ttu-id="da1d4-154">300</span><span class="sxs-lookup"><span data-stu-id="da1d4-154">300</span></span>
- <span data-ttu-id="da1d4-155">900</span><span class="sxs-lookup"><span data-stu-id="da1d4-155">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-156">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="da1d4-156">-ReplicationMethod</span></span>
<span data-ttu-id="da1d4-157">指定複製方法。</span><span class="sxs-lookup"><span data-stu-id="da1d4-157">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-158">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="da1d4-158">-ReplicationPort</span></span>
<span data-ttu-id="da1d4-159">指定用於複製的埠。</span><span class="sxs-lookup"><span data-stu-id="da1d4-159">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-160">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="da1d4-160">-ReplicationStartTime</span></span>
<span data-ttu-id="da1d4-161">指定複製開始時間。</span><span class="sxs-lookup"><span data-stu-id="da1d4-161">Specifies the replication start time.</span></span>
<span data-ttu-id="da1d4-162">從工作開始，該作業不能遲于24小時。</span><span class="sxs-lookup"><span data-stu-id="da1d4-162">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-163">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="da1d4-163">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="da1d4-164">要針對其發出警告的 RPO 閾值（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="da1d4-164">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1d4-165">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="da1d4-165">-VmmToVmm</span></span>
<span data-ttu-id="da1d4-166">[切換] 參數指出已使用預先決定的原則，在兩個 Hyper-v 網站之間複製 VMM 管理的 Hyper-v 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="da1d4-166">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="da1d4-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="da1d4-167">-VMwareToAzure</span></span>
<span data-ttu-id="da1d4-168">[切換] 參數指出已使用所指出的原則將 VMware 虛擬機器複製到 Azure。</span><span class="sxs-lookup"><span data-stu-id="da1d4-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="da1d4-169">-確認</span><span class="sxs-lookup"><span data-stu-id="da1d4-169">-Confirm</span></span>
<span data-ttu-id="da1d4-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da1d4-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da1d4-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da1d4-171">-WhatIf</span></span>
<span data-ttu-id="da1d4-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="da1d4-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da1d4-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="da1d4-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da1d4-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da1d4-174">CommonParameters</span></span>
<span data-ttu-id="da1d4-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da1d4-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da1d4-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="da1d4-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da1d4-177">輸入</span><span class="sxs-lookup"><span data-stu-id="da1d4-177">INPUTS</span></span>

### <span data-ttu-id="da1d4-178">RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="da1d4-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="da1d4-179">輸出</span><span class="sxs-lookup"><span data-stu-id="da1d4-179">OUTPUTS</span></span>

### <span data-ttu-id="da1d4-180">System.object</span><span class="sxs-lookup"><span data-stu-id="da1d4-180">System.Object</span></span>

## <span data-ttu-id="da1d4-181">筆記</span><span class="sxs-lookup"><span data-stu-id="da1d4-181">NOTES</span></span>

## <span data-ttu-id="da1d4-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="da1d4-182">RELATED LINKS</span></span>
