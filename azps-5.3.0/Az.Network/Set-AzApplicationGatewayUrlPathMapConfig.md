---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448928"
---
# <span data-ttu-id="129f1-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="129f1-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="129f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="129f1-102">SYNOPSIS</span></span>
<span data-ttu-id="129f1-103">將 URL 路徑對應陣列的設定設為後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="129f1-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="129f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="129f1-104">SYNTAX</span></span>

### <span data-ttu-id="129f1-105">BackendSetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="129f1-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="129f1-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="129f1-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="129f1-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="129f1-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="129f1-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="129f1-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="129f1-109">說明</span><span class="sxs-lookup"><span data-stu-id="129f1-109">DESCRIPTION</span></span>
<span data-ttu-id="129f1-110">AzApplicationGatewayUrlPathMapConfig Cmdlet 會將 URL 路徑映射陣列的 **設定** 設定為後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="129f1-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="129f1-111">示例</span><span class="sxs-lookup"><span data-stu-id="129f1-111">EXAMPLES</span></span>

### <span data-ttu-id="129f1-112">範例1：更新 URL 路徑對應</span><span class="sxs-lookup"><span data-stu-id="129f1-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="129f1-113">第一個命令會取得名為 appGwName 的應用程式閘道，並將結果儲存在 $appgw 變數中。</span><span class="sxs-lookup"><span data-stu-id="129f1-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="129f1-114">第二個命令會更新應用程式閘道中名為 map01 的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="129f1-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="129f1-115">第三個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="129f1-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="129f1-116">參數</span><span class="sxs-lookup"><span data-stu-id="129f1-116">PARAMETERS</span></span>

### <span data-ttu-id="129f1-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="129f1-117">-ApplicationGateway</span></span>
<span data-ttu-id="129f1-118">指定此 Cmdlet 設定 URL 路徑對應配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="129f1-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="129f1-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="129f1-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="129f1-120">指定在 *pathRules* 參數中指定的規則不相符時，要路由的預設後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="129f1-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="129f1-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="129f1-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="129f1-122">指定預設的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="129f1-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="129f1-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="129f1-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="129f1-124">指定要在 *pathRules* 參數中指定的規則都不相符時使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="129f1-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="129f1-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="129f1-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="129f1-126">指定預設的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="129f1-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="129f1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="129f1-127">-DefaultProfile</span></span>
<span data-ttu-id="129f1-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="129f1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="129f1-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="129f1-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="129f1-130">應用程式閘道預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="129f1-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="129f1-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="129f1-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="129f1-132">應用程式閘道預設 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="129f1-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="129f1-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="129f1-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="129f1-134">應用程式閘道的預設重寫規則集</span><span class="sxs-lookup"><span data-stu-id="129f1-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="129f1-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="129f1-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="129f1-136">應用程式閘道的預設重寫規則集識別碼</span><span class="sxs-lookup"><span data-stu-id="129f1-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="129f1-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="129f1-137">-Name</span></span>
<span data-ttu-id="129f1-138">指定此 Cmdlet 針對其設定配置的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="129f1-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="129f1-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="129f1-139">-PathRules</span></span>
<span data-ttu-id="129f1-140">指定路徑規則清單。</span><span class="sxs-lookup"><span data-stu-id="129f1-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="129f1-141">請注意，路徑規則是區分順序的，它們會依指定順序加以套用。</span><span class="sxs-lookup"><span data-stu-id="129f1-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="129f1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="129f1-142">CommonParameters</span></span>
<span data-ttu-id="129f1-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="129f1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="129f1-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="129f1-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="129f1-145">輸入</span><span class="sxs-lookup"><span data-stu-id="129f1-145">INPUTS</span></span>

### <span data-ttu-id="129f1-146">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="129f1-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="129f1-147">輸出</span><span class="sxs-lookup"><span data-stu-id="129f1-147">OUTPUTS</span></span>

### <span data-ttu-id="129f1-148">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="129f1-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="129f1-149">筆記</span><span class="sxs-lookup"><span data-stu-id="129f1-149">NOTES</span></span>

## <span data-ttu-id="129f1-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="129f1-150">RELATED LINKS</span></span>

[<span data-ttu-id="129f1-151">附加 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="129f1-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="129f1-152">AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="129f1-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="129f1-153">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="129f1-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="129f1-154">移除-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="129f1-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


