---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: f3cd7edf0def90f4245e20c540332d08e045865f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902874"
---
# <span data-ttu-id="428ae-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="428ae-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="428ae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="428ae-102">SYNOPSIS</span></span>
<span data-ttu-id="428ae-103">為應用程式閘道防火牆原則建立新自訂規則。</span><span class="sxs-lookup"><span data-stu-id="428ae-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="428ae-104">語法</span><span class="sxs-lookup"><span data-stu-id="428ae-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="428ae-105">描述</span><span class="sxs-lookup"><span data-stu-id="428ae-105">DESCRIPTION</span></span>
<span data-ttu-id="428ae-106">**New-AzApplicationGatewayFirewallCustomRule** 會建立防火牆原則的自訂規則。</span><span class="sxs-lookup"><span data-stu-id="428ae-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="428ae-107">例子</span><span class="sxs-lookup"><span data-stu-id="428ae-107">EXAMPLES</span></span>

### <span data-ttu-id="428ae-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="428ae-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="428ae-109">命令會建立一個新的自訂規則，其中名稱為範例規則、優先順序 1，而規則類型為 MatchRule 且條件變數中定義的條件，則動作會允許。</span><span class="sxs-lookup"><span data-stu-id="428ae-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="428ae-110">新的比對自訂規則會儲存于$customRule。</span><span class="sxs-lookup"><span data-stu-id="428ae-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="428ae-111">參數</span><span class="sxs-lookup"><span data-stu-id="428ae-111">PARAMETERS</span></span>

### <span data-ttu-id="428ae-112">-動作</span><span class="sxs-lookup"><span data-stu-id="428ae-112">-Action</span></span>
<span data-ttu-id="428ae-113">動作類型。</span><span class="sxs-lookup"><span data-stu-id="428ae-113">Type of Actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428ae-114">-DefaultProfile</span></span>
<span data-ttu-id="428ae-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="428ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428ae-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="428ae-116">-MatchCondition</span></span>
<span data-ttu-id="428ae-117">符合條件的清單。</span><span class="sxs-lookup"><span data-stu-id="428ae-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428ae-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="428ae-118">-Name</span></span>
<span data-ttu-id="428ae-119">規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="428ae-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="428ae-120">-優先順序</span><span class="sxs-lookup"><span data-stu-id="428ae-120">-Priority</span></span>
<span data-ttu-id="428ae-121">說明規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="428ae-121">Describes priority of the rule.</span></span>
<span data-ttu-id="428ae-122">值較低的規則會先評估，再評估值較高的規則。</span><span class="sxs-lookup"><span data-stu-id="428ae-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428ae-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="428ae-123">-RuleType</span></span>
<span data-ttu-id="428ae-124">描述規則類型。</span><span class="sxs-lookup"><span data-stu-id="428ae-124">Describes type of rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428ae-125">CommonParameters</span></span>
<span data-ttu-id="428ae-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="428ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428ae-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="428ae-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428ae-128">輸入</span><span class="sxs-lookup"><span data-stu-id="428ae-128">INPUTS</span></span>

### <span data-ttu-id="428ae-129">沒有</span><span class="sxs-lookup"><span data-stu-id="428ae-129">None</span></span>

## <span data-ttu-id="428ae-130">輸出</span><span class="sxs-lookup"><span data-stu-id="428ae-130">OUTPUTS</span></span>

### <span data-ttu-id="428ae-131">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="428ae-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="428ae-132">筆記</span><span class="sxs-lookup"><span data-stu-id="428ae-132">NOTES</span></span>

## <span data-ttu-id="428ae-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="428ae-133">RELATED LINKS</span></span>
