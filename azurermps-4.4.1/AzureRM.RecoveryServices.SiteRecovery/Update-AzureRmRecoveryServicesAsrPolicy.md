---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453319"
---
# <span data-ttu-id="d876c-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d876c-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="d876c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d876c-102">SYNOPSIS</span></span>
<span data-ttu-id="d876c-103">更新 Azure 網站恢復複製原則。</span><span class="sxs-lookup"><span data-stu-id="d876c-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d876c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d876c-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d876c-105">說明</span><span class="sxs-lookup"><span data-stu-id="d876c-105">DESCRIPTION</span></span>
<span data-ttu-id="d876c-106">**AzureRmRecoveryServicesAsrPolicy** Cmdlet 會更新指定的 Azure Site Recovery 複製原則。</span><span class="sxs-lookup"><span data-stu-id="d876c-106">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="d876c-107">示例</span><span class="sxs-lookup"><span data-stu-id="d876c-107">EXAMPLES</span></span>

### <span data-ttu-id="d876c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d876c-108">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="d876c-109">使用指定的參數啟動更新複製原則作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="d876c-109">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d876c-110">參數</span><span class="sxs-lookup"><span data-stu-id="d876c-110">PARAMETERS</span></span>

### <span data-ttu-id="d876c-111">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="d876c-111">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="d876c-112">指定要建立應用程式一致復原點的頻率 (，單位為小時) 。</span><span class="sxs-lookup"><span data-stu-id="d876c-112">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="d876c-113">-驗證</span><span class="sxs-lookup"><span data-stu-id="d876c-113">-Authentication</span></span>
<span data-ttu-id="d876c-114">指定所使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="d876c-114">Specifies the type of authentication used.</span></span>
<span data-ttu-id="d876c-115">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d876c-115">Valid values are:</span></span>

- <span data-ttu-id="d876c-116">憑證</span><span class="sxs-lookup"><span data-stu-id="d876c-116">Certificate</span></span>
-  <span data-ttu-id="d876c-117">V5</span><span class="sxs-lookup"><span data-stu-id="d876c-117">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d876c-118">壓縮</span><span class="sxs-lookup"><span data-stu-id="d876c-118">-Compression</span></span>
<span data-ttu-id="d876c-119">指定是否應啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="d876c-119">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d876c-120">-加密</span><span class="sxs-lookup"><span data-stu-id="d876c-120">-Encryption</span></span>
<span data-ttu-id="d876c-121">指定應該啟用還是停用加密。</span><span class="sxs-lookup"><span data-stu-id="d876c-121">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d876c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d876c-122">-InputObject</span></span>
<span data-ttu-id="d876c-123">Cmdlet 的輸入物件：指定對應到要更新之複製原則的 ASR 複製原則物件。</span><span class="sxs-lookup"><span data-stu-id="d876c-123">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d876c-124">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="d876c-124">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="d876c-125">指定要保留的復原點數。</span><span class="sxs-lookup"><span data-stu-id="d876c-125">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="d876c-126">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d876c-126">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="d876c-127">指定複製目標的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="d876c-127">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="d876c-128">如果您在使用 New-AzureRmRecoveryServicesASRReplicationProtectedItem Cmdlet 啟用複製時未提供備用，就會將它當作複製的目標儲存空間帳戶使用。</span><span class="sxs-lookup"><span data-stu-id="d876c-128">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d876c-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="d876c-129">-ReplicaDeletion</span></span>
<span data-ttu-id="d876c-130">指定在停用從 VMM 管理的網站到另一個網站的複製時，是否應該刪除複本虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d876c-130">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d876c-131">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="d876c-131">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="d876c-132">指定複製頻率間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d876c-132">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="d876c-133">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d876c-133">Valid values are:</span></span>

- <span data-ttu-id="d876c-134">為期</span><span class="sxs-lookup"><span data-stu-id="d876c-134">30</span></span>
- <span data-ttu-id="d876c-135">300</span><span class="sxs-lookup"><span data-stu-id="d876c-135">300</span></span>
- <span data-ttu-id="d876c-136">900</span><span class="sxs-lookup"><span data-stu-id="d876c-136">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d876c-137">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="d876c-137">-ReplicationMethod</span></span>
<span data-ttu-id="d876c-138">指定複製方法。</span><span class="sxs-lookup"><span data-stu-id="d876c-138">Specifies the replication method.</span></span>
<span data-ttu-id="d876c-139">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d876c-139">Valid values are:</span></span>

- <span data-ttu-id="d876c-140">Online</span><span class="sxs-lookup"><span data-stu-id="d876c-140">Online</span></span>
- <span data-ttu-id="d876c-141">處於</span><span class="sxs-lookup"><span data-stu-id="d876c-141">Offline</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d876c-142">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="d876c-142">-ReplicationPort</span></span>
<span data-ttu-id="d876c-143">指定用於複製的埠。</span><span class="sxs-lookup"><span data-stu-id="d876c-143">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d876c-144">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="d876c-144">-ReplicationStartTime</span></span>
<span data-ttu-id="d876c-145">指定複製開始時間。</span><span class="sxs-lookup"><span data-stu-id="d876c-145">Specifies the replication start time.</span></span>
<span data-ttu-id="d876c-146">從工作開始，該作業不能遲于24小時。</span><span class="sxs-lookup"><span data-stu-id="d876c-146">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="d876c-147">-確認</span><span class="sxs-lookup"><span data-stu-id="d876c-147">-Confirm</span></span>
<span data-ttu-id="d876c-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d876c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d876c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d876c-149">-WhatIf</span></span>
<span data-ttu-id="d876c-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d876c-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d876c-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d876c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d876c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d876c-152">CommonParameters</span></span>
<span data-ttu-id="d876c-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d876c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d876c-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d876c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d876c-155">輸入</span><span class="sxs-lookup"><span data-stu-id="d876c-155">INPUTS</span></span>

### <span data-ttu-id="d876c-156">RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d876c-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="d876c-157">輸出</span><span class="sxs-lookup"><span data-stu-id="d876c-157">OUTPUTS</span></span>

### <span data-ttu-id="d876c-158">System.object</span><span class="sxs-lookup"><span data-stu-id="d876c-158">System.Object</span></span>

## <span data-ttu-id="d876c-159">筆記</span><span class="sxs-lookup"><span data-stu-id="d876c-159">NOTES</span></span>

## <span data-ttu-id="d876c-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="d876c-160">RELATED LINKS</span></span>

