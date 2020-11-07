---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 31790ead292c9146aa73f41c56e79f3bdf51c715
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794501"
---
# <span data-ttu-id="d0388-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0388-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="d0388-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0388-102">SYNOPSIS</span></span>
<span data-ttu-id="d0388-103">將 IP 配置新增至虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="d0388-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="d0388-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0388-104">SYNTAX</span></span>

### <span data-ttu-id="d0388-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0388-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0388-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d0388-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0388-107">說明</span><span class="sxs-lookup"><span data-stu-id="d0388-107">DESCRIPTION</span></span>
<span data-ttu-id="d0388-108">**AzVirtualNetworkGatewayIpConfig** Cmdlet 會將 IP 配置新增至虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="d0388-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="d0388-109">示例</span><span class="sxs-lookup"><span data-stu-id="d0388-109">EXAMPLES</span></span>

### <span data-ttu-id="d0388-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="d0388-110">1:</span></span>
```

```

## <span data-ttu-id="d0388-111">參數</span><span class="sxs-lookup"><span data-stu-id="d0388-111">PARAMETERS</span></span>

### <span data-ttu-id="d0388-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0388-112">-DefaultProfile</span></span>
<span data-ttu-id="d0388-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0388-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0388-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0388-114">-Name</span></span>
<span data-ttu-id="d0388-115">指定要新增的閘道 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="d0388-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="d0388-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d0388-116">-PrivateIpAddress</span></span>
<span data-ttu-id="d0388-117">指定私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d0388-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="d0388-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d0388-118">-PublicIpAddress</span></span>
<span data-ttu-id="d0388-119">指定公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d0388-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="d0388-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d0388-120">-PublicIpAddressId</span></span>
<span data-ttu-id="d0388-121">指定公用 IP 位址的 ID。</span><span class="sxs-lookup"><span data-stu-id="d0388-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="d0388-122">-子網</span><span class="sxs-lookup"><span data-stu-id="d0388-122">-Subnet</span></span>
<span data-ttu-id="d0388-123">指定 **PSSubnet** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0388-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="d0388-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d0388-124">-SubnetId</span></span>
<span data-ttu-id="d0388-125">指定子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0388-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="d0388-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0388-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d0388-127">指定 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0388-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="d0388-128">這個 Cmdlet 會修改您指定的 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0388-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="d0388-129">您可以使用 Get-AzVirtualNetworkGateway Cmdlet 來檢索 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0388-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="d0388-130">-確認</span><span class="sxs-lookup"><span data-stu-id="d0388-130">-Confirm</span></span>
<span data-ttu-id="d0388-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0388-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0388-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0388-132">-WhatIf</span></span>
<span data-ttu-id="d0388-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0388-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0388-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0388-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0388-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0388-135">CommonParameters</span></span>
<span data-ttu-id="d0388-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0388-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0388-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0388-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0388-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d0388-138">INPUTS</span></span>

### <span data-ttu-id="d0388-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0388-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="d0388-140">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d0388-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="d0388-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d0388-141">OUTPUTS</span></span>

### <span data-ttu-id="d0388-142">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d0388-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d0388-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d0388-143">NOTES</span></span>

## <span data-ttu-id="d0388-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0388-144">RELATED LINKS</span></span>

[<span data-ttu-id="d0388-145">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0388-145">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d0388-146">新-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0388-146">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="d0388-147">移除-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0388-147">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)


