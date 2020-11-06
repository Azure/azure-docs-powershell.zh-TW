---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e96a57a00d6314015d1d13f4f540d3f763c96c23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448032"
---
# <span data-ttu-id="f37a2-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f37a2-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="f37a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f37a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f37a2-103">啟動計畫的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="f37a2-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f37a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="f37a2-104">SYNTAX</span></span>

### <span data-ttu-id="f37a2-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="f37a2-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f37a2-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f37a2-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f37a2-107">說明</span><span class="sxs-lookup"><span data-stu-id="f37a2-107">DESCRIPTION</span></span>
<span data-ttu-id="f37a2-108">**AzureRmRecoveryServicesAsrPlannedFailoverJob** Cmdlet 會針對 Azure Site Recovery 複製受保護的專案或復原方案啟動已規劃的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="f37a2-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="f37a2-109">您可以使用 Get-AzureRmRecoveryServicesAsrJob Cmdlet 來檢查作業是否成功完成。</span><span class="sxs-lookup"><span data-stu-id="f37a2-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="f37a2-110">示例</span><span class="sxs-lookup"><span data-stu-id="f37a2-110">EXAMPLES</span></span>

### <span data-ttu-id="f37a2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f37a2-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="f37a2-112">針對指定的 ASR 恢復方案啟動已計畫的容錯移轉，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f37a2-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f37a2-113">參數</span><span class="sxs-lookup"><span data-stu-id="f37a2-113">PARAMETERS</span></span>

### <span data-ttu-id="f37a2-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="f37a2-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="f37a2-115">如果找不到在備用位置復原中使用的主要區域 (，請建立虛擬機器。 ) 此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f37a2-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f37a2-116">是的</span><span class="sxs-lookup"><span data-stu-id="f37a2-116">Yes</span></span>
- <span data-ttu-id="f37a2-117">不</span><span class="sxs-lookup"><span data-stu-id="f37a2-117">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f37a2-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f37a2-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="f37a2-119">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="f37a2-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="f37a2-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f37a2-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="f37a2-121">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="f37a2-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="f37a2-122">方向</span><span class="sxs-lookup"><span data-stu-id="f37a2-122">-Direction</span></span>
<span data-ttu-id="f37a2-123">指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="f37a2-123">Specifies the direction of the failover.</span></span>
<span data-ttu-id="f37a2-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f37a2-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f37a2-125">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f37a2-125">PrimaryToRecovery</span></span>
- <span data-ttu-id="f37a2-126">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f37a2-126">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f37a2-127">-優化</span><span class="sxs-lookup"><span data-stu-id="f37a2-127">-Optimize</span></span>
<span data-ttu-id="f37a2-128">指定要優化的專案。</span><span class="sxs-lookup"><span data-stu-id="f37a2-128">Specifies what to optimize for.</span></span>
<span data-ttu-id="f37a2-129">當從 Azure site 完成容錯移轉到需要大量資料同步處理的內部部署網站時，就會套用此參數。</span><span class="sxs-lookup"><span data-stu-id="f37a2-129">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="f37a2-130">有效值為：</span><span class="sxs-lookup"><span data-stu-id="f37a2-130">Valid values are:</span></span>

- <span data-ttu-id="f37a2-131">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="f37a2-131">ForDowntime</span></span>
- <span data-ttu-id="f37a2-132">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="f37a2-132">ForSynchronization</span></span>

<span data-ttu-id="f37a2-133">指定 **ForDowntime** 時，這表示資料在進行容錯移轉前已同步處理，以將停機時間降至最低。</span><span class="sxs-lookup"><span data-stu-id="f37a2-133">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="f37a2-134">不需關閉虛擬機器，就能執行同步處理。</span><span class="sxs-lookup"><span data-stu-id="f37a2-134">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="f37a2-135">同步處理完成後，作業就會暫停。</span><span class="sxs-lookup"><span data-stu-id="f37a2-135">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="f37a2-136">繼續工作以執行額外的同步處理操作，以關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f37a2-136">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="f37a2-137">指定 **ForSynchronization** 時，這表示資料只會在容錯移轉期間進行同步處理，因此資料同步處理會最小化。</span><span class="sxs-lookup"><span data-stu-id="f37a2-137">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="f37a2-138">如果啟用此設定，就會立即關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f37a2-138">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="f37a2-139">[關閉] 後開始進行同步處理，以完成容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="f37a2-139">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f37a2-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f37a2-140">-RecoveryPlan</span></span>
<span data-ttu-id="f37a2-141">指定對應到復原方案的 ASR 恢復方案物件，以進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="f37a2-141">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="f37a2-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f37a2-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f37a2-143">指定對應至要進行容錯移轉之複製受保護專案的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="f37a2-143">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f37a2-144">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f37a2-144">-ServicesProvider</span></span>
<span data-ttu-id="f37a2-145">透過指定 ASR services 提供者物件（與主機上執行的 ASR 服務提供程式相對應），來識別要在其上建立虛擬機器的主機（在容錯移轉到備用位置時）。</span><span class="sxs-lookup"><span data-stu-id="f37a2-145">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span> 

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f37a2-146">-確認</span><span class="sxs-lookup"><span data-stu-id="f37a2-146">-Confirm</span></span>
<span data-ttu-id="f37a2-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f37a2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f37a2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f37a2-148">-WhatIf</span></span>
<span data-ttu-id="f37a2-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f37a2-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f37a2-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f37a2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f37a2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f37a2-151">CommonParameters</span></span>
<span data-ttu-id="f37a2-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f37a2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f37a2-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f37a2-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f37a2-154">輸入</span><span class="sxs-lookup"><span data-stu-id="f37a2-154">INPUTS</span></span>

### <span data-ttu-id="f37a2-155">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f37a2-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="f37a2-156">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f37a2-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f37a2-157">輸出</span><span class="sxs-lookup"><span data-stu-id="f37a2-157">OUTPUTS</span></span>

### <span data-ttu-id="f37a2-158">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f37a2-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f37a2-159">筆記</span><span class="sxs-lookup"><span data-stu-id="f37a2-159">NOTES</span></span>

## <span data-ttu-id="f37a2-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="f37a2-160">RELATED LINKS</span></span>

