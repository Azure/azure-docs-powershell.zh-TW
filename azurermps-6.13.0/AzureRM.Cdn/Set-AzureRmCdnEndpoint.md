---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 3705cd0b20927c4b10360b7e02d507227ef2ec53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450262"
---
# <span data-ttu-id="9a041-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a041-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="9a041-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a041-102">SYNOPSIS</span></span>
<span data-ttu-id="9a041-103">更新 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="9a041-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a041-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a041-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a041-105">說明</span><span class="sxs-lookup"><span data-stu-id="9a041-105">DESCRIPTION</span></span>
<span data-ttu-id="9a041-106">**AzureRmCdnEndpoint** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 端點。</span><span class="sxs-lookup"><span data-stu-id="9a041-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="9a041-107">示例</span><span class="sxs-lookup"><span data-stu-id="9a041-107">EXAMPLES</span></span>

## <span data-ttu-id="9a041-108">參數</span><span class="sxs-lookup"><span data-stu-id="9a041-108">PARAMETERS</span></span>

### <span data-ttu-id="9a041-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a041-109">-CdnEndpoint</span></span>
<span data-ttu-id="9a041-110">指定此 Cmdlet 更新的端點。</span><span class="sxs-lookup"><span data-stu-id="9a041-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a041-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a041-111">-DefaultProfile</span></span>
<span data-ttu-id="9a041-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9a041-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a041-113">-確認</span><span class="sxs-lookup"><span data-stu-id="9a041-113">-Confirm</span></span>
<span data-ttu-id="9a041-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a041-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a041-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a041-115">-WhatIf</span></span>
<span data-ttu-id="9a041-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a041-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a041-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a041-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a041-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a041-118">CommonParameters</span></span>
<span data-ttu-id="9a041-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a041-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a041-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a041-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a041-121">輸入</span><span class="sxs-lookup"><span data-stu-id="9a041-121">INPUTS</span></span>

### <span data-ttu-id="9a041-122">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="9a041-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="9a041-123">參數： CdnEndpoint (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9a041-123">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="9a041-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9a041-124">OUTPUTS</span></span>

### <span data-ttu-id="9a041-125">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="9a041-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9a041-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9a041-126">NOTES</span></span>

## <span data-ttu-id="9a041-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a041-127">RELATED LINKS</span></span>

[<span data-ttu-id="9a041-128">AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a041-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9a041-129">新-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a041-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9a041-130">移除-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a041-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9a041-131">開始-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a041-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9a041-132">停止 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a041-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


