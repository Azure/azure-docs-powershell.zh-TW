---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: ee39fdfcb40c394bfbd7f1d804d8d9785a63f7c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621046"
---
# <span data-ttu-id="f5000-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f5000-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="f5000-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5000-102">SYNOPSIS</span></span>
<span data-ttu-id="f5000-103">啟動計畫的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="f5000-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="f5000-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5000-104">SYNTAX</span></span>

### <span data-ttu-id="f5000-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="f5000-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5000-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f5000-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5000-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5000-107">DESCRIPTION</span></span>
<span data-ttu-id="f5000-108">**AzRecoveryServicesAsrPlannedFailoverJob** Cmdlet 會針對 Azure Site Recovery 複製受保護的專案或復原方案啟動已規劃的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="f5000-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="f5000-109">您可以使用 Get-AzRecoveryServicesAsrJob Cmdlet 來檢查作業是否成功完成。</span><span class="sxs-lookup"><span data-stu-id="f5000-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="f5000-110">示例</span><span class="sxs-lookup"><span data-stu-id="f5000-110">EXAMPLES</span></span>

### <span data-ttu-id="f5000-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f5000-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="f5000-112">針對指定的 ASR 恢復方案啟動已計畫的容錯移轉，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f5000-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f5000-113">參數</span><span class="sxs-lookup"><span data-stu-id="f5000-113">PARAMETERS</span></span>

### <span data-ttu-id="f5000-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="f5000-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="f5000-115">如果找不到在備用位置復原中使用的主要區域 (，請建立虛擬機器。 ) 此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f5000-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5000-116">是的</span><span class="sxs-lookup"><span data-stu-id="f5000-116">Yes</span></span>
- <span data-ttu-id="f5000-117">不</span><span class="sxs-lookup"><span data-stu-id="f5000-117">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5000-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f5000-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="f5000-119">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="f5000-119">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5000-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f5000-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="f5000-121">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="f5000-121">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5000-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5000-122">-DefaultProfile</span></span>
<span data-ttu-id="f5000-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5000-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f5000-124">方向</span><span class="sxs-lookup"><span data-stu-id="f5000-124">-Direction</span></span>
<span data-ttu-id="f5000-125">指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="f5000-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="f5000-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f5000-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5000-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f5000-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="f5000-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f5000-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5000-129">-優化</span><span class="sxs-lookup"><span data-stu-id="f5000-129">-Optimize</span></span>
<span data-ttu-id="f5000-130">指定要優化的專案。</span><span class="sxs-lookup"><span data-stu-id="f5000-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="f5000-131">當從 Azure 網站完成容錯移轉到需要大量資料同步處理的內部部署網站時，就會套用此參數。</span><span class="sxs-lookup"><span data-stu-id="f5000-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="f5000-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="f5000-132">Valid values are:</span></span>

- <span data-ttu-id="f5000-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="f5000-133">ForDowntime</span></span>
- <span data-ttu-id="f5000-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="f5000-134">ForSynchronization</span></span>

<span data-ttu-id="f5000-135">指定 **ForDowntime** 時，這表示資料在進行容錯移轉前已同步處理，以將停機時間降至最低。</span><span class="sxs-lookup"><span data-stu-id="f5000-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="f5000-136">不需關閉虛擬機器，就能執行同步處理。</span><span class="sxs-lookup"><span data-stu-id="f5000-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="f5000-137">同步處理完成後，作業就會暫停。</span><span class="sxs-lookup"><span data-stu-id="f5000-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="f5000-138">繼續工作以執行額外的同步處理操作，以關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f5000-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="f5000-139">指定 **ForSynchronization** 時，這表示資料只會在容錯移轉期間進行同步處理，因此資料同步處理會最小化。</span><span class="sxs-lookup"><span data-stu-id="f5000-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="f5000-140">如果啟用此設定，就會立即關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f5000-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="f5000-141">[關閉] 後開始進行同步處理，以完成容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="f5000-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5000-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f5000-142">-RecoveryPlan</span></span>
<span data-ttu-id="f5000-143">指定對應到復原方案的 ASR 恢復方案物件，以進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="f5000-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="f5000-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5000-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f5000-145">指定對應至要進行容錯移轉之複製受保護專案的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="f5000-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5000-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f5000-146">-ServicesProvider</span></span>
<span data-ttu-id="f5000-147">透過指定 ASR services 提供者物件（與主機上執行的 ASR 服務提供程式相對應），來識別要在其上建立虛擬機器的主機（在容錯移轉到備用位置時）。</span><span class="sxs-lookup"><span data-stu-id="f5000-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5000-148">-確認</span><span class="sxs-lookup"><span data-stu-id="f5000-148">-Confirm</span></span>
<span data-ttu-id="f5000-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5000-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5000-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5000-150">-WhatIf</span></span>
<span data-ttu-id="f5000-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5000-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5000-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5000-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5000-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5000-153">CommonParameters</span></span>
<span data-ttu-id="f5000-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5000-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5000-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5000-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5000-156">輸入</span><span class="sxs-lookup"><span data-stu-id="f5000-156">INPUTS</span></span>

### <span data-ttu-id="f5000-157">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f5000-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="f5000-158">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5000-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f5000-159">輸出</span><span class="sxs-lookup"><span data-stu-id="f5000-159">OUTPUTS</span></span>

### <span data-ttu-id="f5000-160">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f5000-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f5000-161">筆記</span><span class="sxs-lookup"><span data-stu-id="f5000-161">NOTES</span></span>

## <span data-ttu-id="f5000-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5000-162">RELATED LINKS</span></span>
