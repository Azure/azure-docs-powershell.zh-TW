---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: cc84daecf4c98a48bb37ff0edd38f1136960a273
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452187"
---
# <span data-ttu-id="2c3d5-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c3d5-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2c3d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c3d5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3d5-103">將 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c3d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c3d5-104">SYNTAX</span></span>

### <span data-ttu-id="2c3d5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c3d5-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c3d5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2c3d5-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c3d5-107">說明</span><span class="sxs-lookup"><span data-stu-id="2c3d5-107">DESCRIPTION</span></span>
<span data-ttu-id="2c3d5-108">**AzureRmApplicationGatewayIPConfiguration** Cmdlet 會將 IP 配置新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="2c3d5-109">IP 配置包含部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="2c3d5-110">示例</span><span class="sxs-lookup"><span data-stu-id="2c3d5-110">EXAMPLES</span></span>

### <span data-ttu-id="2c3d5-111">範例1：將虛擬網路配置新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="2c3d5-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="2c3d5-112">第一個命令會建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="2c3d5-113">第二個命令會使用先前建立的虛擬網路來建立子網。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="2c3d5-114">第三個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2c3d5-115">[Fouth] 命令會將 IP 設定新增至儲存在 $AppGw 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2c3d5-116">參數</span><span class="sxs-lookup"><span data-stu-id="2c3d5-116">PARAMETERS</span></span>

### <span data-ttu-id="2c3d5-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c3d5-117">-ApplicationGateway</span></span>
<span data-ttu-id="2c3d5-118">指定此 Cmdlet 新增 IP 配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="2c3d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3d5-119">-DefaultProfile</span></span>
<span data-ttu-id="2c3d5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c3d5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c3d5-121">-Name</span></span>
<span data-ttu-id="2c3d5-122">指定要新增的 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="2c3d5-123">-子網</span><span class="sxs-lookup"><span data-stu-id="2c3d5-123">-Subnet</span></span>
<span data-ttu-id="2c3d5-124">指定子網。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-124">Specifies a subnet.</span></span>
<span data-ttu-id="2c3d5-125">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="2c3d5-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2c3d5-126">-SubnetId</span></span>
<span data-ttu-id="2c3d5-127">指定子網 ID。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="2c3d5-128">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="2c3d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3d5-129">CommonParameters</span></span>
<span data-ttu-id="2c3d5-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3d5-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c3d5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3d5-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2c3d5-132">INPUTS</span></span>

### <span data-ttu-id="2c3d5-133">System.object</span><span class="sxs-lookup"><span data-stu-id="2c3d5-133">System.String</span></span>

## <span data-ttu-id="2c3d5-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2c3d5-134">OUTPUTS</span></span>

### <span data-ttu-id="2c3d5-135">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2c3d5-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2c3d5-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2c3d5-136">NOTES</span></span>

## <span data-ttu-id="2c3d5-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c3d5-137">RELATED LINKS</span></span>

[<span data-ttu-id="2c3d5-138">AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c3d5-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2c3d5-139">新-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c3d5-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2c3d5-140">移除-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c3d5-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2c3d5-141">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c3d5-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


