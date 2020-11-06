---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 05fc2025b8023708f17b3494cd5568f13503eee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453331"
---
# <span data-ttu-id="01d88-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="01d88-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="01d88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01d88-102">SYNOPSIS</span></span>
<span data-ttu-id="01d88-103">刪除指定的 ASR 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="01d88-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01d88-104">句法</span><span class="sxs-lookup"><span data-stu-id="01d88-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01d88-105">說明</span><span class="sxs-lookup"><span data-stu-id="01d88-105">DESCRIPTION</span></span>
<span data-ttu-id="01d88-106">**AzureRmRecoveryServicesAsrStorageClassificationMapping** Cmdlet 會刪除指定的 Azure Site Recovery 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="01d88-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="01d88-107">示例</span><span class="sxs-lookup"><span data-stu-id="01d88-107">EXAMPLES</span></span>

### <span data-ttu-id="01d88-108">範例1</span><span class="sxs-lookup"><span data-stu-id="01d88-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="01d88-109">開始刪除指定的儲存分類對應，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="01d88-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="01d88-110">參數</span><span class="sxs-lookup"><span data-stu-id="01d88-110">PARAMETERS</span></span>

### <span data-ttu-id="01d88-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01d88-111">-InputObject</span></span>
<span data-ttu-id="01d88-112">Cmdlet 的輸入物件：與要刪除之 ASR 儲存分類對應的 ASR 儲存分類對應物件。</span><span class="sxs-lookup"><span data-stu-id="01d88-112">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01d88-113">-確認</span><span class="sxs-lookup"><span data-stu-id="01d88-113">-Confirm</span></span>
<span data-ttu-id="01d88-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="01d88-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01d88-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01d88-115">-WhatIf</span></span>
<span data-ttu-id="01d88-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01d88-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01d88-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01d88-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01d88-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d88-118">CommonParameters</span></span>
<span data-ttu-id="01d88-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01d88-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d88-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="01d88-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d88-121">輸入</span><span class="sxs-lookup"><span data-stu-id="01d88-121">INPUTS</span></span>

### <span data-ttu-id="01d88-122">RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="01d88-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="01d88-123">輸出</span><span class="sxs-lookup"><span data-stu-id="01d88-123">OUTPUTS</span></span>

### <span data-ttu-id="01d88-124">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="01d88-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="01d88-125">筆記</span><span class="sxs-lookup"><span data-stu-id="01d88-125">NOTES</span></span>

## <span data-ttu-id="01d88-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="01d88-126">RELATED LINKS</span></span>

[<span data-ttu-id="01d88-127">AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="01d88-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="01d88-128">新-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="01d88-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
