---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5a96ea5ac1ded346e289d44f54762909d5f96e31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901970"
---
# <span data-ttu-id="8bf1b-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="8bf1b-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="8bf1b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8bf1b-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf1b-103">建立新的已停用規則組組。</span><span class="sxs-lookup"><span data-stu-id="8bf1b-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="8bf1b-104">語法</span><span class="sxs-lookup"><span data-stu-id="8bf1b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bf1b-105">描述</span><span class="sxs-lookup"><span data-stu-id="8bf1b-105">DESCRIPTION</span></span>
<span data-ttu-id="8bf1b-106">**New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** Cmdlet 會建立新的停用規則組組。</span><span class="sxs-lookup"><span data-stu-id="8bf1b-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="8bf1b-107">例子</span><span class="sxs-lookup"><span data-stu-id="8bf1b-107">EXAMPLES</span></span>

### <span data-ttu-id="8bf1b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8bf1b-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="8bf1b-109">該命令會針對名為「REQUEST-942-APPLICATION-ATTACK-SQLI」的規則群組，建立一個新的已停用規則組，並停用規則 942130 和規則 942140。</span><span class="sxs-lookup"><span data-stu-id="8bf1b-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="8bf1b-110">新的已停用規則組組會儲存于 $disabledRuleGroup 1。</span><span class="sxs-lookup"><span data-stu-id="8bf1b-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="8bf1b-111">參數</span><span class="sxs-lookup"><span data-stu-id="8bf1b-111">PARAMETERS</span></span>

### <span data-ttu-id="8bf1b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf1b-112">-DefaultProfile</span></span>
<span data-ttu-id="8bf1b-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8bf1b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bf1b-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf1b-114">-RuleGroupName</span></span>
<span data-ttu-id="8bf1b-115">將會停用的規則組名。</span><span class="sxs-lookup"><span data-stu-id="8bf1b-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="8bf1b-116">-規則</span><span class="sxs-lookup"><span data-stu-id="8bf1b-116">-Rules</span></span>
<span data-ttu-id="8bf1b-117">將會停用的規則清單。</span><span class="sxs-lookup"><span data-stu-id="8bf1b-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="8bf1b-118">如果為 Null，規則組的所有規則都會停用。</span><span class="sxs-lookup"><span data-stu-id="8bf1b-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf1b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf1b-119">CommonParameters</span></span>
<span data-ttu-id="8bf1b-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8bf1b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf1b-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8bf1b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf1b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8bf1b-122">INPUTS</span></span>

### <span data-ttu-id="8bf1b-123">沒有</span><span class="sxs-lookup"><span data-stu-id="8bf1b-123">None</span></span>

## <span data-ttu-id="8bf1b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="8bf1b-124">OUTPUTS</span></span>

### <span data-ttu-id="8bf1b-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="8bf1b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="8bf1b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8bf1b-126">NOTES</span></span>

## <span data-ttu-id="8bf1b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8bf1b-127">RELATED LINKS</span></span>

[<span data-ttu-id="8bf1b-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="8bf1b-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="8bf1b-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="8bf1b-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

