---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 3d26a5285fbe96c0e77c56819567e21820cddf4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624785"
---
# <span data-ttu-id="2f5c9-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2f5c9-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="2f5c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5c9-103">刪除指定的 Azure Site Recovery 防護容器對應。</span><span class="sxs-lookup"><span data-stu-id="2f5c9-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f5c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f5c9-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f5c9-105">說明</span><span class="sxs-lookup"><span data-stu-id="2f5c9-105">DESCRIPTION</span></span>
<span data-ttu-id="2f5c9-106">**AzureRmRecoveryServicesAsrProtectionContainerMapping** Cmdlet 會刪除指定的 Azure Site Recovery 防護容器對應。</span><span class="sxs-lookup"><span data-stu-id="2f5c9-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="2f5c9-107">示例</span><span class="sxs-lookup"><span data-stu-id="2f5c9-107">EXAMPLES</span></span>

### <span data-ttu-id="2f5c9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2f5c9-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="2f5c9-109">開始刪除指定的保護容器對應，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="2f5c9-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2f5c9-110">參數</span><span class="sxs-lookup"><span data-stu-id="2f5c9-110">PARAMETERS</span></span>

### <span data-ttu-id="2f5c9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2f5c9-111">-Force</span></span>
<span data-ttu-id="2f5c9-112">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="2f5c9-112">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="2f5c9-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f5c9-113">-InputObject</span></span>
<span data-ttu-id="2f5c9-114">Cmdlet 的輸入物件：與要刪除之保護容器相對應的 ASR 保護容器對應物件。</span><span class="sxs-lookup"><span data-stu-id="2f5c9-114">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f5c9-115">-確認</span><span class="sxs-lookup"><span data-stu-id="2f5c9-115">-Confirm</span></span>
<span data-ttu-id="2f5c9-116">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="2f5c9-116">Specify if confirmation is required.</span></span> <span data-ttu-id="2f5c9-117">將確認參數的值設定為 $false，以略過確認</span><span class="sxs-lookup"><span data-stu-id="2f5c9-117">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="2f5c9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f5c9-118">-WhatIf</span></span>
<span data-ttu-id="2f5c9-119">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f5c9-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="2f5c9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5c9-120">CommonParameters</span></span>
<span data-ttu-id="2f5c9-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f5c9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5c9-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f5c9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5c9-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2f5c9-123">INPUTS</span></span>

### <span data-ttu-id="2f5c9-124">RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2f5c9-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="2f5c9-125">輸出</span><span class="sxs-lookup"><span data-stu-id="2f5c9-125">OUTPUTS</span></span>

### <span data-ttu-id="2f5c9-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2f5c9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2f5c9-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2f5c9-127">NOTES</span></span>

## <span data-ttu-id="2f5c9-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f5c9-128">RELATED LINKS</span></span>

[<span data-ttu-id="2f5c9-129">AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2f5c9-129">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="2f5c9-130">新-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2f5c9-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
