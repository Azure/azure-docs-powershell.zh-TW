---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 0f186de1ad548be0c566c6fac2b8d1505885bfe0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287468"
---
# <span data-ttu-id="23e0b-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="23e0b-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="23e0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="23e0b-103">建立應用程式閘道的 WAF 配置。</span><span class="sxs-lookup"><span data-stu-id="23e0b-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="23e0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="23e0b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23e0b-105">說明</span><span class="sxs-lookup"><span data-stu-id="23e0b-105">DESCRIPTION</span></span>
<span data-ttu-id="23e0b-106">**新的-AzApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet 會建立 web 應用程式防火牆 (WAF Azure 應用程式閘道的) 設定。</span><span class="sxs-lookup"><span data-stu-id="23e0b-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="23e0b-107">示例</span><span class="sxs-lookup"><span data-stu-id="23e0b-107">EXAMPLES</span></span>

### <span data-ttu-id="23e0b-108">範例1：建立應用程式閘道的 web 應用程式防火牆設定</span><span class="sxs-lookup"><span data-stu-id="23e0b-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="23e0b-109">第一個命令會針對名為「要求-942-應用程式-SQLI」的規則群組建立新的已停用規則群組設定，並停用規則942130與規則942140。</span><span class="sxs-lookup"><span data-stu-id="23e0b-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="23e0b-110">第二個命令會針對名為「要求 921--通訊協定-PROTOCOL」的規則群組，建立另一個停用的規則群組設定。</span><span class="sxs-lookup"><span data-stu-id="23e0b-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="23e0b-111">不會明確傳遞任何規則，因此規則群組的所有規則都將停用。</span><span class="sxs-lookup"><span data-stu-id="23e0b-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="23e0b-112">最後一個命令接著會建立 WAF 設定，並停用防火牆規則，$disabledRuleGroup 1 和 $disabledRuleGroup 2 中已設定。</span><span class="sxs-lookup"><span data-stu-id="23e0b-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="23e0b-113">新的 WAF 設定會儲存在 $firewallConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="23e0b-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="23e0b-114">參數</span><span class="sxs-lookup"><span data-stu-id="23e0b-114">PARAMETERS</span></span>

### <span data-ttu-id="23e0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e0b-115">-DefaultProfile</span></span>
<span data-ttu-id="23e0b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23e0b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23e0b-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="23e0b-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="23e0b-118">已停用的規則群組。</span><span class="sxs-lookup"><span data-stu-id="23e0b-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0b-119">-啟用</span><span class="sxs-lookup"><span data-stu-id="23e0b-119">-Enabled</span></span>
<span data-ttu-id="23e0b-120">指出是否已啟用 WAF。</span><span class="sxs-lookup"><span data-stu-id="23e0b-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0b-121">-排除</span><span class="sxs-lookup"><span data-stu-id="23e0b-121">-Exclusion</span></span>
<span data-ttu-id="23e0b-122">排除清單。</span><span class="sxs-lookup"><span data-stu-id="23e0b-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0b-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="23e0b-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="23e0b-124">最大檔案上傳限制（MB）。</span><span class="sxs-lookup"><span data-stu-id="23e0b-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="23e0b-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="23e0b-125">-FirewallMode</span></span>
<span data-ttu-id="23e0b-126">指定 web 應用程式防火牆模式。</span><span class="sxs-lookup"><span data-stu-id="23e0b-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="23e0b-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="23e0b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="23e0b-128">偵測</span><span class="sxs-lookup"><span data-stu-id="23e0b-128">Detection</span></span>
- <span data-ttu-id="23e0b-129">防護</span><span class="sxs-lookup"><span data-stu-id="23e0b-129">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0b-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="23e0b-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="23e0b-131">最大要求主體大小（KB）。</span><span class="sxs-lookup"><span data-stu-id="23e0b-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="23e0b-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="23e0b-132">-RequestBodyCheck</span></span>
<span data-ttu-id="23e0b-133">是否已核取要求正文。</span><span class="sxs-lookup"><span data-stu-id="23e0b-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="23e0b-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="23e0b-134">-RuleSetType</span></span>
<span data-ttu-id="23e0b-135">Web 應用程式防火牆規則集的類型。</span><span class="sxs-lookup"><span data-stu-id="23e0b-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="23e0b-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="23e0b-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="23e0b-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="23e0b-137">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0b-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="23e0b-138">-RuleSetVersion</span></span>
<span data-ttu-id="23e0b-139">規則集類型的版本。</span><span class="sxs-lookup"><span data-stu-id="23e0b-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0b-140">-確認</span><span class="sxs-lookup"><span data-stu-id="23e0b-140">-Confirm</span></span>
<span data-ttu-id="23e0b-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23e0b-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e0b-142">-WhatIf</span></span>
<span data-ttu-id="23e0b-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23e0b-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23e0b-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23e0b-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e0b-145">CommonParameters</span></span>
<span data-ttu-id="23e0b-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23e0b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e0b-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23e0b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e0b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="23e0b-148">INPUTS</span></span>

### <span data-ttu-id="23e0b-149">所有</span><span class="sxs-lookup"><span data-stu-id="23e0b-149">None</span></span>

## <span data-ttu-id="23e0b-150">輸出</span><span class="sxs-lookup"><span data-stu-id="23e0b-150">OUTPUTS</span></span>

### <span data-ttu-id="23e0b-151">PSApplicationGatewayWebApplicationFirewallConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="23e0b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="23e0b-152">筆記</span><span class="sxs-lookup"><span data-stu-id="23e0b-152">NOTES</span></span>

## <span data-ttu-id="23e0b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="23e0b-153">RELATED LINKS</span></span>

[<span data-ttu-id="23e0b-154">AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="23e0b-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="23e0b-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="23e0b-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


