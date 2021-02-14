---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: d120054a7eef5afd27101d84911a1a57a0b4819a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134699"
---
# <span data-ttu-id="27645-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="27645-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="27645-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27645-102">SYNOPSIS</span></span>
<span data-ttu-id="27645-103">建立 Azure Site Recovery 複製原則。</span><span class="sxs-lookup"><span data-stu-id="27645-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="27645-104">句法</span><span class="sxs-lookup"><span data-stu-id="27645-104">SYNTAX</span></span>

### <span data-ttu-id="27645-105">HyperVToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="27645-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27645-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="27645-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27645-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="27645-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27645-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="27645-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27645-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="27645-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27645-110">說明</span><span class="sxs-lookup"><span data-stu-id="27645-110">DESCRIPTION</span></span>
<span data-ttu-id="27645-111">**新的-AzRecoveryServicesAsrPolicy** Cmdlet 會建立 Azure Site Recovery 複製原則。</span><span class="sxs-lookup"><span data-stu-id="27645-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="27645-112">複製原則是用來指定複製設定，例如複製頻率和復原點數的數量。</span><span class="sxs-lookup"><span data-stu-id="27645-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="27645-113">示例</span><span class="sxs-lookup"><span data-stu-id="27645-113">EXAMPLES</span></span>

### <span data-ttu-id="27645-114">範例1</span><span class="sxs-lookup"><span data-stu-id="27645-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="27645-115">使用指定的參數開始複製原則建立作業，並傳回用來追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="27645-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="27645-116">範例2</span><span class="sxs-lookup"><span data-stu-id="27645-116">Example 2</span></span>
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

<span data-ttu-id="27645-117">使用指定的參數開始複製原則建立作業，並傳回用來追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="27645-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="27645-118">範例3</span><span class="sxs-lookup"><span data-stu-id="27645-118">Example 3</span></span>
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

### <span data-ttu-id="27645-119">範例4</span><span class="sxs-lookup"><span data-stu-id="27645-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="27645-120">使用指定的參數開始複製原則建立作業，並傳回用來追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="27645-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="27645-121">參數</span><span class="sxs-lookup"><span data-stu-id="27645-121">PARAMETERS</span></span>

### <span data-ttu-id="27645-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="27645-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="27645-123">指定要建立應用程式一致復原點的頻率 (，單位為小時) 。</span><span class="sxs-lookup"><span data-stu-id="27645-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="27645-124">-驗證</span><span class="sxs-lookup"><span data-stu-id="27645-124">-Authentication</span></span>
<span data-ttu-id="27645-125">指定所使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="27645-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="27645-126">有效值為：</span><span class="sxs-lookup"><span data-stu-id="27645-126">Valid values are:</span></span>

- <span data-ttu-id="27645-127">憑證</span><span class="sxs-lookup"><span data-stu-id="27645-127">Certificate</span></span>
-  <span data-ttu-id="27645-128">V5</span><span class="sxs-lookup"><span data-stu-id="27645-128">Kerberos</span></span>

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

### <span data-ttu-id="27645-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="27645-129">-AzureToAzure</span></span>
<span data-ttu-id="27645-130">Switch 參數指定 azure 到 azure 策略建立的情況。</span><span class="sxs-lookup"><span data-stu-id="27645-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

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

### <span data-ttu-id="27645-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="27645-131">-AzureToVMware</span></span>
<span data-ttu-id="27645-132">Switch 參數指定 azure 到 vMWare 原則建立的情況。</span><span class="sxs-lookup"><span data-stu-id="27645-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

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

### <span data-ttu-id="27645-133">壓縮</span><span class="sxs-lookup"><span data-stu-id="27645-133">-Compression</span></span>
<span data-ttu-id="27645-134">指定是否應啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="27645-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="27645-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27645-135">-DefaultProfile</span></span>
<span data-ttu-id="27645-136">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27645-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="27645-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="27645-137">-HyperVToAzure</span></span>
<span data-ttu-id="27645-138">指定原則的切換參數是用來將 Hyper-v 虛擬機器複製到 Azure</span><span class="sxs-lookup"><span data-stu-id="27645-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="27645-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="27645-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="27645-140">指定原則的 multiVm 同步處理狀態。</span><span class="sxs-lookup"><span data-stu-id="27645-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="27645-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="27645-141">-Name</span></span>
<span data-ttu-id="27645-142">指定 ASR 複製原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="27645-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="27645-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="27645-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="27645-144">指定要保留的復原點數。</span><span class="sxs-lookup"><span data-stu-id="27645-144">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="27645-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="27645-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="27645-146">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="27645-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="27645-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="27645-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="27645-148">保留指定時間的復原點數（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="27645-148">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="27645-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="27645-149">-ReplicaDeletion</span></span>
<span data-ttu-id="27645-150">指定在停用從 VMM 管理的網站到另一個網站的複製時，是否應該刪除複本虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="27645-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="27645-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="27645-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="27645-152">指定複製頻率間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="27645-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="27645-153">有效值為：</span><span class="sxs-lookup"><span data-stu-id="27645-153">Valid values are:</span></span>

- <span data-ttu-id="27645-154">為期</span><span class="sxs-lookup"><span data-stu-id="27645-154">30</span></span>
- <span data-ttu-id="27645-155">300</span><span class="sxs-lookup"><span data-stu-id="27645-155">300</span></span>
- <span data-ttu-id="27645-156">900</span><span class="sxs-lookup"><span data-stu-id="27645-156">900</span></span>

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

### <span data-ttu-id="27645-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="27645-157">-ReplicationMethod</span></span>
<span data-ttu-id="27645-158">指定複製方法。</span><span class="sxs-lookup"><span data-stu-id="27645-158">Specifies the replication method.</span></span>
<span data-ttu-id="27645-159">有效值為：</span><span class="sxs-lookup"><span data-stu-id="27645-159">Valid values are:</span></span>

- <span data-ttu-id="27645-160">Online</span><span class="sxs-lookup"><span data-stu-id="27645-160">Online</span></span>
- <span data-ttu-id="27645-161">處於</span><span class="sxs-lookup"><span data-stu-id="27645-161">Offline</span></span>

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

### <span data-ttu-id="27645-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="27645-162">-ReplicationPort</span></span>
<span data-ttu-id="27645-163">指定用於複製的埠。</span><span class="sxs-lookup"><span data-stu-id="27645-163">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="27645-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="27645-164">-ReplicationProvider</span></span>
<span data-ttu-id="27645-165">指定原則的複製提供者。</span><span class="sxs-lookup"><span data-stu-id="27645-165">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="27645-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="27645-166">-ReplicationStartTime</span></span>
<span data-ttu-id="27645-167">指定複製開始時間。</span><span class="sxs-lookup"><span data-stu-id="27645-167">Specifies the replication start time.</span></span>
<span data-ttu-id="27645-168">從工作開始，該作業不能遲于24小時。</span><span class="sxs-lookup"><span data-stu-id="27645-168">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="27645-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="27645-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="27645-170">要針對其發出警告的 RPO 閾值（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="27645-170">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="27645-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="27645-171">-VmmToVmm</span></span>
<span data-ttu-id="27645-172">將參數切換為指定原則的做法是在 VMM 伺服器所管理的 Hyper-v 網站之間進行複製。</span><span class="sxs-lookup"><span data-stu-id="27645-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="27645-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="27645-173">-VMwareToAzure</span></span>
<span data-ttu-id="27645-174">切換參數：指定所建立的複製原則將用來將 VMware 虛擬機器和/或物理伺服器複製到 Azure。</span><span class="sxs-lookup"><span data-stu-id="27645-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="27645-175">-確認</span><span class="sxs-lookup"><span data-stu-id="27645-175">-Confirm</span></span>
<span data-ttu-id="27645-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="27645-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27645-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27645-177">-WhatIf</span></span>
<span data-ttu-id="27645-178">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27645-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27645-179">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27645-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27645-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27645-180">CommonParameters</span></span>
<span data-ttu-id="27645-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27645-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27645-182">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="27645-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27645-183">輸入</span><span class="sxs-lookup"><span data-stu-id="27645-183">INPUTS</span></span>

### <span data-ttu-id="27645-184">所有</span><span class="sxs-lookup"><span data-stu-id="27645-184">None</span></span>

## <span data-ttu-id="27645-185">輸出</span><span class="sxs-lookup"><span data-stu-id="27645-185">OUTPUTS</span></span>

### <span data-ttu-id="27645-186">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="27645-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="27645-187">筆記</span><span class="sxs-lookup"><span data-stu-id="27645-187">NOTES</span></span>

## <span data-ttu-id="27645-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="27645-188">RELATED LINKS</span></span>

[<span data-ttu-id="27645-189">AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="27645-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="27645-190">移除-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="27645-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
