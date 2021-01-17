---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286967"
---
# <span data-ttu-id="ff208-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff208-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="ff208-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff208-102">SYNOPSIS</span></span>
<span data-ttu-id="ff208-103">建立應用程式閘道的重寫規則頭設定。</span><span class="sxs-lookup"><span data-stu-id="ff208-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="ff208-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff208-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff208-105">說明</span><span class="sxs-lookup"><span data-stu-id="ff208-105">DESCRIPTION</span></span>
<span data-ttu-id="ff208-106">**AzApplicationGatewayRewriteRuleHeaderConfiguration** Cmdlet 會建立 Azure 應用程式閘道的重寫規則動作集。</span><span class="sxs-lookup"><span data-stu-id="ff208-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="ff208-107">示例</span><span class="sxs-lookup"><span data-stu-id="ff208-107">EXAMPLES</span></span>

### <span data-ttu-id="ff208-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ff208-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="ff208-109">這個命令會建立重寫規則頭設定，並將結果儲存在名為 $hc 的變數中。</span><span class="sxs-lookup"><span data-stu-id="ff208-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="ff208-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff208-110">PARAMETERS</span></span>

### <span data-ttu-id="ff208-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff208-111">-DefaultProfile</span></span>
<span data-ttu-id="ff208-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff208-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff208-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="ff208-113">-HeaderName</span></span>
<span data-ttu-id="ff208-114">要重寫之標頭的名稱</span><span class="sxs-lookup"><span data-stu-id="ff208-114">Name of the Header to rewrite</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff208-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="ff208-115">-HeaderValue</span></span>
<span data-ttu-id="ff208-116">指定標頭名稱之集合的標頭值。</span><span class="sxs-lookup"><span data-stu-id="ff208-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="ff208-117">如果省略此選項，則會刪除頁首</span><span class="sxs-lookup"><span data-stu-id="ff208-117">Header will be deleted if this is omitted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff208-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff208-118">CommonParameters</span></span>
<span data-ttu-id="ff208-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff208-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff208-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff208-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff208-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ff208-121">INPUTS</span></span>

### <span data-ttu-id="ff208-122">所有</span><span class="sxs-lookup"><span data-stu-id="ff208-122">None</span></span>

## <span data-ttu-id="ff208-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ff208-123">OUTPUTS</span></span>

### <span data-ttu-id="ff208-124">PSApplicationGatewayHeaderConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ff208-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="ff208-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ff208-125">NOTES</span></span>

## <span data-ttu-id="ff208-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff208-126">RELATED LINKS</span></span>

[<span data-ttu-id="ff208-127">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff208-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ff208-128">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff208-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ff208-129">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff208-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ff208-130">移除-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff208-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ff208-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff208-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ff208-132">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ff208-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="ff208-133">新-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ff208-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
