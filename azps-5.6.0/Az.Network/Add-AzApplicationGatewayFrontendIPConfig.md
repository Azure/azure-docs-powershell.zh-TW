---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 32e8671267efddd94252e592de45cb014b5dd0de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905917"
---
# <span data-ttu-id="dae18-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="dae18-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="dae18-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dae18-102">SYNOPSIS</span></span>
<span data-ttu-id="dae18-103">新增前端 IP 組配置至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="dae18-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="dae18-104">語法</span><span class="sxs-lookup"><span data-stu-id="dae18-104">SYNTAX</span></span>

### <span data-ttu-id="dae18-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dae18-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dae18-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dae18-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dae18-107">描述</span><span class="sxs-lookup"><span data-stu-id="dae18-107">DESCRIPTION</span></span>
<span data-ttu-id="dae18-108">**Add-AzApplicationGatewayFrontendIPConfig** Cmdlet 會新增前端 IP 組配置至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="dae18-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="dae18-109">應用程式閘道支援兩種類型的前端 IP 組式：</span><span class="sxs-lookup"><span data-stu-id="dae18-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="dae18-110">公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="dae18-110">Public IP addresses</span></span>
- <span data-ttu-id="dae18-111">使用內部負載平衡的 IP 位址 (ILB) 應用程式閘道最多隻能有一個公用 IP 和一個私人 IP。</span><span class="sxs-lookup"><span data-stu-id="dae18-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="dae18-112">將公用 IP 位址和私人 IP 位址新增為個別的前端 IP。</span><span class="sxs-lookup"><span data-stu-id="dae18-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="dae18-113">例子</span><span class="sxs-lookup"><span data-stu-id="dae18-113">EXAMPLES</span></span>

### <span data-ttu-id="dae18-114">範例 1：新增公用 IP 做為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="dae18-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="dae18-115">第一個命令會建立公用 IP 位址物件，並儲存在$PublicIp變數中。</span><span class="sxs-lookup"><span data-stu-id="dae18-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="dae18-116">第二個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="dae18-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dae18-117">第三個命令會使用儲存在 $AppGw 中的位址，為 $AppGw 中的閘道新增名為 FrontEndIp01 的前端 IP $PublicIp。</span><span class="sxs-lookup"><span data-stu-id="dae18-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="dae18-118">範例 2：將靜態私人 IP 新增為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="dae18-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="dae18-119">第一個命令會獲得一個名為 VNet01 的虛擬網路，該網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="dae18-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="dae18-120">第二個命令會使用第一個命令$VNet名為子網01 的子網組$Subnet變數。</span><span class="sxs-lookup"><span data-stu-id="dae18-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="dae18-121">第三個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="dae18-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dae18-122">第四個命令會使用第二個命令的 $Subnet 和私人 IP 位址 10.0.1.1 新增名為 FrontendIP02 的前端 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="dae18-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="dae18-123">範例 3：新增動態私人 IP 做為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="dae18-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="dae18-124">第一個命令會獲得一個名為 VNet01 的虛擬網路，該網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="dae18-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="dae18-125">第二個命令會使用第一個命令$VNet名為子網01 的子網組$Subnet變數。</span><span class="sxs-lookup"><span data-stu-id="dae18-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="dae18-126">第三個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="dae18-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dae18-127">第四個命令會使用第二個命令$Subnet稱為 FrontendIP02 的前端 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="dae18-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="dae18-128">參數</span><span class="sxs-lookup"><span data-stu-id="dae18-128">PARAMETERS</span></span>

### <span data-ttu-id="dae18-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dae18-129">-ApplicationGateway</span></span>
<span data-ttu-id="dae18-130">指定此 Cmdlet 新增前端 IP 設定檔的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="dae18-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="dae18-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae18-131">-DefaultProfile</span></span>
<span data-ttu-id="dae18-132">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dae18-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dae18-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="dae18-133">-Name</span></span>
<span data-ttu-id="dae18-134">指定要新增的前端 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="dae18-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="dae18-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="dae18-135">-PrivateIPAddress</span></span>
<span data-ttu-id="dae18-136">指定要新增為應用程式閘道前端 IP 的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="dae18-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="dae18-137">如果指定，此 IP 會從子網靜態配置。</span><span class="sxs-lookup"><span data-stu-id="dae18-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="dae18-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="dae18-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="dae18-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="dae18-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="dae18-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dae18-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="dae18-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dae18-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="dae18-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="dae18-142">-PublicIPAddress</span></span>
<span data-ttu-id="dae18-143">指定此 Cmdlet 新增為應用程式閘道前端 IP 位址的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="dae18-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="dae18-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="dae18-144">-PublicIPAddressId</span></span>
<span data-ttu-id="dae18-145">指定此 Cmdlet 新增為應用程式閘道前端 IP 位址之公用 IP 位址的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dae18-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="dae18-146">-子網</span><span class="sxs-lookup"><span data-stu-id="dae18-146">-Subnet</span></span>
<span data-ttu-id="dae18-147">指定此 Cmdlet 新增為前端 IP 配置的子網。</span><span class="sxs-lookup"><span data-stu-id="dae18-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="dae18-148">如果您指定此參數，表示應用程式閘道支援私人 IP 型設定。</span><span class="sxs-lookup"><span data-stu-id="dae18-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="dae18-149">如果 *已指定 PrivateIPAddress* 參數，應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="dae18-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="dae18-150">如果 *未指定 PrivateIPAddress，* 此子網的其中一個 IP 位址會動態取用為應用程式閘道的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="dae18-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="dae18-151">-子網Id</span><span class="sxs-lookup"><span data-stu-id="dae18-151">-SubnetId</span></span>
<span data-ttu-id="dae18-152">指定此 Cmdlet 新增為前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="dae18-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="dae18-153">傳遞子網表示私人 IP。</span><span class="sxs-lookup"><span data-stu-id="dae18-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="dae18-154">如果 *已指定 PrivateIPAddress* 參數，應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="dae18-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="dae18-155">否則，此子網的其中一個 IP 會動態選取為應用程式閘道的前端 IP。</span><span class="sxs-lookup"><span data-stu-id="dae18-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="dae18-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae18-156">CommonParameters</span></span>
<span data-ttu-id="dae18-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dae18-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae18-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dae18-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae18-159">輸入</span><span class="sxs-lookup"><span data-stu-id="dae18-159">INPUTS</span></span>

### <span data-ttu-id="dae18-160">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dae18-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dae18-161">輸出</span><span class="sxs-lookup"><span data-stu-id="dae18-161">OUTPUTS</span></span>

### <span data-ttu-id="dae18-162">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dae18-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dae18-163">筆記</span><span class="sxs-lookup"><span data-stu-id="dae18-163">NOTES</span></span>

## <span data-ttu-id="dae18-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="dae18-164">RELATED LINKS</span></span>

[<span data-ttu-id="dae18-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="dae18-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="dae18-166">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="dae18-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="dae18-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="dae18-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="dae18-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="dae18-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


