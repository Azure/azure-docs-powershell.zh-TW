---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 27c90687b212c0ed41dcb080df1be5686a876725
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625408"
---
# <span data-ttu-id="21b9b-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="21b9b-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="21b9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="21b9b-103">移除 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="21b9b-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21b9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="21b9b-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21b9b-105">說明</span><span class="sxs-lookup"><span data-stu-id="21b9b-105">DESCRIPTION</span></span>
<span data-ttu-id="21b9b-106">**AzureRmSiteRecoveryProtectionContainerMapping** Cmdlet 會移除 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="21b9b-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="21b9b-107">示例</span><span class="sxs-lookup"><span data-stu-id="21b9b-107">EXAMPLES</span></span>

## <span data-ttu-id="21b9b-108">參數</span><span class="sxs-lookup"><span data-stu-id="21b9b-108">PARAMETERS</span></span>

### <span data-ttu-id="21b9b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b9b-109">-DefaultProfile</span></span>
<span data-ttu-id="21b9b-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21b9b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21b9b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="21b9b-111">-Force</span></span>
<span data-ttu-id="21b9b-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="21b9b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="21b9b-113">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="21b9b-113">-ProtectionContainerMapping</span></span>
<span data-ttu-id="21b9b-114">指定 Azure Site Recovery 保護容器對應物件。</span><span class="sxs-lookup"><span data-stu-id="21b9b-114">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21b9b-115">-確認</span><span class="sxs-lookup"><span data-stu-id="21b9b-115">-Confirm</span></span>
<span data-ttu-id="21b9b-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21b9b-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b9b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21b9b-117">-WhatIf</span></span>
<span data-ttu-id="21b9b-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21b9b-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="21b9b-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21b9b-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b9b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b9b-120">CommonParameters</span></span>
<span data-ttu-id="21b9b-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21b9b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b9b-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21b9b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b9b-123">輸入</span><span class="sxs-lookup"><span data-stu-id="21b9b-123">INPUTS</span></span>

### <span data-ttu-id="21b9b-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="21b9b-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="21b9b-125">形參 "ProtectionContainerMapping" 接受管線中 "ASRProtectionContainerMapping" 類型的值</span><span class="sxs-lookup"><span data-stu-id="21b9b-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="21b9b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="21b9b-126">OUTPUTS</span></span>

### <span data-ttu-id="21b9b-127">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="21b9b-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="21b9b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="21b9b-128">NOTES</span></span>

## <span data-ttu-id="21b9b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="21b9b-129">RELATED LINKS</span></span>

[<span data-ttu-id="21b9b-130">AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="21b9b-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="21b9b-131">新-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="21b9b-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
