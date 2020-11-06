---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 08dc5728e13423fdd9e05c5d5b5d843b963c4aa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453403"
---
# <span data-ttu-id="b7c6f-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7c6f-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="b7c6f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c6f-103">將 IP 配置新增至虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7c6f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7c6f-104">SYNTAX</span></span>

### <span data-ttu-id="b7c6f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c6f-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c6f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b7c6f-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7c6f-107">說明</span><span class="sxs-lookup"><span data-stu-id="b7c6f-107">DESCRIPTION</span></span>
<span data-ttu-id="b7c6f-108">**AzureRmVirtualNetworkGatewayIpConfig** Cmdlet 會將 IP 配置新增至虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="b7c6f-109">示例</span><span class="sxs-lookup"><span data-stu-id="b7c6f-109">EXAMPLES</span></span>

## <span data-ttu-id="b7c6f-110">參數</span><span class="sxs-lookup"><span data-stu-id="b7c6f-110">PARAMETERS</span></span>

### <span data-ttu-id="b7c6f-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7c6f-111">-Name</span></span>
<span data-ttu-id="b7c6f-112">指定要新增的閘道 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-112">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="b7c6f-113">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b7c6f-113">-PrivateIpAddress</span></span>
<span data-ttu-id="b7c6f-114">指定私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-114">Specifies the private IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c6f-115">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b7c6f-115">-PublicIpAddress</span></span>
<span data-ttu-id="b7c6f-116">指定公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-116">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c6f-117">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b7c6f-117">-PublicIpAddressId</span></span>
<span data-ttu-id="b7c6f-118">指定公用 IP 位址的 ID。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-118">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="b7c6f-119">-子網</span><span class="sxs-lookup"><span data-stu-id="b7c6f-119">-Subnet</span></span>
<span data-ttu-id="b7c6f-120">指定 **PSSubnet** 物件。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-120">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="b7c6f-121">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b7c6f-121">-SubnetId</span></span>
<span data-ttu-id="b7c6f-122">指定子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-122">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="b7c6f-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b7c6f-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b7c6f-124">指定 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-124">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="b7c6f-125">這個 Cmdlet 會修改您指定的 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-125">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="b7c6f-126">您可以使用 Get-AzureRmVirtualNetworkGateway Cmdlet 來檢索 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-126">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c6f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b7c6f-127">-Confirm</span></span>
<span data-ttu-id="b7c6f-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c6f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c6f-129">-WhatIf</span></span>
<span data-ttu-id="b7c6f-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c6f-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c6f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c6f-132">-DefaultProfile</span></span>
<span data-ttu-id="b7c6f-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7c6f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c6f-134">CommonParameters</span></span>
<span data-ttu-id="b7c6f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c6f-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7c6f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c6f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b7c6f-137">INPUTS</span></span>

### <span data-ttu-id="b7c6f-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b7c6f-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="b7c6f-139">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b7c6f-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="b7c6f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b7c6f-140">OUTPUTS</span></span>

### <span data-ttu-id="b7c6f-141">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b7c6f-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b7c6f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b7c6f-142">NOTES</span></span>

## <span data-ttu-id="b7c6f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7c6f-143">RELATED LINKS</span></span>

[<span data-ttu-id="b7c6f-144">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b7c6f-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b7c6f-145">新-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7c6f-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="b7c6f-146">移除-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7c6f-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


