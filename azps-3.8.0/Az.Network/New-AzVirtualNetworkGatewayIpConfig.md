---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959172"
---
# <span data-ttu-id="9d69a-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9d69a-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="9d69a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d69a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d69a-103">建立虛擬網路閘道的 IP 配置</span><span class="sxs-lookup"><span data-stu-id="9d69a-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="9d69a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d69a-104">SYNTAX</span></span>

### <span data-ttu-id="9d69a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d69a-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d69a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9d69a-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d69a-107">說明</span><span class="sxs-lookup"><span data-stu-id="9d69a-107">DESCRIPTION</span></span>
<span data-ttu-id="9d69a-108">**新的-AzVirtualNetworkGatewayIpConfig** Cmdlet 會建立一個指派給虛擬網路閘道的配置， (先前根據子網識別碼建立) 公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9d69a-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="9d69a-109">示例</span><span class="sxs-lookup"><span data-stu-id="9d69a-109">EXAMPLES</span></span>

### <span data-ttu-id="9d69a-110">1：建立虛擬網路閘道的 IP 配置</span><span class="sxs-lookup"><span data-stu-id="9d69a-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="9d69a-111">使用公用 IP 位址來配置虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="9d69a-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="9d69a-112">變數 $myGWsubnet 是使用您想要建立虛擬網路閘道之虛擬網路中 "GatewaySubnet" 的 **AzVirtualNetworkSubnetConfig** Cmdlet 取得的。</span><span class="sxs-lookup"><span data-stu-id="9d69a-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="9d69a-113">使用 **AzPublicIpAddress** Cmdlet 取得變數 $myGWpip。</span><span class="sxs-lookup"><span data-stu-id="9d69a-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="9d69a-114">參數</span><span class="sxs-lookup"><span data-stu-id="9d69a-114">PARAMETERS</span></span>

### <span data-ttu-id="9d69a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d69a-115">-DefaultProfile</span></span>
<span data-ttu-id="9d69a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d69a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d69a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d69a-117">-Name</span></span>
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

### <span data-ttu-id="9d69a-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9d69a-118">-PrivateIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d69a-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9d69a-119">-PublicIpAddress</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d69a-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9d69a-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="9d69a-121">-子網</span><span class="sxs-lookup"><span data-stu-id="9d69a-121">-Subnet</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d69a-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9d69a-122">-SubnetId</span></span>
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

### <span data-ttu-id="9d69a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d69a-123">CommonParameters</span></span>
<span data-ttu-id="9d69a-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d69a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d69a-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d69a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d69a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9d69a-126">INPUTS</span></span>

### <span data-ttu-id="9d69a-127">所有</span><span class="sxs-lookup"><span data-stu-id="9d69a-127">None</span></span>

## <span data-ttu-id="9d69a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9d69a-128">OUTPUTS</span></span>

### <span data-ttu-id="9d69a-129">PSVirtualNetworkGatewayIpConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9d69a-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="9d69a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9d69a-130">NOTES</span></span>

## <span data-ttu-id="9d69a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d69a-131">RELATED LINKS</span></span>

[<span data-ttu-id="9d69a-132">附加 AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9d69a-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="9d69a-133">移除-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9d69a-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
