---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969167"
---
# <span data-ttu-id="4ce20-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ce20-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="4ce20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ce20-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce20-103">將 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4ce20-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="4ce20-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ce20-104">SYNTAX</span></span>

### <span data-ttu-id="4ce20-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce20-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ce20-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4ce20-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ce20-107">說明</span><span class="sxs-lookup"><span data-stu-id="4ce20-107">DESCRIPTION</span></span>
<span data-ttu-id="4ce20-108">**AzApplicationGatewayIPConfiguration** Cmdlet 會將 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4ce20-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="4ce20-109">IP 配置包含部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="4ce20-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="4ce20-110">示例</span><span class="sxs-lookup"><span data-stu-id="4ce20-110">EXAMPLES</span></span>

### <span data-ttu-id="4ce20-111">範例1：將虛擬網路配置新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="4ce20-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="4ce20-112">第一個命令會取得虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="4ce20-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="4ce20-113">第二個命令會使用先前建立的虛擬網路來取得子網。</span><span class="sxs-lookup"><span data-stu-id="4ce20-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="4ce20-114">第三個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4ce20-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4ce20-115">第四個命令會將 IP 配置新增至儲存在 $AppGw 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4ce20-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4ce20-116">參數</span><span class="sxs-lookup"><span data-stu-id="4ce20-116">PARAMETERS</span></span>

### <span data-ttu-id="4ce20-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ce20-117">-ApplicationGateway</span></span>
<span data-ttu-id="4ce20-118">指定此 Cmdlet 新增 IP 配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4ce20-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="4ce20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce20-119">-DefaultProfile</span></span>
<span data-ttu-id="4ce20-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ce20-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ce20-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ce20-121">-Name</span></span>
<span data-ttu-id="4ce20-122">指定要新增的 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="4ce20-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="4ce20-123">-子網</span><span class="sxs-lookup"><span data-stu-id="4ce20-123">-Subnet</span></span>
<span data-ttu-id="4ce20-124">指定子網。</span><span class="sxs-lookup"><span data-stu-id="4ce20-124">Specifies a subnet.</span></span>
<span data-ttu-id="4ce20-125">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="4ce20-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4ce20-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4ce20-126">-SubnetId</span></span>
<span data-ttu-id="4ce20-127">指定子網 ID。</span><span class="sxs-lookup"><span data-stu-id="4ce20-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="4ce20-128">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="4ce20-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4ce20-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce20-129">CommonParameters</span></span>
<span data-ttu-id="4ce20-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ce20-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce20-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ce20-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce20-132">輸入</span><span class="sxs-lookup"><span data-stu-id="4ce20-132">INPUTS</span></span>

### <span data-ttu-id="4ce20-133">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ce20-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ce20-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4ce20-134">OUTPUTS</span></span>

### <span data-ttu-id="4ce20-135">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ce20-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ce20-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4ce20-136">NOTES</span></span>

## <span data-ttu-id="4ce20-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ce20-137">RELATED LINKS</span></span>

[<span data-ttu-id="4ce20-138">AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ce20-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4ce20-139">新-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ce20-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4ce20-140">移除-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ce20-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4ce20-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ce20-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


