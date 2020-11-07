---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 3587005559849072d973242eb6af221c0b8b0557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789017"
---
# <span data-ttu-id="583fe-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="583fe-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="583fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="583fe-102">SYNOPSIS</span></span>
<span data-ttu-id="583fe-103">修改應用程式閘道的重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="583fe-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="583fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="583fe-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="583fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="583fe-105">DESCRIPTION</span></span>
<span data-ttu-id="583fe-106">**AzApplicationGatewayRewriteRuleSet** Cmdlet 會修改要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="583fe-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="583fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="583fe-107">EXAMPLES</span></span>

### <span data-ttu-id="583fe-108">範例1</span><span class="sxs-lookup"><span data-stu-id="583fe-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="583fe-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="583fe-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="583fe-110">第二個命令會修改應用程式閘道的重寫規則集，以使用 $rule 變數中指定的重寫規則。</span><span class="sxs-lookup"><span data-stu-id="583fe-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="583fe-111">參數</span><span class="sxs-lookup"><span data-stu-id="583fe-111">PARAMETERS</span></span>

### <span data-ttu-id="583fe-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="583fe-112">-ApplicationGateway</span></span>
<span data-ttu-id="583fe-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="583fe-113">The applicationGateway</span></span>

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

### <span data-ttu-id="583fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="583fe-114">-DefaultProfile</span></span>
<span data-ttu-id="583fe-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="583fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="583fe-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="583fe-116">-Name</span></span>
<span data-ttu-id="583fe-117">RewriteRuleSet 的名稱</span><span class="sxs-lookup"><span data-stu-id="583fe-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="583fe-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="583fe-118">-RewriteRule</span></span>
<span data-ttu-id="583fe-119">重新寫入規則的清單</span><span class="sxs-lookup"><span data-stu-id="583fe-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="583fe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583fe-120">CommonParameters</span></span>
<span data-ttu-id="583fe-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="583fe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583fe-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="583fe-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583fe-123">輸入</span><span class="sxs-lookup"><span data-stu-id="583fe-123">INPUTS</span></span>

### <span data-ttu-id="583fe-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="583fe-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="583fe-125">輸出</span><span class="sxs-lookup"><span data-stu-id="583fe-125">OUTPUTS</span></span>

### <span data-ttu-id="583fe-126">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="583fe-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="583fe-127">筆記</span><span class="sxs-lookup"><span data-stu-id="583fe-127">NOTES</span></span>

## <span data-ttu-id="583fe-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="583fe-128">RELATED LINKS</span></span>

[<span data-ttu-id="583fe-129">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="583fe-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="583fe-130">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="583fe-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="583fe-131">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="583fe-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="583fe-132">移除-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="583fe-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="583fe-133">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="583fe-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="583fe-134">新-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="583fe-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="583fe-135">新-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="583fe-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
