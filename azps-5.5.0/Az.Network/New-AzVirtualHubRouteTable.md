---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 9648eb1561ae15501f7a395846f7fda71cf5a1f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135790"
---
# <span data-ttu-id="b18af-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b18af-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="b18af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b18af-102">SYNOPSIS</span></span>
<span data-ttu-id="b18af-103">建立 Azure 虛擬中樞路由資料表物件。</span><span class="sxs-lookup"><span data-stu-id="b18af-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="b18af-104">句法</span><span class="sxs-lookup"><span data-stu-id="b18af-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b18af-105">說明</span><span class="sxs-lookup"><span data-stu-id="b18af-105">DESCRIPTION</span></span>
<span data-ttu-id="b18af-106">建立 Azure 虛擬中樞路由資料表物件。</span><span class="sxs-lookup"><span data-stu-id="b18af-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="b18af-107">示例</span><span class="sxs-lookup"><span data-stu-id="b18af-107">EXAMPLES</span></span>

### <span data-ttu-id="b18af-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b18af-108">Example 1</span></span>

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

<span data-ttu-id="b18af-109">上述將建立由多個路由組成的路由資料表，並附加到新的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="b18af-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="b18af-110">這是記憶體中的物件，可用於將路由資料表新增至新的或現有的 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="b18af-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="b18af-111">參數</span><span class="sxs-lookup"><span data-stu-id="b18af-111">PARAMETERS</span></span>

### <span data-ttu-id="b18af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b18af-112">-DefaultProfile</span></span>
<span data-ttu-id="b18af-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b18af-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b18af-114">-Route</span><span class="sxs-lookup"><span data-stu-id="b18af-114">-Route</span></span>
<span data-ttu-id="b18af-115">虛擬中樞路由的清單。</span><span class="sxs-lookup"><span data-stu-id="b18af-115">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="b18af-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b18af-116">CommonParameters</span></span>
<span data-ttu-id="b18af-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b18af-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b18af-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b18af-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b18af-119">輸入</span><span class="sxs-lookup"><span data-stu-id="b18af-119">INPUTS</span></span>

### <span data-ttu-id="b18af-120">所有</span><span class="sxs-lookup"><span data-stu-id="b18af-120">None</span></span>

## <span data-ttu-id="b18af-121">輸出</span><span class="sxs-lookup"><span data-stu-id="b18af-121">OUTPUTS</span></span>

### <span data-ttu-id="b18af-122">PSVirtualHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b18af-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="b18af-123">筆記</span><span class="sxs-lookup"><span data-stu-id="b18af-123">NOTES</span></span>

## <span data-ttu-id="b18af-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="b18af-124">RELATED LINKS</span></span>

[<span data-ttu-id="b18af-125">新-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b18af-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
