---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9b5e618fc4b4be02614d872bfa5bcdabd2b0fec9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132455"
---
# <span data-ttu-id="0eadd-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eadd-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="0eadd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0eadd-102">SYNOPSIS</span></span>
<span data-ttu-id="0eadd-103">修改應用程式閘道的 WAF 設定。</span><span class="sxs-lookup"><span data-stu-id="0eadd-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="0eadd-104">句法</span><span class="sxs-lookup"><span data-stu-id="0eadd-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eadd-105">說明</span><span class="sxs-lookup"><span data-stu-id="0eadd-105">DESCRIPTION</span></span>
<span data-ttu-id="0eadd-106">AzApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 會修改 web 應用程式防火牆 () WAF 應用程式閘道的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="0eadd-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="0eadd-107">示例</span><span class="sxs-lookup"><span data-stu-id="0eadd-107">EXAMPLES</span></span>

### <span data-ttu-id="0eadd-108">範例1：更新應用程式閘道 web 應用程式防火牆設定</span><span class="sxs-lookup"><span data-stu-id="0eadd-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="0eadd-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，然後將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="0eadd-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0eadd-110">第二個命令會啟用儲存在 $AppGw 的應用程式閘道的防火牆設定，並將防火牆模式設定為「偵測」、RuleSetType 到 "OWASP"，以及 RuleSetVersion 到 "3.0"。</span><span class="sxs-lookup"><span data-stu-id="0eadd-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="0eadd-111">參數</span><span class="sxs-lookup"><span data-stu-id="0eadd-111">PARAMETERS</span></span>

### <span data-ttu-id="0eadd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0eadd-112">-ApplicationGateway</span></span>
<span data-ttu-id="0eadd-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="0eadd-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="0eadd-114">您可以使用 Get-AzApplicationGateway Cmdlet 來取得應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="0eadd-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eadd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eadd-115">-DefaultProfile</span></span>
<span data-ttu-id="0eadd-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0eadd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eadd-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="0eadd-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="0eadd-118">已停用的規則群組。</span><span class="sxs-lookup"><span data-stu-id="0eadd-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="0eadd-119">-啟用</span><span class="sxs-lookup"><span data-stu-id="0eadd-119">-Enabled</span></span>
<span data-ttu-id="0eadd-120">指出是否已啟用 web 應用程式防火牆。</span><span class="sxs-lookup"><span data-stu-id="0eadd-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="0eadd-121">-排除</span><span class="sxs-lookup"><span data-stu-id="0eadd-121">-Exclusion</span></span>
<span data-ttu-id="0eadd-122">排除清單。</span><span class="sxs-lookup"><span data-stu-id="0eadd-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="0eadd-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="0eadd-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="0eadd-124">最大檔案上傳限制（MB）。</span><span class="sxs-lookup"><span data-stu-id="0eadd-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="0eadd-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="0eadd-125">-FirewallMode</span></span>
<span data-ttu-id="0eadd-126">指定 web 應用程式防火牆模式。</span><span class="sxs-lookup"><span data-stu-id="0eadd-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="0eadd-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0eadd-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0eadd-128">偵測</span><span class="sxs-lookup"><span data-stu-id="0eadd-128">Detection</span></span>
- <span data-ttu-id="0eadd-129">防護</span><span class="sxs-lookup"><span data-stu-id="0eadd-129">Prevention</span></span>

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

### <span data-ttu-id="0eadd-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="0eadd-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="0eadd-131">最大要求主體大小（KB）。</span><span class="sxs-lookup"><span data-stu-id="0eadd-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="0eadd-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="0eadd-132">-RequestBodyCheck</span></span>
<span data-ttu-id="0eadd-133">是否已核取要求正文。</span><span class="sxs-lookup"><span data-stu-id="0eadd-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="0eadd-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="0eadd-134">-RuleSetType</span></span>
<span data-ttu-id="0eadd-135">Web 應用程式防火牆規則集的類型。</span><span class="sxs-lookup"><span data-stu-id="0eadd-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="0eadd-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0eadd-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="0eadd-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="0eadd-137">OWASP</span></span>

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

### <span data-ttu-id="0eadd-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="0eadd-138">-RuleSetVersion</span></span>
<span data-ttu-id="0eadd-139">規則集類型的版本。</span><span class="sxs-lookup"><span data-stu-id="0eadd-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="0eadd-140">-確認</span><span class="sxs-lookup"><span data-stu-id="0eadd-140">-Confirm</span></span>
<span data-ttu-id="0eadd-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0eadd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eadd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eadd-142">-WhatIf</span></span>
<span data-ttu-id="0eadd-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0eadd-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0eadd-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eadd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eadd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eadd-145">CommonParameters</span></span>
<span data-ttu-id="0eadd-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0eadd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eadd-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0eadd-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eadd-148">輸入</span><span class="sxs-lookup"><span data-stu-id="0eadd-148">INPUTS</span></span>

### <span data-ttu-id="0eadd-149">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0eadd-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0eadd-150">輸出</span><span class="sxs-lookup"><span data-stu-id="0eadd-150">OUTPUTS</span></span>

### <span data-ttu-id="0eadd-151">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0eadd-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0eadd-152">筆記</span><span class="sxs-lookup"><span data-stu-id="0eadd-152">NOTES</span></span>

## <span data-ttu-id="0eadd-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="0eadd-153">RELATED LINKS</span></span>

[<span data-ttu-id="0eadd-154">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0eadd-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0eadd-155">AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eadd-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="0eadd-156">新-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eadd-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


