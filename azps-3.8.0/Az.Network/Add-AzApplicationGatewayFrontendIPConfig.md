---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 30238f9466e87ab732b1b2b6d30bba26bcd4c83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965771"
---
# <span data-ttu-id="f065a-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f065a-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="f065a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f065a-102">SYNOPSIS</span></span>
<span data-ttu-id="f065a-103">將前端 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="f065a-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="f065a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f065a-104">SYNTAX</span></span>

### <span data-ttu-id="f065a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f065a-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f065a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f065a-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f065a-107">說明</span><span class="sxs-lookup"><span data-stu-id="f065a-107">DESCRIPTION</span></span>
<span data-ttu-id="f065a-108">**AzApplicationGatewayFrontendIPConfig** Cmdlet 會將前端 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="f065a-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="f065a-109">應用程式閘道支援兩種類型的前端 IP 配置：</span><span class="sxs-lookup"><span data-stu-id="f065a-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="f065a-110">公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="f065a-110">Public IP addresses</span></span>
- <span data-ttu-id="f065a-111">使用內部負載平衡 (ILB 的私人 IP 位址) 應用程式閘道最多隻能有一個公用 IP 和一個專用 IP。</span><span class="sxs-lookup"><span data-stu-id="f065a-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="f065a-112">將公用 IP 位址和私人 IP 位址新增為個別的前端 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="f065a-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="f065a-113">示例</span><span class="sxs-lookup"><span data-stu-id="f065a-113">EXAMPLES</span></span>

### <span data-ttu-id="f065a-114">範例1：新增公用 IP 作為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="f065a-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="f065a-115">第一個命令會建立公用 IP 位址物件，並將它儲存在 $PublicIp 變數中。</span><span class="sxs-lookup"><span data-stu-id="f065a-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="f065a-116">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將其儲存于名為 ResourceGroup01 的資源群組，然後將其儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f065a-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f065a-117">第三個命令會使用儲存在 $PublicIp 中的位址，為 $AppGw 中的閘道新增名為 FrontEndIp01 的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="f065a-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="f065a-118">範例2：新增靜態專用 IP 作為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="f065a-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="f065a-119">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="f065a-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="f065a-120">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="f065a-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f065a-121">第三個命令會從屬於名為 ResourceGroup01 的資源群組的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f065a-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f065a-122">第四個命令會使用第二個命令的 $Subnet，以及私人 IP 位址10.0.1.1，來新增名為 FrontendIP02 的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="f065a-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="f065a-123">範例3：新增動態專用 IP 作為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="f065a-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="f065a-124">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="f065a-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="f065a-125">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="f065a-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f065a-126">第三個命令會從屬於名為 ResourceGroup01 的資源群組的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f065a-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f065a-127">第四個命令會使用第二個命令中的 $Subnet，新增名為 FrontendIP02 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="f065a-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="f065a-128">參數</span><span class="sxs-lookup"><span data-stu-id="f065a-128">PARAMETERS</span></span>

### <span data-ttu-id="f065a-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f065a-129">-ApplicationGateway</span></span>
<span data-ttu-id="f065a-130">指定此 Cmdlet 新增前端 IP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="f065a-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f065a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f065a-131">-DefaultProfile</span></span>
<span data-ttu-id="f065a-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f065a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f065a-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="f065a-133">-Name</span></span>
<span data-ttu-id="f065a-134">指定要新增的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="f065a-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="f065a-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="f065a-135">-PrivateIPAddress</span></span>
<span data-ttu-id="f065a-136">指定要新增為應用程式閘道的前端 IP 的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f065a-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="f065a-137">如果已指定，此 IP 是從子網上靜態配置。</span><span class="sxs-lookup"><span data-stu-id="f065a-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="f065a-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="f065a-138">-PublicIPAddress</span></span>
<span data-ttu-id="f065a-139">指定此 Cmdlet 將其新增為應用程式閘道的前端 IP 位址的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f065a-139">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="f065a-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="f065a-140">-PublicIPAddressId</span></span>
<span data-ttu-id="f065a-141">指定此 Cmdlet 將其新增為應用程式閘道的前端 IP 位址的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="f065a-141">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="f065a-142">-子網</span><span class="sxs-lookup"><span data-stu-id="f065a-142">-Subnet</span></span>
<span data-ttu-id="f065a-143">指定這個 Cmdlet 新增為前端 IP 配置的子網。</span><span class="sxs-lookup"><span data-stu-id="f065a-143">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="f065a-144">如果您指定此參數，則表示應用程式閘道支援專用 IP 的專用配置。</span><span class="sxs-lookup"><span data-stu-id="f065a-144">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="f065a-145">如果 *PrivateIPAddress* 參數已指定，它應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="f065a-145">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="f065a-146">如果未指定 *PrivateIPAddress* ，則會將此子網上的其中一個 IP 位址動態挑選為應用程式閘道的前端 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="f065a-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="f065a-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f065a-147">-SubnetId</span></span>
<span data-ttu-id="f065a-148">指定這個 Cmdlet 作為前端 IP 設定而新增的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="f065a-148">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="f065a-149">傳遞子網隱含專用 IP。</span><span class="sxs-lookup"><span data-stu-id="f065a-149">Passing subnet implies private IP.</span></span>
<span data-ttu-id="f065a-150">如果 *PrivateIPAddress* 參數已指定，它應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="f065a-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="f065a-151">否則，此子網上的其中一個 IP 會動態挑選為應用程式閘道的前端 IP。</span><span class="sxs-lookup"><span data-stu-id="f065a-151">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="f065a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f065a-152">CommonParameters</span></span>
<span data-ttu-id="f065a-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f065a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f065a-154">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f065a-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f065a-155">輸入</span><span class="sxs-lookup"><span data-stu-id="f065a-155">INPUTS</span></span>

### <span data-ttu-id="f065a-156">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f065a-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f065a-157">輸出</span><span class="sxs-lookup"><span data-stu-id="f065a-157">OUTPUTS</span></span>

### <span data-ttu-id="f065a-158">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f065a-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f065a-159">筆記</span><span class="sxs-lookup"><span data-stu-id="f065a-159">NOTES</span></span>

## <span data-ttu-id="f065a-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="f065a-160">RELATED LINKS</span></span>

[<span data-ttu-id="f065a-161">AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f065a-161">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f065a-162">新-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f065a-162">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f065a-163">移除-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f065a-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f065a-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f065a-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


