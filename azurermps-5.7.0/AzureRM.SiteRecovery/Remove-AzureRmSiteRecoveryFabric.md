---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 43d9603a5938ecef084191ebe77888a5f1769673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454016"
---
# <span data-ttu-id="b60b2-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b60b2-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="b60b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b60b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b60b2-103">移除 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="b60b2-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b60b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b60b2-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b60b2-105">說明</span><span class="sxs-lookup"><span data-stu-id="b60b2-105">DESCRIPTION</span></span>
<span data-ttu-id="b60b2-106">**AzureRmSiteRecoveryFabric** Cmdlet 會移除 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="b60b2-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="b60b2-107">示例</span><span class="sxs-lookup"><span data-stu-id="b60b2-107">EXAMPLES</span></span>

## <span data-ttu-id="b60b2-108">參數</span><span class="sxs-lookup"><span data-stu-id="b60b2-108">PARAMETERS</span></span>

### <span data-ttu-id="b60b2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60b2-109">-DefaultProfile</span></span>
<span data-ttu-id="b60b2-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b60b2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60b2-111">-結構</span><span class="sxs-lookup"><span data-stu-id="b60b2-111">-Fabric</span></span>
<span data-ttu-id="b60b2-112">指定 Azure Site Recovery Fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="b60b2-112">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b60b2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b60b2-113">-Force</span></span>
<span data-ttu-id="b60b2-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b60b2-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b60b2-115">-確認</span><span class="sxs-lookup"><span data-stu-id="b60b2-115">-Confirm</span></span>
<span data-ttu-id="b60b2-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b60b2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60b2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60b2-117">-WhatIf</span></span>
<span data-ttu-id="b60b2-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b60b2-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b60b2-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b60b2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60b2-120">CommonParameters</span></span>
<span data-ttu-id="b60b2-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b60b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60b2-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b60b2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60b2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b60b2-123">INPUTS</span></span>

### <span data-ttu-id="b60b2-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b60b2-124">ASRFabric</span></span>
<span data-ttu-id="b60b2-125">形參 "Fabric" 接受來自管線的 "ASRFabric" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b60b2-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="b60b2-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b60b2-126">OUTPUTS</span></span>

### <span data-ttu-id="b60b2-127">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b60b2-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b60b2-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b60b2-128">NOTES</span></span>

## <span data-ttu-id="b60b2-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b60b2-129">RELATED LINKS</span></span>

[<span data-ttu-id="b60b2-130">AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b60b2-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="b60b2-131">新-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b60b2-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
