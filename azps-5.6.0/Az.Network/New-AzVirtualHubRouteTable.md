---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 5451a38b90f8903ef816a75ba7d7a27dd3aec5fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916385"
---
# <span data-ttu-id="4da4b-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4da4b-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="4da4b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4da4b-102">SYNOPSIS</span></span>
<span data-ttu-id="4da4b-103">建立 Azure 虛擬中樞路由表物件。</span><span class="sxs-lookup"><span data-stu-id="4da4b-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="4da4b-104">語法</span><span class="sxs-lookup"><span data-stu-id="4da4b-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4da4b-105">描述</span><span class="sxs-lookup"><span data-stu-id="4da4b-105">DESCRIPTION</span></span>
<span data-ttu-id="4da4b-106">建立 Azure 虛擬中樞路由表物件。</span><span class="sxs-lookup"><span data-stu-id="4da4b-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="4da4b-107">例子</span><span class="sxs-lookup"><span data-stu-id="4da4b-107">EXAMPLES</span></span>

### <span data-ttu-id="4da4b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4da4b-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="4da4b-109">上述將會建立由多個路由組成的路由資料表，並附加至新的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="4da4b-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="4da4b-110">這是記憶體內的物件，可用來將路由資料表新增到新的或現有的 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="4da4b-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="4da4b-111">參數</span><span class="sxs-lookup"><span data-stu-id="4da4b-111">PARAMETERS</span></span>

### <span data-ttu-id="4da4b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da4b-112">-DefaultProfile</span></span>
<span data-ttu-id="4da4b-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4da4b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4da4b-114">-路由</span><span class="sxs-lookup"><span data-stu-id="4da4b-114">-Route</span></span>
<span data-ttu-id="4da4b-115">虛擬中樞路由清單。</span><span class="sxs-lookup"><span data-stu-id="4da4b-115">List of virtual hub routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da4b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da4b-116">CommonParameters</span></span>
<span data-ttu-id="4da4b-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4da4b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da4b-118">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4da4b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da4b-119">輸入</span><span class="sxs-lookup"><span data-stu-id="4da4b-119">INPUTS</span></span>

### <span data-ttu-id="4da4b-120">沒有</span><span class="sxs-lookup"><span data-stu-id="4da4b-120">None</span></span>

## <span data-ttu-id="4da4b-121">輸出</span><span class="sxs-lookup"><span data-stu-id="4da4b-121">OUTPUTS</span></span>

### <span data-ttu-id="4da4b-122">Microsoft.Azure.Commands.Network.models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4da4b-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="4da4b-123">筆記</span><span class="sxs-lookup"><span data-stu-id="4da4b-123">NOTES</span></span>

## <span data-ttu-id="4da4b-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="4da4b-124">RELATED LINKS</span></span>

[<span data-ttu-id="4da4b-125">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="4da4b-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
