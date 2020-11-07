---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: f5bf4372c1140402cb56ca875b5532387dd06704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625401"
---
# <span data-ttu-id="1175a-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1175a-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="1175a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1175a-102">SYNOPSIS</span></span>
<span data-ttu-id="1175a-103">啟動網站復原計畫的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="1175a-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1175a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1175a-104">SYNTAX</span></span>

### <span data-ttu-id="1175a-105">ByPEObject (預設) </span><span class="sxs-lookup"><span data-stu-id="1175a-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1175a-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1175a-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1175a-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="1175a-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1175a-108">說明</span><span class="sxs-lookup"><span data-stu-id="1175a-108">DESCRIPTION</span></span>
<span data-ttu-id="1175a-109">**AzureRmSiteRecoveryPlannedFailoverJob** Cmdlet 會針對 Azure Site Recovery 保護實體或復原方案啟動計畫的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="1175a-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="1175a-110">您可以使用 Get-AzureRmSiteRecoveryJob Cmdlet 來檢查作業是否成功完成。</span><span class="sxs-lookup"><span data-stu-id="1175a-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="1175a-111">示例</span><span class="sxs-lookup"><span data-stu-id="1175a-111">EXAMPLES</span></span>

## <span data-ttu-id="1175a-112">參數</span><span class="sxs-lookup"><span data-stu-id="1175a-112">PARAMETERS</span></span>

### <span data-ttu-id="1175a-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="1175a-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="1175a-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1175a-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1175a-115">是的</span><span class="sxs-lookup"><span data-stu-id="1175a-115">Yes</span></span>
- <span data-ttu-id="1175a-116">不</span><span class="sxs-lookup"><span data-stu-id="1175a-116">No</span></span>

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

### <span data-ttu-id="1175a-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1175a-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1175a-118">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="1175a-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="1175a-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1175a-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1175a-120">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="1175a-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="1175a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1175a-121">-DefaultProfile</span></span>
<span data-ttu-id="1175a-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1175a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1175a-123">方向</span><span class="sxs-lookup"><span data-stu-id="1175a-123">-Direction</span></span>
<span data-ttu-id="1175a-124">指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="1175a-124">Specifies the direction of the failover.</span></span>
<span data-ttu-id="1175a-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1175a-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1175a-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1175a-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="1175a-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1175a-127">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="1175a-128">-優化</span><span class="sxs-lookup"><span data-stu-id="1175a-128">-Optimize</span></span>
<span data-ttu-id="1175a-129">指定要優化的專案。</span><span class="sxs-lookup"><span data-stu-id="1175a-129">Specifies what to optimize for.</span></span>
<span data-ttu-id="1175a-130">當從 Azure site 完成容錯移轉到需要大量資料同步處理的內部部署網站時，就會套用此參數。</span><span class="sxs-lookup"><span data-stu-id="1175a-130">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="1175a-131">有效值為：</span><span class="sxs-lookup"><span data-stu-id="1175a-131">Valid values are:</span></span>

- <span data-ttu-id="1175a-132">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="1175a-132">ForDowntime</span></span>
- <span data-ttu-id="1175a-133">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="1175a-133">ForSynchronization</span></span>

<span data-ttu-id="1175a-134">指定 **ForDowntime** 時，這表示資料在進行容錯移轉前已同步處理，以將停機時間降至最低。</span><span class="sxs-lookup"><span data-stu-id="1175a-134">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="1175a-135">不需關閉虛擬機器，就能執行同步處理。</span><span class="sxs-lookup"><span data-stu-id="1175a-135">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="1175a-136">同步處理完成後，作業就會暫停。</span><span class="sxs-lookup"><span data-stu-id="1175a-136">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="1175a-137">繼續工作以執行額外的同步處理操作，以關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1175a-137">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="1175a-138">指定 **ForSynchronization** 時，這表示資料只會在容錯移轉期間進行同步處理，因此資料同步處理會最小化。</span><span class="sxs-lookup"><span data-stu-id="1175a-138">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="1175a-139">如果啟用此設定，就會立即關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1175a-139">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="1175a-140">[關閉] 後開始進行同步處理，以完成容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="1175a-140">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="1175a-141">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1175a-141">-ProtectionEntity</span></span>
<span data-ttu-id="1175a-142">指定網站復原保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="1175a-142">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1175a-143">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1175a-143">-RecoveryPlan</span></span>
<span data-ttu-id="1175a-144">指定復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="1175a-144">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="1175a-145">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1175a-145">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="1175a-146">-伺服器</span><span class="sxs-lookup"><span data-stu-id="1175a-146">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1175a-147">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1175a-147">-ServicesProvider</span></span>
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

### <span data-ttu-id="1175a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1175a-148">CommonParameters</span></span>
<span data-ttu-id="1175a-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1175a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1175a-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1175a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1175a-151">輸入</span><span class="sxs-lookup"><span data-stu-id="1175a-151">INPUTS</span></span>

### <span data-ttu-id="1175a-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1175a-152">ASRProtectionEntity</span></span>
<span data-ttu-id="1175a-153">形參 "ProtectionEntity" 接受管線中 "ASRProtectionEntity" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1175a-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="1175a-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1175a-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="1175a-155">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1175a-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="1175a-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1175a-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="1175a-157">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1175a-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="1175a-158">輸出</span><span class="sxs-lookup"><span data-stu-id="1175a-158">OUTPUTS</span></span>

### <span data-ttu-id="1175a-159">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1175a-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1175a-160">筆記</span><span class="sxs-lookup"><span data-stu-id="1175a-160">NOTES</span></span>

## <span data-ttu-id="1175a-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="1175a-161">RELATED LINKS</span></span>

