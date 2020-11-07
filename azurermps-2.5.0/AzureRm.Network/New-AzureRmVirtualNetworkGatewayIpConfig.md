---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 1a043b14ef957eed6ac4983c4a30edf6fc72521f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802309"
---
# <span data-ttu-id="e6e68-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6e68-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="e6e68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6e68-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e68-103">建立虛擬網路閘道的 IP 配置</span><span class="sxs-lookup"><span data-stu-id="e6e68-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6e68-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6e68-104">SYNTAX</span></span>

### <span data-ttu-id="e6e68-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6e68-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6e68-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e6e68-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6e68-107">說明</span><span class="sxs-lookup"><span data-stu-id="e6e68-107">DESCRIPTION</span></span>
<span data-ttu-id="e6e68-108">**新的-AzureRmVirtualNetworkGatewayIpConfig** Cmdlet 會建立一個指派給虛擬網路閘道的配置， (先前根據子網識別碼建立) 公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e6e68-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="e6e68-109">示例</span><span class="sxs-lookup"><span data-stu-id="e6e68-109">EXAMPLES</span></span>

### <span data-ttu-id="e6e68-110">1：建立虛擬網路閘道的 IP 配置</span><span class="sxs-lookup"><span data-stu-id="e6e68-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="e6e68-111">使用公用 IP 位址來配置虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="e6e68-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="e6e68-112">變數 $myGWsubnet 是使用您想要建立虛擬網路閘道之虛擬網路中 "GatewaySubnet" 的 **AzureRmVirtualNetworkSubnetConfig** Cmdlet 取得的。</span><span class="sxs-lookup"><span data-stu-id="e6e68-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="e6e68-113">使用 **AzureRmPublicIpAddress** Cmdlet 取得變數 $myGWpip。</span><span class="sxs-lookup"><span data-stu-id="e6e68-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="e6e68-114">參數</span><span class="sxs-lookup"><span data-stu-id="e6e68-114">PARAMETERS</span></span>

### <span data-ttu-id="e6e68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e68-115">-DefaultProfile</span></span>
<span data-ttu-id="e6e68-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6e68-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6e68-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6e68-117">-Name</span></span>
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

### <span data-ttu-id="e6e68-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="e6e68-118">-PrivateIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e68-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e6e68-119">-PublicIpAddress</span></span>
```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e68-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="e6e68-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="e6e68-121">-子網</span><span class="sxs-lookup"><span data-stu-id="e6e68-121">-Subnet</span></span>
```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e68-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e6e68-122">-SubnetId</span></span>
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

### <span data-ttu-id="e6e68-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e68-123">CommonParameters</span></span>
<span data-ttu-id="e6e68-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6e68-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e68-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6e68-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e68-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e6e68-126">INPUTS</span></span>

## <span data-ttu-id="e6e68-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e6e68-127">OUTPUTS</span></span>

### <span data-ttu-id="e6e68-128">PSVirtualNetworkGatewayIpConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e6e68-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="e6e68-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e6e68-129">NOTES</span></span>

## <span data-ttu-id="e6e68-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6e68-130">RELATED LINKS</span></span>

