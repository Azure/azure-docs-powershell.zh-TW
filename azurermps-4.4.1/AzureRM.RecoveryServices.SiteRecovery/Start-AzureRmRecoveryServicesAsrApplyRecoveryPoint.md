---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 50015893c3bbd45196e4dde24088fe3ce8b595c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625698"
---
# <span data-ttu-id="c82dc-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c82dc-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="c82dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c82dc-102">SYNOPSIS</span></span>
<span data-ttu-id="c82dc-103">在提交容錯移轉作業之前，變更失敗的受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="c82dc-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c82dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="c82dc-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c82dc-105">說明</span><span class="sxs-lookup"><span data-stu-id="c82dc-105">DESCRIPTION</span></span>
<span data-ttu-id="c82dc-106">在提交容錯移轉作業之前， **AzureRmRecoveryServicesAsrApplyRecoveryPoint** 會變更已失敗的受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="c82dc-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="c82dc-107">示例</span><span class="sxs-lookup"><span data-stu-id="c82dc-107">EXAMPLES</span></span>

### <span data-ttu-id="c82dc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c82dc-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="c82dc-109">開始將指定的復原點套用至複製受保護的專案，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="c82dc-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c82dc-110">參數</span><span class="sxs-lookup"><span data-stu-id="c82dc-110">PARAMETERS</span></span>

### <span data-ttu-id="c82dc-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="c82dc-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="c82dc-112">如果正在使用資料加密，指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="c82dc-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="c82dc-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="c82dc-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="c82dc-114">指定要使用資料加密的次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="c82dc-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="c82dc-115">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c82dc-115">-RecoveryPoint</span></span>
<span data-ttu-id="c82dc-116">指定對應至要套用之復原點的復原點物件。</span><span class="sxs-lookup"><span data-stu-id="c82dc-116">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82dc-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c82dc-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c82dc-118">指定 ASR 複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="c82dc-118">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c82dc-119">-確認</span><span class="sxs-lookup"><span data-stu-id="c82dc-119">-Confirm</span></span>
<span data-ttu-id="c82dc-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c82dc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c82dc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c82dc-121">-WhatIf</span></span>
<span data-ttu-id="c82dc-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c82dc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c82dc-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c82dc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c82dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c82dc-124">CommonParameters</span></span>
<span data-ttu-id="c82dc-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c82dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c82dc-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c82dc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c82dc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c82dc-127">INPUTS</span></span>

### <span data-ttu-id="c82dc-128">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c82dc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c82dc-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c82dc-129">OUTPUTS</span></span>

### <span data-ttu-id="c82dc-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c82dc-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c82dc-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c82dc-131">NOTES</span></span>

## <span data-ttu-id="c82dc-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c82dc-132">RELATED LINKS</span></span>

[<span data-ttu-id="c82dc-133">Azure Site Recovery Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c82dc-133">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
