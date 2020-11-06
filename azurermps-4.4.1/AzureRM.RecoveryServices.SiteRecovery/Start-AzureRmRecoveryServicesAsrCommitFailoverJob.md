---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 590512c822bd55b992c8cc58eab4091863792e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452431"
---
# <span data-ttu-id="22dbc-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="22dbc-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="22dbc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="22dbc-103">啟動針對網站復原物件的 [確認容錯移轉] 動作。</span><span class="sxs-lookup"><span data-stu-id="22dbc-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22dbc-104">句法</span><span class="sxs-lookup"><span data-stu-id="22dbc-104">SYNTAX</span></span>

### <span data-ttu-id="22dbc-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="22dbc-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22dbc-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="22dbc-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22dbc-107">說明</span><span class="sxs-lookup"><span data-stu-id="22dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="22dbc-108">在容錯移轉作業之後， **Start AzureRmRecoveryServicesAsrCommitFailoverJob** Cmdlet 會啟動 Azure Site Recovery 物件的 commit 容錯移轉進程。</span><span class="sxs-lookup"><span data-stu-id="22dbc-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="22dbc-109">示例</span><span class="sxs-lookup"><span data-stu-id="22dbc-109">EXAMPLES</span></span>

### <span data-ttu-id="22dbc-110">範例1</span><span class="sxs-lookup"><span data-stu-id="22dbc-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="22dbc-111">針對指定的損毀修復方案啟動「確認容錯移轉」，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="22dbc-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="22dbc-112">參數</span><span class="sxs-lookup"><span data-stu-id="22dbc-112">PARAMETERS</span></span>

### <span data-ttu-id="22dbc-113">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22dbc-113">-RecoveryPlan</span></span>
<span data-ttu-id="22dbc-114">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="22dbc-114">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="22dbc-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="22dbc-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="22dbc-116">指定 ASR 複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="22dbc-116">Specifies an ASR replication protected item object.</span></span>

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

### <span data-ttu-id="22dbc-117">-確認</span><span class="sxs-lookup"><span data-stu-id="22dbc-117">-Confirm</span></span>
<span data-ttu-id="22dbc-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22dbc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22dbc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22dbc-119">-WhatIf</span></span>
<span data-ttu-id="22dbc-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22dbc-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22dbc-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22dbc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22dbc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22dbc-122">CommonParameters</span></span>
<span data-ttu-id="22dbc-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22dbc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22dbc-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22dbc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22dbc-125">輸入</span><span class="sxs-lookup"><span data-stu-id="22dbc-125">INPUTS</span></span>

### <span data-ttu-id="22dbc-126">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22dbc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="22dbc-127">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="22dbc-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="22dbc-128">輸出</span><span class="sxs-lookup"><span data-stu-id="22dbc-128">OUTPUTS</span></span>

### <span data-ttu-id="22dbc-129">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="22dbc-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="22dbc-130">筆記</span><span class="sxs-lookup"><span data-stu-id="22dbc-130">NOTES</span></span>

## <span data-ttu-id="22dbc-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="22dbc-131">RELATED LINKS</span></span>

