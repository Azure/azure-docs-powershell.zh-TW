---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 9c336602aebdb82e4860ee744fb99f3a6fbf5a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446063"
---
# <span data-ttu-id="e6de8-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="e6de8-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="e6de8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6de8-102">SYNOPSIS</span></span>
<span data-ttu-id="e6de8-103">開始複製重新同步。</span><span class="sxs-lookup"><span data-stu-id="e6de8-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6de8-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6de8-104">SYNTAX</span></span>

### <span data-ttu-id="e6de8-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="e6de8-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6de8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6de8-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6de8-107">說明</span><span class="sxs-lookup"><span data-stu-id="e6de8-107">DESCRIPTION</span></span>
<span data-ttu-id="e6de8-108">如果受保護的狀態為重新同步需要的狀態，則 **AzureRmRecoveryServicesAsrResynchronizeReplicationJob** Cmdlet 會開始重新同步複製指定的受保護專案。</span><span class="sxs-lookup"><span data-stu-id="e6de8-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="e6de8-109">示例</span><span class="sxs-lookup"><span data-stu-id="e6de8-109">EXAMPLES</span></span>

### <span data-ttu-id="e6de8-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e6de8-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="e6de8-111">啟動工作以在已傳送的複製受保護的專案上重新同步處理複製。</span><span class="sxs-lookup"><span data-stu-id="e6de8-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="e6de8-112">參數</span><span class="sxs-lookup"><span data-stu-id="e6de8-112">PARAMETERS</span></span>

### <span data-ttu-id="e6de8-113">-確認</span><span class="sxs-lookup"><span data-stu-id="e6de8-113">-Confirm</span></span>
<span data-ttu-id="e6de8-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6de8-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6de8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6de8-115">-DefaultProfile</span></span>
<span data-ttu-id="e6de8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6de8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6de8-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6de8-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e6de8-118">要重新同步複製的 ASR 複製受保護專案。</span><span class="sxs-lookup"><span data-stu-id="e6de8-118">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6de8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6de8-119">-ResourceId</span></span>
<span data-ttu-id="e6de8-120">要重新同步複製受保護專案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6de8-120">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6de8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6de8-121">-WhatIf</span></span>
<span data-ttu-id="e6de8-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6de8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6de8-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6de8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6de8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6de8-124">CommonParameters</span></span>
<span data-ttu-id="e6de8-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6de8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6de8-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6de8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6de8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e6de8-127">INPUTS</span></span>

### <span data-ttu-id="e6de8-128">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6de8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e6de8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e6de8-129">OUTPUTS</span></span>

### <span data-ttu-id="e6de8-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e6de8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e6de8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e6de8-131">NOTES</span></span>

## <span data-ttu-id="e6de8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6de8-132">RELATED LINKS</span></span>
