---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: fd925829248c7f11f047de90ddc2bc0b57f51b71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801206"
---
# <span data-ttu-id="29bb0-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="29bb0-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="29bb0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="29bb0-103">修改應用程式閘道的 WAF 設定。</span><span class="sxs-lookup"><span data-stu-id="29bb0-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29bb0-104">句法</span><span class="sxs-lookup"><span data-stu-id="29bb0-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29bb0-105">說明</span><span class="sxs-lookup"><span data-stu-id="29bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="29bb0-106">AzureRmApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 會修改 web 應用程式防火牆 () WAF 應用程式閘道的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="29bb0-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="29bb0-107">示例</span><span class="sxs-lookup"><span data-stu-id="29bb0-107">EXAMPLES</span></span>

### <span data-ttu-id="29bb0-108">範例1：更新應用程式閘道 web 應用程式防火牆設定</span><span class="sxs-lookup"><span data-stu-id="29bb0-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="29bb0-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，然後將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="29bb0-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="29bb0-110">第二個命令會啟用儲存在 $AppGw 的應用程式閘道的防火牆設定，並將防火牆模式設定為「偵測」、RuleSetType 到 "OWASP"，以及 RuleSetVersion 到 "3.0"。</span><span class="sxs-lookup"><span data-stu-id="29bb0-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="29bb0-111">參數</span><span class="sxs-lookup"><span data-stu-id="29bb0-111">PARAMETERS</span></span>

### <span data-ttu-id="29bb0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29bb0-112">-ApplicationGateway</span></span>
<span data-ttu-id="29bb0-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="29bb0-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="29bb0-114">您可以使用 Get-AzureRmApplicationGateway Cmdlet 來取得應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="29bb0-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="29bb0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bb0-115">-DefaultProfile</span></span>
<span data-ttu-id="29bb0-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29bb0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29bb0-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="29bb0-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="29bb0-118">已停用的規則群組。</span><span class="sxs-lookup"><span data-stu-id="29bb0-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="29bb0-119">-啟用</span><span class="sxs-lookup"><span data-stu-id="29bb0-119">-Enabled</span></span>
<span data-ttu-id="29bb0-120">指出是否已啟用 web 應用程式防火牆。</span><span class="sxs-lookup"><span data-stu-id="29bb0-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="29bb0-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="29bb0-121">-FirewallMode</span></span>
<span data-ttu-id="29bb0-122">指定 web 應用程式防火牆模式。</span><span class="sxs-lookup"><span data-stu-id="29bb0-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="29bb0-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="29bb0-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29bb0-124">偵測</span><span class="sxs-lookup"><span data-stu-id="29bb0-124">Detection</span></span>
- <span data-ttu-id="29bb0-125">防護</span><span class="sxs-lookup"><span data-stu-id="29bb0-125">Prevention</span></span>

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

### <span data-ttu-id="29bb0-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="29bb0-126">-RuleSetType</span></span>
<span data-ttu-id="29bb0-127">Web 應用程式防火牆規則集的類型。</span><span class="sxs-lookup"><span data-stu-id="29bb0-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="29bb0-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="29bb0-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="29bb0-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="29bb0-129">OWASP</span></span>

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

### <span data-ttu-id="29bb0-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="29bb0-130">-RuleSetVersion</span></span>
<span data-ttu-id="29bb0-131">規則集類型的版本。</span><span class="sxs-lookup"><span data-stu-id="29bb0-131">The version of the rule set type.</span></span>
<span data-ttu-id="29bb0-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="29bb0-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="29bb0-133">3.0</span><span class="sxs-lookup"><span data-stu-id="29bb0-133">3.0</span></span>
- <span data-ttu-id="29bb0-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="29bb0-134">2.2.9</span></span>

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

### <span data-ttu-id="29bb0-135">-確認</span><span class="sxs-lookup"><span data-stu-id="29bb0-135">-Confirm</span></span>
<span data-ttu-id="29bb0-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29bb0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29bb0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29bb0-137">-WhatIf</span></span>
<span data-ttu-id="29bb0-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29bb0-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29bb0-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29bb0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29bb0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bb0-140">CommonParameters</span></span>
<span data-ttu-id="29bb0-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29bb0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bb0-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29bb0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bb0-143">輸入</span><span class="sxs-lookup"><span data-stu-id="29bb0-143">INPUTS</span></span>

### <span data-ttu-id="29bb0-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29bb0-144">PSApplicationGateway</span></span>
<span data-ttu-id="29bb0-145">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="29bb0-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="29bb0-146">輸出</span><span class="sxs-lookup"><span data-stu-id="29bb0-146">OUTPUTS</span></span>

### <span data-ttu-id="29bb0-147">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29bb0-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="29bb0-148">筆記</span><span class="sxs-lookup"><span data-stu-id="29bb0-148">NOTES</span></span>

## <span data-ttu-id="29bb0-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="29bb0-149">RELATED LINKS</span></span>

[<span data-ttu-id="29bb0-150">AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29bb0-150">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="29bb0-151">AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="29bb0-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="29bb0-152">新-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="29bb0-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


