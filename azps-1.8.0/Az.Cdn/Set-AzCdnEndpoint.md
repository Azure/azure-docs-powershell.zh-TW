---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: cce3e2f9deb1f5df5c85d4f0b289b97e9cd36820
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622845"
---
# <span data-ttu-id="bbc7d-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbc7d-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="bbc7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbc7d-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc7d-103">更新 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="bbc7d-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="bbc7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbc7d-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbc7d-105">說明</span><span class="sxs-lookup"><span data-stu-id="bbc7d-105">DESCRIPTION</span></span>
<span data-ttu-id="bbc7d-106">**AzCdnEndpoint** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 端點。</span><span class="sxs-lookup"><span data-stu-id="bbc7d-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bbc7d-107">示例</span><span class="sxs-lookup"><span data-stu-id="bbc7d-107">EXAMPLES</span></span>

## <span data-ttu-id="bbc7d-108">參數</span><span class="sxs-lookup"><span data-stu-id="bbc7d-108">PARAMETERS</span></span>

### <span data-ttu-id="bbc7d-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbc7d-109">-CdnEndpoint</span></span>
<span data-ttu-id="bbc7d-110">指定此 Cmdlet 更新的端點。</span><span class="sxs-lookup"><span data-stu-id="bbc7d-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="bbc7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc7d-111">-DefaultProfile</span></span>
<span data-ttu-id="bbc7d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bbc7d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbc7d-113">-確認</span><span class="sxs-lookup"><span data-stu-id="bbc7d-113">-Confirm</span></span>
<span data-ttu-id="bbc7d-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bbc7d-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbc7d-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc7d-115">-WhatIf</span></span>
<span data-ttu-id="bbc7d-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bbc7d-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc7d-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bbc7d-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbc7d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc7d-118">CommonParameters</span></span>
<span data-ttu-id="bbc7d-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbc7d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc7d-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbc7d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc7d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="bbc7d-121">INPUTS</span></span>

### <span data-ttu-id="bbc7d-122">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="bbc7d-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="bbc7d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="bbc7d-123">OUTPUTS</span></span>

### <span data-ttu-id="bbc7d-124">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="bbc7d-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="bbc7d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bbc7d-125">NOTES</span></span>

## <span data-ttu-id="bbc7d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbc7d-126">RELATED LINKS</span></span>

[<span data-ttu-id="bbc7d-127">AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbc7d-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="bbc7d-128">新-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbc7d-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="bbc7d-129">移除-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbc7d-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="bbc7d-130">開始-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbc7d-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="bbc7d-131">停止 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbc7d-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


