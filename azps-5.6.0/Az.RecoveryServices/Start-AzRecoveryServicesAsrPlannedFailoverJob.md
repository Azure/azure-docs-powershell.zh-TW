---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: 78aa310d6fd3cdb7a27de066e234744b3e450520
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914694"
---
# <span data-ttu-id="133da-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="133da-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="133da-102">簡介</span><span class="sxs-lookup"><span data-stu-id="133da-102">SYNOPSIS</span></span>
<span data-ttu-id="133da-103">啟動規劃的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="133da-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="133da-104">語法</span><span class="sxs-lookup"><span data-stu-id="133da-104">SYNTAX</span></span>

### <span data-ttu-id="133da-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="133da-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="133da-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="133da-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="133da-107">描述</span><span class="sxs-lookup"><span data-stu-id="133da-107">DESCRIPTION</span></span>
<span data-ttu-id="133da-108">**Start-AzRecoveryServicesAsrPlanedFailoverJob** Cmdlet 會針對 Azure 網站復原複本受保護的專案或復原計畫啟動規劃的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="133da-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="133da-109">您可以使用 Cmdlet 檢查Get-AzRecoveryServicesAsrJob成功。</span><span class="sxs-lookup"><span data-stu-id="133da-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="133da-110">例子</span><span class="sxs-lookup"><span data-stu-id="133da-110">EXAMPLES</span></span>

### <span data-ttu-id="133da-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="133da-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="133da-112">為指定的 ASR 復原計畫啟動規劃的容錯移轉，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="133da-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="133da-113">參數</span><span class="sxs-lookup"><span data-stu-id="133da-113">PARAMETERS</span></span>

### <span data-ttu-id="133da-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="133da-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="133da-115">如果找不到虛擬機器，但無法回到主要區域 (替代位置復原中使用的區域。) 此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="133da-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="133da-116">是的</span><span class="sxs-lookup"><span data-stu-id="133da-116">Yes</span></span>
- <span data-ttu-id="133da-117">不</span><span class="sxs-lookup"><span data-stu-id="133da-117">No</span></span>

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

### <span data-ttu-id="133da-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="133da-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="133da-119">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="133da-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="133da-120">-DataEncryption二元CertFile</span><span class="sxs-lookup"><span data-stu-id="133da-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="133da-121">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="133da-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="133da-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133da-122">-DefaultProfile</span></span>
<span data-ttu-id="133da-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="133da-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="133da-124">-方向</span><span class="sxs-lookup"><span data-stu-id="133da-124">-Direction</span></span>
<span data-ttu-id="133da-125">指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="133da-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="133da-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="133da-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="133da-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="133da-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="133da-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="133da-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="133da-129">-優化</span><span class="sxs-lookup"><span data-stu-id="133da-129">-Optimize</span></span>
<span data-ttu-id="133da-130">指定優化專案。</span><span class="sxs-lookup"><span data-stu-id="133da-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="133da-131">當從 Azure 網站容錯移轉到需要大量資料同步處理之內部部署網站時，此參數會適用。</span><span class="sxs-lookup"><span data-stu-id="133da-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="133da-132">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="133da-132">Valid values are:</span></span>

- <span data-ttu-id="133da-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="133da-133">ForDowntime</span></span>
- <span data-ttu-id="133da-134">ForSynchrononization</span><span class="sxs-lookup"><span data-stu-id="133da-134">ForSynchronization</span></span>

<span data-ttu-id="133da-135">指定 **ForDowntime** 時，這表示資料在容錯移轉之前已同步處理，以將停機時間降到最低。</span><span class="sxs-lookup"><span data-stu-id="133da-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="133da-136">同步處理執行時不會關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="133da-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="133da-137">同步處理完成後，工作會暫停。</span><span class="sxs-lookup"><span data-stu-id="133da-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="133da-138">繼續執行額外的同步作業，關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="133da-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="133da-139">指定 **ForSynchronization** 時，這表示資料只在容錯移轉期間同步處理，因此資料同步處理會最小化。</span><span class="sxs-lookup"><span data-stu-id="133da-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="133da-140">啟用此設定後，虛擬機器會立即關閉。</span><span class="sxs-lookup"><span data-stu-id="133da-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="133da-141">關閉之後，同步處理即會啟動，以完成容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="133da-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="133da-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="133da-142">-RecoveryPlan</span></span>
<span data-ttu-id="133da-143">指定對應到復原計畫的 ASR 復原計畫物件以失敗。</span><span class="sxs-lookup"><span data-stu-id="133da-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="133da-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="133da-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="133da-145">指定與複製受保護的專案對應的 ASR 複製受保護的專案物件，以失敗。</span><span class="sxs-lookup"><span data-stu-id="133da-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="133da-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="133da-146">-ServicesProvider</span></span>
<span data-ttu-id="133da-147">指定對應到主機上之 ASR 服務提供者物件的 ASR 服務提供者物件，以找出要建立虛擬機器的主機，同時失敗至其他位置。</span><span class="sxs-lookup"><span data-stu-id="133da-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="133da-148">-確認</span><span class="sxs-lookup"><span data-stu-id="133da-148">-Confirm</span></span>
<span data-ttu-id="133da-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="133da-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="133da-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="133da-150">-WhatIf</span></span>
<span data-ttu-id="133da-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="133da-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="133da-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="133da-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="133da-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133da-153">CommonParameters</span></span>
<span data-ttu-id="133da-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="133da-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133da-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="133da-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133da-156">輸入</span><span class="sxs-lookup"><span data-stu-id="133da-156">INPUTS</span></span>

### <span data-ttu-id="133da-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="133da-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="133da-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="133da-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="133da-159">輸出</span><span class="sxs-lookup"><span data-stu-id="133da-159">OUTPUTS</span></span>

### <span data-ttu-id="133da-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="133da-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="133da-161">筆記</span><span class="sxs-lookup"><span data-stu-id="133da-161">NOTES</span></span>

## <span data-ttu-id="133da-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="133da-162">RELATED LINKS</span></span>
