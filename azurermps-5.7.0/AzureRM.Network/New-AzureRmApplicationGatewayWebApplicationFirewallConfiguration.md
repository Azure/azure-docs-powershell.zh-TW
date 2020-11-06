---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bcc40b77208506712a319d7f43d74f8928e18927
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447043"
---
# <span data-ttu-id="313f0-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="313f0-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="313f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="313f0-102">SYNOPSIS</span></span>
<span data-ttu-id="313f0-103">建立應用程式閘道的 WAF 配置。</span><span class="sxs-lookup"><span data-stu-id="313f0-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="313f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="313f0-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="313f0-105">說明</span><span class="sxs-lookup"><span data-stu-id="313f0-105">DESCRIPTION</span></span>
<span data-ttu-id="313f0-106">**新的-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet 會建立 web 應用程式防火牆 (WAF Azure 應用程式閘道的) 設定。</span><span class="sxs-lookup"><span data-stu-id="313f0-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="313f0-107">示例</span><span class="sxs-lookup"><span data-stu-id="313f0-107">EXAMPLES</span></span>

### <span data-ttu-id="313f0-108">範例1：建立應用程式閘道的 web 應用程式防火牆設定</span><span class="sxs-lookup"><span data-stu-id="313f0-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="313f0-109">第一個命令會針對名為「要求-942-應用程式-SQLI」的規則群組建立新的已停用規則群組設定，並停用規則942130與規則942140。</span><span class="sxs-lookup"><span data-stu-id="313f0-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="313f0-110">第二個命令會針對名為「要求 921--通訊協定-PROTOCOL」的規則群組，建立另一個停用的規則群組設定。</span><span class="sxs-lookup"><span data-stu-id="313f0-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="313f0-111">不會明確傳遞任何規則，因此規則群組的所有規則都將停用。</span><span class="sxs-lookup"><span data-stu-id="313f0-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="313f0-112">最後一個命令接著會建立 WAF 設定，並停用防火牆規則，$disabledRuleGroup 1 和 $disabledRuleGroup 2 中已設定。</span><span class="sxs-lookup"><span data-stu-id="313f0-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="313f0-113">新的 WAF 設定會儲存在 $firewallConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="313f0-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="313f0-114">參數</span><span class="sxs-lookup"><span data-stu-id="313f0-114">PARAMETERS</span></span>

### <span data-ttu-id="313f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313f0-115">-DefaultProfile</span></span>
<span data-ttu-id="313f0-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="313f0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313f0-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="313f0-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="313f0-118">已停用的規則群組。</span><span class="sxs-lookup"><span data-stu-id="313f0-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313f0-119">-啟用</span><span class="sxs-lookup"><span data-stu-id="313f0-119">-Enabled</span></span>
<span data-ttu-id="313f0-120">指出是否已啟用 WAF。</span><span class="sxs-lookup"><span data-stu-id="313f0-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313f0-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="313f0-121">-FirewallMode</span></span>
<span data-ttu-id="313f0-122">指定 web 應用程式防火牆模式。</span><span class="sxs-lookup"><span data-stu-id="313f0-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="313f0-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="313f0-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="313f0-124">偵測</span><span class="sxs-lookup"><span data-stu-id="313f0-124">Detection</span></span>
- <span data-ttu-id="313f0-125">防護</span><span class="sxs-lookup"><span data-stu-id="313f0-125">Prevention</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313f0-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="313f0-126">-RuleSetType</span></span>
<span data-ttu-id="313f0-127">Web 應用程式防火牆規則集的類型。</span><span class="sxs-lookup"><span data-stu-id="313f0-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="313f0-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="313f0-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="313f0-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="313f0-129">OWASP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313f0-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="313f0-130">-RuleSetVersion</span></span>
<span data-ttu-id="313f0-131">規則集類型的版本。</span><span class="sxs-lookup"><span data-stu-id="313f0-131">The version of the rule set type.</span></span>
<span data-ttu-id="313f0-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="313f0-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="313f0-133">3.0</span><span class="sxs-lookup"><span data-stu-id="313f0-133">3.0</span></span>
- <span data-ttu-id="313f0-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="313f0-134">2.2.9</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313f0-135">-確認</span><span class="sxs-lookup"><span data-stu-id="313f0-135">-Confirm</span></span>
<span data-ttu-id="313f0-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="313f0-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313f0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="313f0-137">-WhatIf</span></span>
<span data-ttu-id="313f0-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="313f0-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="313f0-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="313f0-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313f0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313f0-140">CommonParameters</span></span>
<span data-ttu-id="313f0-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="313f0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313f0-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="313f0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313f0-143">輸入</span><span class="sxs-lookup"><span data-stu-id="313f0-143">INPUTS</span></span>

### <span data-ttu-id="313f0-144">所有</span><span class="sxs-lookup"><span data-stu-id="313f0-144">None</span></span>
<span data-ttu-id="313f0-145">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="313f0-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="313f0-146">輸出</span><span class="sxs-lookup"><span data-stu-id="313f0-146">OUTPUTS</span></span>

### <span data-ttu-id="313f0-147">PSApplicationGatewayWebApplicationFirewallConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="313f0-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="313f0-148">筆記</span><span class="sxs-lookup"><span data-stu-id="313f0-148">NOTES</span></span>

## <span data-ttu-id="313f0-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="313f0-149">RELATED LINKS</span></span>

[<span data-ttu-id="313f0-150">AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="313f0-150">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="313f0-151">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="313f0-151">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


