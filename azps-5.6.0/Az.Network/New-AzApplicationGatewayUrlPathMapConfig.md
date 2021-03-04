---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ebb73225a8afa7bb4c1061326aa9262dd46d9dc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916912"
---
# <span data-ttu-id="626bb-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="626bb-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="626bb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="626bb-102">SYNOPSIS</span></span>
<span data-ttu-id="626bb-103">建立後端伺服器資料庫 URL 路徑的陣列。</span><span class="sxs-lookup"><span data-stu-id="626bb-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="626bb-104">語法</span><span class="sxs-lookup"><span data-stu-id="626bb-104">SYNTAX</span></span>

### <span data-ttu-id="626bb-105">後端SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="626bb-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="626bb-106">後端SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="626bb-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="626bb-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="626bb-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="626bb-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="626bb-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="626bb-109">描述</span><span class="sxs-lookup"><span data-stu-id="626bb-109">DESCRIPTION</span></span>
<span data-ttu-id="626bb-110">**New-AzApplicationGatewayUrlPathMapConfig** Cmdlet 會建立一個陣列 URL 路徑，以與後端伺服器集區進行連結。</span><span class="sxs-lookup"><span data-stu-id="626bb-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="626bb-111">例子</span><span class="sxs-lookup"><span data-stu-id="626bb-111">EXAMPLES</span></span>

### <span data-ttu-id="626bb-112">範例 1：建立後端伺服器資料庫 URL 路徑的陣列</span><span class="sxs-lookup"><span data-stu-id="626bb-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="626bb-113">此命令會建立一個 URL 路徑陣列，與後端伺服器資料庫進行比對。</span><span class="sxs-lookup"><span data-stu-id="626bb-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="626bb-114">參數</span><span class="sxs-lookup"><span data-stu-id="626bb-114">PARAMETERS</span></span>

### <span data-ttu-id="626bb-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="626bb-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="626bb-116">指定要路由的預設後端位址資料庫，以防 *pathRules* 參數中指定的規則沒有相符。</span><span class="sxs-lookup"><span data-stu-id="626bb-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="626bb-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="626bb-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="626bb-118">指定預設的後端位址資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="626bb-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="626bb-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="626bb-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="626bb-120">指定在 *pathRules* 參數中指定的規則與規則不相符時所使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="626bb-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="626bb-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="626bb-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="626bb-122">指定預設的後端 HTTP 設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="626bb-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="626bb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626bb-123">-DefaultProfile</span></span>
<span data-ttu-id="626bb-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="626bb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="626bb-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="626bb-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="626bb-126">應用程式閘道的預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="626bb-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="626bb-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="626bb-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="626bb-128">應用程式閘道的預設重新導向設定檔識別碼</span><span class="sxs-lookup"><span data-stu-id="626bb-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="626bb-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="626bb-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="626bb-130">應用程式閘道的預設重寫規則集</span><span class="sxs-lookup"><span data-stu-id="626bb-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="626bb-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="626bb-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="626bb-132">應用程式閘道預設重寫規則集的識別碼</span><span class="sxs-lookup"><span data-stu-id="626bb-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="626bb-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="626bb-133">-Name</span></span>
<span data-ttu-id="626bb-134">指定此 Cmdlet 所建立 URL 路徑地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="626bb-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="626bb-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="626bb-135">-PathRules</span></span>
<span data-ttu-id="626bb-136">指定路徑規則的清單。</span><span class="sxs-lookup"><span data-stu-id="626bb-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="626bb-137">請注意，路徑規則會區分順序，因此會以指定的順序來使用規則。</span><span class="sxs-lookup"><span data-stu-id="626bb-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="626bb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626bb-138">CommonParameters</span></span>
<span data-ttu-id="626bb-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="626bb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626bb-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="626bb-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626bb-141">輸入</span><span class="sxs-lookup"><span data-stu-id="626bb-141">INPUTS</span></span>

### <span data-ttu-id="626bb-142">沒有</span><span class="sxs-lookup"><span data-stu-id="626bb-142">None</span></span>

## <span data-ttu-id="626bb-143">輸出</span><span class="sxs-lookup"><span data-stu-id="626bb-143">OUTPUTS</span></span>

### <span data-ttu-id="626bb-144">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="626bb-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="626bb-145">筆記</span><span class="sxs-lookup"><span data-stu-id="626bb-145">NOTES</span></span>

## <span data-ttu-id="626bb-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="626bb-146">RELATED LINKS</span></span>

[<span data-ttu-id="626bb-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="626bb-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="626bb-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="626bb-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="626bb-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="626bb-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="626bb-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="626bb-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


