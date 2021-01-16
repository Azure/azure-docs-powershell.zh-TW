---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 858af0fc06dc9df00eec100c3d07306797e99b56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282295"
---
# <span data-ttu-id="14054-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="14054-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="14054-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14054-102">SYNOPSIS</span></span>
<span data-ttu-id="14054-103">將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="14054-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="14054-104">句法</span><span class="sxs-lookup"><span data-stu-id="14054-104">SYNTAX</span></span>

### <span data-ttu-id="14054-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="14054-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14054-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="14054-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14054-107">說明</span><span class="sxs-lookup"><span data-stu-id="14054-107">DESCRIPTION</span></span>
<span data-ttu-id="14054-108">**AzApplicationGatewayRequestRoutingRule** Cmdlet 會將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="14054-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="14054-109">示例</span><span class="sxs-lookup"><span data-stu-id="14054-109">EXAMPLES</span></span>

### <span data-ttu-id="14054-110">範例1：將要求路由規則新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="14054-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="14054-111">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="14054-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="14054-112">第二個命令會將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="14054-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="14054-113">參數</span><span class="sxs-lookup"><span data-stu-id="14054-113">PARAMETERS</span></span>

### <span data-ttu-id="14054-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14054-114">-ApplicationGateway</span></span>
<span data-ttu-id="14054-115">指定此 Cmdlet 新增要求路由規則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="14054-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="14054-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="14054-116">-BackendAddressPool</span></span>
<span data-ttu-id="14054-117">指定應用程式閘道後端位址集區物件。</span><span class="sxs-lookup"><span data-stu-id="14054-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="14054-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="14054-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="14054-119">指定應用程式閘道後端位址集區 ID。</span><span class="sxs-lookup"><span data-stu-id="14054-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="14054-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="14054-120">-BackendHttpSettings</span></span>
<span data-ttu-id="14054-121">指定應用程式閘道的後端 HTTP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="14054-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="14054-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="14054-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="14054-123">指定應用程式閘道的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="14054-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="14054-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14054-124">-DefaultProfile</span></span>
<span data-ttu-id="14054-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14054-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14054-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="14054-126">-HttpListener</span></span>
<span data-ttu-id="14054-127">指定應用程式閘道 HTTP 攔截器物件。</span><span class="sxs-lookup"><span data-stu-id="14054-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="14054-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="14054-128">-HttpListenerId</span></span>
<span data-ttu-id="14054-129">指定應用程式閘道 HTTP 偵聽程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="14054-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="14054-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="14054-130">-Name</span></span>
<span data-ttu-id="14054-131">指定此 Cmdlet 所新增之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="14054-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="14054-132">-優先順序</span><span class="sxs-lookup"><span data-stu-id="14054-132">-Priority</span></span>
<span data-ttu-id="14054-133">規則的優先順序</span><span class="sxs-lookup"><span data-stu-id="14054-133">The priority of the rule</span></span>

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

### <span data-ttu-id="14054-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="14054-134">-RedirectConfiguration</span></span>
<span data-ttu-id="14054-135">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="14054-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="14054-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="14054-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="14054-137">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="14054-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="14054-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="14054-138">-RewriteRuleSet</span></span>
<span data-ttu-id="14054-139">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="14054-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="14054-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="14054-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="14054-141">應用程式閘道 RewriteRuleSet 的 ID</span><span class="sxs-lookup"><span data-stu-id="14054-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="14054-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="14054-142">-RuleType</span></span>
<span data-ttu-id="14054-143">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="14054-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="14054-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="14054-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="14054-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="14054-145">-UrlPathMapId</span></span>
<span data-ttu-id="14054-146">指定路由規則的 URL 路徑對應 ID。</span><span class="sxs-lookup"><span data-stu-id="14054-146">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="14054-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14054-147">CommonParameters</span></span>
<span data-ttu-id="14054-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14054-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14054-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="14054-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14054-150">輸入</span><span class="sxs-lookup"><span data-stu-id="14054-150">INPUTS</span></span>

### <span data-ttu-id="14054-151">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="14054-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14054-152">輸出</span><span class="sxs-lookup"><span data-stu-id="14054-152">OUTPUTS</span></span>

### <span data-ttu-id="14054-153">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="14054-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14054-154">筆記</span><span class="sxs-lookup"><span data-stu-id="14054-154">NOTES</span></span>

## <span data-ttu-id="14054-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="14054-155">RELATED LINKS</span></span>

[<span data-ttu-id="14054-156">AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="14054-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="14054-157">新-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="14054-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="14054-158">移除-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="14054-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="14054-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="14054-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


