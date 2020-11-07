---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 83289067bef9cf294477dca60a8b26a9b61dcb41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797622"
---
# <span data-ttu-id="5ac3f-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5ac3f-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="5ac3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ac3f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac3f-103">取得局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="5ac3f-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="5ac3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ac3f-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ac3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ac3f-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac3f-106">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="5ac3f-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="5ac3f-107">**AzLocalNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，傳回代表您的內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="5ac3f-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="5ac3f-108">示例</span><span class="sxs-lookup"><span data-stu-id="5ac3f-108">EXAMPLES</span></span>

### <span data-ttu-id="5ac3f-109">1：取得局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="5ac3f-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="5ac3f-110">傳回資源群組 "myRG" 中名稱為 "myLocalGW1" 的本機網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="5ac3f-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="5ac3f-111">2：使用篩選來取得局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="5ac3f-111">2: Get Local Network Gateways using filtering</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="5ac3f-112">傳回在資源群組 "myRG" 中以 "myLocalGW" 為開頭的本機網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="5ac3f-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="5ac3f-113">參數</span><span class="sxs-lookup"><span data-stu-id="5ac3f-113">PARAMETERS</span></span>

### <span data-ttu-id="5ac3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac3f-114">-DefaultProfile</span></span>
<span data-ttu-id="5ac3f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ac3f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ac3f-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ac3f-116">-Name</span></span>
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

### <span data-ttu-id="5ac3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac3f-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5ac3f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac3f-118">CommonParameters</span></span>
<span data-ttu-id="5ac3f-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ac3f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac3f-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5ac3f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac3f-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5ac3f-121">INPUTS</span></span>

### <span data-ttu-id="5ac3f-122">System.object</span><span class="sxs-lookup"><span data-stu-id="5ac3f-122">System.String</span></span>

## <span data-ttu-id="5ac3f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5ac3f-123">OUTPUTS</span></span>

### <span data-ttu-id="5ac3f-124">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5ac3f-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="5ac3f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="5ac3f-125">NOTES</span></span>

## <span data-ttu-id="5ac3f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ac3f-126">RELATED LINKS</span></span>

[<span data-ttu-id="5ac3f-127">新-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5ac3f-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="5ac3f-128">移除-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5ac3f-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="5ac3f-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5ac3f-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
