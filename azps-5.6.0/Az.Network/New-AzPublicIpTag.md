---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 2f46b13570ef1f538658dae6d02000848822c150
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902394"
---
# <span data-ttu-id="098f9-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="098f9-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="098f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="098f9-102">SYNOPSIS</span></span>
<span data-ttu-id="098f9-103">建立 IP 標記。</span><span class="sxs-lookup"><span data-stu-id="098f9-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="098f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="098f9-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="098f9-105">描述</span><span class="sxs-lookup"><span data-stu-id="098f9-105">DESCRIPTION</span></span>
<span data-ttu-id="098f9-106">**New-AzPublicIpTag** Cmdlet 會建立 IP 標記。</span><span class="sxs-lookup"><span data-stu-id="098f9-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="098f9-107">例子</span><span class="sxs-lookup"><span data-stu-id="098f9-107">EXAMPLES</span></span>

### <span data-ttu-id="098f9-108">範例 1：建立新 IP 標記</span><span class="sxs-lookup"><span data-stu-id="098f9-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="098f9-109">此命令會使用標記類型建立新 IP 標記，例如"FirstPartyUsage"，以及類似 "/Sql" 的標記。</span><span class="sxs-lookup"><span data-stu-id="098f9-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="098f9-110">這會在 publicIpAddress 建立中使用這些特定標記來配置。</span><span class="sxs-lookup"><span data-stu-id="098f9-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="098f9-111">參數</span><span class="sxs-lookup"><span data-stu-id="098f9-111">PARAMETERS</span></span>

### <span data-ttu-id="098f9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098f9-112">-DefaultProfile</span></span>
<span data-ttu-id="098f9-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="098f9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="098f9-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="098f9-114">-IpTagType</span></span>
<span data-ttu-id="098f9-115">IpTag 類型範例：FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="098f9-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="098f9-116">-標記</span><span class="sxs-lookup"><span data-stu-id="098f9-116">-Tag</span></span>
<span data-ttu-id="098f9-117">IpTag 值範例：/Sql</span><span class="sxs-lookup"><span data-stu-id="098f9-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="098f9-118">-確認</span><span class="sxs-lookup"><span data-stu-id="098f9-118">-Confirm</span></span>
<span data-ttu-id="098f9-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="098f9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="098f9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="098f9-120">-WhatIf</span></span>
<span data-ttu-id="098f9-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="098f9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="098f9-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="098f9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="098f9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098f9-123">CommonParameters</span></span>
<span data-ttu-id="098f9-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="098f9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098f9-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="098f9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098f9-126">輸入</span><span class="sxs-lookup"><span data-stu-id="098f9-126">INPUTS</span></span>

### <span data-ttu-id="098f9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="098f9-127">System.String</span></span>

## <span data-ttu-id="098f9-128">輸出</span><span class="sxs-lookup"><span data-stu-id="098f9-128">OUTPUTS</span></span>

### <span data-ttu-id="098f9-129">Microsoft.Azure.Commands.Network.models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="098f9-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="098f9-130">筆記</span><span class="sxs-lookup"><span data-stu-id="098f9-130">NOTES</span></span>

## <span data-ttu-id="098f9-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="098f9-131">RELATED LINKS</span></span>
