---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d19f5489adff642ad9b02a7f3bb364338bd1e566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456024"
---
# <span data-ttu-id="c128b-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c128b-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="c128b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c128b-102">SYNOPSIS</span></span>
<span data-ttu-id="c128b-103">將前端 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c128b-103">Adds a front-end IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c128b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c128b-104">SYNTAX</span></span>

### <span data-ttu-id="c128b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c128b-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c128b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c128b-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c128b-107">說明</span><span class="sxs-lookup"><span data-stu-id="c128b-107">DESCRIPTION</span></span>
<span data-ttu-id="c128b-108">**AzureRmApplicationGatewayFrontendIPConfig** Cmdlet 會將前端 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c128b-108">The **Add-AzureRmApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="c128b-109">應用程式閘道支援兩種類型的前端 IP 配置：</span><span class="sxs-lookup"><span data-stu-id="c128b-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="c128b-110">公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="c128b-110">Public IP addresses</span></span>
- <span data-ttu-id="c128b-111">使用內部負載平衡 (ILB 的私人 IP 位址) 應用程式閘道最多隻能有一個公用 IP 和一個專用 IP。</span><span class="sxs-lookup"><span data-stu-id="c128b-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="c128b-112">將公用 IP 位址和私人 IP 位址新增為個別的前端 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="c128b-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="c128b-113">示例</span><span class="sxs-lookup"><span data-stu-id="c128b-113">EXAMPLES</span></span>

### <span data-ttu-id="c128b-114">範例1：新增公用 IP 作為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="c128b-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="c128b-115">第一個命令會建立公用 IP 位址物件，並將它儲存在 $PublicIp 變數中。</span><span class="sxs-lookup"><span data-stu-id="c128b-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="c128b-116">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將其儲存于名為 ResourceGroup01 的資源群組，然後將其儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="c128b-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c128b-117">第三個命令會使用儲存在 $PublicIp 中的位址，為 $AppGw 中的閘道新增名為 FrontEndIp01 的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="c128b-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="c128b-118">範例2：新增靜態專用 IP 作為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="c128b-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="c128b-119">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="c128b-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="c128b-120">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="c128b-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="c128b-121">第三個命令會從屬於名為 ResourceGroup01 的資源群組的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="c128b-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c128b-122">第四個命令會使用第二個命令的 $Subnet，以及私人 IP 位址10.0.1.1，來新增名為 FrontendIP02 的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="c128b-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="c128b-123">範例3：新增動態專用 IP 作為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="c128b-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="c128b-124">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="c128b-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="c128b-125">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="c128b-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="c128b-126">第三個命令會從屬於名為 ResourceGroup01 的資源群組的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="c128b-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c128b-127">第四個命令會使用第二個命令中的 $Subnet，新增名為 FrontendIP02 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="c128b-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="c128b-128">參數</span><span class="sxs-lookup"><span data-stu-id="c128b-128">PARAMETERS</span></span>

### <span data-ttu-id="c128b-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c128b-129">-ApplicationGateway</span></span>
<span data-ttu-id="c128b-130">指定此 Cmdlet 新增前端 IP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c128b-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="c128b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c128b-131">-DefaultProfile</span></span>
<span data-ttu-id="c128b-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c128b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c128b-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="c128b-133">-Name</span></span>
<span data-ttu-id="c128b-134">指定要新增的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="c128b-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="c128b-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="c128b-135">-PrivateIPAddress</span></span>
<span data-ttu-id="c128b-136">指定要新增為應用程式閘道的前端 IP 的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c128b-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="c128b-137">如果已指定，此 IP 是從子網上靜態配置。</span><span class="sxs-lookup"><span data-stu-id="c128b-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="c128b-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="c128b-138">-PublicIPAddress</span></span>
<span data-ttu-id="c128b-139">指定此 Cmdlet 將其新增為應用程式閘道的前端 IP 位址的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c128b-139">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="c128b-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="c128b-140">-PublicIPAddressId</span></span>
<span data-ttu-id="c128b-141">指定此 Cmdlet 將其新增為應用程式閘道的前端 IP 位址的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="c128b-141">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="c128b-142">-子網</span><span class="sxs-lookup"><span data-stu-id="c128b-142">-Subnet</span></span>
<span data-ttu-id="c128b-143">指定這個 Cmdlet 新增為前端 IP 配置的子網。</span><span class="sxs-lookup"><span data-stu-id="c128b-143">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="c128b-144">如果您指定此參數，則表示應用程式閘道支援專用 IP 的專用配置。</span><span class="sxs-lookup"><span data-stu-id="c128b-144">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="c128b-145">如果 *PrivateIPAddress* 參數已指定，它應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="c128b-145">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="c128b-146">如果未指定 *PrivateIPAddress* ，則會將此子網上的其中一個 IP 位址動態挑選為應用程式閘道的前端 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="c128b-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c128b-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c128b-147">-SubnetId</span></span>
<span data-ttu-id="c128b-148">指定這個 Cmdlet 作為前端 IP 設定而新增的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="c128b-148">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="c128b-149">傳遞子網隱含專用 IP。</span><span class="sxs-lookup"><span data-stu-id="c128b-149">Passing subnet implies private IP.</span></span>
<span data-ttu-id="c128b-150">如果 *PrivateIPAddresss* 參數已指定，它應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="c128b-150">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="c128b-151">否則，此子網上的其中一個 IP 會動態挑選為應用程式閘道的前端 IP。</span><span class="sxs-lookup"><span data-stu-id="c128b-151">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="c128b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c128b-152">CommonParameters</span></span>
<span data-ttu-id="c128b-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c128b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c128b-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c128b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c128b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="c128b-155">INPUTS</span></span>

### <span data-ttu-id="c128b-156">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c128b-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="c128b-157">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c128b-157">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="c128b-158">輸出</span><span class="sxs-lookup"><span data-stu-id="c128b-158">OUTPUTS</span></span>

### <span data-ttu-id="c128b-159">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c128b-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c128b-160">筆記</span><span class="sxs-lookup"><span data-stu-id="c128b-160">NOTES</span></span>

## <span data-ttu-id="c128b-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="c128b-161">RELATED LINKS</span></span>

[<span data-ttu-id="c128b-162">AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c128b-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c128b-163">新-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c128b-163">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c128b-164">移除-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c128b-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c128b-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c128b-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


