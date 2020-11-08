---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128970"
---
# <span data-ttu-id="af23e-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="af23e-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="af23e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af23e-102">SYNOPSIS</span></span>
<span data-ttu-id="af23e-103">建立自訂規則的符合條件</span><span class="sxs-lookup"><span data-stu-id="af23e-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="af23e-104">句法</span><span class="sxs-lookup"><span data-stu-id="af23e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af23e-105">說明</span><span class="sxs-lookup"><span data-stu-id="af23e-105">DESCRIPTION</span></span>
<span data-ttu-id="af23e-106">**新的-AzApplicationGatewayFirewallCondition** 會建立防火牆自訂規則的符合條件。</span><span class="sxs-lookup"><span data-stu-id="af23e-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="af23e-107">示例</span><span class="sxs-lookup"><span data-stu-id="af23e-107">EXAMPLES</span></span>

### <span data-ttu-id="af23e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="af23e-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="af23e-109">此命令會使用 $variable 中定義的 match 變數建立新的相符條件，運算子是 Contains 且否定條件為 false，Transfroms 包括小寫和 trim，而 match 值是 abc 與 cde。</span><span class="sxs-lookup"><span data-stu-id="af23e-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="af23e-110">新的 [相符] 條件會儲存在 $condition 中。</span><span class="sxs-lookup"><span data-stu-id="af23e-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="af23e-111">參數</span><span class="sxs-lookup"><span data-stu-id="af23e-111">PARAMETERS</span></span>

### <span data-ttu-id="af23e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af23e-112">-DefaultProfile</span></span>
<span data-ttu-id="af23e-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af23e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af23e-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="af23e-114">-MatchValue</span></span>
<span data-ttu-id="af23e-115">[相符] 值。</span><span class="sxs-lookup"><span data-stu-id="af23e-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af23e-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="af23e-116">-MatchVariable</span></span>
<span data-ttu-id="af23e-117">符合變數的清單。</span><span class="sxs-lookup"><span data-stu-id="af23e-117">List of match variables.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af23e-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="af23e-118">-NegationCondition</span></span>
<span data-ttu-id="af23e-119">描述是否為 [否定] 條件。</span><span class="sxs-lookup"><span data-stu-id="af23e-119">Describes if this is negate condition or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af23e-120">-運算子</span><span class="sxs-lookup"><span data-stu-id="af23e-120">-Operator</span></span>
<span data-ttu-id="af23e-121">描述要相符的運算子。</span><span class="sxs-lookup"><span data-stu-id="af23e-121">Describes operator to be matched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith, Regex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af23e-122">-轉換</span><span class="sxs-lookup"><span data-stu-id="af23e-122">-Transform</span></span>
<span data-ttu-id="af23e-123">轉換清單。</span><span class="sxs-lookup"><span data-stu-id="af23e-123">List of transforms.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Trim, UrlDecode, UrlEncode, RemoveNulls, HtmlEntityDecode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af23e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af23e-124">CommonParameters</span></span>
<span data-ttu-id="af23e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af23e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af23e-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af23e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af23e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="af23e-127">INPUTS</span></span>

### <span data-ttu-id="af23e-128">所有</span><span class="sxs-lookup"><span data-stu-id="af23e-128">None</span></span>

## <span data-ttu-id="af23e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="af23e-129">OUTPUTS</span></span>

### <span data-ttu-id="af23e-130">PSApplicationGatewayFirewallCondition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="af23e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="af23e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="af23e-131">NOTES</span></span>

## <span data-ttu-id="af23e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="af23e-132">RELATED LINKS</span></span>
