---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966215"
---
# <span data-ttu-id="71fc2-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="71fc2-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="71fc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="71fc2-103">建立與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="71fc2-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="71fc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="71fc2-104">SYNTAX</span></span>

### <span data-ttu-id="71fc2-105">BackendSetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="71fc2-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71fc2-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="71fc2-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71fc2-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="71fc2-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71fc2-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="71fc2-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71fc2-109">說明</span><span class="sxs-lookup"><span data-stu-id="71fc2-109">DESCRIPTION</span></span>
<span data-ttu-id="71fc2-110">**AzApplicationGatewayUrlPathMapConfig** Cmdlet 會建立一個與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="71fc2-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="71fc2-111">示例</span><span class="sxs-lookup"><span data-stu-id="71fc2-111">EXAMPLES</span></span>

### <span data-ttu-id="71fc2-112">範例1：建立到後端伺服器池的 URL 路徑對應陣列</span><span class="sxs-lookup"><span data-stu-id="71fc2-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="71fc2-113">這個命令會建立一個與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="71fc2-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="71fc2-114">參數</span><span class="sxs-lookup"><span data-stu-id="71fc2-114">PARAMETERS</span></span>

### <span data-ttu-id="71fc2-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="71fc2-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="71fc2-116">指定在 *pathRules* 參數中指定的規則不相符時，要路由的預設後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="71fc2-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="71fc2-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="71fc2-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="71fc2-118">指定預設的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="71fc2-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="71fc2-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="71fc2-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="71fc2-120">指定要在 *pathRules* 參數中指定的規則都不相符時使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="71fc2-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="71fc2-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="71fc2-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="71fc2-122">指定預設的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="71fc2-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="71fc2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fc2-123">-DefaultProfile</span></span>
<span data-ttu-id="71fc2-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71fc2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71fc2-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="71fc2-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="71fc2-126">應用程式閘道預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="71fc2-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="71fc2-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="71fc2-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="71fc2-128">應用程式閘道預設 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="71fc2-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="71fc2-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71fc2-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="71fc2-130">應用程式閘道的預設重寫規則集</span><span class="sxs-lookup"><span data-stu-id="71fc2-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="71fc2-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="71fc2-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="71fc2-132">應用程式閘道的預設重寫規則集識別碼</span><span class="sxs-lookup"><span data-stu-id="71fc2-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="71fc2-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="71fc2-133">-Name</span></span>
<span data-ttu-id="71fc2-134">指定此 Cmdlet 建立的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="71fc2-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="71fc2-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="71fc2-135">-PathRules</span></span>
<span data-ttu-id="71fc2-136">指定路徑規則清單。</span><span class="sxs-lookup"><span data-stu-id="71fc2-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="71fc2-137">請注意，路徑規則是區分順序的，它們會依指定順序加以套用。</span><span class="sxs-lookup"><span data-stu-id="71fc2-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="71fc2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fc2-138">CommonParameters</span></span>
<span data-ttu-id="71fc2-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71fc2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fc2-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71fc2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fc2-141">輸入</span><span class="sxs-lookup"><span data-stu-id="71fc2-141">INPUTS</span></span>

### <span data-ttu-id="71fc2-142">所有</span><span class="sxs-lookup"><span data-stu-id="71fc2-142">None</span></span>

## <span data-ttu-id="71fc2-143">輸出</span><span class="sxs-lookup"><span data-stu-id="71fc2-143">OUTPUTS</span></span>

### <span data-ttu-id="71fc2-144">PSApplicationGatewayUrlPathMap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="71fc2-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="71fc2-145">筆記</span><span class="sxs-lookup"><span data-stu-id="71fc2-145">NOTES</span></span>

## <span data-ttu-id="71fc2-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="71fc2-146">RELATED LINKS</span></span>

[<span data-ttu-id="71fc2-147">附加 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="71fc2-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="71fc2-148">AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="71fc2-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="71fc2-149">移除-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="71fc2-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="71fc2-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="71fc2-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

