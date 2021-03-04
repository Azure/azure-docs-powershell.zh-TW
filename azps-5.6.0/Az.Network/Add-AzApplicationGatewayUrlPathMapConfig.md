---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 2bc6a8eed22660d966256afbc9783e4edfc04947
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910702"
---
# <span data-ttu-id="5db4b-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5db4b-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5db4b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5db4b-102">SYNOPSIS</span></span>
<span data-ttu-id="5db4b-103">將 URL 路徑的陣列新增到後端伺服器資料庫。</span><span class="sxs-lookup"><span data-stu-id="5db4b-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5db4b-104">語法</span><span class="sxs-lookup"><span data-stu-id="5db4b-104">SYNTAX</span></span>

### <span data-ttu-id="5db4b-105">後端SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="5db4b-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5db4b-106">後端SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5db4b-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5db4b-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="5db4b-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5db4b-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5db4b-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5db4b-109">描述</span><span class="sxs-lookup"><span data-stu-id="5db4b-109">DESCRIPTION</span></span>
<span data-ttu-id="5db4b-110">**Add-AzApplicationGatewayUrlPathMapConfig** Cmdlet 會將 URL 路徑的陣列新增到後端伺服器集區。</span><span class="sxs-lookup"><span data-stu-id="5db4b-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="5db4b-111">例子</span><span class="sxs-lookup"><span data-stu-id="5db4b-111">EXAMPLES</span></span>

### <span data-ttu-id="5db4b-112">範例 1：新增應用程式閘道的 URL 路徑。</span><span class="sxs-lookup"><span data-stu-id="5db4b-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="5db4b-113">第一個命令會獲得名為 appGwName 的應用程式閘道，並儲存在$appgw變數。</span><span class="sxs-lookup"><span data-stu-id="5db4b-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="5db4b-114">第二個命令會獲得後端位址資料庫，並儲存在$pool變數。</span><span class="sxs-lookup"><span data-stu-id="5db4b-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="5db4b-115">第三個命令會獲得後端 HTTP 設定，並儲存在$poolSettings變數。</span><span class="sxs-lookup"><span data-stu-id="5db4b-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="5db4b-116">第四個命令會建立名為 rule01 的新路徑規則組$pathRule變數。</span><span class="sxs-lookup"><span data-stu-id="5db4b-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="5db4b-117">第五個命令會新增 URL 路徑，將名稱為 url01 的 URL 路徑轉換到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5db4b-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="5db4b-118">第六個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5db4b-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="5db4b-119">參數</span><span class="sxs-lookup"><span data-stu-id="5db4b-119">PARAMETERS</span></span>

### <span data-ttu-id="5db4b-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5db4b-120">-ApplicationGateway</span></span>
<span data-ttu-id="5db4b-121">指定此 Cmdlet 新增 URL 路徑地圖組配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5db4b-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="5db4b-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5db4b-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5db4b-123">指定要路由的預設後端位址資料庫，以防 *pathRules* 參數中指定的規則沒有相符。</span><span class="sxs-lookup"><span data-stu-id="5db4b-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5db4b-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5db4b-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5db4b-125">指定預設的後端位址資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="5db4b-125">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="5db4b-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5db4b-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5db4b-127">指定在 *pathRules* 參數中指定的規則與規則不相符時所使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="5db4b-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5db4b-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5db4b-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5db4b-129">指定預設的後端 HTTP 設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="5db4b-129">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="5db4b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db4b-130">-DefaultProfile</span></span>
<span data-ttu-id="5db4b-131">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5db4b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5db4b-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5db4b-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5db4b-133">應用程式閘道的預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5db4b-133">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5db4b-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5db4b-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5db4b-135">應用程式閘道的預設重新導向設定檔識別碼</span><span class="sxs-lookup"><span data-stu-id="5db4b-135">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5db4b-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5db4b-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="5db4b-137">應用程式閘道的預設重寫規則集</span><span class="sxs-lookup"><span data-stu-id="5db4b-137">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="5db4b-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="5db4b-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="5db4b-139">應用程式閘道預設重寫規則集的識別碼</span><span class="sxs-lookup"><span data-stu-id="5db4b-139">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="5db4b-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="5db4b-140">-Name</span></span>
<span data-ttu-id="5db4b-141">指定此 Cmdlet 新增到後端伺服器資料庫的 URL 路徑地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="5db4b-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="5db4b-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5db4b-142">-PathRules</span></span>
<span data-ttu-id="5db4b-143">指定路徑規則的清單。</span><span class="sxs-lookup"><span data-stu-id="5db4b-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="5db4b-144">路徑規則會區分順序，因此會以指定的順序來使用。</span><span class="sxs-lookup"><span data-stu-id="5db4b-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="5db4b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db4b-145">CommonParameters</span></span>
<span data-ttu-id="5db4b-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5db4b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db4b-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5db4b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db4b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="5db4b-148">INPUTS</span></span>

### <span data-ttu-id="5db4b-149">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5db4b-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5db4b-150">輸出</span><span class="sxs-lookup"><span data-stu-id="5db4b-150">OUTPUTS</span></span>

### <span data-ttu-id="5db4b-151">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5db4b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5db4b-152">筆記</span><span class="sxs-lookup"><span data-stu-id="5db4b-152">NOTES</span></span>

## <span data-ttu-id="5db4b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="5db4b-153">RELATED LINKS</span></span>

[<span data-ttu-id="5db4b-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5db4b-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5db4b-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5db4b-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5db4b-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5db4b-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5db4b-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5db4b-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


