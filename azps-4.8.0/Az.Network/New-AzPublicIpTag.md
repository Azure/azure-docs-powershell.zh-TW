---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 5d7d73b3c7f49babc9e80929dab7b3fa2adad20a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128929"
---
# <span data-ttu-id="b6fa4-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="b6fa4-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="b6fa4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="b6fa4-103">建立 IP 標籤。</span><span class="sxs-lookup"><span data-stu-id="b6fa4-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="b6fa4-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6fa4-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6fa4-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6fa4-105">DESCRIPTION</span></span>
<span data-ttu-id="b6fa4-106">**新的-AzPublicIpTag** Cmdlet 會建立 IP 標記。</span><span class="sxs-lookup"><span data-stu-id="b6fa4-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="b6fa4-107">示例</span><span class="sxs-lookup"><span data-stu-id="b6fa4-107">EXAMPLES</span></span>

### <span data-ttu-id="b6fa4-108">範例1：建立新的 IP 標籤</span><span class="sxs-lookup"><span data-stu-id="b6fa4-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="b6fa4-109">這個命令會使用 Tagtype （例如「FirstPartyUsage」）及標記（例如「/Sql」）來建立新的 IP 標記。</span><span class="sxs-lookup"><span data-stu-id="b6fa4-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="b6fa4-110">在 publicIpAddress 建立中使用這些特定標籤來進行分配。</span><span class="sxs-lookup"><span data-stu-id="b6fa4-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="b6fa4-111">參數</span><span class="sxs-lookup"><span data-stu-id="b6fa4-111">PARAMETERS</span></span>

### <span data-ttu-id="b6fa4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6fa4-112">-DefaultProfile</span></span>
<span data-ttu-id="b6fa4-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6fa4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6fa4-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="b6fa4-114">-IpTagType</span></span>
<span data-ttu-id="b6fa4-115">IpTag 類型範例： FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="b6fa4-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6fa4-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6fa4-116">-Tag</span></span>
<span data-ttu-id="b6fa4-117">IpTag 值範例：/Sql</span><span class="sxs-lookup"><span data-stu-id="b6fa4-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6fa4-118">-確認</span><span class="sxs-lookup"><span data-stu-id="b6fa4-118">-Confirm</span></span>
<span data-ttu-id="b6fa4-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b6fa4-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6fa4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6fa4-120">-WhatIf</span></span>
<span data-ttu-id="b6fa4-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6fa4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6fa4-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6fa4-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6fa4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6fa4-123">CommonParameters</span></span>
<span data-ttu-id="b6fa4-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6fa4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6fa4-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b6fa4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6fa4-126">輸入</span><span class="sxs-lookup"><span data-stu-id="b6fa4-126">INPUTS</span></span>

### <span data-ttu-id="b6fa4-127">System.object</span><span class="sxs-lookup"><span data-stu-id="b6fa4-127">System.String</span></span>

## <span data-ttu-id="b6fa4-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b6fa4-128">OUTPUTS</span></span>

### <span data-ttu-id="b6fa4-129">PSPublicIpTag 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b6fa4-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="b6fa4-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b6fa4-130">NOTES</span></span>

## <span data-ttu-id="b6fa4-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6fa4-131">RELATED LINKS</span></span>
