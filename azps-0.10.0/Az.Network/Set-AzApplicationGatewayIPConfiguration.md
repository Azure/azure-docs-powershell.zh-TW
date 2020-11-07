---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 2c14c8c903f892ac5fe822e96fc463528d32f39d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795446"
---
# <span data-ttu-id="8f78d-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f78d-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8f78d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f78d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f78d-103">修改應用程式閘道的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="8f78d-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="8f78d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f78d-104">SYNTAX</span></span>

### <span data-ttu-id="8f78d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f78d-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f78d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8f78d-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f78d-107">說明</span><span class="sxs-lookup"><span data-stu-id="8f78d-107">DESCRIPTION</span></span>
<span data-ttu-id="8f78d-108">**AzApplicationGatewayIPConfiguration** Cmdlet 會修改 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="8f78d-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="8f78d-109">IP 配置包含部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="8f78d-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="8f78d-110">示例</span><span class="sxs-lookup"><span data-stu-id="8f78d-110">EXAMPLES</span></span>

### <span data-ttu-id="8f78d-111">範例1：設定 IP 配置的目標狀態</span><span class="sxs-lookup"><span data-stu-id="8f78d-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="8f78d-112">第一個命令會取得屬於名為 ResourceGroup01 之資源群組的名為 VNet01 的虛擬網路，並將它儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f78d-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="8f78d-113">第二個命令會使用 $VNet 取得名為 Subnet01 的子網配置，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f78d-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="8f78d-114">第三個命令會取得一個名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f78d-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="8f78d-115">第四個命令會將儲存在 $AppGw 中的應用程式閘道的 IP 設定設為儲存在 $Subnet 中的子網配置。</span><span class="sxs-lookup"><span data-stu-id="8f78d-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="8f78d-116">參數</span><span class="sxs-lookup"><span data-stu-id="8f78d-116">PARAMETERS</span></span>

### <span data-ttu-id="8f78d-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f78d-117">-ApplicationGateway</span></span>
<span data-ttu-id="8f78d-118">指定此 Cmdlet 關聯 IP 配置的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="8f78d-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="8f78d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f78d-119">-DefaultProfile</span></span>
<span data-ttu-id="8f78d-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f78d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f78d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f78d-121">-Name</span></span>
<span data-ttu-id="8f78d-122">指定 IP 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f78d-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="8f78d-123">-子網</span><span class="sxs-lookup"><span data-stu-id="8f78d-123">-Subnet</span></span>
<span data-ttu-id="8f78d-124">指定子網。</span><span class="sxs-lookup"><span data-stu-id="8f78d-124">Specifies the subnet.</span></span>
<span data-ttu-id="8f78d-125">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="8f78d-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="8f78d-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8f78d-126">-SubnetId</span></span>
<span data-ttu-id="8f78d-127">指定子網 ID。</span><span class="sxs-lookup"><span data-stu-id="8f78d-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="8f78d-128">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="8f78d-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="8f78d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f78d-129">CommonParameters</span></span>
<span data-ttu-id="8f78d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f78d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f78d-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f78d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f78d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="8f78d-132">INPUTS</span></span>

### <span data-ttu-id="8f78d-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8f78d-133">System.String</span></span>

## <span data-ttu-id="8f78d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8f78d-134">OUTPUTS</span></span>

### <span data-ttu-id="8f78d-135">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8f78d-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8f78d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8f78d-136">NOTES</span></span>

## <span data-ttu-id="8f78d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f78d-137">RELATED LINKS</span></span>

[<span data-ttu-id="8f78d-138">附加 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f78d-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8f78d-139">附加 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f78d-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8f78d-140">AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f78d-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8f78d-141">新-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f78d-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8f78d-142">移除-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f78d-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


