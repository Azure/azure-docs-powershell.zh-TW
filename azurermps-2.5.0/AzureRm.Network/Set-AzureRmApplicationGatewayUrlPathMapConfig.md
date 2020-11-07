---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 7ca1d4f8ee4ab3e83badecd7856fcee35f5b9a23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801597"
---
# <span data-ttu-id="02936-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="02936-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="02936-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02936-102">SYNOPSIS</span></span>
<span data-ttu-id="02936-103">將 URL 路徑對應陣列的設定設為後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="02936-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02936-104">句法</span><span class="sxs-lookup"><span data-stu-id="02936-104">SYNTAX</span></span>

### <span data-ttu-id="02936-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="02936-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02936-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="02936-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02936-107">說明</span><span class="sxs-lookup"><span data-stu-id="02936-107">DESCRIPTION</span></span>
<span data-ttu-id="02936-108">AzureRmApplicationGatewayUrlPathMapConfig Cmdlet 會將 URL 路徑映射陣列的 **設定** 設定為後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="02936-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="02936-109">示例</span><span class="sxs-lookup"><span data-stu-id="02936-109">EXAMPLES</span></span>

### <span data-ttu-id="02936-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="02936-110">1:</span></span>
```

```

## <span data-ttu-id="02936-111">參數</span><span class="sxs-lookup"><span data-stu-id="02936-111">PARAMETERS</span></span>

### <span data-ttu-id="02936-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02936-112">-ApplicationGateway</span></span>
<span data-ttu-id="02936-113">指定此 Cmdlet 設定 URL 路徑對應配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="02936-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02936-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="02936-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="02936-115">指定在 *pathRules* 參數中指定的規則不相符時，要路由的預設後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="02936-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02936-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="02936-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="02936-117">指定預設的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="02936-117">Specifies the default backend address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02936-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="02936-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="02936-119">指定要在 *pathRules* 參數中指定的規則都不相符時使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="02936-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02936-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="02936-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="02936-121">指定預設的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="02936-121">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02936-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02936-122">-DefaultProfile</span></span>
<span data-ttu-id="02936-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02936-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02936-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="02936-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="02936-125">應用程式閘道預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="02936-125">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02936-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="02936-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="02936-127">應用程式閘道預設 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="02936-127">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02936-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="02936-128">-Name</span></span>
<span data-ttu-id="02936-129">指定此 Cmdlet 針對其設定配置的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="02936-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02936-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="02936-130">-PathRules</span></span>
<span data-ttu-id="02936-131">指定路徑規則清單。</span><span class="sxs-lookup"><span data-stu-id="02936-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="02936-132">請注意，路徑規則是區分順序的，它們會依指定順序加以套用。</span><span class="sxs-lookup"><span data-stu-id="02936-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="02936-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02936-133">CommonParameters</span></span>
<span data-ttu-id="02936-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02936-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02936-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02936-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02936-136">輸入</span><span class="sxs-lookup"><span data-stu-id="02936-136">INPUTS</span></span>

### <span data-ttu-id="02936-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02936-137">PSApplicationGateway</span></span>
<span data-ttu-id="02936-138">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="02936-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="02936-139">輸出</span><span class="sxs-lookup"><span data-stu-id="02936-139">OUTPUTS</span></span>

### <span data-ttu-id="02936-140">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="02936-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="02936-141">筆記</span><span class="sxs-lookup"><span data-stu-id="02936-141">NOTES</span></span>

## <span data-ttu-id="02936-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="02936-142">RELATED LINKS</span></span>

[<span data-ttu-id="02936-143">附加 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="02936-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="02936-144">AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="02936-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="02936-145">新-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="02936-145">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="02936-146">移除-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="02936-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


