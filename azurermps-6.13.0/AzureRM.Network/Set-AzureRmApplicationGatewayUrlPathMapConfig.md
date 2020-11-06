---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: d0944ad15beeab3de380801480560bc216a7df16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623408"
---
# <span data-ttu-id="5a7cf-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a7cf-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5a7cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7cf-103">將 URL 路徑對應陣列的設定設為後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a7cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a7cf-104">SYNTAX</span></span>

### <span data-ttu-id="5a7cf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a7cf-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a7cf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5a7cf-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a7cf-107">說明</span><span class="sxs-lookup"><span data-stu-id="5a7cf-107">DESCRIPTION</span></span>
<span data-ttu-id="5a7cf-108">AzureRmApplicationGatewayUrlPathMapConfig Cmdlet 會將 URL 路徑映射陣列的 **設定** 設定為後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5a7cf-109">示例</span><span class="sxs-lookup"><span data-stu-id="5a7cf-109">EXAMPLES</span></span>

## <span data-ttu-id="5a7cf-110">參數</span><span class="sxs-lookup"><span data-stu-id="5a7cf-110">PARAMETERS</span></span>

### <span data-ttu-id="5a7cf-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a7cf-111">-ApplicationGateway</span></span>
<span data-ttu-id="5a7cf-112">指定此 Cmdlet 設定 URL 路徑對應配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-112">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="5a7cf-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5a7cf-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5a7cf-114">指定在 *pathRules* 參數中指定的規則不相符時，要路由的預設後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5a7cf-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5a7cf-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5a7cf-116">指定預設的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="5a7cf-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5a7cf-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5a7cf-118">指定要在 *pathRules* 參數中指定的規則都不相符時使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5a7cf-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5a7cf-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5a7cf-120">指定預設的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="5a7cf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7cf-121">-DefaultProfile</span></span>
<span data-ttu-id="5a7cf-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7cf-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a7cf-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5a7cf-124">應用程式閘道預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a7cf-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5a7cf-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5a7cf-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5a7cf-126">應用程式閘道預設 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="5a7cf-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5a7cf-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a7cf-127">-Name</span></span>
<span data-ttu-id="5a7cf-128">指定此 Cmdlet 針對其設定配置的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-128">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="5a7cf-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5a7cf-129">-PathRules</span></span>
<span data-ttu-id="5a7cf-130">指定路徑規則清單。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="5a7cf-131">請注意，路徑規則是區分順序的，它們會依指定順序加以套用。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7cf-132">CommonParameters</span></span>
<span data-ttu-id="5a7cf-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7cf-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a7cf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7cf-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5a7cf-135">INPUTS</span></span>

### <span data-ttu-id="5a7cf-136">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5a7cf-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="5a7cf-137">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5a7cf-137">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="5a7cf-138">輸出</span><span class="sxs-lookup"><span data-stu-id="5a7cf-138">OUTPUTS</span></span>

### <span data-ttu-id="5a7cf-139">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5a7cf-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5a7cf-140">筆記</span><span class="sxs-lookup"><span data-stu-id="5a7cf-140">NOTES</span></span>

## <span data-ttu-id="5a7cf-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a7cf-141">RELATED LINKS</span></span>

[<span data-ttu-id="5a7cf-142">附加 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a7cf-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5a7cf-143">AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a7cf-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5a7cf-144">新-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a7cf-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5a7cf-145">移除-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a7cf-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


