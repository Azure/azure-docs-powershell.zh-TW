---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 8bd540c30551451bd729126c35c4d778c700591f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914734"
---
# <span data-ttu-id="86fc7-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86fc7-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="86fc7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="86fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="86fc7-103">建立應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="86fc7-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="86fc7-104">語法</span><span class="sxs-lookup"><span data-stu-id="86fc7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86fc7-105">描述</span><span class="sxs-lookup"><span data-stu-id="86fc7-105">DESCRIPTION</span></span>
<span data-ttu-id="86fc7-106">**New-AzApplicationGatewayRewriteRuleSet** Cmdlet 會為 Azure 應用程式閘道建立重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="86fc7-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="86fc7-107">例子</span><span class="sxs-lookup"><span data-stu-id="86fc7-107">EXAMPLES</span></span>

### <span data-ttu-id="86fc7-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="86fc7-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="86fc7-109">此命令會建立名為 ruleet1 的重寫規則集，並儲存在名為 ruleet 的變數中$ruleset。</span><span class="sxs-lookup"><span data-stu-id="86fc7-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="86fc7-110">參數</span><span class="sxs-lookup"><span data-stu-id="86fc7-110">PARAMETERS</span></span>

### <span data-ttu-id="86fc7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86fc7-111">-DefaultProfile</span></span>
<span data-ttu-id="86fc7-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="86fc7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86fc7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="86fc7-113">-Name</span></span>
<span data-ttu-id="86fc7-114">RewriteRuleSet 的名稱</span><span class="sxs-lookup"><span data-stu-id="86fc7-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="86fc7-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="86fc7-115">-RewriteRule</span></span>
<span data-ttu-id="86fc7-116">重寫規則清單</span><span class="sxs-lookup"><span data-stu-id="86fc7-116">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86fc7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86fc7-117">CommonParameters</span></span>
<span data-ttu-id="86fc7-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="86fc7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86fc7-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="86fc7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86fc7-120">輸入</span><span class="sxs-lookup"><span data-stu-id="86fc7-120">INPUTS</span></span>

### <span data-ttu-id="86fc7-121">沒有</span><span class="sxs-lookup"><span data-stu-id="86fc7-121">None</span></span>

## <span data-ttu-id="86fc7-122">輸出</span><span class="sxs-lookup"><span data-stu-id="86fc7-122">OUTPUTS</span></span>

### <span data-ttu-id="86fc7-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86fc7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="86fc7-124">筆記</span><span class="sxs-lookup"><span data-stu-id="86fc7-124">NOTES</span></span>

## <span data-ttu-id="86fc7-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="86fc7-125">RELATED LINKS</span></span>

[<span data-ttu-id="86fc7-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86fc7-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="86fc7-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86fc7-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="86fc7-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86fc7-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="86fc7-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86fc7-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="86fc7-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="86fc7-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="86fc7-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="86fc7-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="86fc7-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="86fc7-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
