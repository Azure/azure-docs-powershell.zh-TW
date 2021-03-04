---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cc2a30e5a5633dcda345184bef121befe710ad8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901957"
---
# <span data-ttu-id="d64d4-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d64d4-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d64d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d64d4-102">SYNOPSIS</span></span>
<span data-ttu-id="d64d4-103">設定後端伺服器集區 URL 路徑的陣列之設定。</span><span class="sxs-lookup"><span data-stu-id="d64d4-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d64d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="d64d4-104">SYNTAX</span></span>

### <span data-ttu-id="d64d4-105">後端SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="d64d4-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d64d4-106">後端SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d64d4-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d64d4-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="d64d4-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d64d4-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d64d4-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d64d4-109">描述</span><span class="sxs-lookup"><span data-stu-id="d64d4-109">DESCRIPTION</span></span>
<span data-ttu-id="d64d4-110">**Set-AzApplicationGatewayUrlPathMapConfig** Cmdlet 會設定後端伺服器集區 URL 路徑的陣列。</span><span class="sxs-lookup"><span data-stu-id="d64d4-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d64d4-111">例子</span><span class="sxs-lookup"><span data-stu-id="d64d4-111">EXAMPLES</span></span>

### <span data-ttu-id="d64d4-112">範例 1：更新 URL 路徑地圖</span><span class="sxs-lookup"><span data-stu-id="d64d4-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="d64d4-113">第一個命令會取得名為 appGwName 的應用程式閘道，並儲存在$appgw變數中。</span><span class="sxs-lookup"><span data-stu-id="d64d4-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="d64d4-114">第二個命令會更新應用程式閘道中名為 map01 的 URL 路徑映射。</span><span class="sxs-lookup"><span data-stu-id="d64d4-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="d64d4-115">第三個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d64d4-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="d64d4-116">參數</span><span class="sxs-lookup"><span data-stu-id="d64d4-116">PARAMETERS</span></span>

### <span data-ttu-id="d64d4-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d64d4-117">-ApplicationGateway</span></span>
<span data-ttu-id="d64d4-118">指定此 Cmdlet 設定 URL 路徑地圖設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d64d4-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="d64d4-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d64d4-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="d64d4-120">指定要路由的預設後端位址資料庫，以防 *pathRules* 參數中指定的規則沒有相符。</span><span class="sxs-lookup"><span data-stu-id="d64d4-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d64d4-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d64d4-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="d64d4-122">指定預設的後端位址資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="d64d4-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="d64d4-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d64d4-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="d64d4-124">指定在 *pathRules* 參數中指定的規則與規則不相符時所使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="d64d4-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d64d4-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d64d4-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="d64d4-126">指定預設的後端 HTTP 設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="d64d4-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="d64d4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64d4-127">-DefaultProfile</span></span>
<span data-ttu-id="d64d4-128">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d64d4-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d64d4-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d64d4-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="d64d4-130">應用程式閘道的預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d64d4-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d64d4-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d64d4-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="d64d4-132">應用程式閘道的預設重新導向設定檔識別碼</span><span class="sxs-lookup"><span data-stu-id="d64d4-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d64d4-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d64d4-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="d64d4-134">應用程式閘道的預設重寫規則集</span><span class="sxs-lookup"><span data-stu-id="d64d4-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="d64d4-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="d64d4-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="d64d4-136">應用程式閘道預設重寫規則集的識別碼</span><span class="sxs-lookup"><span data-stu-id="d64d4-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="d64d4-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="d64d4-137">-Name</span></span>
<span data-ttu-id="d64d4-138">指定此 Cmdlet 設定其 URL 路徑地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="d64d4-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="d64d4-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="d64d4-139">-PathRules</span></span>
<span data-ttu-id="d64d4-140">指定路徑規則的清單。</span><span class="sxs-lookup"><span data-stu-id="d64d4-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="d64d4-141">請注意，路徑規則會區分順序，因此會以指定的順序來使用規則。</span><span class="sxs-lookup"><span data-stu-id="d64d4-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="d64d4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64d4-142">CommonParameters</span></span>
<span data-ttu-id="d64d4-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d64d4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64d4-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d64d4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64d4-145">輸入</span><span class="sxs-lookup"><span data-stu-id="d64d4-145">INPUTS</span></span>

### <span data-ttu-id="d64d4-146">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d64d4-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d64d4-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d64d4-147">OUTPUTS</span></span>

### <span data-ttu-id="d64d4-148">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d64d4-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d64d4-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d64d4-149">NOTES</span></span>

## <span data-ttu-id="d64d4-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d64d4-150">RELATED LINKS</span></span>

[<span data-ttu-id="d64d4-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d64d4-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d64d4-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d64d4-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d64d4-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d64d4-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d64d4-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d64d4-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


