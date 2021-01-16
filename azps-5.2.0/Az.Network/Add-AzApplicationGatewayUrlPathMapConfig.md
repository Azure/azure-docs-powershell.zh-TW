---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277939"
---
# <span data-ttu-id="69dc5-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="69dc5-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="69dc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="69dc5-103">在後端伺服器池中新增 URL 路徑對應的陣列。</span><span class="sxs-lookup"><span data-stu-id="69dc5-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="69dc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="69dc5-104">SYNTAX</span></span>

### <span data-ttu-id="69dc5-105">BackendSetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="69dc5-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69dc5-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="69dc5-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69dc5-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="69dc5-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69dc5-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="69dc5-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69dc5-109">說明</span><span class="sxs-lookup"><span data-stu-id="69dc5-109">DESCRIPTION</span></span>
<span data-ttu-id="69dc5-110">**AzApplicationGatewayUrlPathMapConfig** Cmdlet 會將 URL 路徑對應的陣列新增到後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="69dc5-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="69dc5-111">示例</span><span class="sxs-lookup"><span data-stu-id="69dc5-111">EXAMPLES</span></span>

### <span data-ttu-id="69dc5-112">範例1：新增 URL 路徑對應至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="69dc5-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="69dc5-113">第一個命令會取得名為 appGwName 的應用程式閘道，並將其儲存在 $appgw 變數中。</span><span class="sxs-lookup"><span data-stu-id="69dc5-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="69dc5-114">第二個命令會取得後端位址集區，並將它儲存在 $pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="69dc5-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="69dc5-115">第三個命令會取得後端 HTTP 設定，並將它儲存在 $poolSettings 變數中。</span><span class="sxs-lookup"><span data-stu-id="69dc5-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="69dc5-116">第四個命令會建立名為 rule01 的新路徑規則配置，並將其儲存在 $pathRule 變數中。</span><span class="sxs-lookup"><span data-stu-id="69dc5-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="69dc5-117">第五個命令會將名為 url01 的 url 路徑對應配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="69dc5-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="69dc5-118">第六個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="69dc5-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="69dc5-119">參數</span><span class="sxs-lookup"><span data-stu-id="69dc5-119">PARAMETERS</span></span>

### <span data-ttu-id="69dc5-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69dc5-120">-ApplicationGateway</span></span>
<span data-ttu-id="69dc5-121">指定此 Cmdlet 新增 URL 路徑對應配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="69dc5-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="69dc5-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="69dc5-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="69dc5-123">指定在 *pathRules* 參數中指定的規則不相符時，要路由的預設後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="69dc5-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69dc5-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="69dc5-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="69dc5-125">指定預設的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="69dc5-125">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69dc5-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="69dc5-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="69dc5-127">指定要在 *pathRules* 參數中指定的規則都不相符時使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="69dc5-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69dc5-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="69dc5-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="69dc5-129">指定預設的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="69dc5-129">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69dc5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69dc5-130">-DefaultProfile</span></span>
<span data-ttu-id="69dc5-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69dc5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69dc5-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="69dc5-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="69dc5-133">應用程式閘道預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="69dc5-133">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69dc5-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="69dc5-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="69dc5-135">應用程式閘道預設 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="69dc5-135">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69dc5-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="69dc5-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="69dc5-137">應用程式閘道的預設重寫規則集</span><span class="sxs-lookup"><span data-stu-id="69dc5-137">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69dc5-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="69dc5-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="69dc5-139">應用程式閘道的預設重寫規則集識別碼</span><span class="sxs-lookup"><span data-stu-id="69dc5-139">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69dc5-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="69dc5-140">-Name</span></span>
<span data-ttu-id="69dc5-141">指定此 Cmdlet 新增到後端伺服器池中的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="69dc5-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="69dc5-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="69dc5-142">-PathRules</span></span>
<span data-ttu-id="69dc5-143">指定路徑規則清單。</span><span class="sxs-lookup"><span data-stu-id="69dc5-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="69dc5-144">路徑規則是區分順序的，它們會依指定順序加以套用。</span><span class="sxs-lookup"><span data-stu-id="69dc5-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69dc5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69dc5-145">CommonParameters</span></span>
<span data-ttu-id="69dc5-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69dc5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69dc5-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69dc5-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69dc5-148">輸入</span><span class="sxs-lookup"><span data-stu-id="69dc5-148">INPUTS</span></span>

### <span data-ttu-id="69dc5-149">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="69dc5-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="69dc5-150">輸出</span><span class="sxs-lookup"><span data-stu-id="69dc5-150">OUTPUTS</span></span>

### <span data-ttu-id="69dc5-151">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="69dc5-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="69dc5-152">筆記</span><span class="sxs-lookup"><span data-stu-id="69dc5-152">NOTES</span></span>

## <span data-ttu-id="69dc5-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="69dc5-153">RELATED LINKS</span></span>

[<span data-ttu-id="69dc5-154">AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="69dc5-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="69dc5-155">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="69dc5-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="69dc5-156">移除-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="69dc5-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="69dc5-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="69dc5-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


