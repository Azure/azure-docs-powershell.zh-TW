---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128907"
---
# <span data-ttu-id="b7e88-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="b7e88-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="b7e88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7e88-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e88-103">建立新的已停用規則群組設定。</span><span class="sxs-lookup"><span data-stu-id="b7e88-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="b7e88-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7e88-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7e88-105">說明</span><span class="sxs-lookup"><span data-stu-id="b7e88-105">DESCRIPTION</span></span>
<span data-ttu-id="b7e88-106">**新的-AzApplicationGatewayFirewallDisabledRuleGroupConfig** Cmdlet 會建立新的停用規則群組設定。</span><span class="sxs-lookup"><span data-stu-id="b7e88-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="b7e88-107">示例</span><span class="sxs-lookup"><span data-stu-id="b7e88-107">EXAMPLES</span></span>

### <span data-ttu-id="b7e88-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b7e88-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="b7e88-109">此命令會針對名為「要求-942-應用程式-SQLI」的規則群組建立新的停用規則群組設定，並停用規則942130與規則942140。</span><span class="sxs-lookup"><span data-stu-id="b7e88-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="b7e88-110">新的停用規則群組設定會儲存在 $disabledRuleGroup 1。</span><span class="sxs-lookup"><span data-stu-id="b7e88-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="b7e88-111">參數</span><span class="sxs-lookup"><span data-stu-id="b7e88-111">PARAMETERS</span></span>

### <span data-ttu-id="b7e88-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e88-112">-DefaultProfile</span></span>
<span data-ttu-id="b7e88-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7e88-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7e88-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e88-114">-RuleGroupName</span></span>
<span data-ttu-id="b7e88-115">將停用之規則群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7e88-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="b7e88-116">-規則</span><span class="sxs-lookup"><span data-stu-id="b7e88-116">-Rules</span></span>
<span data-ttu-id="b7e88-117">將停用的規則清單。</span><span class="sxs-lookup"><span data-stu-id="b7e88-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="b7e88-118">如果是 null，則會停用規則群組的所有規則。</span><span class="sxs-lookup"><span data-stu-id="b7e88-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="b7e88-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e88-119">CommonParameters</span></span>
<span data-ttu-id="b7e88-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7e88-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e88-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7e88-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e88-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b7e88-122">INPUTS</span></span>

### <span data-ttu-id="b7e88-123">所有</span><span class="sxs-lookup"><span data-stu-id="b7e88-123">None</span></span>

## <span data-ttu-id="b7e88-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b7e88-124">OUTPUTS</span></span>

### <span data-ttu-id="b7e88-125">PSApplicationGatewayFirewallDisabledRuleGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b7e88-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="b7e88-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b7e88-126">NOTES</span></span>

## <span data-ttu-id="b7e88-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7e88-127">RELATED LINKS</span></span>

[<span data-ttu-id="b7e88-128">新-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e88-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="b7e88-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e88-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

