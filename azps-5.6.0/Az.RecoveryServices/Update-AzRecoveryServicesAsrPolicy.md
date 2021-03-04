---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 2255a2397c7096ec1a7b5f45dc4fa699649b071a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915909"
---
# <span data-ttu-id="f5f15-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f5f15-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="f5f15-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5f15-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f15-103">更新 Azure 網站復原複本政策。</span><span class="sxs-lookup"><span data-stu-id="f5f15-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="f5f15-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5f15-104">SYNTAX</span></span>

### <span data-ttu-id="f5f15-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="f5f15-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5f15-106">VAzToAzure</span><span class="sxs-lookup"><span data-stu-id="f5f15-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5f15-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f5f15-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5f15-108">AzureToVPv</span><span class="sxs-lookup"><span data-stu-id="f5f15-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5f15-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="f5f15-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5f15-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="f5f15-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f15-111">描述</span><span class="sxs-lookup"><span data-stu-id="f5f15-111">DESCRIPTION</span></span>
<span data-ttu-id="f5f15-112">**Update-AzRecoveryServicesAsrPolicy** Cmdlet 會更新指定的 Azure 網站復原複本策略。</span><span class="sxs-lookup"><span data-stu-id="f5f15-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="f5f15-113">例子</span><span class="sxs-lookup"><span data-stu-id="f5f15-113">EXAMPLES</span></span>

### <span data-ttu-id="f5f15-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="f5f15-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="f5f15-115">使用指定的參數啟動更新複寫原則作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="f5f15-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f5f15-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="f5f15-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="f5f15-117">使用指定的參數啟動 Azure 至 Azure 複寫原則作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="f5f15-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f5f15-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="f5f15-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="f5f15-119">使用指定的參數將 Azure 更新為 Azure 複寫原則，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="f5f15-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f5f15-120">參數</span><span class="sxs-lookup"><span data-stu-id="f5f15-120">PARAMETERS</span></span>

### <span data-ttu-id="f5f15-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="f5f15-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="f5f15-122">指定以小時 () 建立應用程式一致修復點的頻率。</span><span class="sxs-lookup"><span data-stu-id="f5f15-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="f5f15-123">-驗證</span><span class="sxs-lookup"><span data-stu-id="f5f15-123">-Authentication</span></span>
<span data-ttu-id="f5f15-124">指定使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="f5f15-124">Specifies the type of authentication used.</span></span>

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

### <span data-ttu-id="f5f15-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f5f15-125">-AzureToAzure</span></span>
<span data-ttu-id="f5f15-126">指定 Azure 到 Azure 的災害復原。</span><span class="sxs-lookup"><span data-stu-id="f5f15-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="f5f15-127">-AzureToVPv</span><span class="sxs-lookup"><span data-stu-id="f5f15-127">-AzureToVMware</span></span>
<span data-ttu-id="f5f15-128">指定 Azure to vMWare 的災害復原。</span><span class="sxs-lookup"><span data-stu-id="f5f15-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="f5f15-129">-壓縮</span><span class="sxs-lookup"><span data-stu-id="f5f15-129">-Compression</span></span>
<span data-ttu-id="f5f15-130">指定是否應啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="f5f15-130">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="f5f15-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f15-131">-DefaultProfile</span></span>
<span data-ttu-id="f5f15-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5f15-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f5f15-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="f5f15-133">-HyperVToAzure</span></span>
<span data-ttu-id="f5f15-134">切換參數，指出指定的策略是用來將 Hyper-V 虛擬機器複製到 Azure。</span><span class="sxs-lookup"><span data-stu-id="f5f15-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="f5f15-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5f15-135">-InputObject</span></span>
<span data-ttu-id="f5f15-136">Cmdlet 的輸入物件：指定對應至要更新之複寫原則的 ASR 複寫原則物件。</span><span class="sxs-lookup"><span data-stu-id="f5f15-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="f5f15-137">-MultiSyncSyncStatus</span><span class="sxs-lookup"><span data-stu-id="f5f15-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="f5f15-138">指定多部虛擬機器同步處理狀態。</span><span class="sxs-lookup"><span data-stu-id="f5f15-138">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="f5f15-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="f5f15-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="f5f15-140">指定要保留的復原點數。</span><span class="sxs-lookup"><span data-stu-id="f5f15-140">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="f5f15-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f5f15-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f5f15-142">指定複製目標的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5f15-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="f5f15-143">在啟用使用 Cmdlet 進行複製時，若未提供替代專案，則用來New-AzRecoveryServicesASRReplicationProtectedItem帳戶。</span><span class="sxs-lookup"><span data-stu-id="f5f15-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


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

### <span data-ttu-id="f5f15-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="f5f15-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="f5f15-145">建立後保留修復點的時間 ，以小時表示。</span><span class="sxs-lookup"><span data-stu-id="f5f15-145">Time in hours to retain recovery points after creation.</span></span>

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

### <span data-ttu-id="f5f15-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="f5f15-146">-ReplicaDeletion</span></span>
<span data-ttu-id="f5f15-147">指定在停用 VMM 受管理網站的複本時，是否應刪除複本虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f5f15-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="f5f15-148">-ReplicationFrequencyIn自秒鐘</span><span class="sxs-lookup"><span data-stu-id="f5f15-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="f5f15-149">指定以秒為單位的複製頻率間隔。</span><span class="sxs-lookup"><span data-stu-id="f5f15-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="f5f15-150">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="f5f15-150">Valid values are:</span></span>

- <span data-ttu-id="f5f15-151">30</span><span class="sxs-lookup"><span data-stu-id="f5f15-151">30</span></span>
- <span data-ttu-id="f5f15-152">300</span><span class="sxs-lookup"><span data-stu-id="f5f15-152">300</span></span>
- <span data-ttu-id="f5f15-153">900</span><span class="sxs-lookup"><span data-stu-id="f5f15-153">900</span></span>

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

### <span data-ttu-id="f5f15-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="f5f15-154">-ReplicationMethod</span></span>
<span data-ttu-id="f5f15-155">指定複製方法。</span><span class="sxs-lookup"><span data-stu-id="f5f15-155">Specifies the replication method.</span></span>

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

### <span data-ttu-id="f5f15-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="f5f15-156">-ReplicationPort</span></span>
<span data-ttu-id="f5f15-157">指定用於複製的埠。</span><span class="sxs-lookup"><span data-stu-id="f5f15-157">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="f5f15-158">-複製啟動時間</span><span class="sxs-lookup"><span data-stu-id="f5f15-158">-ReplicationStartTime</span></span>
<span data-ttu-id="f5f15-159">指定複製開始時間。</span><span class="sxs-lookup"><span data-stu-id="f5f15-159">Specifies the replication start time.</span></span>
<span data-ttu-id="f5f15-160">不得晚于工作開始後 24 小時。</span><span class="sxs-lookup"><span data-stu-id="f5f15-160">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="f5f15-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="f5f15-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="f5f15-162">要警告的 RPO 閾值 ，以分鐘為限。</span><span class="sxs-lookup"><span data-stu-id="f5f15-162">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="f5f15-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="f5f15-163">-VmmToVmm</span></span>
<span data-ttu-id="f5f15-164">切換參數，指出指定的策略是用來在兩個 Hyper-V 網站之間複製 VMM 管理的 Hyper-V 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f5f15-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="f5f15-165">-VAzToAzure</span><span class="sxs-lookup"><span data-stu-id="f5f15-165">-VMwareToAzure</span></span>
<span data-ttu-id="f5f15-166">切換參數，指出指定用於將 VAa 虛擬機器複製到 Azure。</span><span class="sxs-lookup"><span data-stu-id="f5f15-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="f5f15-167">-確認</span><span class="sxs-lookup"><span data-stu-id="f5f15-167">-Confirm</span></span>
<span data-ttu-id="f5f15-168">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f5f15-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5f15-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f15-169">-WhatIf</span></span>
<span data-ttu-id="f5f15-170">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5f15-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5f15-171">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5f15-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5f15-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f15-172">CommonParameters</span></span>
<span data-ttu-id="f5f15-173">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5f15-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f15-174">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5f15-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f15-175">輸入</span><span class="sxs-lookup"><span data-stu-id="f5f15-175">INPUTS</span></span>

### <span data-ttu-id="f5f15-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="f5f15-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="f5f15-177">輸出</span><span class="sxs-lookup"><span data-stu-id="f5f15-177">OUTPUTS</span></span>

### <span data-ttu-id="f5f15-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="f5f15-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f5f15-179">筆記</span><span class="sxs-lookup"><span data-stu-id="f5f15-179">NOTES</span></span>

## <span data-ttu-id="f5f15-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5f15-180">RELATED LINKS</span></span>
