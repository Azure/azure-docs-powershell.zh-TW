---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 17836b900e56fdfd5d90211c9bceb79fce87c66e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626235"
---
# <span data-ttu-id="75803-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="75803-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="75803-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75803-102">SYNOPSIS</span></span>
<span data-ttu-id="75803-103">停止/停用 Azure Site Recovery 複製受保護的專案的複製。</span><span class="sxs-lookup"><span data-stu-id="75803-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75803-104">句法</span><span class="sxs-lookup"><span data-stu-id="75803-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75803-105">說明</span><span class="sxs-lookup"><span data-stu-id="75803-105">DESCRIPTION</span></span>
<span data-ttu-id="75803-106">**AzureRmRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會停用對指定的 Azure 網站復原複製受保護專案的複製。</span><span class="sxs-lookup"><span data-stu-id="75803-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="75803-107">這個操作會導致複製停止受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="75803-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="75803-108">示例</span><span class="sxs-lookup"><span data-stu-id="75803-108">EXAMPLES</span></span>

### <span data-ttu-id="75803-109">範例1</span><span class="sxs-lookup"><span data-stu-id="75803-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="75803-110">針對指定的複製受保護專案啟動 [停用複製] 作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="75803-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="75803-111">參數</span><span class="sxs-lookup"><span data-stu-id="75803-111">PARAMETERS</span></span>

### <span data-ttu-id="75803-112">-Force</span><span class="sxs-lookup"><span data-stu-id="75803-112">-Force</span></span>
<span data-ttu-id="75803-113">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="75803-113">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75803-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75803-114">-InputObject</span></span>
<span data-ttu-id="75803-115">Cmdlet 的輸入物件：對應到要停用複製之受複製受保護專案的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="75803-115">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75803-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="75803-116">-WaitForCompletion</span></span>
<span data-ttu-id="75803-117">指示在傳回前，該指令必須等待操作完成。</span><span class="sxs-lookup"><span data-stu-id="75803-117">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75803-118">-確認</span><span class="sxs-lookup"><span data-stu-id="75803-118">-Confirm</span></span>
<span data-ttu-id="75803-119">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="75803-119">Specify if confirmation is required.</span></span> <span data-ttu-id="75803-120">將確認參數的值設定為 [$false]，以略過確認。</span><span class="sxs-lookup"><span data-stu-id="75803-120">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="75803-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75803-121">-WhatIf</span></span>
<span data-ttu-id="75803-122">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75803-122">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="75803-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75803-123">CommonParameters</span></span>
<span data-ttu-id="75803-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75803-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75803-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75803-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75803-126">輸入</span><span class="sxs-lookup"><span data-stu-id="75803-126">INPUTS</span></span>

### <span data-ttu-id="75803-127">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="75803-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="75803-128">輸出</span><span class="sxs-lookup"><span data-stu-id="75803-128">OUTPUTS</span></span>

### <span data-ttu-id="75803-129">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="75803-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="75803-130">筆記</span><span class="sxs-lookup"><span data-stu-id="75803-130">NOTES</span></span>

## <span data-ttu-id="75803-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="75803-131">RELATED LINKS</span></span>

[<span data-ttu-id="75803-132">AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="75803-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="75803-133">新-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="75803-133">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="75803-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="75803-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
