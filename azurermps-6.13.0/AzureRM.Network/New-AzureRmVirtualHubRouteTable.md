---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRouteTable.md
ms.openlocfilehash: b04585705cb50a9f0acc7b3987fdfbb0a6c64cb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624595"
---
# <span data-ttu-id="c0866-101">New-AzureRmVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c0866-101">New-AzureRmVirtualHubRouteTable</span></span>

## <span data-ttu-id="c0866-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0866-102">SYNOPSIS</span></span>
<span data-ttu-id="c0866-103">建立 Azure 虛擬中樞路由資料表物件。</span><span class="sxs-lookup"><span data-stu-id="c0866-103">Creates an Azure Virtual Hub Route Table object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0866-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0866-104">SYNTAX</span></span>

```
New-AzureRmVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0866-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0866-105">DESCRIPTION</span></span>
<span data-ttu-id="c0866-106">建立 Azure 虛擬中樞路由資料表物件。</span><span class="sxs-lookup"><span data-stu-id="c0866-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="c0866-107">示例</span><span class="sxs-lookup"><span data-stu-id="c0866-107">EXAMPLES</span></span>

### <span data-ttu-id="c0866-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c0866-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

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

<span data-ttu-id="c0866-109">上述將建立由多個路由組成的路由資料表，並附加到新的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="c0866-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="c0866-110">這是記憶體中的物件，可用於將路由資料表新增至新的或現有的 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="c0866-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="c0866-111">參數</span><span class="sxs-lookup"><span data-stu-id="c0866-111">PARAMETERS</span></span>

### <span data-ttu-id="c0866-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0866-112">-DefaultProfile</span></span>
<span data-ttu-id="c0866-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0866-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0866-114">-Route</span><span class="sxs-lookup"><span data-stu-id="c0866-114">-Route</span></span>
<span data-ttu-id="c0866-115">虛擬中樞路由的清單。</span><span class="sxs-lookup"><span data-stu-id="c0866-115">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="c0866-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0866-116">CommonParameters</span></span>
<span data-ttu-id="c0866-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0866-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0866-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0866-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0866-119">輸入</span><span class="sxs-lookup"><span data-stu-id="c0866-119">INPUTS</span></span>

### <span data-ttu-id="c0866-120">所有</span><span class="sxs-lookup"><span data-stu-id="c0866-120">None</span></span>

## <span data-ttu-id="c0866-121">輸出</span><span class="sxs-lookup"><span data-stu-id="c0866-121">OUTPUTS</span></span>

### <span data-ttu-id="c0866-122">PSVirtualHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0866-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="c0866-123">筆記</span><span class="sxs-lookup"><span data-stu-id="c0866-123">NOTES</span></span>

## <span data-ttu-id="c0866-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0866-124">RELATED LINKS</span></span>
