---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 9648eb1561ae15501f7a395846f7fda71cf5a1f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135817"
---
# <span data-ttu-id="f7837-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7837-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="f7837-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7837-102">SYNOPSIS</span></span>
<span data-ttu-id="f7837-103">建立 Azure 虛擬中樞路由資料表物件。</span><span class="sxs-lookup"><span data-stu-id="f7837-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="f7837-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7837-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7837-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7837-105">DESCRIPTION</span></span>
<span data-ttu-id="f7837-106">建立 Azure 虛擬中樞路由資料表物件。</span><span class="sxs-lookup"><span data-stu-id="f7837-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="f7837-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7837-107">EXAMPLES</span></span>

### <span data-ttu-id="f7837-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f7837-108">Example 1</span></span>

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

<span data-ttu-id="f7837-109">上述將建立由多個路由組成的路由資料表，並附加到新的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="f7837-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="f7837-110">這是記憶體中的物件，可用於將路由資料表新增至新的或現有的 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="f7837-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="f7837-111">參數</span><span class="sxs-lookup"><span data-stu-id="f7837-111">PARAMETERS</span></span>

### <span data-ttu-id="f7837-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7837-112">-DefaultProfile</span></span>
<span data-ttu-id="f7837-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7837-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7837-114">-Route</span><span class="sxs-lookup"><span data-stu-id="f7837-114">-Route</span></span>
<span data-ttu-id="f7837-115">虛擬中樞路由的清單。</span><span class="sxs-lookup"><span data-stu-id="f7837-115">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="f7837-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7837-116">CommonParameters</span></span>
<span data-ttu-id="f7837-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7837-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7837-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7837-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7837-119">輸入</span><span class="sxs-lookup"><span data-stu-id="f7837-119">INPUTS</span></span>

### <span data-ttu-id="f7837-120">所有</span><span class="sxs-lookup"><span data-stu-id="f7837-120">None</span></span>

## <span data-ttu-id="f7837-121">輸出</span><span class="sxs-lookup"><span data-stu-id="f7837-121">OUTPUTS</span></span>

### <span data-ttu-id="f7837-122">PSVirtualHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f7837-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="f7837-123">筆記</span><span class="sxs-lookup"><span data-stu-id="f7837-123">NOTES</span></span>

## <span data-ttu-id="f7837-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7837-124">RELATED LINKS</span></span>

[<span data-ttu-id="f7837-125">新-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f7837-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)