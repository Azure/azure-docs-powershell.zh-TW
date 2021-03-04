---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 7d13febefe06ed1c290a0f95cbfda39dea353426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908402"
---
# <span data-ttu-id="46a3d-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="46a3d-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="46a3d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="46a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="46a3d-103">為應用程式閘道建立 WAF 組塊。</span><span class="sxs-lookup"><span data-stu-id="46a3d-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="46a3d-104">語法</span><span class="sxs-lookup"><span data-stu-id="46a3d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a3d-105">描述</span><span class="sxs-lookup"><span data-stu-id="46a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="46a3d-106">**New-AzApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet 會為 Azure 應用程式閘道建立 Web 應用程式防火牆 (WAF) 組式。</span><span class="sxs-lookup"><span data-stu-id="46a3d-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="46a3d-107">例子</span><span class="sxs-lookup"><span data-stu-id="46a3d-107">EXAMPLES</span></span>

### <span data-ttu-id="46a3d-108">範例 1：為應用程式閘道建立 Web 應用程式防火牆組</span><span class="sxs-lookup"><span data-stu-id="46a3d-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="46a3d-109">第一個命令會針對名為「REQUEST-942-APPLICATION-ATTACK-SQLI」的規則群組，建立一個新的已停用規則組，並停用規則 942130 和規則 942140。</span><span class="sxs-lookup"><span data-stu-id="46a3d-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="46a3d-110">第二個命令會為名為「REQUEST-921-PROTOCOL-ATTACK」的規則群組建立另一個已停用的規則組組。</span><span class="sxs-lookup"><span data-stu-id="46a3d-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="46a3d-111">系統不會特別傳遞規則，因此會停用規則組的所有規則。</span><span class="sxs-lookup"><span data-stu-id="46a3d-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="46a3d-112">最後一個命令接著會建立 WAF 群組原則，且防火牆規則會以 $disabledRuleGroup 1 和 $disabledRuleGroup 2 中的$disabledRuleGroup停用。</span><span class="sxs-lookup"><span data-stu-id="46a3d-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="46a3d-113">新的 WAF 組$firewallConfig變數。</span><span class="sxs-lookup"><span data-stu-id="46a3d-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="46a3d-114">參數</span><span class="sxs-lookup"><span data-stu-id="46a3d-114">PARAMETERS</span></span>

### <span data-ttu-id="46a3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a3d-115">-DefaultProfile</span></span>
<span data-ttu-id="46a3d-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="46a3d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46a3d-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="46a3d-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="46a3d-118">已停用的規則群組。</span><span class="sxs-lookup"><span data-stu-id="46a3d-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="46a3d-119">-已啟用</span><span class="sxs-lookup"><span data-stu-id="46a3d-119">-Enabled</span></span>
<span data-ttu-id="46a3d-120">指出 WAF 是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="46a3d-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="46a3d-121">-排除</span><span class="sxs-lookup"><span data-stu-id="46a3d-121">-Exclusion</span></span>
<span data-ttu-id="46a3d-122">排除清單。</span><span class="sxs-lookup"><span data-stu-id="46a3d-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="46a3d-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="46a3d-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="46a3d-124">最大檔案上傳限制 ，以 MB 為單位。</span><span class="sxs-lookup"><span data-stu-id="46a3d-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="46a3d-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="46a3d-125">-FirewallMode</span></span>
<span data-ttu-id="46a3d-126">指定 Web 應用程式防火牆模式。</span><span class="sxs-lookup"><span data-stu-id="46a3d-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="46a3d-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="46a3d-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46a3d-128">檢測</span><span class="sxs-lookup"><span data-stu-id="46a3d-128">Detection</span></span>
- <span data-ttu-id="46a3d-129">預防</span><span class="sxs-lookup"><span data-stu-id="46a3d-129">Prevention</span></span>

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

### <span data-ttu-id="46a3d-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="46a3d-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="46a3d-131">以 KB 為單位的最大要求內文大小。</span><span class="sxs-lookup"><span data-stu-id="46a3d-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="46a3d-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="46a3d-132">-RequestBodyCheck</span></span>
<span data-ttu-id="46a3d-133">是否已檢查要求內檔。</span><span class="sxs-lookup"><span data-stu-id="46a3d-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="46a3d-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="46a3d-134">-RuleSetType</span></span>
<span data-ttu-id="46a3d-135">Web 應用程式防火牆規則集的類型。</span><span class="sxs-lookup"><span data-stu-id="46a3d-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="46a3d-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="46a3d-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="46a3d-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="46a3d-137">OWASP</span></span>

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

### <span data-ttu-id="46a3d-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="46a3d-138">-RuleSetVersion</span></span>
<span data-ttu-id="46a3d-139">規則集類型的版本。</span><span class="sxs-lookup"><span data-stu-id="46a3d-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="46a3d-140">-確認</span><span class="sxs-lookup"><span data-stu-id="46a3d-140">-Confirm</span></span>
<span data-ttu-id="46a3d-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="46a3d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a3d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a3d-142">-WhatIf</span></span>
<span data-ttu-id="46a3d-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46a3d-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46a3d-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46a3d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a3d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a3d-145">CommonParameters</span></span>
<span data-ttu-id="46a3d-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="46a3d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a3d-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="46a3d-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a3d-148">輸入</span><span class="sxs-lookup"><span data-stu-id="46a3d-148">INPUTS</span></span>

### <span data-ttu-id="46a3d-149">沒有</span><span class="sxs-lookup"><span data-stu-id="46a3d-149">None</span></span>

## <span data-ttu-id="46a3d-150">輸出</span><span class="sxs-lookup"><span data-stu-id="46a3d-150">OUTPUTS</span></span>

### <span data-ttu-id="46a3d-151">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="46a3d-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="46a3d-152">筆記</span><span class="sxs-lookup"><span data-stu-id="46a3d-152">NOTES</span></span>

## <span data-ttu-id="46a3d-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="46a3d-153">RELATED LINKS</span></span>

[<span data-ttu-id="46a3d-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="46a3d-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="46a3d-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="46a3d-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


