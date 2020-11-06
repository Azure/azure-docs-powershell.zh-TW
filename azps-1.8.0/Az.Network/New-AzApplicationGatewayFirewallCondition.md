---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: ee7f6f2b824041cf56b27c34dc70358c4229e527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621870"
---
# <span data-ttu-id="d6cb7-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="d6cb7-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="d6cb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cb7-103">建立自訂規則的符合條件</span><span class="sxs-lookup"><span data-stu-id="d6cb7-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="d6cb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6cb7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6cb7-105">說明</span><span class="sxs-lookup"><span data-stu-id="d6cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="d6cb7-106">**新的-AzApplicationGatewayFirewallCondition** 會建立防火牆自訂規則的符合條件。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="d6cb7-107">示例</span><span class="sxs-lookup"><span data-stu-id="d6cb7-107">EXAMPLES</span></span>

### <span data-ttu-id="d6cb7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d6cb7-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzureRmApplicationGatewayFirewallConditon -MatchVariables $variable -Operator Contains -NegationConditon false -Transforms Lowercase, Trim -MatchValues abc, cde
```

<span data-ttu-id="d6cb7-109">此命令會使用 $variable 中定義的 match 變數建立新的相符條件，運算子是 Contains 且否定條件為 false，Transfroms 包括小寫和 trim，而 match 值是 abc 與 cde。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="d6cb7-110">新的 [相符] 條件會儲存在 $condition 中。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="d6cb7-111">參數</span><span class="sxs-lookup"><span data-stu-id="d6cb7-111">PARAMETERS</span></span>

### <span data-ttu-id="d6cb7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6cb7-112">-DefaultProfile</span></span>
<span data-ttu-id="d6cb7-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6cb7-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="d6cb7-114">-MatchValue</span></span>
<span data-ttu-id="d6cb7-115">[相符] 值。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-115">Match value.</span></span>

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

### <span data-ttu-id="d6cb7-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="d6cb7-116">-MatchVariable</span></span>
<span data-ttu-id="d6cb7-117">符合變數的清單。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-117">List of match variables.</span></span>

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

### <span data-ttu-id="d6cb7-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="d6cb7-118">-NegationCondition</span></span>
<span data-ttu-id="d6cb7-119">描述是否為 [否定] 條件。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="d6cb7-120">-運算子</span><span class="sxs-lookup"><span data-stu-id="d6cb7-120">-Operator</span></span>
<span data-ttu-id="d6cb7-121">描述要相符的運算子。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="d6cb7-122">-轉換</span><span class="sxs-lookup"><span data-stu-id="d6cb7-122">-Transform</span></span>
<span data-ttu-id="d6cb7-123">轉換清單。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-123">List of transforms.</span></span>

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

### <span data-ttu-id="d6cb7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cb7-124">CommonParameters</span></span>
<span data-ttu-id="d6cb7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cb7-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d6cb7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cb7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d6cb7-127">INPUTS</span></span>

### <span data-ttu-id="d6cb7-128">所有</span><span class="sxs-lookup"><span data-stu-id="d6cb7-128">None</span></span>

## <span data-ttu-id="d6cb7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d6cb7-129">OUTPUTS</span></span>

### <span data-ttu-id="d6cb7-130">PSApplicationGatewayFirewallCondition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d6cb7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="d6cb7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d6cb7-131">NOTES</span></span>

## <span data-ttu-id="d6cb7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6cb7-132">RELATED LINKS</span></span>