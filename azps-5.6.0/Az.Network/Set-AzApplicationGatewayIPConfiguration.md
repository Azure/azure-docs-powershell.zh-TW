---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: b8a38bd16fcd08104f678752d03dbc4a6d1f054b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915325"
---
# <span data-ttu-id="4fc4b-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc4b-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="4fc4b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4fc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc4b-103">修改應用程式閘道的 IP 群組原則。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="4fc4b-104">語法</span><span class="sxs-lookup"><span data-stu-id="4fc4b-104">SYNTAX</span></span>

### <span data-ttu-id="4fc4b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4fc4b-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc4b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4fc4b-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fc4b-107">描述</span><span class="sxs-lookup"><span data-stu-id="4fc4b-107">DESCRIPTION</span></span>
<span data-ttu-id="4fc4b-108">**Set-AzApplicationGatewayIPConfiguration** Cmdlet 會修改 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="4fc4b-109">IP 群組原則包含部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="4fc4b-110">例子</span><span class="sxs-lookup"><span data-stu-id="4fc4b-110">EXAMPLES</span></span>

### <span data-ttu-id="4fc4b-111">範例 1：更新應用程式閘道的 IP 組</span><span class="sxs-lookup"><span data-stu-id="4fc4b-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="4fc4b-112">第一個命令會獲得名為 VNet01 的虛擬網路，該虛擬網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="4fc4b-113">第二個命令會使用 $VNet 將子網組$Subnet變數。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="4fc4b-114">第三個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4fc4b-115">第四個命令會設定儲存在 $AppGw 中的應用程式閘道之 IP 設定$Subnet。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="4fc4b-116">參數</span><span class="sxs-lookup"><span data-stu-id="4fc4b-116">PARAMETERS</span></span>

### <span data-ttu-id="4fc4b-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fc4b-117">-ApplicationGateway</span></span>
<span data-ttu-id="4fc4b-118">指定此 Cmdlet 與 IP 群組原則建立關聯的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="4fc4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc4b-119">-DefaultProfile</span></span>
<span data-ttu-id="4fc4b-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fc4b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4fc4b-121">-Name</span></span>
<span data-ttu-id="4fc4b-122">指定 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="4fc4b-123">-子網</span><span class="sxs-lookup"><span data-stu-id="4fc4b-123">-Subnet</span></span>
<span data-ttu-id="4fc4b-124">指定子網。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-124">Specifies the subnet.</span></span>
<span data-ttu-id="4fc4b-125">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4fc4b-126">-子網Id</span><span class="sxs-lookup"><span data-stu-id="4fc4b-126">-SubnetId</span></span>
<span data-ttu-id="4fc4b-127">指定子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="4fc4b-128">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4fc4b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc4b-129">CommonParameters</span></span>
<span data-ttu-id="4fc4b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc4b-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4fc4b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc4b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="4fc4b-132">INPUTS</span></span>

### <span data-ttu-id="4fc4b-133">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fc4b-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fc4b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4fc4b-134">OUTPUTS</span></span>

### <span data-ttu-id="4fc4b-135">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fc4b-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fc4b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4fc4b-136">NOTES</span></span>

## <span data-ttu-id="4fc4b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fc4b-137">RELATED LINKS</span></span>

[<span data-ttu-id="4fc4b-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc4b-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4fc4b-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc4b-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4fc4b-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc4b-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4fc4b-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc4b-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4fc4b-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc4b-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


