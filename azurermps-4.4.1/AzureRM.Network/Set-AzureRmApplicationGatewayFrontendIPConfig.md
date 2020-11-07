---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1abb59c6f610182e14bdf9483610cdb9bbbb66bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626588"
---
# <span data-ttu-id="90699-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90699-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="90699-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90699-102">SYNOPSIS</span></span>
<span data-ttu-id="90699-103">修改前端 IP 位址設定。</span><span class="sxs-lookup"><span data-stu-id="90699-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90699-104">句法</span><span class="sxs-lookup"><span data-stu-id="90699-104">SYNTAX</span></span>

### <span data-ttu-id="90699-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="90699-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90699-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="90699-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90699-107">說明</span><span class="sxs-lookup"><span data-stu-id="90699-107">DESCRIPTION</span></span>
<span data-ttu-id="90699-108">**AzureRmApplicationGatewayFrontendIPConfig** Cmdlet 會更新前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="90699-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="90699-109">應用程式閘道支援兩種類型的前端 IP 位址：</span><span class="sxs-lookup"><span data-stu-id="90699-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="90699-110">公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="90699-110">Public IP addresses</span></span>
- <span data-ttu-id="90699-111">針對其配置使用內部負載平衡 (ILB 的私人 IP 位址) </span><span class="sxs-lookup"><span data-stu-id="90699-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="90699-112">應用程式閘道最多隻能有一個公用 IP 位址和一個私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="90699-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="90699-113">公用 IP 位址與私人 IP 位址應分別新增為前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="90699-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="90699-114">示例</span><span class="sxs-lookup"><span data-stu-id="90699-114">EXAMPLES</span></span>

### <span data-ttu-id="90699-115">範例1：將公用 IP 設定為應用程式閘道的前端 IP</span><span class="sxs-lookup"><span data-stu-id="90699-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="90699-116">第一個命令會建立公用 IP 位址物件，並將它儲存在 $PublicIp 變數中。</span><span class="sxs-lookup"><span data-stu-id="90699-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="90699-117">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將其儲存于名為 ResourceGroup01 的資源群組，然後將其儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="90699-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="90699-118">第三個命令會使用儲存在 $PublicIp 中的位址，更新名為 $AppGw FrontEndIp01 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="90699-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="90699-119">範例2：將靜態專用 IP 設定為應用程式閘道的前端 IP</span><span class="sxs-lookup"><span data-stu-id="90699-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="90699-120">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="90699-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="90699-121">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="90699-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="90699-122">第三個命令會從屬於名為 ResourceGroup01 的資源群組的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="90699-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="90699-123">第四個命令會使用第二個命令的 $Subnet，以及私人 IP 位址10.0.1.1，來新增名為 FrontendIP02 的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="90699-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="90699-124">範例3：將動態專用 IP 設定為應用程式閘道的前端 IP</span><span class="sxs-lookup"><span data-stu-id="90699-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="90699-125">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="90699-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="90699-126">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="90699-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="90699-127">第三個命令會從屬於名為 ResourceGroup01 的資源群組的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="90699-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="90699-128">第四個命令會使用第二個命令中的 $Subnet，新增名為 FrontendIP02 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="90699-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="90699-129">參數</span><span class="sxs-lookup"><span data-stu-id="90699-129">PARAMETERS</span></span>

### <span data-ttu-id="90699-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90699-130">-ApplicationGateway</span></span>
<span data-ttu-id="90699-131">指定要修改前端 IP 設定的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="90699-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="90699-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="90699-132">-Name</span></span>
<span data-ttu-id="90699-133">指定此 Cmdlet 所修改之前端 IP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="90699-133">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="90699-134">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="90699-134">-PrivateIPAddress</span></span>
<span data-ttu-id="90699-135">指定私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="90699-135">Specifies the private IP address.</span></span>
<span data-ttu-id="90699-136">如果已指定，此 IP 是從子網上靜態配置。</span><span class="sxs-lookup"><span data-stu-id="90699-136">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="90699-137">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="90699-137">-PublicIPAddress</span></span>
<span data-ttu-id="90699-138">指定公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="90699-138">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="90699-139">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="90699-139">-PublicIPAddressId</span></span>
<span data-ttu-id="90699-140">指定公用 IP 位址的 ID。</span><span class="sxs-lookup"><span data-stu-id="90699-140">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="90699-141">-子網</span><span class="sxs-lookup"><span data-stu-id="90699-141">-Subnet</span></span>
<span data-ttu-id="90699-142">指定應用程式閘道使用的子網。</span><span class="sxs-lookup"><span data-stu-id="90699-142">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="90699-143">如果閘道使用的是私人 IP 位址，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="90699-143">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="90699-144">如果已指定 *PrivateIPAddress* 位址，則它應該屬於該子網上。</span><span class="sxs-lookup"><span data-stu-id="90699-144">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="90699-145">如果未指定 *PrivateIPAddress* ，則會將此子網上的其中一個 IP 位址動態挑選為應用程式閘道的前端 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="90699-145">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="90699-146">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="90699-146">-SubnetId</span></span>
<span data-ttu-id="90699-147">指定子網 ID。</span><span class="sxs-lookup"><span data-stu-id="90699-147">Specifies the subnet ID.</span></span>
<span data-ttu-id="90699-148">如果閘道使用的是私人 IP 位址，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="90699-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="90699-149">如果 *PrivateIPAddress* 參數已指定，它應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="90699-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="90699-150">如果未指定 *PrivateIPAddress* ，則會將此子網上的其中一個 IP 位址動態挑選為應用程式閘道的前端 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="90699-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="90699-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90699-151">-DefaultProfile</span></span>
<span data-ttu-id="90699-152">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90699-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90699-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90699-153">CommonParameters</span></span>
<span data-ttu-id="90699-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90699-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90699-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90699-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90699-156">輸入</span><span class="sxs-lookup"><span data-stu-id="90699-156">INPUTS</span></span>

### <span data-ttu-id="90699-157">System.object</span><span class="sxs-lookup"><span data-stu-id="90699-157">System.String</span></span>

## <span data-ttu-id="90699-158">輸出</span><span class="sxs-lookup"><span data-stu-id="90699-158">OUTPUTS</span></span>

### <span data-ttu-id="90699-159">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="90699-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="90699-160">筆記</span><span class="sxs-lookup"><span data-stu-id="90699-160">NOTES</span></span>

## <span data-ttu-id="90699-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="90699-161">RELATED LINKS</span></span>

[<span data-ttu-id="90699-162">附加 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90699-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="90699-163">附加 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90699-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="90699-164">AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90699-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="90699-165">新-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90699-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="90699-166">移除-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90699-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


