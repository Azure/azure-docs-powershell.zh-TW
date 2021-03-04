---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: a69f5a3a1da8ec2ac8937793051f0361bf5e0681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916913"
---
# <span data-ttu-id="4af2a-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4af2a-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="4af2a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4af2a-102">SYNOPSIS</span></span>
<span data-ttu-id="4af2a-103">建立應用程式閘道的重寫規則。</span><span class="sxs-lookup"><span data-stu-id="4af2a-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="4af2a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4af2a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4af2a-105">描述</span><span class="sxs-lookup"><span data-stu-id="4af2a-105">DESCRIPTION</span></span>
<span data-ttu-id="4af2a-106">**New-AzApplicationGatewayRewriteRule** Cmdlet 會建立 Azure 應用程式閘道的重寫規則。</span><span class="sxs-lookup"><span data-stu-id="4af2a-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="4af2a-107">例子</span><span class="sxs-lookup"><span data-stu-id="4af2a-107">EXAMPLES</span></span>

### <span data-ttu-id="4af2a-108">範例 1：建立應用程式閘道的重寫規則</span><span class="sxs-lookup"><span data-stu-id="4af2a-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="4af2a-109">此命令會建立名為 rule1 的重寫規則，並儲存在名為 rule 的變數中$rule。</span><span class="sxs-lookup"><span data-stu-id="4af2a-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="4af2a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4af2a-110">PARAMETERS</span></span>

### <span data-ttu-id="4af2a-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="4af2a-111">-ActionSet</span></span>
<span data-ttu-id="4af2a-112">重寫規則的 ActionSet</span><span class="sxs-lookup"><span data-stu-id="4af2a-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af2a-113">-條件</span><span class="sxs-lookup"><span data-stu-id="4af2a-113">-Condition</span></span>
<span data-ttu-id="4af2a-114">重寫規則執行的條件</span><span class="sxs-lookup"><span data-stu-id="4af2a-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af2a-115">-DefaultProfile</span></span>
<span data-ttu-id="4af2a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4af2a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4af2a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4af2a-117">-Name</span></span>
<span data-ttu-id="4af2a-118">重寫規則的名稱</span><span class="sxs-lookup"><span data-stu-id="4af2a-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="4af2a-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="4af2a-119">-RuleSequence</span></span>
<span data-ttu-id="4af2a-120">重寫規則集合中此重寫規則的規則順序</span><span class="sxs-lookup"><span data-stu-id="4af2a-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af2a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af2a-121">CommonParameters</span></span>
<span data-ttu-id="4af2a-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4af2a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af2a-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4af2a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af2a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4af2a-124">INPUTS</span></span>

### <span data-ttu-id="4af2a-125">沒有</span><span class="sxs-lookup"><span data-stu-id="4af2a-125">None</span></span>

## <span data-ttu-id="4af2a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4af2a-126">OUTPUTS</span></span>

### <span data-ttu-id="4af2a-127">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4af2a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="4af2a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4af2a-128">NOTES</span></span>

## <span data-ttu-id="4af2a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4af2a-129">RELATED LINKS</span></span>

[<span data-ttu-id="4af2a-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4af2a-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4af2a-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4af2a-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4af2a-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4af2a-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4af2a-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4af2a-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4af2a-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4af2a-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4af2a-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4af2a-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="4af2a-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4af2a-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
