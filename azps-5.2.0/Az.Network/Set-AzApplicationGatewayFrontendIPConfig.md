---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274796"
---
# <span data-ttu-id="4da52-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4da52-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="4da52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4da52-102">SYNOPSIS</span></span>
<span data-ttu-id="4da52-103">修改前端 IP 位址設定。</span><span class="sxs-lookup"><span data-stu-id="4da52-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="4da52-104">句法</span><span class="sxs-lookup"><span data-stu-id="4da52-104">SYNTAX</span></span>

### <span data-ttu-id="4da52-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4da52-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4da52-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4da52-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4da52-107">說明</span><span class="sxs-lookup"><span data-stu-id="4da52-107">DESCRIPTION</span></span>
<span data-ttu-id="4da52-108">**AzApplicationGatewayFrontendIPConfig** Cmdlet 會更新前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="4da52-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="4da52-109">應用程式閘道支援兩種類型的前端 IP 位址：</span><span class="sxs-lookup"><span data-stu-id="4da52-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="4da52-110">公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="4da52-110">Public IP addresses</span></span>
- <span data-ttu-id="4da52-111">配置使用內部負載平衡 (ILB 的私人 IP 位址) 應用程式閘道最多隻能有一個公用 IP 位址和一個私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4da52-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="4da52-112">公用 IP 位址與私人 IP 位址應分別新增為前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4da52-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="4da52-113">示例</span><span class="sxs-lookup"><span data-stu-id="4da52-113">EXAMPLES</span></span>

### <span data-ttu-id="4da52-114">範例1：將公用 IP 設定為應用程式閘道的前端 IP</span><span class="sxs-lookup"><span data-stu-id="4da52-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="4da52-115">第一個命令會建立公用 IP 位址物件，並將它儲存在 $PublicIp 變數中。</span><span class="sxs-lookup"><span data-stu-id="4da52-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="4da52-116">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將其儲存于名為 ResourceGroup01 的資源群組，然後將其儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4da52-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4da52-117">第三個命令會使用儲存在 $PublicIp 中的位址，更新名為 $AppGw FrontEndIp01 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="4da52-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="4da52-118">範例2：將靜態專用 IP 設定為應用程式閘道的前端 IP</span><span class="sxs-lookup"><span data-stu-id="4da52-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="4da52-119">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="4da52-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="4da52-120">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="4da52-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="4da52-121">第三個命令會從屬於名為 ResourceGroup01 的資源群組的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4da52-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4da52-122">第四個命令會使用第二個命令的 $Subnet，以及私人 IP 位址10.0.1.1，來新增名為 FrontendIP02 的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="4da52-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="4da52-123">範例3：將動態專用 IP 設定為應用程式閘道的前端 IP</span><span class="sxs-lookup"><span data-stu-id="4da52-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="4da52-124">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="4da52-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="4da52-125">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="4da52-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="4da52-126">第三個命令會從屬於名為 ResourceGroup01 的資源群組的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4da52-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4da52-127">第四個命令會使用第二個命令中的 $Subnet，新增名為 FrontendIP02 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="4da52-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="4da52-128">參數</span><span class="sxs-lookup"><span data-stu-id="4da52-128">PARAMETERS</span></span>

### <span data-ttu-id="4da52-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4da52-129">-ApplicationGateway</span></span>
<span data-ttu-id="4da52-130">指定要修改前端 IP 設定的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="4da52-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4da52-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da52-131">-DefaultProfile</span></span>
<span data-ttu-id="4da52-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4da52-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da52-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="4da52-133">-Name</span></span>
<span data-ttu-id="4da52-134">指定此 Cmdlet 所修改之前端 IP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="4da52-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4da52-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="4da52-135">-PrivateIPAddress</span></span>
<span data-ttu-id="4da52-136">指定私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4da52-136">Specifies the private IP address.</span></span>
<span data-ttu-id="4da52-137">如果已指定，此 IP 是從子網上靜態配置。</span><span class="sxs-lookup"><span data-stu-id="4da52-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="4da52-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4da52-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="4da52-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4da52-139">PrivateLinkConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da52-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4da52-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="4da52-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4da52-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="4da52-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="4da52-142">-PublicIPAddress</span></span>
<span data-ttu-id="4da52-143">指定公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4da52-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="4da52-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="4da52-144">-PublicIPAddressId</span></span>
<span data-ttu-id="4da52-145">指定公用 IP 位址的 ID。</span><span class="sxs-lookup"><span data-stu-id="4da52-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="4da52-146">-子網</span><span class="sxs-lookup"><span data-stu-id="4da52-146">-Subnet</span></span>
<span data-ttu-id="4da52-147">指定應用程式閘道使用的子網。</span><span class="sxs-lookup"><span data-stu-id="4da52-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="4da52-148">如果閘道使用的是私人 IP 位址，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="4da52-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="4da52-149">如果已指定 *PrivateIPAddress* 位址，則它應該屬於該子網上。</span><span class="sxs-lookup"><span data-stu-id="4da52-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="4da52-150">如果未指定 *PrivateIPAddress* ，則會將此子網上的其中一個 IP 位址動態挑選為應用程式閘道的前端 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="4da52-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="4da52-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4da52-151">-SubnetId</span></span>
<span data-ttu-id="4da52-152">指定子網 ID。</span><span class="sxs-lookup"><span data-stu-id="4da52-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="4da52-153">如果閘道使用的是私人 IP 位址，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="4da52-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="4da52-154">如果 *PrivateIPAddress* 參數已指定，它應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="4da52-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="4da52-155">如果未指定 *PrivateIPAddress* ，則會將此子網上的其中一個 IP 位址動態挑選為應用程式閘道的前端 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="4da52-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="4da52-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da52-156">CommonParameters</span></span>
<span data-ttu-id="4da52-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4da52-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da52-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4da52-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da52-159">輸入</span><span class="sxs-lookup"><span data-stu-id="4da52-159">INPUTS</span></span>

### <span data-ttu-id="4da52-160">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4da52-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4da52-161">輸出</span><span class="sxs-lookup"><span data-stu-id="4da52-161">OUTPUTS</span></span>

### <span data-ttu-id="4da52-162">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4da52-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4da52-163">筆記</span><span class="sxs-lookup"><span data-stu-id="4da52-163">NOTES</span></span>

## <span data-ttu-id="4da52-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="4da52-164">RELATED LINKS</span></span>

[<span data-ttu-id="4da52-165">附加 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4da52-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4da52-166">附加 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4da52-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4da52-167">AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4da52-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4da52-168">新-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4da52-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4da52-169">移除-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4da52-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


