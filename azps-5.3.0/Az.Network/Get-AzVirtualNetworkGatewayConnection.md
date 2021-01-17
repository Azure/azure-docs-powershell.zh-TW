---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449316"
---
# <span data-ttu-id="b45eb-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b45eb-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b45eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b45eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b45eb-103">取得虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="b45eb-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="b45eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="b45eb-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b45eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="b45eb-105">DESCRIPTION</span></span>
<span data-ttu-id="b45eb-106">虛擬網路閘道連線是代表連接至 Azure 中虛擬網路閘道的 IPsec 隧道 (點對點或 Vnet 到 Vnet) 的物件。</span><span class="sxs-lookup"><span data-stu-id="b45eb-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="b45eb-107">**AzVirtualNetworkGatewayConnection** Cmdlet 會根據名稱和資源群組名稱，傳回連線物件。</span><span class="sxs-lookup"><span data-stu-id="b45eb-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="b45eb-108">如果未指定-Name 參數就發出 **AzVirtualNetworkGatewayConnection** Cmdlet，則輸出將不會顯示 ConnectionStatus 和 SharedKey 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b45eb-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="b45eb-109">示例</span><span class="sxs-lookup"><span data-stu-id="b45eb-109">EXAMPLES</span></span>

### <span data-ttu-id="b45eb-110">1：取得虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="b45eb-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="b45eb-111">傳回資源群組 "myRG" 中名稱為 "myTunnel" 的虛擬網路閘道連線物件</span><span class="sxs-lookup"><span data-stu-id="b45eb-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="b45eb-112">2：使用篩選來取得所有虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="b45eb-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="b45eb-113">傳回在資源群組 "myRG" 中以 "myTunnel" 為開頭的所有虛擬網路閘道連接</span><span class="sxs-lookup"><span data-stu-id="b45eb-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="b45eb-114">參數</span><span class="sxs-lookup"><span data-stu-id="b45eb-114">PARAMETERS</span></span>

### <span data-ttu-id="b45eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b45eb-115">-DefaultProfile</span></span>
<span data-ttu-id="b45eb-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b45eb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b45eb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b45eb-117">-Name</span></span>
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

### <span data-ttu-id="b45eb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b45eb-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b45eb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b45eb-119">CommonParameters</span></span>
<span data-ttu-id="b45eb-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b45eb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b45eb-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b45eb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b45eb-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b45eb-122">INPUTS</span></span>

### <span data-ttu-id="b45eb-123">System.object</span><span class="sxs-lookup"><span data-stu-id="b45eb-123">System.String</span></span>

## <span data-ttu-id="b45eb-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b45eb-124">OUTPUTS</span></span>

### <span data-ttu-id="b45eb-125">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b45eb-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b45eb-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b45eb-126">NOTES</span></span>

## <span data-ttu-id="b45eb-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b45eb-127">RELATED LINKS</span></span>

[<span data-ttu-id="b45eb-128">新-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b45eb-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b45eb-129">移除-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b45eb-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b45eb-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b45eb-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
