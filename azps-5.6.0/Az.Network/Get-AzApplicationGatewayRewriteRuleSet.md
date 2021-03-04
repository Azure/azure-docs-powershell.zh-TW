---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 935e2df3de68d9ab8444cd1037d5c48951d6a335
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912786"
---
# <span data-ttu-id="2e630-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e630-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="2e630-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2e630-102">SYNOPSIS</span></span>
<span data-ttu-id="2e630-103">獲得應用程式閘道的重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="2e630-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="2e630-104">語法</span><span class="sxs-lookup"><span data-stu-id="2e630-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e630-105">描述</span><span class="sxs-lookup"><span data-stu-id="2e630-105">DESCRIPTION</span></span>
<span data-ttu-id="2e630-106">獲得應用程式閘道的重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="2e630-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="2e630-107">例子</span><span class="sxs-lookup"><span data-stu-id="2e630-107">EXAMPLES</span></span>

### <span data-ttu-id="2e630-108">範例 1：取得特定的重寫規則集</span><span class="sxs-lookup"><span data-stu-id="2e630-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="2e630-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並儲存在名為 applicationGateway01 的$AppGW。</span><span class="sxs-lookup"><span data-stu-id="2e630-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="2e630-110">第二個命令會從儲存在名為 RuleSet01 之變數的應用程式閘道中，獲得名為 RuleSet01 的重寫規則$AppGW。</span><span class="sxs-lookup"><span data-stu-id="2e630-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="2e630-111">參數</span><span class="sxs-lookup"><span data-stu-id="2e630-111">PARAMETERS</span></span>

### <span data-ttu-id="2e630-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e630-112">-ApplicationGateway</span></span>
<span data-ttu-id="2e630-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="2e630-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2e630-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e630-114">-DefaultProfile</span></span>
<span data-ttu-id="2e630-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e630-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e630-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e630-116">-Name</span></span>
<span data-ttu-id="2e630-117">應用程式閘道 RewriteRuleSet 的名稱</span><span class="sxs-lookup"><span data-stu-id="2e630-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2e630-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e630-118">CommonParameters</span></span>
<span data-ttu-id="2e630-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2e630-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e630-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e630-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e630-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2e630-121">INPUTS</span></span>

### <span data-ttu-id="2e630-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e630-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2e630-123">輸出</span><span class="sxs-lookup"><span data-stu-id="2e630-123">OUTPUTS</span></span>

### <span data-ttu-id="2e630-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e630-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="2e630-125">筆記</span><span class="sxs-lookup"><span data-stu-id="2e630-125">NOTES</span></span>

## <span data-ttu-id="2e630-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e630-126">RELATED LINKS</span></span>

[<span data-ttu-id="2e630-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e630-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2e630-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e630-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2e630-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e630-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2e630-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e630-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2e630-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2e630-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="2e630-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2e630-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="2e630-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e630-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
