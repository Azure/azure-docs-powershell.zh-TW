---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 2ce0cb130e6c4d25d4b076d06224364011ced2b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455228"
---
# <span data-ttu-id="b1dda-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1dda-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b1dda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1dda-102">SYNOPSIS</span></span>
<span data-ttu-id="b1dda-103">將 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b1dda-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1dda-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1dda-104">SYNTAX</span></span>

### <span data-ttu-id="b1dda-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1dda-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1dda-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b1dda-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1dda-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1dda-107">DESCRIPTION</span></span>
<span data-ttu-id="b1dda-108">**AzureRmApplicationGatewayIPConfiguration** Cmdlet 會將 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b1dda-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="b1dda-109">IP 配置包含部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="b1dda-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="b1dda-110">示例</span><span class="sxs-lookup"><span data-stu-id="b1dda-110">EXAMPLES</span></span>

### <span data-ttu-id="b1dda-111">範例1：將虛擬網路配置新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="b1dda-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="b1dda-112">第一個命令會建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b1dda-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="b1dda-113">第二個命令會使用先前建立的虛擬網路來建立子網。</span><span class="sxs-lookup"><span data-stu-id="b1dda-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="b1dda-114">第三個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1dda-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b1dda-115">[Fouth] 命令會將 IP 設定新增至儲存在 $AppGw 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b1dda-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b1dda-116">參數</span><span class="sxs-lookup"><span data-stu-id="b1dda-116">PARAMETERS</span></span>

### <span data-ttu-id="b1dda-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1dda-117">-ApplicationGateway</span></span>
<span data-ttu-id="b1dda-118">指定此 Cmdlet 新增 IP 配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b1dda-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="b1dda-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1dda-119">-DefaultProfile</span></span>
<span data-ttu-id="b1dda-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1dda-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1dda-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1dda-121">-Name</span></span>
<span data-ttu-id="b1dda-122">指定要新增的 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="b1dda-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="b1dda-123">-子網</span><span class="sxs-lookup"><span data-stu-id="b1dda-123">-Subnet</span></span>
<span data-ttu-id="b1dda-124">指定子網。</span><span class="sxs-lookup"><span data-stu-id="b1dda-124">Specifies a subnet.</span></span>
<span data-ttu-id="b1dda-125">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="b1dda-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="b1dda-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b1dda-126">-SubnetId</span></span>
<span data-ttu-id="b1dda-127">指定子網 ID。</span><span class="sxs-lookup"><span data-stu-id="b1dda-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="b1dda-128">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="b1dda-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="b1dda-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1dda-129">CommonParameters</span></span>
<span data-ttu-id="b1dda-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1dda-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1dda-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1dda-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1dda-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b1dda-132">INPUTS</span></span>

### <span data-ttu-id="b1dda-133">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b1dda-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="b1dda-134">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="b1dda-134">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="b1dda-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b1dda-135">OUTPUTS</span></span>

### <span data-ttu-id="b1dda-136">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b1dda-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1dda-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b1dda-137">NOTES</span></span>

## <span data-ttu-id="b1dda-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1dda-138">RELATED LINKS</span></span>

[<span data-ttu-id="b1dda-139">AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1dda-139">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b1dda-140">新-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1dda-140">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b1dda-141">移除-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1dda-141">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b1dda-142">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1dda-142">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


