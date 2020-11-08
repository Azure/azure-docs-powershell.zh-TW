---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: b0335fd0700b256650809c4548efe4d1e620442b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141462"
---
# <span data-ttu-id="e3903-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e3903-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e3903-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3903-102">SYNOPSIS</span></span>
<span data-ttu-id="e3903-103">將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e3903-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="e3903-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3903-104">SYNTAX</span></span>

### <span data-ttu-id="e3903-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e3903-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3903-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e3903-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3903-107">說明</span><span class="sxs-lookup"><span data-stu-id="e3903-107">DESCRIPTION</span></span>
<span data-ttu-id="e3903-108">**AzApplicationGatewayRequestRoutingRule** Cmdlet 會將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e3903-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="e3903-109">示例</span><span class="sxs-lookup"><span data-stu-id="e3903-109">EXAMPLES</span></span>

### <span data-ttu-id="e3903-110">範例1：將要求路由規則新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="e3903-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="e3903-111">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="e3903-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e3903-112">第二個命令會將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e3903-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="e3903-113">參數</span><span class="sxs-lookup"><span data-stu-id="e3903-113">PARAMETERS</span></span>

### <span data-ttu-id="e3903-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3903-114">-ApplicationGateway</span></span>
<span data-ttu-id="e3903-115">指定此 Cmdlet 新增要求路由規則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e3903-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="e3903-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e3903-116">-BackendAddressPool</span></span>
<span data-ttu-id="e3903-117">指定應用程式閘道後端位址集區物件。</span><span class="sxs-lookup"><span data-stu-id="e3903-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="e3903-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e3903-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="e3903-119">指定應用程式閘道後端位址集區 ID。</span><span class="sxs-lookup"><span data-stu-id="e3903-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="e3903-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e3903-120">-BackendHttpSettings</span></span>
<span data-ttu-id="e3903-121">指定應用程式閘道的後端 HTTP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="e3903-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="e3903-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e3903-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e3903-123">指定應用程式閘道的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="e3903-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="e3903-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3903-124">-DefaultProfile</span></span>
<span data-ttu-id="e3903-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3903-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3903-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e3903-126">-HttpListener</span></span>
<span data-ttu-id="e3903-127">指定應用程式閘道 HTTP 攔截器物件。</span><span class="sxs-lookup"><span data-stu-id="e3903-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="e3903-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="e3903-128">-HttpListenerId</span></span>
<span data-ttu-id="e3903-129">指定應用程式閘道 HTTP 偵聽程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3903-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="e3903-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3903-130">-Name</span></span>
<span data-ttu-id="e3903-131">指定此 Cmdlet 所新增之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3903-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="e3903-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3903-132">-RedirectConfiguration</span></span>
<span data-ttu-id="e3903-133">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3903-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e3903-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e3903-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="e3903-135">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="e3903-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e3903-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3903-136">-RewriteRuleSet</span></span>
<span data-ttu-id="e3903-137">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3903-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="e3903-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="e3903-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="e3903-139">應用程式閘道 RewriteRuleSet 的 ID</span><span class="sxs-lookup"><span data-stu-id="e3903-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="e3903-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e3903-140">-RuleType</span></span>
<span data-ttu-id="e3903-141">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="e3903-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="e3903-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e3903-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="e3903-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="e3903-143">-UrlPathMapId</span></span>
<span data-ttu-id="e3903-144">指定路由規則的 URL 路徑對應 ID。</span><span class="sxs-lookup"><span data-stu-id="e3903-144">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="e3903-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3903-145">CommonParameters</span></span>
<span data-ttu-id="e3903-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3903-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3903-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3903-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3903-148">輸入</span><span class="sxs-lookup"><span data-stu-id="e3903-148">INPUTS</span></span>

### <span data-ttu-id="e3903-149">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3903-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3903-150">輸出</span><span class="sxs-lookup"><span data-stu-id="e3903-150">OUTPUTS</span></span>

### <span data-ttu-id="e3903-151">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3903-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3903-152">筆記</span><span class="sxs-lookup"><span data-stu-id="e3903-152">NOTES</span></span>

## <span data-ttu-id="e3903-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3903-153">RELATED LINKS</span></span>

[<span data-ttu-id="e3903-154">AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e3903-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e3903-155">新-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e3903-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e3903-156">移除-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e3903-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e3903-157">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e3903-157">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

