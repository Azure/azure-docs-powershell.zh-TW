---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797849"
---
# <span data-ttu-id="b4c0a-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4c0a-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b4c0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c0a-103">取得應用程式閘道的重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="b4c0a-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="b4c0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4c0a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4c0a-105">說明</span><span class="sxs-lookup"><span data-stu-id="b4c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="b4c0a-106">取得應用程式閘道的重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="b4c0a-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="b4c0a-107">示例</span><span class="sxs-lookup"><span data-stu-id="b4c0a-107">EXAMPLES</span></span>

### <span data-ttu-id="b4c0a-108">範例1：取得特定的重寫規則集</span><span class="sxs-lookup"><span data-stu-id="b4c0a-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="b4c0a-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b4c0a-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b4c0a-110">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道，取得名為 RuleSet01 的重新寫入規則集。</span><span class="sxs-lookup"><span data-stu-id="b4c0a-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="b4c0a-111">參數</span><span class="sxs-lookup"><span data-stu-id="b4c0a-111">PARAMETERS</span></span>

### <span data-ttu-id="b4c0a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4c0a-112">-ApplicationGateway</span></span>
<span data-ttu-id="b4c0a-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4c0a-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4c0a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c0a-114">-DefaultProfile</span></span>
<span data-ttu-id="b4c0a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4c0a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4c0a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4c0a-116">-Name</span></span>
<span data-ttu-id="b4c0a-117">應用程式閘道 RewriteRuleSet 的名稱</span><span class="sxs-lookup"><span data-stu-id="b4c0a-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b4c0a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c0a-118">CommonParameters</span></span>
<span data-ttu-id="b4c0a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4c0a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c0a-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b4c0a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c0a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="b4c0a-121">INPUTS</span></span>

### <span data-ttu-id="b4c0a-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b4c0a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4c0a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="b4c0a-123">OUTPUTS</span></span>

### <span data-ttu-id="b4c0a-124">PSApplicationGatewayRewriteRuleSet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b4c0a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b4c0a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b4c0a-125">NOTES</span></span>

## <span data-ttu-id="b4c0a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4c0a-126">RELATED LINKS</span></span>

[<span data-ttu-id="b4c0a-127">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4c0a-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b4c0a-128">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4c0a-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b4c0a-129">移除-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4c0a-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b4c0a-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4c0a-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b4c0a-131">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b4c0a-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b4c0a-132">新-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b4c0a-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b4c0a-133">新-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4c0a-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)