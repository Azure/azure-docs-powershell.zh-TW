---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: e4b972944f757c9b0072f091dc820de5fa5d5b1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904986"
---
# <span data-ttu-id="a8d61-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a8d61-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="a8d61-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a8d61-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d61-103">建立虛擬網路閘道連接</span><span class="sxs-lookup"><span data-stu-id="a8d61-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="a8d61-104">語法</span><span class="sxs-lookup"><span data-stu-id="a8d61-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8d61-105">描述</span><span class="sxs-lookup"><span data-stu-id="a8d61-105">DESCRIPTION</span></span>
<span data-ttu-id="a8d61-106">虛擬網路閘道連接是代表 IPsec 服務物件 (網站對網站或 Vnet-to-Vnet) 連接至 Azure 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="a8d61-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="a8d61-107">**Get-AzVirtualNetworkGatewayConnection** Cmdlet 會根據名稱和資源組名，會返回您的連線物件。</span><span class="sxs-lookup"><span data-stu-id="a8d61-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="a8d61-108">如果 **Get-AzVirtualNetworkGatewayConnection** Cmdlet 在未指定 -Name 參數的情況下發行，輸出將不會顯示 ConnectionStatus 和 SharedKey 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a8d61-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="a8d61-109">例子</span><span class="sxs-lookup"><span data-stu-id="a8d61-109">EXAMPLES</span></span>

### <span data-ttu-id="a8d61-110">1：取得虛擬網路閘道連接</span><span class="sxs-lookup"><span data-stu-id="a8d61-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="a8d61-111">在資源群組 "myRG" 中，以名稱為 "myTun圳" 的虛擬網路閘道連線物件</span><span class="sxs-lookup"><span data-stu-id="a8d61-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="a8d61-112">2：使用篩選取得所有虛擬網路閘道連接</span><span class="sxs-lookup"><span data-stu-id="a8d61-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="a8d61-113">會返回資源群組 "myRG" 中以 "myTun圳" 為起始的所有虛擬網路閘道連接</span><span class="sxs-lookup"><span data-stu-id="a8d61-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="a8d61-114">參數</span><span class="sxs-lookup"><span data-stu-id="a8d61-114">PARAMETERS</span></span>

### <span data-ttu-id="a8d61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d61-115">-DefaultProfile</span></span>
<span data-ttu-id="a8d61-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8d61-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8d61-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8d61-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a8d61-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8d61-118">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a8d61-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d61-119">CommonParameters</span></span>
<span data-ttu-id="a8d61-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a8d61-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d61-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8d61-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d61-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a8d61-122">INPUTS</span></span>

### <span data-ttu-id="a8d61-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a8d61-123">System.String</span></span>

## <span data-ttu-id="a8d61-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a8d61-124">OUTPUTS</span></span>

### <span data-ttu-id="a8d61-125">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a8d61-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="a8d61-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a8d61-126">NOTES</span></span>

## <span data-ttu-id="a8d61-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8d61-127">RELATED LINKS</span></span>

[<span data-ttu-id="a8d61-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a8d61-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="a8d61-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a8d61-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="a8d61-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a8d61-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
