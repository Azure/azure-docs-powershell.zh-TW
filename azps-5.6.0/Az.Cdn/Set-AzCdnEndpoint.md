---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 4270f7c9781ef960cdbb20a8a067a3dc22255723
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913585"
---
# <span data-ttu-id="2dc61-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc61-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="2dc61-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2dc61-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc61-103">更新 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="2dc61-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="2dc61-104">語法</span><span class="sxs-lookup"><span data-stu-id="2dc61-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2dc61-105">描述</span><span class="sxs-lookup"><span data-stu-id="2dc61-105">DESCRIPTION</span></span>
<span data-ttu-id="2dc61-106">**Set-AzCdnEndpoint** Cmdlet 會更新 AZURE 內容傳遞網路 (CDN) 端點。</span><span class="sxs-lookup"><span data-stu-id="2dc61-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2dc61-107">例子</span><span class="sxs-lookup"><span data-stu-id="2dc61-107">EXAMPLES</span></span>

## <span data-ttu-id="2dc61-108">參數</span><span class="sxs-lookup"><span data-stu-id="2dc61-108">PARAMETERS</span></span>

### <span data-ttu-id="2dc61-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc61-109">-CdnEndpoint</span></span>
<span data-ttu-id="2dc61-110">指定此 Cmdlet 更新的端點。</span><span class="sxs-lookup"><span data-stu-id="2dc61-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="2dc61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc61-111">-DefaultProfile</span></span>
<span data-ttu-id="2dc61-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2dc61-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dc61-113">-確認</span><span class="sxs-lookup"><span data-stu-id="2dc61-113">-Confirm</span></span>
<span data-ttu-id="2dc61-114">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2dc61-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dc61-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dc61-115">-WhatIf</span></span>
<span data-ttu-id="2dc61-116">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2dc61-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dc61-117">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2dc61-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dc61-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc61-118">CommonParameters</span></span>
<span data-ttu-id="2dc61-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2dc61-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc61-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dc61-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc61-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2dc61-121">INPUTS</span></span>

### <span data-ttu-id="2dc61-122">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc61-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2dc61-123">輸出</span><span class="sxs-lookup"><span data-stu-id="2dc61-123">OUTPUTS</span></span>

### <span data-ttu-id="2dc61-124">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc61-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2dc61-125">筆記</span><span class="sxs-lookup"><span data-stu-id="2dc61-125">NOTES</span></span>

## <span data-ttu-id="2dc61-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="2dc61-126">RELATED LINKS</span></span>

[<span data-ttu-id="2dc61-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc61-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="2dc61-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc61-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="2dc61-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc61-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="2dc61-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc61-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="2dc61-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc61-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


