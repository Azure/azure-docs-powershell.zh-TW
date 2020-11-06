---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 821f31ba8f42ff8a7b94839aad344a2f144353d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453412"
---
# <span data-ttu-id="4e7d7-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e7d7-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4e7d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="4e7d7-103">在後端伺服器池中新增 URL 路徑對應的陣列。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e7d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e7d7-104">SYNTAX</span></span>

### <span data-ttu-id="4e7d7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e7d7-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e7d7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4e7d7-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e7d7-107">說明</span><span class="sxs-lookup"><span data-stu-id="4e7d7-107">DESCRIPTION</span></span>
<span data-ttu-id="4e7d7-108">**AzureRmApplicationGatewayUrlPathMapConfig** Cmdlet 會將 URL 路徑對應的陣列新增到後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="4e7d7-109">示例</span><span class="sxs-lookup"><span data-stu-id="4e7d7-109">EXAMPLES</span></span>

## <span data-ttu-id="4e7d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e7d7-110">PARAMETERS</span></span>

### <span data-ttu-id="4e7d7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e7d7-111">-ApplicationGateway</span></span>
<span data-ttu-id="4e7d7-112">指定此 Cmdlet 新增 URL 路徑對應配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="4e7d7-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4e7d7-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="4e7d7-114">指定在 *pathRules* 參數中指定的規則不相符時，要路由的預設後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="4e7d7-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4e7d7-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="4e7d7-116">指定預設的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="4e7d7-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4e7d7-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="4e7d7-118">指定要在 *pathRules* 參數中指定的規則都不相符時使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="4e7d7-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="4e7d7-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="4e7d7-120">指定預設的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="4e7d7-121">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e7d7-121">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="4e7d7-122">應用程式閘道預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e7d7-122">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="4e7d7-123">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4e7d7-123">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="4e7d7-124">應用程式閘道預設 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="4e7d7-124">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="4e7d7-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e7d7-125">-Name</span></span>
<span data-ttu-id="4e7d7-126">指定此 Cmdlet 新增到後端伺服器池中的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-126">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="4e7d7-127">-PathRules</span><span class="sxs-lookup"><span data-stu-id="4e7d7-127">-PathRules</span></span>
<span data-ttu-id="4e7d7-128">指定路徑規則清單。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-128">Specifies a list of path rules.</span></span>
<span data-ttu-id="4e7d7-129">路徑規則是區分順序的，它們會依指定順序加以套用。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-129">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="4e7d7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e7d7-130">-DefaultProfile</span></span>
<span data-ttu-id="4e7d7-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e7d7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e7d7-132">CommonParameters</span></span>
<span data-ttu-id="4e7d7-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e7d7-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e7d7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e7d7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4e7d7-135">INPUTS</span></span>

### <span data-ttu-id="4e7d7-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e7d7-136">PSApplicationGateway</span></span>
<span data-ttu-id="4e7d7-137">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="4e7d7-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="4e7d7-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4e7d7-138">OUTPUTS</span></span>

### <span data-ttu-id="4e7d7-139">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e7d7-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e7d7-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4e7d7-140">NOTES</span></span>

## <span data-ttu-id="4e7d7-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e7d7-141">RELATED LINKS</span></span>

[<span data-ttu-id="4e7d7-142">AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e7d7-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4e7d7-143">新-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e7d7-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4e7d7-144">移除-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e7d7-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4e7d7-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e7d7-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)

