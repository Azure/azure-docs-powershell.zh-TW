---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 17ef06c6f91f650da95ddcbfb87b09a60c1948d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903118"
---
# <span data-ttu-id="f5bc9-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc9-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="f5bc9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="f5bc9-103">修改前端 IP 位址組式。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="f5bc9-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5bc9-104">SYNTAX</span></span>

### <span data-ttu-id="f5bc9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5bc9-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5bc9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f5bc9-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5bc9-107">描述</span><span class="sxs-lookup"><span data-stu-id="f5bc9-107">DESCRIPTION</span></span>
<span data-ttu-id="f5bc9-108">**Set-AzApplicationGatewayFrontendIPConfig** Cmdlet 會更新前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="f5bc9-109">應用程式閘道支援兩種類型的前端 IP 位址：</span><span class="sxs-lookup"><span data-stu-id="f5bc9-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="f5bc9-110">公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="f5bc9-110">Public IP addresses</span></span>
- <span data-ttu-id="f5bc9-111">此組配置的私人 IP 位址使用內部負載平衡 (ILB) 應用程式閘道最多隻能有一個公用 IP 位址和一個私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="f5bc9-112">公用 IP 位址和私人 IP 位址應個別新增為前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="f5bc9-113">例子</span><span class="sxs-lookup"><span data-stu-id="f5bc9-113">EXAMPLES</span></span>

### <span data-ttu-id="f5bc9-114">範例 1：將公用 IP 設定為應用程式閘道的前端 IP</span><span class="sxs-lookup"><span data-stu-id="f5bc9-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="f5bc9-115">第一個命令會建立公用 IP 位址物件，並儲存在$PublicIp變數中。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="f5bc9-116">第二個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f5bc9-117">第三個命令會使用儲存在 $AppGw 中的位址更新名為 FrontEndIp01 的前端 IP 組$PublicIp。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="f5bc9-118">範例 2：將靜態私人 IP 設定為應用程式閘道的前端 IP</span><span class="sxs-lookup"><span data-stu-id="f5bc9-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="f5bc9-119">第一個命令會獲得一個名為 VNet01 的虛擬網路，該網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="f5bc9-120">第二個命令會使用第一個命令$VNet名為子網01 的子網組$Subnet變數。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f5bc9-121">第三個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f5bc9-122">第四個命令會使用第二個命令的 $Subnet 和私人 IP 位址 10.0.1.1 新增名為 FrontendIP02 的前端 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="f5bc9-123">範例 3：將動態私人 IP 設定為應用程式閘道的前端 IP</span><span class="sxs-lookup"><span data-stu-id="f5bc9-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="f5bc9-124">第一個命令會獲得一個名為 VNet01 的虛擬網路，該網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="f5bc9-125">第二個命令會使用第一個命令$VNet名為子網01 的子網組$Subnet變數。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f5bc9-126">第三個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f5bc9-127">第四個命令會使用第二個命令$Subnet稱為 FrontendIP02 的前端 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="f5bc9-128">參數</span><span class="sxs-lookup"><span data-stu-id="f5bc9-128">PARAMETERS</span></span>

### <span data-ttu-id="f5bc9-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5bc9-129">-ApplicationGateway</span></span>
<span data-ttu-id="f5bc9-130">指定要修改前端 IP 群組原則的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="f5bc9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5bc9-131">-DefaultProfile</span></span>
<span data-ttu-id="f5bc9-132">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5bc9-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5bc9-133">-Name</span></span>
<span data-ttu-id="f5bc9-134">指定此 Cmdlet 修改的前端 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f5bc9-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="f5bc9-135">-PrivateIPAddress</span></span>
<span data-ttu-id="f5bc9-136">指定私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-136">Specifies the private IP address.</span></span>
<span data-ttu-id="f5bc9-137">如果指定，此 IP 會從子網靜態配置。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="f5bc9-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5bc9-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="f5bc9-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5bc9-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="f5bc9-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f5bc9-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="f5bc9-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f5bc9-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="f5bc9-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="f5bc9-142">-PublicIPAddress</span></span>
<span data-ttu-id="f5bc9-143">指定公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="f5bc9-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="f5bc9-144">-PublicIPAddressId</span></span>
<span data-ttu-id="f5bc9-145">指定公用 IP 位址的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="f5bc9-146">-子網</span><span class="sxs-lookup"><span data-stu-id="f5bc9-146">-Subnet</span></span>
<span data-ttu-id="f5bc9-147">指定應用程式閘道使用的子網。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="f5bc9-148">如果閘道使用私人 IP 位址，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="f5bc9-149">如果 *已指定 PrivateIPAddress* 位址，該位址應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="f5bc9-150">如果 *未指定 PrivateIPAddress，* 此子網的其中一個 IP 位址會動態取用為應用程式閘道的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="f5bc9-151">-子網Id</span><span class="sxs-lookup"><span data-stu-id="f5bc9-151">-SubnetId</span></span>
<span data-ttu-id="f5bc9-152">指定子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="f5bc9-153">如果閘道使用私人 IP 位址，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="f5bc9-154">如果 *已指定 PrivateIPAddress* 參數，應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="f5bc9-155">如果 *未指定 PrivateIPAddress，* 此子網的其中一個 IP 位址會動態取用為應用程式閘道的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="f5bc9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5bc9-156">CommonParameters</span></span>
<span data-ttu-id="f5bc9-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5bc9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5bc9-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5bc9-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5bc9-159">輸入</span><span class="sxs-lookup"><span data-stu-id="f5bc9-159">INPUTS</span></span>

### <span data-ttu-id="f5bc9-160">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5bc9-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f5bc9-161">輸出</span><span class="sxs-lookup"><span data-stu-id="f5bc9-161">OUTPUTS</span></span>

### <span data-ttu-id="f5bc9-162">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5bc9-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f5bc9-163">筆記</span><span class="sxs-lookup"><span data-stu-id="f5bc9-163">NOTES</span></span>

## <span data-ttu-id="f5bc9-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5bc9-164">RELATED LINKS</span></span>

[<span data-ttu-id="f5bc9-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc9-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f5bc9-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc9-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f5bc9-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc9-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f5bc9-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc9-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f5bc9-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc9-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


