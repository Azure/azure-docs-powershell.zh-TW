---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 340baa4b7a7d0afaf0e0523cb8c2f14f8270bf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802437"
---
# <span data-ttu-id="10318-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="10318-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="10318-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10318-102">SYNOPSIS</span></span>
<span data-ttu-id="10318-103">將 IP 配置新增至虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="10318-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10318-104">句法</span><span class="sxs-lookup"><span data-stu-id="10318-104">SYNTAX</span></span>

### <span data-ttu-id="10318-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10318-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10318-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="10318-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10318-107">說明</span><span class="sxs-lookup"><span data-stu-id="10318-107">DESCRIPTION</span></span>
<span data-ttu-id="10318-108">**AzureRmVirtualNetworkGatewayIpConfig** Cmdlet 會將 IP 配置新增至虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="10318-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="10318-109">示例</span><span class="sxs-lookup"><span data-stu-id="10318-109">EXAMPLES</span></span>

### <span data-ttu-id="10318-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="10318-110">1:</span></span>
```

```

## <span data-ttu-id="10318-111">參數</span><span class="sxs-lookup"><span data-stu-id="10318-111">PARAMETERS</span></span>

### <span data-ttu-id="10318-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10318-112">-DefaultProfile</span></span>
<span data-ttu-id="10318-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10318-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10318-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="10318-114">-Name</span></span>
<span data-ttu-id="10318-115">指定要新增的閘道 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="10318-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="10318-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="10318-116">-PrivateIpAddress</span></span>
<span data-ttu-id="10318-117">指定私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="10318-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="10318-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="10318-118">-PublicIpAddress</span></span>
<span data-ttu-id="10318-119">指定公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="10318-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="10318-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="10318-120">-PublicIpAddressId</span></span>
<span data-ttu-id="10318-121">指定公用 IP 位址的 ID。</span><span class="sxs-lookup"><span data-stu-id="10318-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="10318-122">-子網</span><span class="sxs-lookup"><span data-stu-id="10318-122">-Subnet</span></span>
<span data-ttu-id="10318-123">指定 **PSSubnet** 物件。</span><span class="sxs-lookup"><span data-stu-id="10318-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="10318-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="10318-124">-SubnetId</span></span>
<span data-ttu-id="10318-125">指定子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="10318-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="10318-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="10318-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="10318-127">指定 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="10318-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="10318-128">這個 Cmdlet 會修改您指定的 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="10318-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="10318-129">您可以使用 Get-AzureRmVirtualNetworkGateway Cmdlet 來檢索 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="10318-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10318-130">-確認</span><span class="sxs-lookup"><span data-stu-id="10318-130">-Confirm</span></span>
<span data-ttu-id="10318-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10318-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10318-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10318-132">-WhatIf</span></span>
<span data-ttu-id="10318-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10318-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10318-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10318-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10318-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10318-135">CommonParameters</span></span>
<span data-ttu-id="10318-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10318-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10318-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10318-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10318-138">輸入</span><span class="sxs-lookup"><span data-stu-id="10318-138">INPUTS</span></span>

### <span data-ttu-id="10318-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="10318-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="10318-140">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="10318-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="10318-141">輸出</span><span class="sxs-lookup"><span data-stu-id="10318-141">OUTPUTS</span></span>

### <span data-ttu-id="10318-142">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="10318-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="10318-143">筆記</span><span class="sxs-lookup"><span data-stu-id="10318-143">NOTES</span></span>

## <span data-ttu-id="10318-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="10318-144">RELATED LINKS</span></span>

[<span data-ttu-id="10318-145">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="10318-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="10318-146">新-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="10318-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="10318-147">移除-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="10318-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


