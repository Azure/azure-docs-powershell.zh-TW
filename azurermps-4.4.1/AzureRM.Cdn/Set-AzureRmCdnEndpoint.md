---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 70a6e57b45e1703b06343cb66d5b83b526b55063
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450014"
---
# <span data-ttu-id="246e2-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="246e2-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="246e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="246e2-102">SYNOPSIS</span></span>
<span data-ttu-id="246e2-103">更新 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="246e2-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="246e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="246e2-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="246e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="246e2-105">DESCRIPTION</span></span>
<span data-ttu-id="246e2-106">**AzureRmCdnEndpoint** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 端點。</span><span class="sxs-lookup"><span data-stu-id="246e2-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="246e2-107">示例</span><span class="sxs-lookup"><span data-stu-id="246e2-107">EXAMPLES</span></span>

## <span data-ttu-id="246e2-108">參數</span><span class="sxs-lookup"><span data-stu-id="246e2-108">PARAMETERS</span></span>

### <span data-ttu-id="246e2-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="246e2-109">-CdnEndpoint</span></span>
<span data-ttu-id="246e2-110">指定此 Cmdlet 更新的端點。</span><span class="sxs-lookup"><span data-stu-id="246e2-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="246e2-111">-確認</span><span class="sxs-lookup"><span data-stu-id="246e2-111">-Confirm</span></span>
<span data-ttu-id="246e2-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="246e2-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="246e2-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="246e2-113">-WhatIf</span></span>
<span data-ttu-id="246e2-114">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="246e2-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="246e2-115">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="246e2-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="246e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246e2-116">-DefaultProfile</span></span>
<span data-ttu-id="246e2-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="246e2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="246e2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246e2-118">CommonParameters</span></span>
<span data-ttu-id="246e2-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="246e2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246e2-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="246e2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246e2-121">輸入</span><span class="sxs-lookup"><span data-stu-id="246e2-121">INPUTS</span></span>

### <span data-ttu-id="246e2-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="246e2-122">PSEndpoint</span></span>
<span data-ttu-id="246e2-123">形參 "CdnEndpoint" 接受管線中 "PSEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="246e2-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="246e2-124">輸出</span><span class="sxs-lookup"><span data-stu-id="246e2-124">OUTPUTS</span></span>

### <span data-ttu-id="246e2-125">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="246e2-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="246e2-126">筆記</span><span class="sxs-lookup"><span data-stu-id="246e2-126">NOTES</span></span>

## <span data-ttu-id="246e2-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="246e2-127">RELATED LINKS</span></span>

[<span data-ttu-id="246e2-128">AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="246e2-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="246e2-129">新-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="246e2-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="246e2-130">移除-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="246e2-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="246e2-131">開始-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="246e2-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="246e2-132">停止 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="246e2-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


