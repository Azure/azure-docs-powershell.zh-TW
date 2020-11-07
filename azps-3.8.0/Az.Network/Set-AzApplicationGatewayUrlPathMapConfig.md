---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798665"
---
# <span data-ttu-id="1ec3a-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ec3a-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="1ec3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ec3a-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec3a-103">將 URL 路徑對應陣列的設定設為後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="1ec3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ec3a-104">SYNTAX</span></span>

### <span data-ttu-id="1ec3a-105">BackendSetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="1ec3a-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ec3a-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec3a-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ec3a-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="1ec3a-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ec3a-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec3a-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ec3a-109">說明</span><span class="sxs-lookup"><span data-stu-id="1ec3a-109">DESCRIPTION</span></span>
<span data-ttu-id="1ec3a-110">AzApplicationGatewayUrlPathMapConfig Cmdlet 會將 URL 路徑映射陣列的 **設定** 設定為後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="1ec3a-111">示例</span><span class="sxs-lookup"><span data-stu-id="1ec3a-111">EXAMPLES</span></span>

### <span data-ttu-id="1ec3a-112">範例1：更新 URL 路徑對應</span><span class="sxs-lookup"><span data-stu-id="1ec3a-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="1ec3a-113">第一個命令會取得名為 appGwName 的應用程式閘道，並將結果儲存在 $appgw 變數中。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="1ec3a-114">第二個命令會更新應用程式閘道中名為 map01 的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="1ec3a-115">第三個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="1ec3a-116">參數</span><span class="sxs-lookup"><span data-stu-id="1ec3a-116">PARAMETERS</span></span>

### <span data-ttu-id="1ec3a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ec3a-117">-ApplicationGateway</span></span>
<span data-ttu-id="1ec3a-118">指定此 Cmdlet 設定 URL 路徑對應配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="1ec3a-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1ec3a-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="1ec3a-120">指定在 *pathRules* 參數中指定的規則不相符時，要路由的預設後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="1ec3a-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1ec3a-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="1ec3a-122">指定預設的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="1ec3a-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1ec3a-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="1ec3a-124">指定要在 *pathRules* 參數中指定的規則都不相符時使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="1ec3a-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="1ec3a-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="1ec3a-126">指定預設的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="1ec3a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec3a-127">-DefaultProfile</span></span>
<span data-ttu-id="1ec3a-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ec3a-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ec3a-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="1ec3a-130">應用程式閘道預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ec3a-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="1ec3a-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1ec3a-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="1ec3a-132">應用程式閘道預設 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="1ec3a-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="1ec3a-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ec3a-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="1ec3a-134">應用程式閘道的預設重寫規則集</span><span class="sxs-lookup"><span data-stu-id="1ec3a-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="1ec3a-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="1ec3a-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="1ec3a-136">應用程式閘道的預設重寫規則集識別碼</span><span class="sxs-lookup"><span data-stu-id="1ec3a-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="1ec3a-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ec3a-137">-Name</span></span>
<span data-ttu-id="1ec3a-138">指定此 Cmdlet 針對其設定配置的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="1ec3a-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="1ec3a-139">-PathRules</span></span>
<span data-ttu-id="1ec3a-140">指定路徑規則清單。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="1ec3a-141">請注意，路徑規則是區分順序的，它們會依指定順序加以套用。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="1ec3a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec3a-142">CommonParameters</span></span>
<span data-ttu-id="1ec3a-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec3a-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ec3a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec3a-145">輸入</span><span class="sxs-lookup"><span data-stu-id="1ec3a-145">INPUTS</span></span>

### <span data-ttu-id="1ec3a-146">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1ec3a-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ec3a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="1ec3a-147">OUTPUTS</span></span>

### <span data-ttu-id="1ec3a-148">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1ec3a-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ec3a-149">筆記</span><span class="sxs-lookup"><span data-stu-id="1ec3a-149">NOTES</span></span>

## <span data-ttu-id="1ec3a-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ec3a-150">RELATED LINKS</span></span>

[<span data-ttu-id="1ec3a-151">附加 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ec3a-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1ec3a-152">AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ec3a-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1ec3a-153">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ec3a-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1ec3a-154">移除-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ec3a-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


