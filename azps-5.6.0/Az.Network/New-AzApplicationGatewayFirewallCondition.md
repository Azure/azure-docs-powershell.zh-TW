---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 096fb182ae330750eeb23e365bc929edb17b21f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916390"
---
# <span data-ttu-id="8e59b-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="8e59b-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="8e59b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8e59b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e59b-103">建立自訂規則的相符條件</span><span class="sxs-lookup"><span data-stu-id="8e59b-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="8e59b-104">語法</span><span class="sxs-lookup"><span data-stu-id="8e59b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e59b-105">描述</span><span class="sxs-lookup"><span data-stu-id="8e59b-105">DESCRIPTION</span></span>
<span data-ttu-id="8e59b-106">**New-AzApplicationGatewayFirewallCondition** 會為防火牆自訂規則建立相符條件。</span><span class="sxs-lookup"><span data-stu-id="8e59b-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="8e59b-107">例子</span><span class="sxs-lookup"><span data-stu-id="8e59b-107">EXAMPLES</span></span>

### <span data-ttu-id="8e59b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8e59b-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="8e59b-109">命令會使用 $variable 中定義的比對變數來建立新的比對條件，運算子為 Contains 且負置條件為 False，轉譯條件包括小寫和修剪，比對值為 abc 和 cde。</span><span class="sxs-lookup"><span data-stu-id="8e59b-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="8e59b-110">新的比對條件會儲存于$condition。</span><span class="sxs-lookup"><span data-stu-id="8e59b-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="8e59b-111">參數</span><span class="sxs-lookup"><span data-stu-id="8e59b-111">PARAMETERS</span></span>

### <span data-ttu-id="8e59b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e59b-112">-DefaultProfile</span></span>
<span data-ttu-id="8e59b-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e59b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e59b-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="8e59b-114">-MatchValue</span></span>
<span data-ttu-id="8e59b-115">比對值。</span><span class="sxs-lookup"><span data-stu-id="8e59b-115">Match value.</span></span>

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

### <span data-ttu-id="8e59b-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="8e59b-116">-MatchVariable</span></span>
<span data-ttu-id="8e59b-117">符合變數的清單。</span><span class="sxs-lookup"><span data-stu-id="8e59b-117">List of match variables.</span></span>

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

### <span data-ttu-id="8e59b-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="8e59b-118">-NegationCondition</span></span>
<span data-ttu-id="8e59b-119">說明這是否為否定條件。</span><span class="sxs-lookup"><span data-stu-id="8e59b-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="8e59b-120">-運算子</span><span class="sxs-lookup"><span data-stu-id="8e59b-120">-Operator</span></span>
<span data-ttu-id="8e59b-121">描述要相符的運算子。</span><span class="sxs-lookup"><span data-stu-id="8e59b-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="8e59b-122">-轉換</span><span class="sxs-lookup"><span data-stu-id="8e59b-122">-Transform</span></span>
<span data-ttu-id="8e59b-123">轉換清單。</span><span class="sxs-lookup"><span data-stu-id="8e59b-123">List of transforms.</span></span>

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

### <span data-ttu-id="8e59b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e59b-124">CommonParameters</span></span>
<span data-ttu-id="8e59b-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8e59b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e59b-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8e59b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e59b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8e59b-127">INPUTS</span></span>

### <span data-ttu-id="8e59b-128">沒有</span><span class="sxs-lookup"><span data-stu-id="8e59b-128">None</span></span>

## <span data-ttu-id="8e59b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8e59b-129">OUTPUTS</span></span>

### <span data-ttu-id="8e59b-130">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="8e59b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="8e59b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8e59b-131">NOTES</span></span>

## <span data-ttu-id="8e59b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e59b-132">RELATED LINKS</span></span>
