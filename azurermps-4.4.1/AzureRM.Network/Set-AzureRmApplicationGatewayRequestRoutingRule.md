---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: a6cf6c4918dcaacb49ca9257acb436cec0556767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446713"
---
# <span data-ttu-id="6e9a2-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e9a2-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6e9a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e9a2-102">SYNOPSIS</span></span>
<span data-ttu-id="6e9a2-103">修改應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e9a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e9a2-104">SYNTAX</span></span>

### <span data-ttu-id="6e9a2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e9a2-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e9a2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6e9a2-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e9a2-107">說明</span><span class="sxs-lookup"><span data-stu-id="6e9a2-107">DESCRIPTION</span></span>
<span data-ttu-id="6e9a2-108">**AzureRmApplicationGatewayRequestRoutingRule** Cmdlet 會修改要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="6e9a2-109">示例</span><span class="sxs-lookup"><span data-stu-id="6e9a2-109">EXAMPLES</span></span>

### <span data-ttu-id="6e9a2-110">範例1：更新要求路由規則</span><span class="sxs-lookup"><span data-stu-id="6e9a2-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="6e9a2-111">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="6e9a2-112">第二個命令會修改應用程式閘道的要求路由規則，以使用 $Setting 變數中指定的後端 HTTP 設定、$Listener 變數中指定的 HTTP 偵聽程式，以及在 $Pool 變數中指定的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="6e9a2-113">參數</span><span class="sxs-lookup"><span data-stu-id="6e9a2-113">PARAMETERS</span></span>

### <span data-ttu-id="6e9a2-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e9a2-114">-ApplicationGateway</span></span>
<span data-ttu-id="6e9a2-115">指定應用程式閘道物件，此 Cmdlet 會將請求路由規則關聯。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="6e9a2-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6e9a2-116">-BackendAddressPool</span></span>
<span data-ttu-id="6e9a2-117">指定應用程式閘道後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="6e9a2-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6e9a2-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="6e9a2-119">指定應用程式閘道後端位址集區 ID。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="6e9a2-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6e9a2-120">-BackendHttpSettings</span></span>
<span data-ttu-id="6e9a2-121">指定應用程式閘道後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="6e9a2-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6e9a2-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="6e9a2-123">指定應用程式閘道後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="6e9a2-124">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="6e9a2-124">-HttpListener</span></span>
<span data-ttu-id="6e9a2-125">指定應用程式閘道 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-125">Specifies the application gateway HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a2-126">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="6e9a2-126">-HttpListenerId</span></span>
<span data-ttu-id="6e9a2-127">指定應用程式閘道 HTTP 偵聽程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-127">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="6e9a2-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e9a2-128">-Name</span></span>
<span data-ttu-id="6e9a2-129">指定此 Cmdlet 所修改之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-129">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6e9a2-130">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e9a2-130">-RedirectConfiguration</span></span>
<span data-ttu-id="6e9a2-131">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e9a2-131">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6e9a2-132">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6e9a2-132">-RedirectConfigurationId</span></span>
<span data-ttu-id="6e9a2-133">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="6e9a2-133">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6e9a2-134">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6e9a2-134">-RuleType</span></span>
<span data-ttu-id="6e9a2-135">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-135">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a2-136">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="6e9a2-136">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a2-137">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="6e9a2-137">-UrlPathMapId</span></span>
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

### <span data-ttu-id="6e9a2-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e9a2-138">-DefaultProfile</span></span>
<span data-ttu-id="6e9a2-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e9a2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e9a2-140">CommonParameters</span></span>
<span data-ttu-id="6e9a2-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e9a2-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6e9a2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e9a2-143">輸入</span><span class="sxs-lookup"><span data-stu-id="6e9a2-143">INPUTS</span></span>

### <span data-ttu-id="6e9a2-144">System.object</span><span class="sxs-lookup"><span data-stu-id="6e9a2-144">System.String</span></span>

## <span data-ttu-id="6e9a2-145">輸出</span><span class="sxs-lookup"><span data-stu-id="6e9a2-145">OUTPUTS</span></span>

### <span data-ttu-id="6e9a2-146">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6e9a2-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6e9a2-147">筆記</span><span class="sxs-lookup"><span data-stu-id="6e9a2-147">NOTES</span></span>

## <span data-ttu-id="6e9a2-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e9a2-148">RELATED LINKS</span></span>

[<span data-ttu-id="6e9a2-149">附加 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e9a2-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6e9a2-150">AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e9a2-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6e9a2-151">新-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e9a2-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6e9a2-152">移除-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e9a2-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)


