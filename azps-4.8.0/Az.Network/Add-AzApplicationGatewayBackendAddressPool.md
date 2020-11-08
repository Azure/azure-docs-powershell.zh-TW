---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127060"
---
# <span data-ttu-id="b62cc-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b62cc-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b62cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b62cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b62cc-103">將後端位址集區新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b62cc-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="b62cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b62cc-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b62cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="b62cc-105">DESCRIPTION</span></span>
<span data-ttu-id="b62cc-106">**AzApplicationGatewayBackendAddressPool** Cmdlet 會將後端位址集區新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b62cc-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="b62cc-107">可使用 IP 位址指定後端位址、完全合格的功能變數名稱 (FQDN) 或 IP 配置 Id。</span><span class="sxs-lookup"><span data-stu-id="b62cc-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="b62cc-108">示例</span><span class="sxs-lookup"><span data-stu-id="b62cc-108">EXAMPLES</span></span>

### <span data-ttu-id="b62cc-109">範例1：使用後端伺服器 FQDN 新增後端位址集區</span><span class="sxs-lookup"><span data-stu-id="b62cc-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="b62cc-110">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會使用 Fqdn，新增儲存在 $AppGw 中之應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="b62cc-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="b62cc-111">範例2：使用後端伺服器 IP 位址新增後端位址集區</span><span class="sxs-lookup"><span data-stu-id="b62cc-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="b62cc-112">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會使用 IP 位址，新增儲存在 $AppGw 中之應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="b62cc-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="b62cc-113">參數</span><span class="sxs-lookup"><span data-stu-id="b62cc-113">PARAMETERS</span></span>

### <span data-ttu-id="b62cc-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b62cc-114">-ApplicationGateway</span></span>
<span data-ttu-id="b62cc-115">指定此 Cmdlet 新增後端位址集區的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b62cc-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="b62cc-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="b62cc-116">-BackendFqdns</span></span>
<span data-ttu-id="b62cc-117">指定這個 Cmdlet 作為後端伺服器池加入的後端 Fqdn 清單。</span><span class="sxs-lookup"><span data-stu-id="b62cc-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="b62cc-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="b62cc-118">-BackendIPAddresses</span></span>
<span data-ttu-id="b62cc-119">指定此 Cmdlet 新增為後端伺服器池的後端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="b62cc-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="b62cc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62cc-120">-DefaultProfile</span></span>
<span data-ttu-id="b62cc-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b62cc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b62cc-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b62cc-122">-Name</span></span>
<span data-ttu-id="b62cc-123">指定此 Cmdlet 所新增之後端伺服器池的名稱。</span><span class="sxs-lookup"><span data-stu-id="b62cc-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b62cc-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b62cc-124">-Confirm</span></span>
<span data-ttu-id="b62cc-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b62cc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b62cc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b62cc-126">-WhatIf</span></span>
<span data-ttu-id="b62cc-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b62cc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b62cc-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b62cc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b62cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62cc-129">CommonParameters</span></span>
<span data-ttu-id="b62cc-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b62cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62cc-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b62cc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62cc-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b62cc-132">INPUTS</span></span>

### <span data-ttu-id="b62cc-133">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b62cc-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b62cc-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b62cc-134">OUTPUTS</span></span>

### <span data-ttu-id="b62cc-135">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b62cc-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b62cc-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b62cc-136">NOTES</span></span>

## <span data-ttu-id="b62cc-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b62cc-137">RELATED LINKS</span></span>

[<span data-ttu-id="b62cc-138">AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b62cc-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b62cc-139">AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b62cc-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b62cc-140">新-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b62cc-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b62cc-141">移除-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b62cc-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b62cc-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b62cc-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b62cc-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b62cc-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
