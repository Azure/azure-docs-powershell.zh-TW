---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 53963e7672881255cf23df99e53a1471c3c42250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916717"
---
# <span data-ttu-id="6b7df-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6b7df-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6b7df-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6b7df-102">SYNOPSIS</span></span>
<span data-ttu-id="6b7df-103">建立應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="6b7df-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="6b7df-104">語法</span><span class="sxs-lookup"><span data-stu-id="6b7df-104">SYNTAX</span></span>

### <span data-ttu-id="6b7df-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b7df-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b7df-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6b7df-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b7df-107">描述</span><span class="sxs-lookup"><span data-stu-id="6b7df-107">DESCRIPTION</span></span>
<span data-ttu-id="6b7df-108">**Add-AzApplicationGatewayRequestRoutingRule** Cmdlet 會建立 Azure 應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="6b7df-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="6b7df-109">例子</span><span class="sxs-lookup"><span data-stu-id="6b7df-109">EXAMPLES</span></span>

### <span data-ttu-id="6b7df-110">範例 1：建立應用程式閘道的要求路由規則</span><span class="sxs-lookup"><span data-stu-id="6b7df-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="6b7df-111">此命令會建立名為 Rule01 的基本要求路由規則，並且將結果儲存在名為 $Rule 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6b7df-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="6b7df-112">參數</span><span class="sxs-lookup"><span data-stu-id="6b7df-112">PARAMETERS</span></span>

### <span data-ttu-id="6b7df-113">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="6b7df-113">-BackendAddressPool</span></span>
<span data-ttu-id="6b7df-114">指定要建立要求路由規則的後端位址集區做為物件。</span><span class="sxs-lookup"><span data-stu-id="6b7df-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="6b7df-115">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6b7df-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="6b7df-116">指定要建立之要求路由規則的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b7df-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="6b7df-117">-後端HttpSettings</span><span class="sxs-lookup"><span data-stu-id="6b7df-117">-BackendHttpSettings</span></span>
<span data-ttu-id="6b7df-118">指定要建立要求路由規則的後端 HTTP 設定做為物件。</span><span class="sxs-lookup"><span data-stu-id="6b7df-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="6b7df-119">-後端HttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6b7df-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="6b7df-120">指定要建立之要求路由規則的後端 HTTP 設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b7df-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="6b7df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b7df-121">-DefaultProfile</span></span>
<span data-ttu-id="6b7df-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b7df-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b7df-123">-HTTPListener</span><span class="sxs-lookup"><span data-stu-id="6b7df-123">-HttpListener</span></span>
<span data-ttu-id="6b7df-124">指定要建立要求路由規則的後端 HTTP 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="6b7df-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="6b7df-125">-HTTPListenerId</span><span class="sxs-lookup"><span data-stu-id="6b7df-125">-HttpListenerId</span></span>
<span data-ttu-id="6b7df-126">指定要建立要求路由規則的後端 HTTP 聆聽者識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b7df-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="6b7df-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b7df-127">-Name</span></span>
<span data-ttu-id="6b7df-128">指定此 Cmdlet 所建立之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b7df-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6b7df-129">-優先順序</span><span class="sxs-lookup"><span data-stu-id="6b7df-129">-Priority</span></span>
<span data-ttu-id="6b7df-130">規則的優先順序</span><span class="sxs-lookup"><span data-stu-id="6b7df-130">The priority of the rule</span></span>

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

### <span data-ttu-id="6b7df-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b7df-131">-RedirectConfiguration</span></span>
<span data-ttu-id="6b7df-132">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b7df-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6b7df-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6b7df-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="6b7df-134">應用程式閘道 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="6b7df-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6b7df-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b7df-135">-RewriteRuleSet</span></span>
<span data-ttu-id="6b7df-136">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b7df-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6b7df-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="6b7df-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="6b7df-138">應用程式閘道 RewriteRuleSet 的識別碼</span><span class="sxs-lookup"><span data-stu-id="6b7df-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6b7df-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6b7df-139">-RuleType</span></span>
<span data-ttu-id="6b7df-140">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="6b7df-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="6b7df-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="6b7df-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="6b7df-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="6b7df-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="6b7df-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b7df-143">CommonParameters</span></span>
<span data-ttu-id="6b7df-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6b7df-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b7df-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b7df-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b7df-146">輸入</span><span class="sxs-lookup"><span data-stu-id="6b7df-146">INPUTS</span></span>

### <span data-ttu-id="6b7df-147">沒有</span><span class="sxs-lookup"><span data-stu-id="6b7df-147">None</span></span>

## <span data-ttu-id="6b7df-148">輸出</span><span class="sxs-lookup"><span data-stu-id="6b7df-148">OUTPUTS</span></span>

### <span data-ttu-id="6b7df-149">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6b7df-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6b7df-150">筆記</span><span class="sxs-lookup"><span data-stu-id="6b7df-150">NOTES</span></span>

## <span data-ttu-id="6b7df-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b7df-151">RELATED LINKS</span></span>

[<span data-ttu-id="6b7df-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6b7df-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6b7df-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6b7df-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6b7df-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6b7df-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6b7df-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6b7df-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


