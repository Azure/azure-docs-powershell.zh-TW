---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 4b0fd2fd55b255a9734a0c6b0c325f7ac113b4e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794543"
---
# <span data-ttu-id="6121e-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6121e-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="6121e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6121e-102">SYNOPSIS</span></span>
<span data-ttu-id="6121e-103">將前端 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6121e-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="6121e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6121e-104">SYNTAX</span></span>

### <span data-ttu-id="6121e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6121e-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6121e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6121e-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6121e-107">說明</span><span class="sxs-lookup"><span data-stu-id="6121e-107">DESCRIPTION</span></span>
<span data-ttu-id="6121e-108">**AzApplicationGatewayFrontendIPConfig** Cmdlet 會將前端 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6121e-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="6121e-109">應用程式閘道支援兩種類型的前端 IP 配置：</span><span class="sxs-lookup"><span data-stu-id="6121e-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="6121e-110">公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="6121e-110">Public IP addresses</span></span>
- <span data-ttu-id="6121e-111">使用內部負載平衡的私人 IP 位址 (ILB) </span><span class="sxs-lookup"><span data-stu-id="6121e-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="6121e-112">應用程式閘道最多隻能有一個公用 IP 和一個專用 IP。</span><span class="sxs-lookup"><span data-stu-id="6121e-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="6121e-113">將公用 IP 位址和私人 IP 位址新增為個別的前端 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="6121e-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="6121e-114">示例</span><span class="sxs-lookup"><span data-stu-id="6121e-114">EXAMPLES</span></span>

### <span data-ttu-id="6121e-115">範例1：新增公用 IP 作為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="6121e-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="6121e-116">第一個命令會建立公用 IP 位址物件，並將它儲存在 $PublicIp 變數中。</span><span class="sxs-lookup"><span data-stu-id="6121e-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="6121e-117">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將其儲存于名為 ResourceGroup01 的資源群組，然後將其儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="6121e-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6121e-118">第三個命令會使用儲存在 $PublicIp 中的位址，為 $AppGw 中的閘道新增名為 FrontEndIp01 的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="6121e-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="6121e-119">範例2：新增靜態專用 IP 作為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="6121e-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="6121e-120">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="6121e-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="6121e-121">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="6121e-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="6121e-122">第三個命令會從屬於名為 ResourceGroup01 的資源群組的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="6121e-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6121e-123">第四個命令會使用第二個命令的 $Subnet，以及私人 IP 位址10.0.1.1，來新增名為 FrontendIP02 的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="6121e-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="6121e-124">範例3：新增動態專用 IP 作為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="6121e-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="6121e-125">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="6121e-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="6121e-126">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="6121e-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="6121e-127">第三個命令會從屬於名為 ResourceGroup01 的資源群組的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="6121e-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6121e-128">第四個命令會使用第二個命令中的 $Subnet，新增名為 FrontendIP02 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="6121e-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="6121e-129">參數</span><span class="sxs-lookup"><span data-stu-id="6121e-129">PARAMETERS</span></span>

### <span data-ttu-id="6121e-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6121e-130">-ApplicationGateway</span></span>
<span data-ttu-id="6121e-131">指定此 Cmdlet 新增前端 IP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6121e-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6121e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6121e-132">-DefaultProfile</span></span>
<span data-ttu-id="6121e-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6121e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6121e-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="6121e-134">-Name</span></span>
<span data-ttu-id="6121e-135">指定要新增的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="6121e-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="6121e-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="6121e-136">-PrivateIPAddress</span></span>
<span data-ttu-id="6121e-137">指定要新增為應用程式閘道的前端 IP 的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6121e-137">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="6121e-138">如果已指定，此 IP 是從子網上靜態配置。</span><span class="sxs-lookup"><span data-stu-id="6121e-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="6121e-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="6121e-139">-PublicIPAddress</span></span>
<span data-ttu-id="6121e-140">指定此 Cmdlet 將其新增為應用程式閘道的前端 IP 位址的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6121e-140">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="6121e-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="6121e-141">-PublicIPAddressId</span></span>
<span data-ttu-id="6121e-142">指定此 Cmdlet 將其新增為應用程式閘道的前端 IP 位址的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="6121e-142">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="6121e-143">-子網</span><span class="sxs-lookup"><span data-stu-id="6121e-143">-Subnet</span></span>
<span data-ttu-id="6121e-144">指定這個 Cmdlet 新增為前端 IP 配置的子網。</span><span class="sxs-lookup"><span data-stu-id="6121e-144">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="6121e-145">如果您指定此參數，則表示應用程式閘道支援專用 IP 的專用配置。</span><span class="sxs-lookup"><span data-stu-id="6121e-145">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="6121e-146">如果 *PrivateIPAddress* 參數已指定，它應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="6121e-146">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="6121e-147">如果未指定 *PrivateIPAddress* ，則會將此子網上的其中一個 IP 位址動態挑選為應用程式閘道的前端 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="6121e-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="6121e-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6121e-148">-SubnetId</span></span>
<span data-ttu-id="6121e-149">指定這個 Cmdlet 作為前端 IP 設定而新增的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="6121e-149">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="6121e-150">傳遞子網隱含專用 IP。</span><span class="sxs-lookup"><span data-stu-id="6121e-150">Passing subnet implies private IP.</span></span>
<span data-ttu-id="6121e-151">如果 *PrivateIPAddresss* 參數已指定，它應該屬於這個子網。</span><span class="sxs-lookup"><span data-stu-id="6121e-151">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="6121e-152">否則，此子網上的其中一個 IP 會動態挑選為應用程式閘道的前端 IP。</span><span class="sxs-lookup"><span data-stu-id="6121e-152">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="6121e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6121e-153">CommonParameters</span></span>
<span data-ttu-id="6121e-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6121e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6121e-155">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6121e-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6121e-156">輸入</span><span class="sxs-lookup"><span data-stu-id="6121e-156">INPUTS</span></span>

### <span data-ttu-id="6121e-157">System.object</span><span class="sxs-lookup"><span data-stu-id="6121e-157">System.String</span></span>

## <span data-ttu-id="6121e-158">輸出</span><span class="sxs-lookup"><span data-stu-id="6121e-158">OUTPUTS</span></span>

### <span data-ttu-id="6121e-159">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6121e-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6121e-160">筆記</span><span class="sxs-lookup"><span data-stu-id="6121e-160">NOTES</span></span>

## <span data-ttu-id="6121e-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="6121e-161">RELATED LINKS</span></span>

[<span data-ttu-id="6121e-162">AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6121e-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6121e-163">新-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6121e-163">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6121e-164">移除-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6121e-164">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6121e-165">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6121e-165">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


