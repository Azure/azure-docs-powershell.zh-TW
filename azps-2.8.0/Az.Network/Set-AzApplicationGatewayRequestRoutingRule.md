---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: bd6888402a2e3a88b9d3d19da752b0ac18d20f32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790525"
---
# <span data-ttu-id="992b4-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="992b4-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="992b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="992b4-102">SYNOPSIS</span></span>
<span data-ttu-id="992b4-103">修改應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="992b4-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="992b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="992b4-104">SYNTAX</span></span>

### <span data-ttu-id="992b4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="992b4-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="992b4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="992b4-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="992b4-107">說明</span><span class="sxs-lookup"><span data-stu-id="992b4-107">DESCRIPTION</span></span>
<span data-ttu-id="992b4-108">**AzApplicationGatewayRequestRoutingRule** Cmdlet 會修改要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="992b4-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="992b4-109">示例</span><span class="sxs-lookup"><span data-stu-id="992b4-109">EXAMPLES</span></span>

### <span data-ttu-id="992b4-110">範例1：更新要求路由規則</span><span class="sxs-lookup"><span data-stu-id="992b4-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="992b4-111">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="992b4-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="992b4-112">第二個命令會修改應用程式閘道的要求路由規則，以使用 $Setting 變數中指定的後端 HTTP 設定、$Listener 變數中指定的 HTTP 偵聽程式，以及在 $Pool 變數中指定的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="992b4-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="992b4-113">參數</span><span class="sxs-lookup"><span data-stu-id="992b4-113">PARAMETERS</span></span>

### <span data-ttu-id="992b4-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="992b4-114">-ApplicationGateway</span></span>
<span data-ttu-id="992b4-115">指定應用程式閘道物件，此 Cmdlet 會將請求路由規則關聯。</span><span class="sxs-lookup"><span data-stu-id="992b4-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="992b4-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="992b4-116">-BackendAddressPool</span></span>
<span data-ttu-id="992b4-117">指定應用程式閘道後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="992b4-117">Specifies the application gateway back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="992b4-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="992b4-119">指定應用程式閘道後端位址集區 ID。</span><span class="sxs-lookup"><span data-stu-id="992b4-119">Specifies the application gateway back-end address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="992b4-120">-BackendHttpSettings</span></span>
<span data-ttu-id="992b4-121">指定應用程式閘道後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="992b4-121">Specifies the application gateway backend HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="992b4-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="992b4-123">指定應用程式閘道後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="992b4-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992b4-124">-DefaultProfile</span></span>
<span data-ttu-id="992b4-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="992b4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="992b4-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="992b4-126">-HttpListener</span></span>
<span data-ttu-id="992b4-127">指定應用程式閘道 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="992b4-127">Specifies the application gateway HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="992b4-128">-HttpListenerId</span></span>
<span data-ttu-id="992b4-129">指定應用程式閘道 HTTP 偵聽程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="992b4-129">Specifies the application gateway HTTP listener ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="992b4-130">-Name</span></span>
<span data-ttu-id="992b4-131">指定此 Cmdlet 所修改之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="992b4-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="992b4-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="992b4-132">-RedirectConfiguration</span></span>
<span data-ttu-id="992b4-133">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="992b4-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="992b4-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="992b4-135">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="992b4-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="992b4-136">-RewriteRuleSet</span></span>
<span data-ttu-id="992b4-137">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="992b4-137">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="992b4-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="992b4-139">應用程式閘道 RewriteRuleSet 的 ID</span><span class="sxs-lookup"><span data-stu-id="992b4-139">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="992b4-140">-RuleType</span></span>
<span data-ttu-id="992b4-141">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="992b4-141">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="992b4-142">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="992b4-143">-UrlPathMapId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992b4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992b4-144">CommonParameters</span></span>
<span data-ttu-id="992b4-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="992b4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992b4-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="992b4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992b4-147">輸入</span><span class="sxs-lookup"><span data-stu-id="992b4-147">INPUTS</span></span>

### <span data-ttu-id="992b4-148">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="992b4-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="992b4-149">輸出</span><span class="sxs-lookup"><span data-stu-id="992b4-149">OUTPUTS</span></span>

### <span data-ttu-id="992b4-150">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="992b4-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="992b4-151">筆記</span><span class="sxs-lookup"><span data-stu-id="992b4-151">NOTES</span></span>

## <span data-ttu-id="992b4-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="992b4-152">RELATED LINKS</span></span>

[<span data-ttu-id="992b4-153">附加 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="992b4-153">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="992b4-154">AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="992b4-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="992b4-155">新-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="992b4-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="992b4-156">移除-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="992b4-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


