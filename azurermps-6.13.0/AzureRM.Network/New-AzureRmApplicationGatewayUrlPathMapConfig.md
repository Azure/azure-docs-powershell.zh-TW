---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 6752526e5c6f035d6446c4e6e3ed31724bdbd337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626379"
---
# <span data-ttu-id="7d6b5-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7d6b5-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7d6b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6b5-103">建立與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d6b5-104">SYNTAX</span></span>

### <span data-ttu-id="7d6b5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d6b5-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d6b5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7d6b5-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d6b5-107">說明</span><span class="sxs-lookup"><span data-stu-id="7d6b5-107">DESCRIPTION</span></span>
<span data-ttu-id="7d6b5-108">**AzureRmApplicationGatewayUrlPathMapConfig** Cmdlet 會建立一個與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7d6b5-109">示例</span><span class="sxs-lookup"><span data-stu-id="7d6b5-109">EXAMPLES</span></span>

### <span data-ttu-id="7d6b5-110">範例1：建立到後端伺服器池的 URL 路徑對應陣列</span><span class="sxs-lookup"><span data-stu-id="7d6b5-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="7d6b5-111">這個命令會建立一個與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7d6b5-112">參數</span><span class="sxs-lookup"><span data-stu-id="7d6b5-112">PARAMETERS</span></span>

### <span data-ttu-id="7d6b5-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7d6b5-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="7d6b5-114">指定在 *pathRules* 參數中指定的規則不相符時，要路由的預設後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="7d6b5-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7d6b5-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="7d6b5-116">指定預設的後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="7d6b5-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7d6b5-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="7d6b5-118">指定要在 *pathRules* 參數中指定的規則都不相符時使用的預設後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="7d6b5-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="7d6b5-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="7d6b5-120">指定預設的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="7d6b5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6b5-121">-DefaultProfile</span></span>
<span data-ttu-id="7d6b5-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d6b5-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d6b5-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="7d6b5-124">應用程式閘道預設 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d6b5-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="7d6b5-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7d6b5-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="7d6b5-126">應用程式閘道預設 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="7d6b5-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="7d6b5-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d6b5-127">-Name</span></span>
<span data-ttu-id="7d6b5-128">指定此 Cmdlet 建立的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7d6b5-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="7d6b5-129">-PathRules</span></span>
<span data-ttu-id="7d6b5-130">指定路徑規則清單。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="7d6b5-131">請注意，路徑規則是區分順序的，它們會依指定順序加以套用。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="7d6b5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6b5-132">CommonParameters</span></span>
<span data-ttu-id="7d6b5-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6b5-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d6b5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6b5-135">輸入</span><span class="sxs-lookup"><span data-stu-id="7d6b5-135">INPUTS</span></span>

### <span data-ttu-id="7d6b5-136">所有</span><span class="sxs-lookup"><span data-stu-id="7d6b5-136">None</span></span>

## <span data-ttu-id="7d6b5-137">輸出</span><span class="sxs-lookup"><span data-stu-id="7d6b5-137">OUTPUTS</span></span>

### <span data-ttu-id="7d6b5-138">PSApplicationGatewayUrlPathMap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7d6b5-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="7d6b5-139">筆記</span><span class="sxs-lookup"><span data-stu-id="7d6b5-139">NOTES</span></span>

## <span data-ttu-id="7d6b5-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d6b5-140">RELATED LINKS</span></span>

[<span data-ttu-id="7d6b5-141">附加 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7d6b5-141">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7d6b5-142">AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7d6b5-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7d6b5-143">移除-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7d6b5-143">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7d6b5-144">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7d6b5-144">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


