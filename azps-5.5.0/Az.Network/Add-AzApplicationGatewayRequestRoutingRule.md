---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 858af0fc06dc9df00eec100c3d07306797e99b56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131411"
---
# <span data-ttu-id="b18e1-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b18e1-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b18e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b18e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b18e1-103">將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b18e1-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="b18e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="b18e1-104">SYNTAX</span></span>

### <span data-ttu-id="b18e1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b18e1-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b18e1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b18e1-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b18e1-107">說明</span><span class="sxs-lookup"><span data-stu-id="b18e1-107">DESCRIPTION</span></span>
<span data-ttu-id="b18e1-108">**AzApplicationGatewayRequestRoutingRule** Cmdlet 會將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b18e1-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="b18e1-109">示例</span><span class="sxs-lookup"><span data-stu-id="b18e1-109">EXAMPLES</span></span>

### <span data-ttu-id="b18e1-110">範例1：將要求路由規則新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="b18e1-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="b18e1-111">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="b18e1-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b18e1-112">第二個命令會將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b18e1-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="b18e1-113">參數</span><span class="sxs-lookup"><span data-stu-id="b18e1-113">PARAMETERS</span></span>

### <span data-ttu-id="b18e1-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b18e1-114">-ApplicationGateway</span></span>
<span data-ttu-id="b18e1-115">指定此 Cmdlet 新增要求路由規則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b18e1-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="b18e1-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b18e1-116">-BackendAddressPool</span></span>
<span data-ttu-id="b18e1-117">指定應用程式閘道後端位址集區物件。</span><span class="sxs-lookup"><span data-stu-id="b18e1-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="b18e1-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b18e1-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="b18e1-119">指定應用程式閘道後端位址集區 ID。</span><span class="sxs-lookup"><span data-stu-id="b18e1-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="b18e1-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b18e1-120">-BackendHttpSettings</span></span>
<span data-ttu-id="b18e1-121">指定應用程式閘道的後端 HTTP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="b18e1-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="b18e1-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="b18e1-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="b18e1-123">指定應用程式閘道的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="b18e1-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="b18e1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b18e1-124">-DefaultProfile</span></span>
<span data-ttu-id="b18e1-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b18e1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b18e1-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="b18e1-126">-HttpListener</span></span>
<span data-ttu-id="b18e1-127">指定應用程式閘道 HTTP 攔截器物件。</span><span class="sxs-lookup"><span data-stu-id="b18e1-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="b18e1-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="b18e1-128">-HttpListenerId</span></span>
<span data-ttu-id="b18e1-129">指定應用程式閘道 HTTP 偵聽程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="b18e1-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="b18e1-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="b18e1-130">-Name</span></span>
<span data-ttu-id="b18e1-131">指定此 Cmdlet 所新增之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b18e1-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="b18e1-132">-優先順序</span><span class="sxs-lookup"><span data-stu-id="b18e1-132">-Priority</span></span>
<span data-ttu-id="b18e1-133">規則的優先順序</span><span class="sxs-lookup"><span data-stu-id="b18e1-133">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18e1-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b18e1-134">-RedirectConfiguration</span></span>
<span data-ttu-id="b18e1-135">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b18e1-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="b18e1-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b18e1-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="b18e1-137">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="b18e1-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="b18e1-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b18e1-138">-RewriteRuleSet</span></span>
<span data-ttu-id="b18e1-139">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b18e1-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b18e1-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="b18e1-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="b18e1-141">應用程式閘道 RewriteRuleSet 的 ID</span><span class="sxs-lookup"><span data-stu-id="b18e1-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b18e1-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="b18e1-142">-RuleType</span></span>
<span data-ttu-id="b18e1-143">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="b18e1-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="b18e1-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="b18e1-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="b18e1-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="b18e1-145">-UrlPathMapId</span></span>
<span data-ttu-id="b18e1-146">指定路由規則的 URL 路徑對應 ID。</span><span class="sxs-lookup"><span data-stu-id="b18e1-146">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="b18e1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b18e1-147">CommonParameters</span></span>
<span data-ttu-id="b18e1-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b18e1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b18e1-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b18e1-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b18e1-150">輸入</span><span class="sxs-lookup"><span data-stu-id="b18e1-150">INPUTS</span></span>

### <span data-ttu-id="b18e1-151">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b18e1-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b18e1-152">輸出</span><span class="sxs-lookup"><span data-stu-id="b18e1-152">OUTPUTS</span></span>

### <span data-ttu-id="b18e1-153">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b18e1-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b18e1-154">筆記</span><span class="sxs-lookup"><span data-stu-id="b18e1-154">NOTES</span></span>

## <span data-ttu-id="b18e1-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="b18e1-155">RELATED LINKS</span></span>

[<span data-ttu-id="b18e1-156">AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b18e1-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b18e1-157">新-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b18e1-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b18e1-158">移除-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b18e1-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b18e1-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b18e1-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


