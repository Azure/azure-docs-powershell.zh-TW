---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 961edb46c71b60f0c3c43523d8d88486f1414d3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916054"
---
# <span data-ttu-id="b891c-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b891c-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="b891c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b891c-102">SYNOPSIS</span></span>
<span data-ttu-id="b891c-103">獲得本地網路閘道</span><span class="sxs-lookup"><span data-stu-id="b891c-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="b891c-104">語法</span><span class="sxs-lookup"><span data-stu-id="b891c-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b891c-105">描述</span><span class="sxs-lookup"><span data-stu-id="b891c-105">DESCRIPTION</span></span>
<span data-ttu-id="b891c-106">Local Network Gateway 是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="b891c-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="b891c-107">**Get-AzLocalNetworkGateway** Cmdlet 會根據名稱和資源組名，會返回代表您部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="b891c-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b891c-108">例子</span><span class="sxs-lookup"><span data-stu-id="b891c-108">EXAMPLES</span></span>

### <span data-ttu-id="b891c-109">範例 1：取得本地網路閘道</span><span class="sxs-lookup"><span data-stu-id="b891c-109">Example 1: Get a Local Network Gateway</span></span>
```powershell
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

<span data-ttu-id="b891c-110">在資源群組 "myRG" 中，會返回名稱為 "myLocalGW1" 的 Local Network Gateway 物件</span><span class="sxs-lookup"><span data-stu-id="b891c-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="b891c-111">範例 2：使用篩選取得本地網路閘道</span><span class="sxs-lookup"><span data-stu-id="b891c-111">Example 2: Get Local Network Gateways using filtering</span></span>
```powershell
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

<span data-ttu-id="b891c-112">會以名稱從資源群組 "myRG" 內的 "myLocalGW" 開始，返回 Local Network 閘道的物件</span><span class="sxs-lookup"><span data-stu-id="b891c-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="b891c-113">參數</span><span class="sxs-lookup"><span data-stu-id="b891c-113">PARAMETERS</span></span>

### <span data-ttu-id="b891c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b891c-114">-DefaultProfile</span></span>
<span data-ttu-id="b891c-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b891c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b891c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b891c-116">-Name</span></span>
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

### <span data-ttu-id="b891c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b891c-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b891c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b891c-118">CommonParameters</span></span>
<span data-ttu-id="b891c-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b891c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b891c-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b891c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b891c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="b891c-121">INPUTS</span></span>

### <span data-ttu-id="b891c-122">System.String</span><span class="sxs-lookup"><span data-stu-id="b891c-122">System.String</span></span>

## <span data-ttu-id="b891c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="b891c-123">OUTPUTS</span></span>

### <span data-ttu-id="b891c-124">Microsoft.Azure.Commands.Network.models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b891c-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="b891c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b891c-125">NOTES</span></span>

## <span data-ttu-id="b891c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b891c-126">RELATED LINKS</span></span>

[<span data-ttu-id="b891c-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b891c-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="b891c-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b891c-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="b891c-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b891c-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
