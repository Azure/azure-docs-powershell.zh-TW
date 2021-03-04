---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 17661a05a970a9661543220c35b122638ddbc524
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909577"
---
# <span data-ttu-id="6e4b5-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e4b5-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="6e4b5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6e4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4b5-103">新增 IP 組配置至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="6e4b5-104">語法</span><span class="sxs-lookup"><span data-stu-id="6e4b5-104">SYNTAX</span></span>

### <span data-ttu-id="6e4b5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e4b5-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e4b5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6e4b5-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e4b5-107">描述</span><span class="sxs-lookup"><span data-stu-id="6e4b5-107">DESCRIPTION</span></span>
<span data-ttu-id="6e4b5-108">**Add-AzApplicationGatewayIPConfiguration** Cmdlet 會新增 IP 設定檔至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="6e4b5-109">IP 群組原則包含部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="6e4b5-110">例子</span><span class="sxs-lookup"><span data-stu-id="6e4b5-110">EXAMPLES</span></span>

### <span data-ttu-id="6e4b5-111">範例 1：新增虛擬網路組配置至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="6e4b5-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="6e4b5-112">第一個命令會獲得一個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="6e4b5-113">第二個命令會使用先前建立之虛擬網路來建立子網。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="6e4b5-114">第三個命令會獲得應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6e4b5-115">第四個命令會將 IP 組$AppGw。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="6e4b5-116">參數</span><span class="sxs-lookup"><span data-stu-id="6e4b5-116">PARAMETERS</span></span>

### <span data-ttu-id="6e4b5-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e4b5-117">-ApplicationGateway</span></span>
<span data-ttu-id="6e4b5-118">指定此 Cmdlet 新增 IP 群組原則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="6e4b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e4b5-119">-DefaultProfile</span></span>
<span data-ttu-id="6e4b5-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e4b5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e4b5-121">-Name</span></span>
<span data-ttu-id="6e4b5-122">指定要新增的 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="6e4b5-123">-子網</span><span class="sxs-lookup"><span data-stu-id="6e4b5-123">-Subnet</span></span>
<span data-ttu-id="6e4b5-124">指定子網。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-124">Specifies a subnet.</span></span>
<span data-ttu-id="6e4b5-125">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="6e4b5-126">-子網Id</span><span class="sxs-lookup"><span data-stu-id="6e4b5-126">-SubnetId</span></span>
<span data-ttu-id="6e4b5-127">指定子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="6e4b5-128">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="6e4b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4b5-129">CommonParameters</span></span>
<span data-ttu-id="6e4b5-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4b5-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6e4b5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4b5-132">輸入</span><span class="sxs-lookup"><span data-stu-id="6e4b5-132">INPUTS</span></span>

### <span data-ttu-id="6e4b5-133">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e4b5-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6e4b5-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6e4b5-134">OUTPUTS</span></span>

### <span data-ttu-id="6e4b5-135">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e4b5-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6e4b5-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6e4b5-136">NOTES</span></span>

## <span data-ttu-id="6e4b5-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e4b5-137">RELATED LINKS</span></span>

[<span data-ttu-id="6e4b5-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e4b5-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6e4b5-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e4b5-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6e4b5-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e4b5-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6e4b5-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e4b5-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


