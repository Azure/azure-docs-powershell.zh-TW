---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448048"
---
# <span data-ttu-id="d5b42-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d5b42-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="d5b42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5b42-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b42-103">建立 Azure Site Recovery 複製原則。</span><span class="sxs-lookup"><span data-stu-id="d5b42-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5b42-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5b42-104">SYNTAX</span></span>

### <span data-ttu-id="d5b42-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="d5b42-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5b42-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d5b42-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5b42-107">說明</span><span class="sxs-lookup"><span data-stu-id="d5b42-107">DESCRIPTION</span></span>
<span data-ttu-id="d5b42-108">**新的-AzureRmRecoveryServicesAsrPolicy** Cmdlet 會建立 Azure Site Recovery 複製原則。</span><span class="sxs-lookup"><span data-stu-id="d5b42-108">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="d5b42-109">複製原則是用來指定複製設定，例如複製頻率和復原點數的數量。</span><span class="sxs-lookup"><span data-stu-id="d5b42-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="d5b42-110">示例</span><span class="sxs-lookup"><span data-stu-id="d5b42-110">EXAMPLES</span></span>

### <span data-ttu-id="d5b42-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d5b42-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="d5b42-112">使用指定的參數開始複製原則建立作業，並傳回用來追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="d5b42-112">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d5b42-113">參數</span><span class="sxs-lookup"><span data-stu-id="d5b42-113">PARAMETERS</span></span>

### <span data-ttu-id="d5b42-114">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="d5b42-114">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="d5b42-115">指定要建立應用程式一致復原點的頻率 (，單位為小時) 。</span><span class="sxs-lookup"><span data-stu-id="d5b42-115">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-116">-驗證</span><span class="sxs-lookup"><span data-stu-id="d5b42-116">-Authentication</span></span>
<span data-ttu-id="d5b42-117">指定所使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="d5b42-117">Specifies the type of authentication used.</span></span>
<span data-ttu-id="d5b42-118">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d5b42-118">Valid values are:</span></span>

- <span data-ttu-id="d5b42-119">憑證</span><span class="sxs-lookup"><span data-stu-id="d5b42-119">Certificate</span></span>
-  <span data-ttu-id="d5b42-120">V5</span><span class="sxs-lookup"><span data-stu-id="d5b42-120">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-121">壓縮</span><span class="sxs-lookup"><span data-stu-id="d5b42-121">-Compression</span></span>
<span data-ttu-id="d5b42-122">指定是否應啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="d5b42-122">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-123">-加密</span><span class="sxs-lookup"><span data-stu-id="d5b42-123">-Encryption</span></span>
<span data-ttu-id="d5b42-124">指定應該啟用還是停用加密。</span><span class="sxs-lookup"><span data-stu-id="d5b42-124">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d5b42-125">-Name</span></span>
<span data-ttu-id="d5b42-126">指定 ASR 複製原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5b42-126">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="d5b42-127">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="d5b42-127">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="d5b42-128">指定要保留的復原點數。</span><span class="sxs-lookup"><span data-stu-id="d5b42-128">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-129">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d5b42-129">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="d5b42-130">指定複製目標的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5b42-130">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="d5b42-131">如果您在使用 New-AzureRmRecoveryServicesASRReplicationProtectedItem Cmdlet 啟用複製時未提供備用，就會將它當作複製的目標儲存空間帳戶使用。</span><span class="sxs-lookup"><span data-stu-id="d5b42-131">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-132">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="d5b42-132">-ReplicaDeletion</span></span>
<span data-ttu-id="d5b42-133">指定在停用從 VMM 管理的網站到另一個網站的複製時，是否應該刪除複本虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d5b42-133">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-134">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="d5b42-134">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="d5b42-135">指定複製頻率間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d5b42-135">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="d5b42-136">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d5b42-136">Valid values are:</span></span>

- <span data-ttu-id="d5b42-137">為期</span><span class="sxs-lookup"><span data-stu-id="d5b42-137">30</span></span>
- <span data-ttu-id="d5b42-138">300</span><span class="sxs-lookup"><span data-stu-id="d5b42-138">300</span></span>
- <span data-ttu-id="d5b42-139">900</span><span class="sxs-lookup"><span data-stu-id="d5b42-139">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-140">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="d5b42-140">-ReplicationMethod</span></span>
<span data-ttu-id="d5b42-141">指定複製方法。</span><span class="sxs-lookup"><span data-stu-id="d5b42-141">Specifies the replication method.</span></span>
<span data-ttu-id="d5b42-142">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d5b42-142">Valid values are:</span></span>

- <span data-ttu-id="d5b42-143">Online</span><span class="sxs-lookup"><span data-stu-id="d5b42-143">Online</span></span>
- <span data-ttu-id="d5b42-144">處於</span><span class="sxs-lookup"><span data-stu-id="d5b42-144">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-145">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="d5b42-145">-ReplicationPort</span></span>
<span data-ttu-id="d5b42-146">指定用於複製的埠。</span><span class="sxs-lookup"><span data-stu-id="d5b42-146">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-147">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="d5b42-147">-ReplicationProvider</span></span>
<span data-ttu-id="d5b42-148">指定複製提供者。</span><span class="sxs-lookup"><span data-stu-id="d5b42-148">Specifies the replication provider.</span></span>
<span data-ttu-id="d5b42-149">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d5b42-149">Valid values are:</span></span>

- <span data-ttu-id="d5b42-150">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="d5b42-150">HyperVReplica2012R2</span></span>
- <span data-ttu-id="d5b42-151">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="d5b42-151">HyperVReplica2012</span></span>
- <span data-ttu-id="d5b42-152">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="d5b42-152">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-153">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="d5b42-153">-ReplicationStartTime</span></span>
<span data-ttu-id="d5b42-154">指定複製開始時間。</span><span class="sxs-lookup"><span data-stu-id="d5b42-154">Specifies the replication start time.</span></span>
<span data-ttu-id="d5b42-155">從工作開始，該作業不能遲于24小時。</span><span class="sxs-lookup"><span data-stu-id="d5b42-155">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b42-156">-確認</span><span class="sxs-lookup"><span data-stu-id="d5b42-156">-Confirm</span></span>
<span data-ttu-id="d5b42-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d5b42-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5b42-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5b42-158">-WhatIf</span></span>
<span data-ttu-id="d5b42-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5b42-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5b42-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5b42-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5b42-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b42-161">CommonParameters</span></span>
<span data-ttu-id="d5b42-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5b42-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b42-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d5b42-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b42-164">輸入</span><span class="sxs-lookup"><span data-stu-id="d5b42-164">INPUTS</span></span>

### <span data-ttu-id="d5b42-165">所有</span><span class="sxs-lookup"><span data-stu-id="d5b42-165">None</span></span>

## <span data-ttu-id="d5b42-166">輸出</span><span class="sxs-lookup"><span data-stu-id="d5b42-166">OUTPUTS</span></span>

### <span data-ttu-id="d5b42-167">System.object</span><span class="sxs-lookup"><span data-stu-id="d5b42-167">System.Object</span></span>

## <span data-ttu-id="d5b42-168">筆記</span><span class="sxs-lookup"><span data-stu-id="d5b42-168">NOTES</span></span>

## <span data-ttu-id="d5b42-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5b42-169">RELATED LINKS</span></span>

[<span data-ttu-id="d5b42-170">AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d5b42-170">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="d5b42-171">移除-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d5b42-171">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
