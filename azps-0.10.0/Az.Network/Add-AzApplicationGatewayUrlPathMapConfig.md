---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: eedf03e2468be36fadc519fc2e6b931c82433fc0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794526"
---
# <span data-ttu-id="0aa87-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0aa87-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="0aa87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0aa87-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa87-103">在後端伺服器池中新增 URL 路徑對應的陣列。</span><span class="sxs-lookup"><span data-stu-id="0aa87-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="0aa87-104">句法</span><span class="sxs-lookup"><span data-stu-id="0aa87-104">SYNTAX</span></span>

### <span data-ttu-id="0aa87-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0aa87-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0aa87-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0aa87-106">SetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0aa87-107">說明</span><span class="sxs-lookup"><span data-stu-id="0aa87-107">DESCRIPTION</span></span>
<span data-ttu-id="0aa87-108">**AzApplicationGatewayUrlPathMapConfig** Cmdlet 會將 URL 路徑對應的陣列新增到後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="0aa87-108">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="0aa87-109">示例</span><span class="sxs-lookup"><span data-stu-id="0aa87-109">EXAMPLES</span></span>

### <span data-ttu-id="0aa87-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="0aa87-110">1:</span></span>
```

```

## <span data-ttu-id="0aa87-111">參數</span><span class="sxs-lookup"><span data-stu-id="0aa87-111">PARAMETERS</span></span>

### <span data-ttu-id="0aa87-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0aa87-112">-ApplicationGateway</span></span>
<span data-ttu-id="0aa87-113">指定此 Cmdlet 新增 URL 路徑對應配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0aa87-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="0aa87-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0aa87-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="0aa87-115">指定在 *pathRules* 參數中指定的規則不相符時，要路由的預設後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="0aa87-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="0aa87-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0aa87-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="0aa87-117">指定預設的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="0aa87-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="0aa87-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0aa87-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="0aa87-119">指定要在 *pathRules* 參數中指定的規則都不相符時使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="0aa87-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="0aa87-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0aa87-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="0aa87-121">指定預設的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="0aa87-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="0aa87-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa87-122">-DefaultProfile</span></span>
<span data-ttu-id="0aa87-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0aa87-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aa87-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aa87-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="0aa87-125">應用程式閘道預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aa87-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="0aa87-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0aa87-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="0aa87-127">應用程式閘道預設 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="0aa87-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="0aa87-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="0aa87-128">-Name</span></span>
<span data-ttu-id="0aa87-129">指定此 Cmdlet 新增到後端伺服器池中的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="0aa87-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="0aa87-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="0aa87-130">-PathRules</span></span>
<span data-ttu-id="0aa87-131">指定路徑規則清單。</span><span class="sxs-lookup"><span data-stu-id="0aa87-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="0aa87-132">路徑規則是區分順序的，它們會依指定順序加以套用。</span><span class="sxs-lookup"><span data-stu-id="0aa87-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="0aa87-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa87-133">CommonParameters</span></span>
<span data-ttu-id="0aa87-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0aa87-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa87-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0aa87-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa87-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0aa87-136">INPUTS</span></span>

### <span data-ttu-id="0aa87-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0aa87-137">PSApplicationGateway</span></span>
<span data-ttu-id="0aa87-138">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0aa87-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="0aa87-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0aa87-139">OUTPUTS</span></span>

### <span data-ttu-id="0aa87-140">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0aa87-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0aa87-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0aa87-141">NOTES</span></span>

## <span data-ttu-id="0aa87-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0aa87-142">RELATED LINKS</span></span>

[<span data-ttu-id="0aa87-143">AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0aa87-143">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0aa87-144">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0aa87-144">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0aa87-145">移除-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0aa87-145">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0aa87-146">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0aa87-146">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


