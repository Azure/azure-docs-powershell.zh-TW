---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: e43d5277566311fe77ee239d88e55f658aca8b40
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800074"
---
# <span data-ttu-id="fabb2-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fabb2-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="fabb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fabb2-102">SYNOPSIS</span></span>
<span data-ttu-id="fabb2-103">建立與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="fabb2-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fabb2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fabb2-104">SYNTAX</span></span>

### <span data-ttu-id="fabb2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fabb2-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fabb2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fabb2-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fabb2-107">說明</span><span class="sxs-lookup"><span data-stu-id="fabb2-107">DESCRIPTION</span></span>
<span data-ttu-id="fabb2-108">**AzureRmApplicationGatewayUrlPathMapConfig** Cmdlet 會建立一個與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="fabb2-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="fabb2-109">示例</span><span class="sxs-lookup"><span data-stu-id="fabb2-109">EXAMPLES</span></span>

### <span data-ttu-id="fabb2-110">範例1：建立到後端伺服器池的 URL 路徑對應陣列</span><span class="sxs-lookup"><span data-stu-id="fabb2-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="fabb2-111">這個命令會建立一個與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="fabb2-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="fabb2-112">參數</span><span class="sxs-lookup"><span data-stu-id="fabb2-112">PARAMETERS</span></span>

### <span data-ttu-id="fabb2-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fabb2-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="fabb2-114">指定在 *pathRules* 參數中指定的規則不相符時，要路由的預設後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="fabb2-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="fabb2-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="fabb2-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="fabb2-116">指定預設的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="fabb2-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="fabb2-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fabb2-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="fabb2-118">指定要在 *pathRules* 參數中指定的規則都不相符時使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="fabb2-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="fabb2-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="fabb2-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="fabb2-120">指定預設的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="fabb2-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="fabb2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabb2-121">-DefaultProfile</span></span>
<span data-ttu-id="fabb2-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fabb2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fabb2-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fabb2-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="fabb2-124">應用程式閘道預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fabb2-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="fabb2-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fabb2-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="fabb2-126">應用程式閘道預設 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="fabb2-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="fabb2-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="fabb2-127">-Name</span></span>
<span data-ttu-id="fabb2-128">指定此 Cmdlet 建立的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="fabb2-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fabb2-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="fabb2-129">-PathRules</span></span>
<span data-ttu-id="fabb2-130">指定路徑規則清單。</span><span class="sxs-lookup"><span data-stu-id="fabb2-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="fabb2-131">請注意，路徑規則是區分順序的，它們會依指定順序加以套用。</span><span class="sxs-lookup"><span data-stu-id="fabb2-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="fabb2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabb2-132">CommonParameters</span></span>
<span data-ttu-id="fabb2-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fabb2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabb2-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fabb2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabb2-135">輸入</span><span class="sxs-lookup"><span data-stu-id="fabb2-135">INPUTS</span></span>

## <span data-ttu-id="fabb2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="fabb2-136">OUTPUTS</span></span>

### <span data-ttu-id="fabb2-137">PSApplicationGatewayUrlPathMap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fabb2-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="fabb2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="fabb2-138">NOTES</span></span>

## <span data-ttu-id="fabb2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="fabb2-139">RELATED LINKS</span></span>

[<span data-ttu-id="fabb2-140">附加 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fabb2-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="fabb2-141">AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fabb2-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="fabb2-142">移除-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fabb2-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="fabb2-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fabb2-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


