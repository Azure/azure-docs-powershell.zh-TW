---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 95d0e82609c2cb8bfcbbfcf57d1354d219da9f9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913138"
---
# <span data-ttu-id="1ded6-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ded6-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="1ded6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ded6-102">SYNOPSIS</span></span>
<span data-ttu-id="1ded6-103">修改應用程式閘道的 WAF 群組原則。</span><span class="sxs-lookup"><span data-stu-id="1ded6-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="1ded6-104">語法</span><span class="sxs-lookup"><span data-stu-id="1ded6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ded6-105">描述</span><span class="sxs-lookup"><span data-stu-id="1ded6-105">DESCRIPTION</span></span>
<span data-ttu-id="1ded6-106">**Set-AzApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet 會修改 Web 應用程式防火牆 (WAF) 應用程式閘道的設定。</span><span class="sxs-lookup"><span data-stu-id="1ded6-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="1ded6-107">例子</span><span class="sxs-lookup"><span data-stu-id="1ded6-107">EXAMPLES</span></span>

### <span data-ttu-id="1ded6-108">範例 1：更新應用程式閘道 Web 應用程式防火牆組</span><span class="sxs-lookup"><span data-stu-id="1ded6-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="1ded6-109">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，然後將它儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="1ded6-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1ded6-110">第二個命令會啟用儲存在 $AppGw 的應用程式閘道的防火牆設定，並且將防火牆模式設定為 "Detection"，RuleSetType 設定為 "OWASP"，而 RuleSetVersion 則設定為 "3.0"。</span><span class="sxs-lookup"><span data-stu-id="1ded6-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="1ded6-111">參數</span><span class="sxs-lookup"><span data-stu-id="1ded6-111">PARAMETERS</span></span>

### <span data-ttu-id="1ded6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ded6-112">-ApplicationGateway</span></span>
<span data-ttu-id="1ded6-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="1ded6-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="1ded6-114">您可以使用 Get-AzApplicationGateway Cmdlet 取得應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="1ded6-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="1ded6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ded6-115">-DefaultProfile</span></span>
<span data-ttu-id="1ded6-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ded6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ded6-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="1ded6-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="1ded6-118">已停用的規則群組。</span><span class="sxs-lookup"><span data-stu-id="1ded6-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="1ded6-119">-已啟用</span><span class="sxs-lookup"><span data-stu-id="1ded6-119">-Enabled</span></span>
<span data-ttu-id="1ded6-120">指出 Web 應用程式防火牆是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="1ded6-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="1ded6-121">-排除</span><span class="sxs-lookup"><span data-stu-id="1ded6-121">-Exclusion</span></span>
<span data-ttu-id="1ded6-122">排除清單。</span><span class="sxs-lookup"><span data-stu-id="1ded6-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="1ded6-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="1ded6-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="1ded6-124">最大檔案上傳限制 ，以 MB 為單位。</span><span class="sxs-lookup"><span data-stu-id="1ded6-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="1ded6-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="1ded6-125">-FirewallMode</span></span>
<span data-ttu-id="1ded6-126">指定 Web 應用程式防火牆模式。</span><span class="sxs-lookup"><span data-stu-id="1ded6-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="1ded6-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1ded6-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ded6-128">檢測</span><span class="sxs-lookup"><span data-stu-id="1ded6-128">Detection</span></span>
- <span data-ttu-id="1ded6-129">預防</span><span class="sxs-lookup"><span data-stu-id="1ded6-129">Prevention</span></span>

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

### <span data-ttu-id="1ded6-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="1ded6-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="1ded6-131">以 KB 為單位的最大要求內文大小。</span><span class="sxs-lookup"><span data-stu-id="1ded6-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="1ded6-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="1ded6-132">-RequestBodyCheck</span></span>
<span data-ttu-id="1ded6-133">是否已檢查要求內檔。</span><span class="sxs-lookup"><span data-stu-id="1ded6-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="1ded6-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="1ded6-134">-RuleSetType</span></span>
<span data-ttu-id="1ded6-135">Web 應用程式防火牆規則集的類型。</span><span class="sxs-lookup"><span data-stu-id="1ded6-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="1ded6-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1ded6-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="1ded6-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="1ded6-137">OWASP</span></span>

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

### <span data-ttu-id="1ded6-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="1ded6-138">-RuleSetVersion</span></span>
<span data-ttu-id="1ded6-139">規則集類型的版本。</span><span class="sxs-lookup"><span data-stu-id="1ded6-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="1ded6-140">-確認</span><span class="sxs-lookup"><span data-stu-id="1ded6-140">-Confirm</span></span>
<span data-ttu-id="1ded6-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1ded6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ded6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ded6-142">-WhatIf</span></span>
<span data-ttu-id="1ded6-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ded6-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ded6-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ded6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ded6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ded6-145">CommonParameters</span></span>
<span data-ttu-id="1ded6-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ded6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ded6-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1ded6-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ded6-148">輸入</span><span class="sxs-lookup"><span data-stu-id="1ded6-148">INPUTS</span></span>

### <span data-ttu-id="1ded6-149">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ded6-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ded6-150">輸出</span><span class="sxs-lookup"><span data-stu-id="1ded6-150">OUTPUTS</span></span>

### <span data-ttu-id="1ded6-151">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ded6-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ded6-152">筆記</span><span class="sxs-lookup"><span data-stu-id="1ded6-152">NOTES</span></span>

## <span data-ttu-id="1ded6-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ded6-153">RELATED LINKS</span></span>

[<span data-ttu-id="1ded6-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ded6-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="1ded6-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ded6-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="1ded6-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ded6-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


