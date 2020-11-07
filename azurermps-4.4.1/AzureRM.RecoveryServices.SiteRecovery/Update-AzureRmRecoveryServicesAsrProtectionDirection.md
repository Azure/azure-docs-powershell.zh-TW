---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625092"
---
# <span data-ttu-id="13e71-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="13e71-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="13e71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13e71-102">SYNOPSIS</span></span>
<span data-ttu-id="13e71-103">更新指定的複製受保護專案或復原方案的複製方向。</span><span class="sxs-lookup"><span data-stu-id="13e71-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="13e71-104">用來重新保護/反向複製失敗的複製專案或復原方案。</span><span class="sxs-lookup"><span data-stu-id="13e71-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13e71-105">句法</span><span class="sxs-lookup"><span data-stu-id="13e71-105">SYNTAX</span></span>

### <span data-ttu-id="13e71-106">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="13e71-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13e71-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="13e71-107">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13e71-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="13e71-108">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13e71-109">說明</span><span class="sxs-lookup"><span data-stu-id="13e71-109">DESCRIPTION</span></span>
<span data-ttu-id="13e71-110">**AzureRmRecoveryServicesAsrProtectionDirection** Cmdlet 會在完成認可式容錯移轉作業之後，更新指定 Azure Site Recovery 物件的複製方向。</span><span class="sxs-lookup"><span data-stu-id="13e71-110">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="13e71-111">示例</span><span class="sxs-lookup"><span data-stu-id="13e71-111">EXAMPLES</span></span>

### <span data-ttu-id="13e71-112">範例1</span><span class="sxs-lookup"><span data-stu-id="13e71-112">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="13e71-113">啟動指定 recoveyr 方案的更新方向作業，並傳回用於追蹤作業的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="13e71-113">Start the update direction operation for the specified recoveyr plan and returns the ASR job object used to track the operation.</span></span>

## <span data-ttu-id="13e71-114">參數</span><span class="sxs-lookup"><span data-stu-id="13e71-114">PARAMETERS</span></span>

### <span data-ttu-id="13e71-115">方向</span><span class="sxs-lookup"><span data-stu-id="13e71-115">-Direction</span></span>
<span data-ttu-id="13e71-116">指定要用於在容錯移轉後進行更新操作的方向。</span><span class="sxs-lookup"><span data-stu-id="13e71-116">Specifies the direction to be used for the update operation post a failover.</span></span>  
<span data-ttu-id="13e71-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="13e71-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13e71-118">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="13e71-118">PrimaryToRecovery</span></span>
- <span data-ttu-id="13e71-119">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="13e71-119">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="13e71-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="13e71-120">-RecoveryPlan</span></span>
<span data-ttu-id="13e71-121">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="13e71-121">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="13e71-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="13e71-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="13e71-123">指定 ASR 複製受保護的專案</span><span class="sxs-lookup"><span data-stu-id="13e71-123">Specifies an ASR replication protected item</span></span>

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

### <span data-ttu-id="13e71-124">-確認</span><span class="sxs-lookup"><span data-stu-id="13e71-124">-Confirm</span></span>
<span data-ttu-id="13e71-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13e71-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13e71-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13e71-126">-WhatIf</span></span>
<span data-ttu-id="13e71-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13e71-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13e71-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13e71-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13e71-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e71-129">CommonParameters</span></span>
<span data-ttu-id="13e71-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13e71-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e71-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13e71-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e71-132">輸入</span><span class="sxs-lookup"><span data-stu-id="13e71-132">INPUTS</span></span>

### <span data-ttu-id="13e71-133">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="13e71-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="13e71-134">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="13e71-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="13e71-135">輸出</span><span class="sxs-lookup"><span data-stu-id="13e71-135">OUTPUTS</span></span>

### <span data-ttu-id="13e71-136">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="13e71-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="13e71-137">筆記</span><span class="sxs-lookup"><span data-stu-id="13e71-137">NOTES</span></span>

## <span data-ttu-id="13e71-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="13e71-138">RELATED LINKS</span></span>

