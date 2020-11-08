---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: d8e22f5eb0e504757bd94fa5235d07ad3e3db998
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966276"
---
# <span data-ttu-id="d339d-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="d339d-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="d339d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d339d-102">SYNOPSIS</span></span>
<span data-ttu-id="d339d-103">為應用程式閘道防火牆原則建立新的自訂規則。</span><span class="sxs-lookup"><span data-stu-id="d339d-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="d339d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d339d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d339d-105">說明</span><span class="sxs-lookup"><span data-stu-id="d339d-105">DESCRIPTION</span></span>
<span data-ttu-id="d339d-106">**新的-AzApplicationGatewayFirewallCustomRule** 會建立防火牆原則的自訂規則。</span><span class="sxs-lookup"><span data-stu-id="d339d-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="d339d-107">示例</span><span class="sxs-lookup"><span data-stu-id="d339d-107">EXAMPLES</span></span>

### <span data-ttu-id="d339d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d339d-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -matchConditons $condtion -Action Allow
```

<span data-ttu-id="d339d-109">此命令會建立新的自訂規則，並提供範例-規則、優先順序1及規則類型的 MatchRule，並在 condition 變數中定義條件，該動作將會是 allow。</span><span class="sxs-lookup"><span data-stu-id="d339d-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="d339d-110">新的 [符合自訂規則] 會儲存在 $customRule 中。</span><span class="sxs-lookup"><span data-stu-id="d339d-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="d339d-111">參數</span><span class="sxs-lookup"><span data-stu-id="d339d-111">PARAMETERS</span></span>

### <span data-ttu-id="d339d-112">-動作</span><span class="sxs-lookup"><span data-stu-id="d339d-112">-Action</span></span>
<span data-ttu-id="d339d-113">動作類型。</span><span class="sxs-lookup"><span data-stu-id="d339d-113">Type of Actions.</span></span>

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

### <span data-ttu-id="d339d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d339d-114">-DefaultProfile</span></span>
<span data-ttu-id="d339d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d339d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d339d-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="d339d-116">-MatchCondition</span></span>
<span data-ttu-id="d339d-117">符合條件的清單。</span><span class="sxs-lookup"><span data-stu-id="d339d-117">List of match conditions.</span></span>

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

### <span data-ttu-id="d339d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="d339d-118">-Name</span></span>
<span data-ttu-id="d339d-119">規則名稱。</span><span class="sxs-lookup"><span data-stu-id="d339d-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="d339d-120">-優先順序</span><span class="sxs-lookup"><span data-stu-id="d339d-120">-Priority</span></span>
<span data-ttu-id="d339d-121">描述規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="d339d-121">Describes priority of the rule.</span></span>
<span data-ttu-id="d339d-122">在具有較高值的規則之前，會先評估較低值的規則。</span><span class="sxs-lookup"><span data-stu-id="d339d-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="d339d-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="d339d-123">-RuleType</span></span>
<span data-ttu-id="d339d-124">說明規則類型。</span><span class="sxs-lookup"><span data-stu-id="d339d-124">Describes type of rule.</span></span>

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

### <span data-ttu-id="d339d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d339d-125">CommonParameters</span></span>
<span data-ttu-id="d339d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d339d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d339d-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d339d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d339d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d339d-128">INPUTS</span></span>

### <span data-ttu-id="d339d-129">所有</span><span class="sxs-lookup"><span data-stu-id="d339d-129">None</span></span>

## <span data-ttu-id="d339d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d339d-130">OUTPUTS</span></span>

### <span data-ttu-id="d339d-131">PSApplicationGatewayFirewallCustomRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d339d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="d339d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d339d-132">NOTES</span></span>

## <span data-ttu-id="d339d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d339d-133">RELATED LINKS</span></span>