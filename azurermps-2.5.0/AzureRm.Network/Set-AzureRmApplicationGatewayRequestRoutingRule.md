---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: e3b52040090ace745f58e8c3dd56ac59bb5d9b73
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800745"
---
# <span data-ttu-id="859da-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="859da-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="859da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="859da-102">SYNOPSIS</span></span>
<span data-ttu-id="859da-103">修改應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="859da-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="859da-104">句法</span><span class="sxs-lookup"><span data-stu-id="859da-104">SYNTAX</span></span>

### <span data-ttu-id="859da-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="859da-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="859da-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="859da-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="859da-107">說明</span><span class="sxs-lookup"><span data-stu-id="859da-107">DESCRIPTION</span></span>
<span data-ttu-id="859da-108">**AzureRmApplicationGatewayRequestRoutingRule** Cmdlet 會修改要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="859da-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="859da-109">示例</span><span class="sxs-lookup"><span data-stu-id="859da-109">EXAMPLES</span></span>

### <span data-ttu-id="859da-110">範例1：更新要求路由規則</span><span class="sxs-lookup"><span data-stu-id="859da-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="859da-111">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="859da-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="859da-112">第二個命令會修改應用程式閘道的要求路由規則，以使用 $Setting 變數中指定的後端 HTTP 設定、$Listener 變數中指定的 HTTP 偵聽程式，以及在 $Pool 變數中指定的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="859da-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="859da-113">參數</span><span class="sxs-lookup"><span data-stu-id="859da-113">PARAMETERS</span></span>

### <span data-ttu-id="859da-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="859da-114">-ApplicationGateway</span></span>
<span data-ttu-id="859da-115">指定應用程式閘道物件，此 Cmdlet 會將請求路由規則關聯。</span><span class="sxs-lookup"><span data-stu-id="859da-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="859da-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="859da-116">-BackendAddressPool</span></span>
<span data-ttu-id="859da-117">指定應用程式閘道後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="859da-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="859da-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="859da-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="859da-119">指定應用程式閘道後端位址集區 ID。</span><span class="sxs-lookup"><span data-stu-id="859da-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="859da-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="859da-120">-BackendHttpSettings</span></span>
<span data-ttu-id="859da-121">指定應用程式閘道後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="859da-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="859da-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="859da-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="859da-123">指定應用程式閘道後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="859da-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="859da-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859da-124">-DefaultProfile</span></span>
<span data-ttu-id="859da-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="859da-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="859da-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="859da-126">-HttpListener</span></span>
<span data-ttu-id="859da-127">指定應用程式閘道 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="859da-127">Specifies the application gateway HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859da-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="859da-128">-HttpListenerId</span></span>
<span data-ttu-id="859da-129">指定應用程式閘道 HTTP 偵聽程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="859da-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="859da-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="859da-130">-Name</span></span>
<span data-ttu-id="859da-131">指定此 Cmdlet 所修改之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="859da-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="859da-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="859da-132">-RedirectConfiguration</span></span>
<span data-ttu-id="859da-133">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="859da-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="859da-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="859da-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="859da-135">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="859da-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="859da-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="859da-136">-RuleType</span></span>
<span data-ttu-id="859da-137">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="859da-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859da-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="859da-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859da-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="859da-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="859da-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859da-140">CommonParameters</span></span>
<span data-ttu-id="859da-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="859da-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859da-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="859da-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859da-143">輸入</span><span class="sxs-lookup"><span data-stu-id="859da-143">INPUTS</span></span>

### <span data-ttu-id="859da-144">System.object</span><span class="sxs-lookup"><span data-stu-id="859da-144">System.String</span></span>

## <span data-ttu-id="859da-145">輸出</span><span class="sxs-lookup"><span data-stu-id="859da-145">OUTPUTS</span></span>

### <span data-ttu-id="859da-146">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="859da-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="859da-147">筆記</span><span class="sxs-lookup"><span data-stu-id="859da-147">NOTES</span></span>

## <span data-ttu-id="859da-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="859da-148">RELATED LINKS</span></span>

[<span data-ttu-id="859da-149">附加 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="859da-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="859da-150">AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="859da-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="859da-151">新-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="859da-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="859da-152">移除-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="859da-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)


