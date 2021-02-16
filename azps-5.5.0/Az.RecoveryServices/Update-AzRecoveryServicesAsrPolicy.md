---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 31b43930737627a3013f60a82c2ec30626b8518c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128506"
---
# <span data-ttu-id="2b761-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="2b761-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="2b761-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b761-102">SYNOPSIS</span></span>
<span data-ttu-id="2b761-103">更新 Azure 網站恢復複製原則。</span><span class="sxs-lookup"><span data-stu-id="2b761-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="2b761-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b761-104">SYNTAX</span></span>

### <span data-ttu-id="2b761-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="2b761-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b761-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="2b761-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b761-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="2b761-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b761-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="2b761-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b761-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="2b761-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b761-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="2b761-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b761-111">說明</span><span class="sxs-lookup"><span data-stu-id="2b761-111">DESCRIPTION</span></span>
<span data-ttu-id="2b761-112">**AzRecoveryServicesAsrPolicy** Cmdlet 會更新指定的 Azure Site Recovery 複製原則。</span><span class="sxs-lookup"><span data-stu-id="2b761-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="2b761-113">示例</span><span class="sxs-lookup"><span data-stu-id="2b761-113">EXAMPLES</span></span>

### <span data-ttu-id="2b761-114">範例1</span><span class="sxs-lookup"><span data-stu-id="2b761-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="2b761-115">使用指定的參數啟動更新複製原則作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="2b761-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2b761-116">範例2</span><span class="sxs-lookup"><span data-stu-id="2b761-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="2b761-117">使用指定的參數開始將 azure to azure 複製原則作業更新，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="2b761-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2b761-118">範例3</span><span class="sxs-lookup"><span data-stu-id="2b761-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="2b761-119">使用指定的參數開始將 azure 更新到 azure 複製原則，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="2b761-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2b761-120">參數</span><span class="sxs-lookup"><span data-stu-id="2b761-120">PARAMETERS</span></span>

### <span data-ttu-id="2b761-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="2b761-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="2b761-122">指定要建立應用程式一致復原點的頻率 (，單位為小時) 。</span><span class="sxs-lookup"><span data-stu-id="2b761-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="2b761-123">-驗證</span><span class="sxs-lookup"><span data-stu-id="2b761-123">-Authentication</span></span>
<span data-ttu-id="2b761-124">指定所使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="2b761-124">Specifies the type of authentication used.</span></span>

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

### <span data-ttu-id="2b761-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="2b761-125">-AzureToAzure</span></span>
<span data-ttu-id="2b761-126">指定 Azure 到 Azure 災害復原。</span><span class="sxs-lookup"><span data-stu-id="2b761-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="2b761-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="2b761-127">-AzureToVMware</span></span>
<span data-ttu-id="2b761-128">指定 Azure to vMWare 災害復原。</span><span class="sxs-lookup"><span data-stu-id="2b761-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="2b761-129">壓縮</span><span class="sxs-lookup"><span data-stu-id="2b761-129">-Compression</span></span>
<span data-ttu-id="2b761-130">指定是否應啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="2b761-130">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="2b761-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b761-131">-DefaultProfile</span></span>
<span data-ttu-id="2b761-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b761-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2b761-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="2b761-133">-HyperVToAzure</span></span>
<span data-ttu-id="2b761-134">[切換] 參數指出指定的原則是用來將 Hyper-v 虛擬機器複製到 Azure。</span><span class="sxs-lookup"><span data-stu-id="2b761-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="2b761-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b761-135">-InputObject</span></span>
<span data-ttu-id="2b761-136">Cmdlet 的輸入物件：指定對應到要更新之複製原則的 ASR 複製原則物件。</span><span class="sxs-lookup"><span data-stu-id="2b761-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="2b761-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="2b761-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="2b761-138">指定原則的 multiVm 同步處理狀態。</span><span class="sxs-lookup"><span data-stu-id="2b761-138">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="2b761-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="2b761-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="2b761-140">指定要保留的復原點數。</span><span class="sxs-lookup"><span data-stu-id="2b761-140">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="2b761-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2b761-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="2b761-142">指定複製目標的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b761-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="2b761-143">如果您在使用 New-AzRecoveryServicesASRReplicationProtectedItem Cmdlet 啟用複製時未提供備用，就會將它當作複製的目標儲存空間帳戶使用。</span><span class="sxs-lookup"><span data-stu-id="2b761-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


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

### <span data-ttu-id="2b761-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="2b761-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="2b761-145">在建立之後保留復原點的時間（小時）。</span><span class="sxs-lookup"><span data-stu-id="2b761-145">Time in hours to retain recovery points after creation.</span></span>

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

### <span data-ttu-id="2b761-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="2b761-146">-ReplicaDeletion</span></span>
<span data-ttu-id="2b761-147">指定在停用從 VMM 管理的網站到另一個網站的複製時，是否應該刪除複本虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2b761-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="2b761-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="2b761-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="2b761-149">指定複製頻率間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2b761-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="2b761-150">有效值為：</span><span class="sxs-lookup"><span data-stu-id="2b761-150">Valid values are:</span></span>

- <span data-ttu-id="2b761-151">為期</span><span class="sxs-lookup"><span data-stu-id="2b761-151">30</span></span>
- <span data-ttu-id="2b761-152">300</span><span class="sxs-lookup"><span data-stu-id="2b761-152">300</span></span>
- <span data-ttu-id="2b761-153">900</span><span class="sxs-lookup"><span data-stu-id="2b761-153">900</span></span>

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

### <span data-ttu-id="2b761-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="2b761-154">-ReplicationMethod</span></span>
<span data-ttu-id="2b761-155">指定複製方法。</span><span class="sxs-lookup"><span data-stu-id="2b761-155">Specifies the replication method.</span></span>

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

### <span data-ttu-id="2b761-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="2b761-156">-ReplicationPort</span></span>
<span data-ttu-id="2b761-157">指定用於複製的埠。</span><span class="sxs-lookup"><span data-stu-id="2b761-157">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="2b761-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="2b761-158">-ReplicationStartTime</span></span>
<span data-ttu-id="2b761-159">指定複製開始時間。</span><span class="sxs-lookup"><span data-stu-id="2b761-159">Specifies the replication start time.</span></span>
<span data-ttu-id="2b761-160">從工作開始，該作業不能遲于24小時。</span><span class="sxs-lookup"><span data-stu-id="2b761-160">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="2b761-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="2b761-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="2b761-162">要針對其發出警告的 RPO 閾值（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="2b761-162">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="2b761-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="2b761-163">-VmmToVmm</span></span>
<span data-ttu-id="2b761-164">[切換] 參數指出指定的原則是用來在兩個 Hyper-v 網站之間複製 VMM 管理的 Hyper-v 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2b761-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="2b761-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="2b761-165">-VMwareToAzure</span></span>
<span data-ttu-id="2b761-166">[切換] 參數指出指定的原則是用來將 VMware 虛擬機器複製到 Azure。</span><span class="sxs-lookup"><span data-stu-id="2b761-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="2b761-167">-確認</span><span class="sxs-lookup"><span data-stu-id="2b761-167">-Confirm</span></span>
<span data-ttu-id="2b761-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b761-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b761-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b761-169">-WhatIf</span></span>
<span data-ttu-id="2b761-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b761-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b761-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b761-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b761-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b761-172">CommonParameters</span></span>
<span data-ttu-id="2b761-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b761-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b761-174">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b761-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b761-175">輸入</span><span class="sxs-lookup"><span data-stu-id="2b761-175">INPUTS</span></span>

### <span data-ttu-id="2b761-176">RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="2b761-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="2b761-177">輸出</span><span class="sxs-lookup"><span data-stu-id="2b761-177">OUTPUTS</span></span>

### <span data-ttu-id="2b761-178">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2b761-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2b761-179">筆記</span><span class="sxs-lookup"><span data-stu-id="2b761-179">NOTES</span></span>

## <span data-ttu-id="2b761-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b761-180">RELATED LINKS</span></span>
