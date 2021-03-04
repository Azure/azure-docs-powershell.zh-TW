---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: d86810ec15d38ecbe57a7471297b4ac167a2e526
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909549"
---
# <span data-ttu-id="16329-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16329-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="16329-102">簡介</span><span class="sxs-lookup"><span data-stu-id="16329-102">SYNOPSIS</span></span>
<span data-ttu-id="16329-103">新增要求路由規則至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="16329-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="16329-104">語法</span><span class="sxs-lookup"><span data-stu-id="16329-104">SYNTAX</span></span>

### <span data-ttu-id="16329-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="16329-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16329-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="16329-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16329-107">描述</span><span class="sxs-lookup"><span data-stu-id="16329-107">DESCRIPTION</span></span>
<span data-ttu-id="16329-108">**Add-AzApplicationGatewayRequestRoutingRule** Cmdlet 會新增要求路由規則至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="16329-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="16329-109">例子</span><span class="sxs-lookup"><span data-stu-id="16329-109">EXAMPLES</span></span>

### <span data-ttu-id="16329-110">範例 1：新增要求路由規則至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="16329-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="16329-111">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="16329-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="16329-112">第二個命令會將要求路由規則新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="16329-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="16329-113">參數</span><span class="sxs-lookup"><span data-stu-id="16329-113">PARAMETERS</span></span>

### <span data-ttu-id="16329-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16329-114">-ApplicationGateway</span></span>
<span data-ttu-id="16329-115">指定此 Cmdlet 新增要求路由規則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="16329-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="16329-116">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="16329-116">-BackendAddressPool</span></span>
<span data-ttu-id="16329-117">指定應用程式閘道後端位址區物件。</span><span class="sxs-lookup"><span data-stu-id="16329-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="16329-118">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="16329-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="16329-119">指定應用程式閘道後端位址區識別碼。</span><span class="sxs-lookup"><span data-stu-id="16329-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="16329-120">-後端HttpSettings</span><span class="sxs-lookup"><span data-stu-id="16329-120">-BackendHttpSettings</span></span>
<span data-ttu-id="16329-121">指定應用程式閘道的後端 HTTP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="16329-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="16329-122">-後端HttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="16329-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="16329-123">指定應用程式閘道的後端 HTTP 設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="16329-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="16329-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16329-124">-DefaultProfile</span></span>
<span data-ttu-id="16329-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="16329-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16329-126">-HTTPListener</span><span class="sxs-lookup"><span data-stu-id="16329-126">-HttpListener</span></span>
<span data-ttu-id="16329-127">指定應用程式閘道 HTTP 聆聽者物件。</span><span class="sxs-lookup"><span data-stu-id="16329-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="16329-128">-HTTPListenerId</span><span class="sxs-lookup"><span data-stu-id="16329-128">-HttpListenerId</span></span>
<span data-ttu-id="16329-129">指定應用程式閘道 HTTP 聆聽者識別碼。</span><span class="sxs-lookup"><span data-stu-id="16329-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="16329-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="16329-130">-Name</span></span>
<span data-ttu-id="16329-131">指定此 Cmdlet 新增的要求路由規則名稱。</span><span class="sxs-lookup"><span data-stu-id="16329-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="16329-132">-優先順序</span><span class="sxs-lookup"><span data-stu-id="16329-132">-Priority</span></span>
<span data-ttu-id="16329-133">規則的優先順序</span><span class="sxs-lookup"><span data-stu-id="16329-133">The priority of the rule</span></span>

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

### <span data-ttu-id="16329-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="16329-134">-RedirectConfiguration</span></span>
<span data-ttu-id="16329-135">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="16329-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="16329-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="16329-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="16329-137">應用程式閘道 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="16329-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="16329-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="16329-138">-RewriteRuleSet</span></span>
<span data-ttu-id="16329-139">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="16329-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="16329-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="16329-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="16329-141">應用程式閘道 RewriteRuleSet 的識別碼</span><span class="sxs-lookup"><span data-stu-id="16329-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="16329-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="16329-142">-RuleType</span></span>
<span data-ttu-id="16329-143">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="16329-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="16329-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="16329-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="16329-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="16329-145">-UrlPathMapId</span></span>
<span data-ttu-id="16329-146">指定路由規則的 URL 路徑地圖識別碼。</span><span class="sxs-lookup"><span data-stu-id="16329-146">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="16329-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16329-147">CommonParameters</span></span>
<span data-ttu-id="16329-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="16329-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16329-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16329-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16329-150">輸入</span><span class="sxs-lookup"><span data-stu-id="16329-150">INPUTS</span></span>

### <span data-ttu-id="16329-151">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16329-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16329-152">輸出</span><span class="sxs-lookup"><span data-stu-id="16329-152">OUTPUTS</span></span>

### <span data-ttu-id="16329-153">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16329-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16329-154">筆記</span><span class="sxs-lookup"><span data-stu-id="16329-154">NOTES</span></span>

## <span data-ttu-id="16329-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="16329-155">RELATED LINKS</span></span>

[<span data-ttu-id="16329-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16329-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="16329-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16329-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="16329-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16329-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="16329-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16329-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


