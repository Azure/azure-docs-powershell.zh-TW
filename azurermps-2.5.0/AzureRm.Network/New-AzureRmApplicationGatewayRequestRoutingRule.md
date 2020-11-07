---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 2f4b1abc5d6cd6d55eef3c45c01a2939842e32c6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801610"
---
# <span data-ttu-id="dfdb6-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dfdb6-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="dfdb6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfdb6-102">SYNOPSIS</span></span>
<span data-ttu-id="dfdb6-103">建立應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfdb6-104">句法</span><span class="sxs-lookup"><span data-stu-id="dfdb6-104">SYNTAX</span></span>

### <span data-ttu-id="dfdb6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dfdb6-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dfdb6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dfdb6-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfdb6-107">說明</span><span class="sxs-lookup"><span data-stu-id="dfdb6-107">DESCRIPTION</span></span>
<span data-ttu-id="dfdb6-108">**AzureRmApplicationGatewayRequestRoutingRule** Cmdlet 會建立 Azure 應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="dfdb6-109">示例</span><span class="sxs-lookup"><span data-stu-id="dfdb6-109">EXAMPLES</span></span>

### <span data-ttu-id="dfdb6-110">範例1：建立應用程式閘道的要求路由規則</span><span class="sxs-lookup"><span data-stu-id="dfdb6-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="dfdb6-111">這個命令會建立一個名為 Rule01 的基本要求路由規則，並將結果儲存在名為 $Rule 的變數中。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="dfdb6-112">參數</span><span class="sxs-lookup"><span data-stu-id="dfdb6-112">PARAMETERS</span></span>

### <span data-ttu-id="dfdb6-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dfdb6-113">-BackendAddressPool</span></span>
<span data-ttu-id="dfdb6-114">針對要建立的要求路由規則，將後端位址集區指定為物件。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="dfdb6-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="dfdb6-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="dfdb6-116">指定要建立之要求路由規則的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="dfdb6-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="dfdb6-117">-BackendHttpSettings</span></span>
<span data-ttu-id="dfdb6-118">針對要建立的要求路由規則，將後端 HTTP 設定指定為物件。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="dfdb6-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="dfdb6-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="dfdb6-120">指定要建立之要求路由規則的後端 HTTP 設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="dfdb6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfdb6-121">-DefaultProfile</span></span>
<span data-ttu-id="dfdb6-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfdb6-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="dfdb6-123">-HttpListener</span></span>
<span data-ttu-id="dfdb6-124">針對要建立的要求路由規則指定後端 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="dfdb6-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="dfdb6-125">-HttpListenerId</span></span>
<span data-ttu-id="dfdb6-126">指定要建立之要求路由規則的後端 HTTP 偵聽程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="dfdb6-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="dfdb6-127">-Name</span></span>
<span data-ttu-id="dfdb6-128">指定此 Cmdlet 所建立之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="dfdb6-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfdb6-129">-RedirectConfiguration</span></span>
<span data-ttu-id="dfdb6-130">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfdb6-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="dfdb6-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dfdb6-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="dfdb6-132">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="dfdb6-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="dfdb6-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="dfdb6-133">-RuleType</span></span>
<span data-ttu-id="dfdb6-134">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="dfdb6-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="dfdb6-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="dfdb6-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="dfdb6-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="dfdb6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfdb6-137">CommonParameters</span></span>
<span data-ttu-id="dfdb6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfdb6-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dfdb6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfdb6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="dfdb6-140">INPUTS</span></span>

### <span data-ttu-id="dfdb6-141">System.object</span><span class="sxs-lookup"><span data-stu-id="dfdb6-141">System.String</span></span>

## <span data-ttu-id="dfdb6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="dfdb6-142">OUTPUTS</span></span>

### <span data-ttu-id="dfdb6-143">PSApplicationGatewayRequestRoutingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dfdb6-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="dfdb6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="dfdb6-144">NOTES</span></span>

## <span data-ttu-id="dfdb6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfdb6-145">RELATED LINKS</span></span>

[<span data-ttu-id="dfdb6-146">附加 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dfdb6-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="dfdb6-147">AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dfdb6-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="dfdb6-148">移除-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dfdb6-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="dfdb6-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dfdb6-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


