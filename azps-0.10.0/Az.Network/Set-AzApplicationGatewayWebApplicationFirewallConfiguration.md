---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bf4a87ebae55329e4594d11559fda0aee9047cbc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795429"
---
# <span data-ttu-id="856f8-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="856f8-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="856f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="856f8-102">SYNOPSIS</span></span>
<span data-ttu-id="856f8-103">修改應用程式閘道的 WAF 設定。</span><span class="sxs-lookup"><span data-stu-id="856f8-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="856f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="856f8-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="856f8-105">說明</span><span class="sxs-lookup"><span data-stu-id="856f8-105">DESCRIPTION</span></span>
<span data-ttu-id="856f8-106">AzApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 會修改 web 應用程式防火牆 () WAF 應用程式閘道的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="856f8-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="856f8-107">示例</span><span class="sxs-lookup"><span data-stu-id="856f8-107">EXAMPLES</span></span>

### <span data-ttu-id="856f8-108">範例1：更新應用程式閘道 web 應用程式防火牆設定</span><span class="sxs-lookup"><span data-stu-id="856f8-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="856f8-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，然後將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="856f8-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="856f8-110">第二個命令會啟用儲存在 $AppGw 的應用程式閘道的防火牆設定，並將防火牆模式設定為「偵測」、RuleSetType 到 "OWASP"，以及 RuleSetVersion 到 "3.0"。</span><span class="sxs-lookup"><span data-stu-id="856f8-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="856f8-111">參數</span><span class="sxs-lookup"><span data-stu-id="856f8-111">PARAMETERS</span></span>

### <span data-ttu-id="856f8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="856f8-112">-ApplicationGateway</span></span>
<span data-ttu-id="856f8-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="856f8-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="856f8-114">您可以使用 Get-AzApplicationGateway Cmdlet 來取得應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="856f8-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="856f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856f8-115">-DefaultProfile</span></span>
<span data-ttu-id="856f8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="856f8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="856f8-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="856f8-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="856f8-118">已停用的規則群組。</span><span class="sxs-lookup"><span data-stu-id="856f8-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="856f8-119">-啟用</span><span class="sxs-lookup"><span data-stu-id="856f8-119">-Enabled</span></span>
<span data-ttu-id="856f8-120">指出是否已啟用 web 應用程式防火牆。</span><span class="sxs-lookup"><span data-stu-id="856f8-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="856f8-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="856f8-121">-FirewallMode</span></span>
<span data-ttu-id="856f8-122">指定 web 應用程式防火牆模式。</span><span class="sxs-lookup"><span data-stu-id="856f8-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="856f8-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="856f8-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="856f8-124">偵測</span><span class="sxs-lookup"><span data-stu-id="856f8-124">Detection</span></span>
- <span data-ttu-id="856f8-125">防護</span><span class="sxs-lookup"><span data-stu-id="856f8-125">Prevention</span></span>

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

### <span data-ttu-id="856f8-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="856f8-126">-RuleSetType</span></span>
<span data-ttu-id="856f8-127">Web 應用程式防火牆規則集的類型。</span><span class="sxs-lookup"><span data-stu-id="856f8-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="856f8-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="856f8-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="856f8-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="856f8-129">OWASP</span></span>

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

### <span data-ttu-id="856f8-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="856f8-130">-RuleSetVersion</span></span>
<span data-ttu-id="856f8-131">規則集類型的版本。</span><span class="sxs-lookup"><span data-stu-id="856f8-131">The version of the rule set type.</span></span>
<span data-ttu-id="856f8-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="856f8-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="856f8-133">3.0</span><span class="sxs-lookup"><span data-stu-id="856f8-133">3.0</span></span>
- <span data-ttu-id="856f8-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="856f8-134">2.2.9</span></span>

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

### <span data-ttu-id="856f8-135">-確認</span><span class="sxs-lookup"><span data-stu-id="856f8-135">-Confirm</span></span>
<span data-ttu-id="856f8-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="856f8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="856f8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="856f8-137">-WhatIf</span></span>
<span data-ttu-id="856f8-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="856f8-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="856f8-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="856f8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="856f8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856f8-140">CommonParameters</span></span>
<span data-ttu-id="856f8-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="856f8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856f8-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="856f8-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856f8-143">輸入</span><span class="sxs-lookup"><span data-stu-id="856f8-143">INPUTS</span></span>

### <span data-ttu-id="856f8-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="856f8-144">PSApplicationGateway</span></span>
<span data-ttu-id="856f8-145">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="856f8-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="856f8-146">輸出</span><span class="sxs-lookup"><span data-stu-id="856f8-146">OUTPUTS</span></span>

### <span data-ttu-id="856f8-147">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="856f8-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="856f8-148">筆記</span><span class="sxs-lookup"><span data-stu-id="856f8-148">NOTES</span></span>

## <span data-ttu-id="856f8-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="856f8-149">RELATED LINKS</span></span>

[<span data-ttu-id="856f8-150">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="856f8-150">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="856f8-151">AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="856f8-151">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="856f8-152">新-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="856f8-152">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


