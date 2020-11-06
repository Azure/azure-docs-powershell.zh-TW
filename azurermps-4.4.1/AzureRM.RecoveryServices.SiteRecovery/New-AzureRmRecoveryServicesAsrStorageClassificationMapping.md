---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 14cd1606bc4c8d1709b0ddd64e845a2e84b26df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448038"
---
# <span data-ttu-id="a9ea5-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="a9ea5-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="a9ea5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ea5-103">在 [恢復服務] 保存庫中建立 ASR 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9ea5-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9ea5-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9ea5-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9ea5-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ea5-106">**AzureRmRecoveryServicesAsrStorageClassificationMapping** Cmdlet 會建立 [恢復服務] 保存庫的儲存分類。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="a9ea5-107">示例</span><span class="sxs-lookup"><span data-stu-id="a9ea5-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ea5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a9ea5-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="a9ea5-109">使用指定的參數啟動儲存分類對應建立作業，並傳回用來追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a9ea5-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9ea5-110">PARAMETERS</span></span>

### <span data-ttu-id="a9ea5-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9ea5-111">-Name</span></span>
<span data-ttu-id="a9ea5-112">指定 ASR 儲存分類對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-112">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ea5-113">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="a9ea5-113">-PrimaryStorageClassification</span></span>
<span data-ttu-id="a9ea5-114">指定對應的主要 ASR 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-114">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ea5-115">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="a9ea5-115">-RecoveryStorageClassification</span></span>
<span data-ttu-id="a9ea5-116">指定對應的 [恢復 ASR] 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-116">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ea5-117">-確認</span><span class="sxs-lookup"><span data-stu-id="a9ea5-117">-Confirm</span></span>
<span data-ttu-id="a9ea5-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ea5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ea5-119">-WhatIf</span></span>
<span data-ttu-id="a9ea5-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9ea5-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9ea5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ea5-122">CommonParameters</span></span>
<span data-ttu-id="a9ea5-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ea5-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9ea5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ea5-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a9ea5-125">INPUTS</span></span>

### <span data-ttu-id="a9ea5-126">RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="a9ea5-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="a9ea5-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a9ea5-127">OUTPUTS</span></span>

### <span data-ttu-id="a9ea5-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a9ea5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a9ea5-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a9ea5-129">NOTES</span></span>

## <span data-ttu-id="a9ea5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9ea5-130">RELATED LINKS</span></span>

[<span data-ttu-id="a9ea5-131">AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="a9ea5-131">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="a9ea5-132">移除-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="a9ea5-132">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
