---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95f3e4b11d9253a232fc119faf39a4fa51fab60a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281521"
---
# <span data-ttu-id="6ec31-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6ec31-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6ec31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ec31-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec31-103">建立應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="6ec31-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="6ec31-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ec31-104">SYNTAX</span></span>

### <span data-ttu-id="6ec31-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ec31-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ec31-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6ec31-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ec31-107">說明</span><span class="sxs-lookup"><span data-stu-id="6ec31-107">DESCRIPTION</span></span>
<span data-ttu-id="6ec31-108">**AzApplicationGatewayRequestRoutingRule** Cmdlet 會建立 Azure 應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="6ec31-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="6ec31-109">示例</span><span class="sxs-lookup"><span data-stu-id="6ec31-109">EXAMPLES</span></span>

### <span data-ttu-id="6ec31-110">範例1：建立應用程式閘道的要求路由規則</span><span class="sxs-lookup"><span data-stu-id="6ec31-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="6ec31-111">這個命令會建立一個名為 Rule01 的基本要求路由規則，並將結果儲存在名為 $Rule 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6ec31-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="6ec31-112">參數</span><span class="sxs-lookup"><span data-stu-id="6ec31-112">PARAMETERS</span></span>

### <span data-ttu-id="6ec31-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6ec31-113">-BackendAddressPool</span></span>
<span data-ttu-id="6ec31-114">針對要建立的要求路由規則，將後端位址集區指定為物件。</span><span class="sxs-lookup"><span data-stu-id="6ec31-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="6ec31-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6ec31-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="6ec31-116">指定要建立之要求路由規則的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ec31-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="6ec31-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6ec31-117">-BackendHttpSettings</span></span>
<span data-ttu-id="6ec31-118">針對要建立的要求路由規則，將後端 HTTP 設定指定為物件。</span><span class="sxs-lookup"><span data-stu-id="6ec31-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="6ec31-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6ec31-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="6ec31-120">指定要建立之要求路由規則的後端 HTTP 設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ec31-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="6ec31-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec31-121">-DefaultProfile</span></span>
<span data-ttu-id="6ec31-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ec31-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ec31-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="6ec31-123">-HttpListener</span></span>
<span data-ttu-id="6ec31-124">針對要建立的要求路由規則指定後端 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="6ec31-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="6ec31-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="6ec31-125">-HttpListenerId</span></span>
<span data-ttu-id="6ec31-126">指定要建立之要求路由規則的後端 HTTP 偵聽程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ec31-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="6ec31-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ec31-127">-Name</span></span>
<span data-ttu-id="6ec31-128">指定此 Cmdlet 所建立之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ec31-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6ec31-129">-優先順序</span><span class="sxs-lookup"><span data-stu-id="6ec31-129">-Priority</span></span>
<span data-ttu-id="6ec31-130">規則的優先順序</span><span class="sxs-lookup"><span data-stu-id="6ec31-130">The priority of the rule</span></span>

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

### <span data-ttu-id="6ec31-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec31-131">-RedirectConfiguration</span></span>
<span data-ttu-id="6ec31-132">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec31-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6ec31-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6ec31-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="6ec31-134">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="6ec31-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6ec31-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec31-135">-RewriteRuleSet</span></span>
<span data-ttu-id="6ec31-136">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec31-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6ec31-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="6ec31-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="6ec31-138">應用程式閘道 RewriteRuleSet 的 ID</span><span class="sxs-lookup"><span data-stu-id="6ec31-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6ec31-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6ec31-139">-RuleType</span></span>
<span data-ttu-id="6ec31-140">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="6ec31-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="6ec31-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="6ec31-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="6ec31-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="6ec31-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="6ec31-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec31-143">CommonParameters</span></span>
<span data-ttu-id="6ec31-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ec31-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec31-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6ec31-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec31-146">輸入</span><span class="sxs-lookup"><span data-stu-id="6ec31-146">INPUTS</span></span>

### <span data-ttu-id="6ec31-147">所有</span><span class="sxs-lookup"><span data-stu-id="6ec31-147">None</span></span>

## <span data-ttu-id="6ec31-148">輸出</span><span class="sxs-lookup"><span data-stu-id="6ec31-148">OUTPUTS</span></span>

### <span data-ttu-id="6ec31-149">PSApplicationGatewayRequestRoutingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6ec31-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6ec31-150">筆記</span><span class="sxs-lookup"><span data-stu-id="6ec31-150">NOTES</span></span>

## <span data-ttu-id="6ec31-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ec31-151">RELATED LINKS</span></span>

[<span data-ttu-id="6ec31-152">附加 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6ec31-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6ec31-153">AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6ec31-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6ec31-154">移除-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6ec31-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6ec31-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6ec31-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


