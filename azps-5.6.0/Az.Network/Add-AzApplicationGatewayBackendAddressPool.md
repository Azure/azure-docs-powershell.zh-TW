---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 9c5da09a801e78ad93ad609dc91f0c254309aa6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905926"
---
# <span data-ttu-id="dc3ad-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc3ad-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="dc3ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dc3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3ad-103">新增後端位址區至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="dc3ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="dc3ad-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc3ad-105">描述</span><span class="sxs-lookup"><span data-stu-id="dc3ad-105">DESCRIPTION</span></span>
<span data-ttu-id="dc3ad-106">**Add-AzApplicationGatewayBackendAddressPool** Cmdlet 會新增後端位址集區至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="dc3ad-107">後端位址可以使用 IP 位址指定，IP 位址是 FQDN (IP) 或 IP 組) 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="dc3ad-108">例子</span><span class="sxs-lookup"><span data-stu-id="dc3ad-108">EXAMPLES</span></span>

### <span data-ttu-id="dc3ad-109">範例 1：使用後端伺服器 FQDN 新增後端位址資料庫</span><span class="sxs-lookup"><span data-stu-id="dc3ad-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="dc3ad-110">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在 $AppGw 變數中。第二個命令會使用 FQDN 新增儲存在 $AppGw 應用程式閘道的後端位址區。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="dc3ad-111">範例 2：使用後端伺服器 IP 位址新增後端位址資料庫</span><span class="sxs-lookup"><span data-stu-id="dc3ad-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="dc3ad-112">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在 $AppGw 變數中。第二個命令會使用 IP 位址新增儲存在 $AppGw 之應用程式閘道的後端位址區。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="dc3ad-113">參數</span><span class="sxs-lookup"><span data-stu-id="dc3ad-113">PARAMETERS</span></span>

### <span data-ttu-id="dc3ad-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc3ad-114">-ApplicationGateway</span></span>
<span data-ttu-id="dc3ad-115">指定此 Cmdlet 新增後端位址區的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="dc3ad-116">-後端Fqdns</span><span class="sxs-lookup"><span data-stu-id="dc3ad-116">-BackendFqdns</span></span>
<span data-ttu-id="dc3ad-117">指定此 Cmdlet 新增為後端伺服器資料庫的後端 FQDN 清單。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3ad-118">-後端IPAddresses</span><span class="sxs-lookup"><span data-stu-id="dc3ad-118">-BackendIPAddresses</span></span>
<span data-ttu-id="dc3ad-119">指定此 Cmdlet 新增為後端伺服器資料庫的後端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3ad-120">-DefaultProfile</span></span>
<span data-ttu-id="dc3ad-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc3ad-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc3ad-122">-Name</span></span>
<span data-ttu-id="dc3ad-123">指定此 Cmdlet 新增的後端伺服器資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="dc3ad-124">-確認</span><span class="sxs-lookup"><span data-stu-id="dc3ad-124">-Confirm</span></span>
<span data-ttu-id="dc3ad-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3ad-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc3ad-126">-WhatIf</span></span>
<span data-ttu-id="dc3ad-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc3ad-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3ad-129">CommonParameters</span></span>
<span data-ttu-id="dc3ad-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3ad-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dc3ad-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3ad-132">輸入</span><span class="sxs-lookup"><span data-stu-id="dc3ad-132">INPUTS</span></span>

### <span data-ttu-id="dc3ad-133">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc3ad-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc3ad-134">輸出</span><span class="sxs-lookup"><span data-stu-id="dc3ad-134">OUTPUTS</span></span>

### <span data-ttu-id="dc3ad-135">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc3ad-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc3ad-136">筆記</span><span class="sxs-lookup"><span data-stu-id="dc3ad-136">NOTES</span></span>

## <span data-ttu-id="dc3ad-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc3ad-137">RELATED LINKS</span></span>

[<span data-ttu-id="dc3ad-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc3ad-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc3ad-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc3ad-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc3ad-140">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc3ad-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc3ad-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc3ad-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc3ad-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc3ad-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc3ad-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc3ad-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
