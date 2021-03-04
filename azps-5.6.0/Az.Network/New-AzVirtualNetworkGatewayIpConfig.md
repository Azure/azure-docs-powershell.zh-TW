---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: cfbfd8df28cf4f0d9c11e654694172b86a549141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904957"
---
# <span data-ttu-id="3b25c-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b25c-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="3b25c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b25c-102">SYNOPSIS</span></span>
<span data-ttu-id="3b25c-103">建立虛擬網路閘道的 IP 組</span><span class="sxs-lookup"><span data-stu-id="3b25c-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="3b25c-104">語法</span><span class="sxs-lookup"><span data-stu-id="3b25c-104">SYNTAX</span></span>

### <span data-ttu-id="3b25c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b25c-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b25c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3b25c-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b25c-107">描述</span><span class="sxs-lookup"><span data-stu-id="3b25c-107">DESCRIPTION</span></span>
<span data-ttu-id="3b25c-108">**New-AzVirtualNetworkGatewayIpConfig** Cmdlet 會建立指派給虛擬網路閘道的組 (先前根據子網識別碼建立) 公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3b25c-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="3b25c-109">例子</span><span class="sxs-lookup"><span data-stu-id="3b25c-109">EXAMPLES</span></span>

### <span data-ttu-id="3b25c-110">1：建立虛擬網路閘道的 IP 組</span><span class="sxs-lookup"><span data-stu-id="3b25c-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="3b25c-111">設定具有公用 IP 位址的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="3b25c-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="3b25c-112">變數 $myGWsubnet是使用您建立虛擬網路閘道之 「GatewaySubnet」上的 **Get-AzVirtualNetworkSubnetConfig** Cmdlet 取得。</span><span class="sxs-lookup"><span data-stu-id="3b25c-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="3b25c-113">此變數$myGWpip **New-AzPublicIpAddress** Cmdlet 取得。</span><span class="sxs-lookup"><span data-stu-id="3b25c-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="3b25c-114">參數</span><span class="sxs-lookup"><span data-stu-id="3b25c-114">PARAMETERS</span></span>

### <span data-ttu-id="3b25c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b25c-115">-DefaultProfile</span></span>
<span data-ttu-id="3b25c-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b25c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b25c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b25c-117">-Name</span></span>
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

### <span data-ttu-id="3b25c-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3b25c-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="3b25c-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3b25c-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="3b25c-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3b25c-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="3b25c-121">-子網</span><span class="sxs-lookup"><span data-stu-id="3b25c-121">-Subnet</span></span>
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

### <span data-ttu-id="3b25c-122">-子網Id</span><span class="sxs-lookup"><span data-stu-id="3b25c-122">-SubnetId</span></span>
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

### <span data-ttu-id="3b25c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b25c-123">CommonParameters</span></span>
<span data-ttu-id="3b25c-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b25c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b25c-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3b25c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b25c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3b25c-126">INPUTS</span></span>

### <span data-ttu-id="3b25c-127">沒有</span><span class="sxs-lookup"><span data-stu-id="3b25c-127">None</span></span>

## <span data-ttu-id="3b25c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3b25c-128">OUTPUTS</span></span>

### <span data-ttu-id="3b25c-129">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b25c-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="3b25c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3b25c-130">NOTES</span></span>

## <span data-ttu-id="3b25c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b25c-131">RELATED LINKS</span></span>

[<span data-ttu-id="3b25c-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b25c-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="3b25c-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b25c-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
