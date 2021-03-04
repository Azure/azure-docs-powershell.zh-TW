---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 214f408a5120982a903ed0d0d934c44073c32df8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910698"
---
# <span data-ttu-id="372c9-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="372c9-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="372c9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="372c9-102">SYNOPSIS</span></span>
<span data-ttu-id="372c9-103">為應用程式閘道建立前端 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="372c9-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="372c9-104">語法</span><span class="sxs-lookup"><span data-stu-id="372c9-104">SYNTAX</span></span>

### <span data-ttu-id="372c9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="372c9-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="372c9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="372c9-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="372c9-107">描述</span><span class="sxs-lookup"><span data-stu-id="372c9-107">DESCRIPTION</span></span>
<span data-ttu-id="372c9-108">**New-AzApplicationGatewayFrontendIPConfig** Cmdlet 會為 Azure 應用程式閘道建立前端 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="372c9-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="372c9-109">應用程式閘道支援兩種類型的前端 IP 組式：</span><span class="sxs-lookup"><span data-stu-id="372c9-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="372c9-110">公用 IP 位址 -- 使用內部負載平衡的私人 IP 位址 (ILB) 。</span><span class="sxs-lookup"><span data-stu-id="372c9-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="372c9-111">應用程式閘道最多隻能有一個公用 IP 位址和一個私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="372c9-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="372c9-112">公用 IP 位址和私人 IP 位址應個別新增為前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="372c9-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="372c9-113">例子</span><span class="sxs-lookup"><span data-stu-id="372c9-113">EXAMPLES</span></span>

### <span data-ttu-id="372c9-114">範例 1：使用公用 IP 資源物件建立前端 IP 組</span><span class="sxs-lookup"><span data-stu-id="372c9-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="372c9-115">第一個命令會建立公用 IP 資源物件，並儲存在$PublicIP變數中。</span><span class="sxs-lookup"><span data-stu-id="372c9-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="372c9-116">第二個命令$PublicIP建立名為 FrontEndIP01 的新前端 IP 組$FrontEnd變數。</span><span class="sxs-lookup"><span data-stu-id="372c9-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="372c9-117">範例 2：建立靜態私人 IP 做為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="372c9-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="372c9-118">第一個命令會獲得一個名為 VNet01 的虛擬網路，該網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="372c9-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="372c9-119">第二個命令會使用第一個命令$VNet名為子網01 的子網組$Subnet變數。</span><span class="sxs-lookup"><span data-stu-id="372c9-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="372c9-120">第三個命令會使用第二個命令的 $Subnet 和私人 IP 位址 10.0.1.1 建立名為 FrontEndIP02 的前端 IP 組式，然後將它儲存在 $FrontEnd 變數中。</span><span class="sxs-lookup"><span data-stu-id="372c9-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="372c9-121">範例 3：建立動態私人 IP 做為前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="372c9-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="372c9-122">第一個命令會獲得一個名為 VNet01 的虛擬網路，該網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="372c9-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="372c9-123">第二個命令會使用第一個命令$VNet名為子網01 的子網組$Subnet變數。</span><span class="sxs-lookup"><span data-stu-id="372c9-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="372c9-124">第三個命令會使用第二個命令的 $Subnet 建立名為 FrontEndIP03 的前端 IP 組$FrontEnd變數。</span><span class="sxs-lookup"><span data-stu-id="372c9-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="372c9-125">參數</span><span class="sxs-lookup"><span data-stu-id="372c9-125">PARAMETERS</span></span>

### <span data-ttu-id="372c9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372c9-126">-DefaultProfile</span></span>
<span data-ttu-id="372c9-127">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="372c9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="372c9-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="372c9-128">-Name</span></span>
<span data-ttu-id="372c9-129">指定此 Cmdlet 所建立前端 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="372c9-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="372c9-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="372c9-130">-PrivateIPAddress</span></span>
<span data-ttu-id="372c9-131">指定此 Cmdlet 與應用程式閘道前端 IP 位址關聯的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="372c9-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="372c9-132">只有在已指定子網時，才能指定這項功能。</span><span class="sxs-lookup"><span data-stu-id="372c9-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="372c9-133">此 IP 是從子網靜態配置。</span><span class="sxs-lookup"><span data-stu-id="372c9-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="372c9-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="372c9-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="372c9-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="372c9-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="372c9-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="372c9-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="372c9-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="372c9-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="372c9-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="372c9-138">-PublicIPAddress</span></span>
<span data-ttu-id="372c9-139">指定此 Cmdlet 與應用程式閘道前端 IP 位址關聯之公用 IP 位址物件。</span><span class="sxs-lookup"><span data-stu-id="372c9-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="372c9-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="372c9-140">-PublicIPAddressId</span></span>
<span data-ttu-id="372c9-141">指定此 Cmdlet 與應用程式閘道前端 IP 關聯之公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="372c9-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="372c9-142">-子網</span><span class="sxs-lookup"><span data-stu-id="372c9-142">-Subnet</span></span>
<span data-ttu-id="372c9-143">指定此 Cmdlet 與應用程式閘道前端 IP 位址關聯之子網物件。</span><span class="sxs-lookup"><span data-stu-id="372c9-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="372c9-144">如果您指定此參數，表示閘道使用私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="372c9-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="372c9-145">如果 *已指定 PrivateIPAddress* 參數，它應屬於此參數指定的子網。</span><span class="sxs-lookup"><span data-stu-id="372c9-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="372c9-146">如果 *未指定 PrivateIPAddress，* 此子網的其中一個 IP 位址會動態取用為應用程式閘道的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="372c9-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="372c9-147">-子網Id</span><span class="sxs-lookup"><span data-stu-id="372c9-147">-SubnetId</span></span>
<span data-ttu-id="372c9-148">指定此 Cmdlet 與應用程式閘道前端 IP 組配置的關聯子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="372c9-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="372c9-149">如果您指定 *子網參數* ，表示閘道使用私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="372c9-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="372c9-150">如果 *已指定 PrivateIPAddress* 參數，它應屬於子網指定的 *子網*。</span><span class="sxs-lookup"><span data-stu-id="372c9-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="372c9-151">如果 *未指定 PrivateIPAddress，* 此子網的其中一個 IP 位址會動態取用為應用程式閘道的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="372c9-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="372c9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372c9-152">CommonParameters</span></span>
<span data-ttu-id="372c9-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="372c9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372c9-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="372c9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372c9-155">輸入</span><span class="sxs-lookup"><span data-stu-id="372c9-155">INPUTS</span></span>

### <span data-ttu-id="372c9-156">沒有</span><span class="sxs-lookup"><span data-stu-id="372c9-156">None</span></span>

## <span data-ttu-id="372c9-157">輸出</span><span class="sxs-lookup"><span data-stu-id="372c9-157">OUTPUTS</span></span>

### <span data-ttu-id="372c9-158">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="372c9-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="372c9-159">筆記</span><span class="sxs-lookup"><span data-stu-id="372c9-159">NOTES</span></span>

## <span data-ttu-id="372c9-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="372c9-160">RELATED LINKS</span></span>

[<span data-ttu-id="372c9-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="372c9-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="372c9-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="372c9-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="372c9-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="372c9-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="372c9-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="372c9-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


