---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 832fd96f34e18413bfd72e1a05826954f3ae58e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915926"
---
# <span data-ttu-id="6e39c-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e39c-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6e39c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6e39c-102">SYNOPSIS</span></span>
<span data-ttu-id="6e39c-103">修改應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="6e39c-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="6e39c-104">語法</span><span class="sxs-lookup"><span data-stu-id="6e39c-104">SYNTAX</span></span>

### <span data-ttu-id="6e39c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e39c-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e39c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6e39c-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e39c-107">描述</span><span class="sxs-lookup"><span data-stu-id="6e39c-107">DESCRIPTION</span></span>
<span data-ttu-id="6e39c-108">**Set-AzApplicationGatewayRequestRoutingRule** Cmdlet 會修改要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="6e39c-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="6e39c-109">例子</span><span class="sxs-lookup"><span data-stu-id="6e39c-109">EXAMPLES</span></span>

### <span data-ttu-id="6e39c-110">範例 1：更新要求路由規則</span><span class="sxs-lookup"><span data-stu-id="6e39c-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="6e39c-111">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="6e39c-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6e39c-112">第二個命令會修改應用程式閘道的要求路由規則，以使用 $Setting 變數中指定的後端 HTTP 設定、在 $Listener 變數中指定的 HTTP 聆聽程式，以及 $Pool 變數中指定的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="6e39c-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="6e39c-113">參數</span><span class="sxs-lookup"><span data-stu-id="6e39c-113">PARAMETERS</span></span>

### <span data-ttu-id="6e39c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e39c-114">-ApplicationGateway</span></span>
<span data-ttu-id="6e39c-115">指定此 Cmdlet 與要求路由規則關聯的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="6e39c-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="6e39c-116">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="6e39c-116">-BackendAddressPool</span></span>
<span data-ttu-id="6e39c-117">指定應用程式閘道後端位址區。</span><span class="sxs-lookup"><span data-stu-id="6e39c-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="6e39c-118">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6e39c-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="6e39c-119">指定應用程式閘道後端位址區識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e39c-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="6e39c-120">-後端HttpSettings</span><span class="sxs-lookup"><span data-stu-id="6e39c-120">-BackendHttpSettings</span></span>
<span data-ttu-id="6e39c-121">指定應用程式閘道後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="6e39c-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="6e39c-122">-後端HttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6e39c-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="6e39c-123">指定應用程式閘道後端 HTTP 設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e39c-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="6e39c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e39c-124">-DefaultProfile</span></span>
<span data-ttu-id="6e39c-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e39c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e39c-126">-HTTPListener</span><span class="sxs-lookup"><span data-stu-id="6e39c-126">-HttpListener</span></span>
<span data-ttu-id="6e39c-127">指定應用程式閘道 HTTP 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="6e39c-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="6e39c-128">-HTTPListenerId</span><span class="sxs-lookup"><span data-stu-id="6e39c-128">-HttpListenerId</span></span>
<span data-ttu-id="6e39c-129">指定應用程式閘道 HTTP 聆聽者識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e39c-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="6e39c-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e39c-130">-Name</span></span>
<span data-ttu-id="6e39c-131">指定此 Cmdlet 修改之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e39c-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6e39c-132">-優先順序</span><span class="sxs-lookup"><span data-stu-id="6e39c-132">-Priority</span></span>
<span data-ttu-id="6e39c-133">規則的優先順序</span><span class="sxs-lookup"><span data-stu-id="6e39c-133">The priority of the rule</span></span>

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

### <span data-ttu-id="6e39c-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e39c-134">-RedirectConfiguration</span></span>
<span data-ttu-id="6e39c-135">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e39c-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6e39c-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6e39c-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="6e39c-137">應用程式閘道 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="6e39c-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6e39c-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e39c-138">-RewriteRuleSet</span></span>
<span data-ttu-id="6e39c-139">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e39c-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6e39c-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="6e39c-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="6e39c-141">應用程式閘道 RewriteRuleSet 的識別碼</span><span class="sxs-lookup"><span data-stu-id="6e39c-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6e39c-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6e39c-142">-RuleType</span></span>
<span data-ttu-id="6e39c-143">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="6e39c-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="6e39c-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="6e39c-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="6e39c-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="6e39c-145">-UrlPathMapId</span></span>
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

### <span data-ttu-id="6e39c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e39c-146">CommonParameters</span></span>
<span data-ttu-id="6e39c-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6e39c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e39c-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e39c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e39c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="6e39c-149">INPUTS</span></span>

### <span data-ttu-id="6e39c-150">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e39c-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6e39c-151">輸出</span><span class="sxs-lookup"><span data-stu-id="6e39c-151">OUTPUTS</span></span>

### <span data-ttu-id="6e39c-152">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e39c-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6e39c-153">筆記</span><span class="sxs-lookup"><span data-stu-id="6e39c-153">NOTES</span></span>

## <span data-ttu-id="6e39c-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e39c-154">RELATED LINKS</span></span>

[<span data-ttu-id="6e39c-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e39c-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6e39c-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e39c-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6e39c-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e39c-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6e39c-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e39c-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


