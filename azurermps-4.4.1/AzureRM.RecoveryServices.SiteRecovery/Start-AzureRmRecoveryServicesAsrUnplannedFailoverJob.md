---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625098"
---
# <span data-ttu-id="3549c-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="3549c-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="3549c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3549c-102">SYNOPSIS</span></span>
<span data-ttu-id="3549c-103">啟動未計畫的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="3549c-103">Starts an unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3549c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3549c-104">SYNTAX</span></span>

### <span data-ttu-id="3549c-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="3549c-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3549c-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="3549c-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3549c-107">說明</span><span class="sxs-lookup"><span data-stu-id="3549c-107">DESCRIPTION</span></span>
<span data-ttu-id="3549c-108">**AzureRmRecoveryServicesAsrUnplannedFailoverJob** Cmdlet 會啟動 Azure Site Recovery 複製受保護的專案或復原方案的未計畫式容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="3549c-108">The **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="3549c-109">您可以使用 Get-AzureRmRecoveryServicesAsrJob Cmdlet 來檢查作業是否成功完成。</span><span class="sxs-lookup"><span data-stu-id="3549c-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="3549c-110">示例</span><span class="sxs-lookup"><span data-stu-id="3549c-110">EXAMPLES</span></span>

### <span data-ttu-id="3549c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3549c-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="3549c-112">使用指定的參數開始針對指定的復原方案啟動未計畫的容錯移轉作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="3549c-112">Starts the unplanned failover operation for the specified recovery plan using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3549c-113">參數</span><span class="sxs-lookup"><span data-stu-id="3549c-113">PARAMETERS</span></span>

### <span data-ttu-id="3549c-114">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="3549c-114">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="3549c-115">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="3549c-115">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="3549c-116">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="3549c-116">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="3549c-117">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="3549c-117">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="3549c-118">方向</span><span class="sxs-lookup"><span data-stu-id="3549c-118">-Direction</span></span>
<span data-ttu-id="3549c-119">指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="3549c-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="3549c-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3549c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3549c-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="3549c-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="3549c-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="3549c-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="3549c-123">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="3549c-123">-PerformSourceSideAction</span></span>
<span data-ttu-id="3549c-124">表示在復原方案中指定的任何來源網站作業，都必須在容錯移轉時，嘗試執行。</span><span class="sxs-lookup"><span data-stu-id="3549c-124">Indicates that any source site operations specified in the recovery plan must be attempted to be performed as part of the fail over.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3549c-125">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3549c-125">-RecoveryPlan</span></span>
<span data-ttu-id="3549c-126">指定與執行容錯移轉作業之復原方案相對應的 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="3549c-126">Specifies an ASR recovery plan object corresponding to the recovery plan on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="3549c-127">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3549c-127">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3549c-128">指定與執行容錯移轉作業之複製受保護專案相對應的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="3549c-128">Specifies the ASR replication protected item object corresponding to the replication protected item on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="3549c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="3549c-129">-Confirm</span></span>
<span data-ttu-id="3549c-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3549c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3549c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3549c-131">-WhatIf</span></span>
<span data-ttu-id="3549c-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3549c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3549c-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3549c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3549c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3549c-134">CommonParameters</span></span>
<span data-ttu-id="3549c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3549c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3549c-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3549c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3549c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3549c-137">INPUTS</span></span>

### <span data-ttu-id="3549c-138">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3549c-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="3549c-139">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3549c-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="3549c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3549c-140">OUTPUTS</span></span>

### <span data-ttu-id="3549c-141">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3549c-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3549c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="3549c-142">NOTES</span></span>

## <span data-ttu-id="3549c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="3549c-143">RELATED LINKS</span></span>

[<span data-ttu-id="3549c-144">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="3549c-144">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)


