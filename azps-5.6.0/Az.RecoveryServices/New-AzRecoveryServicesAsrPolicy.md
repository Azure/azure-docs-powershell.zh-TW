---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 3edbee06d2e4079d8c2283cc1b3af166d81450de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903109"
---
# <span data-ttu-id="ef538-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ef538-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="ef538-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef538-102">SYNOPSIS</span></span>
<span data-ttu-id="ef538-103">建立 Azure 網站復原複本策略。</span><span class="sxs-lookup"><span data-stu-id="ef538-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="ef538-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef538-104">SYNTAX</span></span>

### <span data-ttu-id="ef538-105">HyperVToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="ef538-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef538-106">VAzToAzure</span><span class="sxs-lookup"><span data-stu-id="ef538-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef538-107">AzureToVPv</span><span class="sxs-lookup"><span data-stu-id="ef538-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef538-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="ef538-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef538-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ef538-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef538-110">描述</span><span class="sxs-lookup"><span data-stu-id="ef538-110">DESCRIPTION</span></span>
<span data-ttu-id="ef538-111">**New-AzRecoveryServicesAsrPolicy** Cmdlet 會建立 Azure 網站復原複本策略。</span><span class="sxs-lookup"><span data-stu-id="ef538-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="ef538-112">複寫原則是用來指定複本設定，例如複本頻率及復原點數目。</span><span class="sxs-lookup"><span data-stu-id="ef538-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="ef538-113">例子</span><span class="sxs-lookup"><span data-stu-id="ef538-113">EXAMPLES</span></span>

### <span data-ttu-id="ef538-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="ef538-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="ef538-115">使用指定的參數啟動複寫原則建立作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="ef538-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ef538-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="ef538-116">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="ef538-117">使用指定的參數啟動複寫原則建立作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="ef538-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ef538-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="ef538-118">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="ef538-119">範例 4</span><span class="sxs-lookup"><span data-stu-id="ef538-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="ef538-120">使用指定的參數啟動複寫原則建立作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="ef538-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ef538-121">參數</span><span class="sxs-lookup"><span data-stu-id="ef538-121">PARAMETERS</span></span>

### <span data-ttu-id="ef538-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="ef538-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="ef538-123">指定以小時 () 建立應用程式一致修復點的頻率。</span><span class="sxs-lookup"><span data-stu-id="ef538-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="ef538-124">-驗證</span><span class="sxs-lookup"><span data-stu-id="ef538-124">-Authentication</span></span>
<span data-ttu-id="ef538-125">指定使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="ef538-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="ef538-126">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="ef538-126">Valid values are:</span></span>

- <span data-ttu-id="ef538-127">證書</span><span class="sxs-lookup"><span data-stu-id="ef538-127">Certificate</span></span>
-  <span data-ttu-id="ef538-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="ef538-128">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="ef538-129">-AzureToAzure</span></span>
<span data-ttu-id="ef538-130">參數參數會指定 Azure 建立至 Azure 策略的情境。</span><span class="sxs-lookup"><span data-stu-id="ef538-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

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

### <span data-ttu-id="ef538-131">-AzureToVPv</span><span class="sxs-lookup"><span data-stu-id="ef538-131">-AzureToVMware</span></span>
<span data-ttu-id="ef538-132">參數參數會指定 azure 到 vMWare 建立之策略的情境。</span><span class="sxs-lookup"><span data-stu-id="ef538-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

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

### <span data-ttu-id="ef538-133">-壓縮</span><span class="sxs-lookup"><span data-stu-id="ef538-133">-Compression</span></span>
<span data-ttu-id="ef538-134">指定是否應啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="ef538-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef538-135">-DefaultProfile</span></span>
<span data-ttu-id="ef538-136">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef538-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ef538-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="ef538-137">-HyperVToAzure</span></span>
<span data-ttu-id="ef538-138">切換參數以指定用於將 Hyper-V 虛擬機器複製到 Azure 的策略</span><span class="sxs-lookup"><span data-stu-id="ef538-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-139">-MultiSyncSyncStatus</span><span class="sxs-lookup"><span data-stu-id="ef538-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="ef538-140">指定多部虛擬機器同步處理狀態。</span><span class="sxs-lookup"><span data-stu-id="ef538-140">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef538-141">-Name</span></span>
<span data-ttu-id="ef538-142">指定 ASR 複寫原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef538-142">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="ef538-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="ef538-144">指定要保留的復原點數。</span><span class="sxs-lookup"><span data-stu-id="ef538-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ef538-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="ef538-146">指定要複製到的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef538-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="ef538-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="ef538-148">將修復點保留為以小時表示的給定時間。</span><span class="sxs-lookup"><span data-stu-id="ef538-148">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="ef538-149">-ReplicaDeletion</span></span>
<span data-ttu-id="ef538-150">指定在停用 VMM 受管理網站的複本時，是否應刪除複本虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ef538-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-151">-ReplicationFrequencyIn自秒鐘</span><span class="sxs-lookup"><span data-stu-id="ef538-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="ef538-152">指定以秒為單位的複製頻率間隔。</span><span class="sxs-lookup"><span data-stu-id="ef538-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="ef538-153">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="ef538-153">Valid values are:</span></span>

- <span data-ttu-id="ef538-154">30</span><span class="sxs-lookup"><span data-stu-id="ef538-154">30</span></span>
- <span data-ttu-id="ef538-155">300</span><span class="sxs-lookup"><span data-stu-id="ef538-155">300</span></span>
- <span data-ttu-id="ef538-156">900</span><span class="sxs-lookup"><span data-stu-id="ef538-156">900</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="ef538-157">-ReplicationMethod</span></span>
<span data-ttu-id="ef538-158">指定複製方法。</span><span class="sxs-lookup"><span data-stu-id="ef538-158">Specifies the replication method.</span></span>
<span data-ttu-id="ef538-159">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="ef538-159">Valid values are:</span></span>

- <span data-ttu-id="ef538-160">線上</span><span class="sxs-lookup"><span data-stu-id="ef538-160">Online</span></span>
- <span data-ttu-id="ef538-161">離線</span><span class="sxs-lookup"><span data-stu-id="ef538-161">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="ef538-162">-ReplicationPort</span></span>
<span data-ttu-id="ef538-163">指定用於複製的埠。</span><span class="sxs-lookup"><span data-stu-id="ef538-163">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="ef538-164">-ReplicationProvider</span></span>
<span data-ttu-id="ef538-165">指定該策略的複製提供者。</span><span class="sxs-lookup"><span data-stu-id="ef538-165">Specifies the replication provider for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-166">-複製啟動時間</span><span class="sxs-lookup"><span data-stu-id="ef538-166">-ReplicationStartTime</span></span>
<span data-ttu-id="ef538-167">指定複製開始時間。</span><span class="sxs-lookup"><span data-stu-id="ef538-167">Specifies the replication start time.</span></span>
<span data-ttu-id="ef538-168">不得晚于工作開始後 24 小時。</span><span class="sxs-lookup"><span data-stu-id="ef538-168">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="ef538-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="ef538-170">要警告的 RPO 閾值 ，以分鐘為限。</span><span class="sxs-lookup"><span data-stu-id="ef538-170">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="ef538-171">-VmmToVmm</span></span>
<span data-ttu-id="ef538-172">切換參數以指定策略，以在 VMM 伺服器管理的 Hyper-V 網站之間複製。</span><span class="sxs-lookup"><span data-stu-id="ef538-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef538-173">-VAzToAzure</span><span class="sxs-lookup"><span data-stu-id="ef538-173">-VMwareToAzure</span></span>
<span data-ttu-id="ef538-174">切換參數，指定要建立之複寫原則將用來將 V是否虛擬機器和/或實體伺服器複製到 Azure。</span><span class="sxs-lookup"><span data-stu-id="ef538-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="ef538-175">-確認</span><span class="sxs-lookup"><span data-stu-id="ef538-175">-Confirm</span></span>
<span data-ttu-id="ef538-176">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ef538-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef538-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef538-177">-WhatIf</span></span>
<span data-ttu-id="ef538-178">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef538-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef538-179">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef538-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef538-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef538-180">CommonParameters</span></span>
<span data-ttu-id="ef538-181">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef538-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef538-182">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef538-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef538-183">輸入</span><span class="sxs-lookup"><span data-stu-id="ef538-183">INPUTS</span></span>

### <span data-ttu-id="ef538-184">沒有</span><span class="sxs-lookup"><span data-stu-id="ef538-184">None</span></span>

## <span data-ttu-id="ef538-185">輸出</span><span class="sxs-lookup"><span data-stu-id="ef538-185">OUTPUTS</span></span>

### <span data-ttu-id="ef538-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ef538-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ef538-187">筆記</span><span class="sxs-lookup"><span data-stu-id="ef538-187">NOTES</span></span>

## <span data-ttu-id="ef538-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef538-188">RELATED LINKS</span></span>

[<span data-ttu-id="ef538-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ef538-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="ef538-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ef538-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
