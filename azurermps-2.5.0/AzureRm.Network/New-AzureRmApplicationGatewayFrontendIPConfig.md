---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 2003d93a50b1730a162cc910ef289748a86a2954
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800097"
---
# <span data-ttu-id="e7a47-101">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e7a47-101">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="e7a47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7a47-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a47-103">為應用程式閘道建立前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="e7a47-103">Creates a front-end IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7a47-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7a47-104">SYNTAX</span></span>

### <span data-ttu-id="e7a47-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a47-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7a47-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e7a47-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7a47-107">說明</span><span class="sxs-lookup"><span data-stu-id="e7a47-107">DESCRIPTION</span></span>
<span data-ttu-id="e7a47-108">**新的-AzureRmApplicationGatewayFrontendIPConfig** Cmdlet 會針對 Azure 應用程式閘道建立前端 IP configuraton。</span><span class="sxs-lookup"><span data-stu-id="e7a47-108">The **New-AzureRmApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuraton for an Azure application gateway.</span></span>
<span data-ttu-id="e7a47-109">應用程式閘道支援兩種類型的前端 IP 配置：</span><span class="sxs-lookup"><span data-stu-id="e7a47-109">An application gateway supports two types of front-end IP configuration:</span></span> 

- <span data-ttu-id="e7a47-110">公用 IP 位址--使用內部負載平衡 (ILB) 的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e7a47-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>

<span data-ttu-id="e7a47-111">應用程式閘道最多隻能有一個公用 IP 位址和一個私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e7a47-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="e7a47-112">公用 IP 位址與私人 IP 位址應分別新增為前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e7a47-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="e7a47-113">示例</span><span class="sxs-lookup"><span data-stu-id="e7a47-113">EXAMPLES</span></span>

### <span data-ttu-id="e7a47-114">範例1：使用公用 IP 資源物件建立前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="e7a47-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="e7a47-115">第一個命令會建立公用 IP 資源物件，並將它儲存在 $PublicIP 變數中。</span><span class="sxs-lookup"><span data-stu-id="e7a47-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="e7a47-116">第二個命令使用 $PublicIP 來建立名為 FrontEndIP01 的新前端 IP 配置，並將它儲存在 $FrontEnd 變數中。</span><span class="sxs-lookup"><span data-stu-id="e7a47-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="e7a47-117">範例2：建立靜態專用 IP 作為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="e7a47-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="e7a47-118">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="e7a47-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="e7a47-119">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="e7a47-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e7a47-120">第三個命令會使用第二個命令與私人 IP 位址10.0.1.1 中的 $Subnet，建立名為 FrontEndIP02 的前端 IP 設定，然後將它儲存在 $FrontEnd 變數中。</span><span class="sxs-lookup"><span data-stu-id="e7a47-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="e7a47-121">範例3：建立作為前端 IP 位址的動態私人 IP 位址</span><span class="sxs-lookup"><span data-stu-id="e7a47-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="e7a47-122">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="e7a47-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="e7a47-123">第二個命令會從第一個命令取得名為 $VNet Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="e7a47-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e7a47-124">第三個命令會使用第二個命令的 $Subnet 建立名為 FrontEndIP03 的前端 IP 設定，並將它儲存在 $FrontEnd 變數中。</span><span class="sxs-lookup"><span data-stu-id="e7a47-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="e7a47-125">參數</span><span class="sxs-lookup"><span data-stu-id="e7a47-125">PARAMETERS</span></span>

### <span data-ttu-id="e7a47-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a47-126">-DefaultProfile</span></span>
<span data-ttu-id="e7a47-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7a47-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7a47-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7a47-128">-Name</span></span>
<span data-ttu-id="e7a47-129">指定此 Cmdlet 所建立之前端 IP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7a47-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e7a47-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="e7a47-130">-PrivateIPAddress</span></span>
<span data-ttu-id="e7a47-131">指定這個 Cmdlet 與應用程式閘道的前端 IP 位址相關聯的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e7a47-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="e7a47-132">只有在指定子網的情況下，才能指定此選項。</span><span class="sxs-lookup"><span data-stu-id="e7a47-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="e7a47-133">這個 IP 是從子網上靜態指派的。</span><span class="sxs-lookup"><span data-stu-id="e7a47-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="e7a47-134">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="e7a47-134">-PublicIPAddress</span></span>
<span data-ttu-id="e7a47-135">指定這個 Cmdlet 與應用程式閘道的前端 IP 位址相關聯的公用 IP 位址物件。</span><span class="sxs-lookup"><span data-stu-id="e7a47-135">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="e7a47-136">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="e7a47-136">-PublicIPAddressId</span></span>
<span data-ttu-id="e7a47-137">指定此 Cmdlet 與應用程式閘道的前端 IP 相關聯的公用 IP 位址 ID。</span><span class="sxs-lookup"><span data-stu-id="e7a47-137">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="e7a47-138">-子網</span><span class="sxs-lookup"><span data-stu-id="e7a47-138">-Subnet</span></span>
<span data-ttu-id="e7a47-139">指定這個 Cmdlet 與應用程式閘道的前端 IP 位址相關聯的子網物件。</span><span class="sxs-lookup"><span data-stu-id="e7a47-139">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="e7a47-140">如果您指定此參數，則表示閘道使用的是私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e7a47-140">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="e7a47-141">如果指定了 *PrivateIPAddresss* 參數，則它應該屬於此參數指定的子網。</span><span class="sxs-lookup"><span data-stu-id="e7a47-141">If the *PrivateIPAddresss* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="e7a47-142">如果未指定 *PrivateIPAddress* ，則會將此子網上的其中一個 IP 位址動態挑選為應用程式閘道的前端 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="e7a47-142">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="e7a47-143">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e7a47-143">-SubnetId</span></span>
<span data-ttu-id="e7a47-144">指定這個 Cmdlet 與應用程式閘道的前端 IP 設定相關的子網 ID。</span><span class="sxs-lookup"><span data-stu-id="e7a47-144">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="e7a47-145">如果您指定 *Subnet* 參數，則表示閘道使用的是私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e7a47-145">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="e7a47-146">如果已指定 *PrivateIPAddress* 參數，則它應該屬於由 *子網* 指定的子網。</span><span class="sxs-lookup"><span data-stu-id="e7a47-146">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="e7a47-147">如果未指定 *PrivateIPAddress* ，則會將此子網上的其中一個 IP 位址動態挑選為應用程式閘道的前端 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="e7a47-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="e7a47-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a47-148">CommonParameters</span></span>
<span data-ttu-id="e7a47-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7a47-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a47-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e7a47-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a47-151">輸入</span><span class="sxs-lookup"><span data-stu-id="e7a47-151">INPUTS</span></span>

### <span data-ttu-id="e7a47-152">System.object</span><span class="sxs-lookup"><span data-stu-id="e7a47-152">System.String</span></span>

## <span data-ttu-id="e7a47-153">輸出</span><span class="sxs-lookup"><span data-stu-id="e7a47-153">OUTPUTS</span></span>

### <span data-ttu-id="e7a47-154">PSApplicationGatewayFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e7a47-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="e7a47-155">筆記</span><span class="sxs-lookup"><span data-stu-id="e7a47-155">NOTES</span></span>

## <span data-ttu-id="e7a47-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7a47-156">RELATED LINKS</span></span>

[<span data-ttu-id="e7a47-157">附加 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e7a47-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e7a47-158">AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e7a47-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e7a47-159">移除-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e7a47-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e7a47-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e7a47-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)

