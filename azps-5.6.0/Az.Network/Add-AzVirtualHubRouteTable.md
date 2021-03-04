---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5cf2756297a932269f2aee87a248a1ba0eeed20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908858"
---
# <span data-ttu-id="fd61c-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fd61c-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="fd61c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd61c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd61c-103">建立虛擬中樞路由資料表資源，這是 VirtualHub 的子項。</span><span class="sxs-lookup"><span data-stu-id="fd61c-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="fd61c-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd61c-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd61c-105">描述</span><span class="sxs-lookup"><span data-stu-id="fd61c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd61c-106">虛擬中樞路由資料表資源包含路由清單，以及可附加及用來路由虛擬中心流量的一份連結清單。</span><span class="sxs-lookup"><span data-stu-id="fd61c-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="fd61c-107">例子</span><span class="sxs-lookup"><span data-stu-id="fd61c-107">EXAMPLES</span></span>

### <span data-ttu-id="fd61c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fd61c-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="fd61c-109">上述命令會從傳送至該資源的路由建立虛擬中樞路由資料表資源，而這個物件可用於在虛擬中樞中路由流量。</span><span class="sxs-lookup"><span data-stu-id="fd61c-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="fd61c-110">參數</span><span class="sxs-lookup"><span data-stu-id="fd61c-110">PARAMETERS</span></span>

### <span data-ttu-id="fd61c-111">-連接</span><span class="sxs-lookup"><span data-stu-id="fd61c-111">-Connection</span></span>
<span data-ttu-id="fd61c-112">此路由資料表附加的關聯清單。</span><span class="sxs-lookup"><span data-stu-id="fd61c-112">List of connections this route table is attached to.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd61c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd61c-113">-DefaultProfile</span></span>
<span data-ttu-id="fd61c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd61c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd61c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd61c-115">-Name</span></span>
<span data-ttu-id="fd61c-116">路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd61c-116">Name of the route table.</span></span>

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

### <span data-ttu-id="fd61c-117">-路由</span><span class="sxs-lookup"><span data-stu-id="fd61c-117">-Route</span></span>
<span data-ttu-id="fd61c-118">虛擬中樞路由清單。</span><span class="sxs-lookup"><span data-stu-id="fd61c-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd61c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd61c-119">CommonParameters</span></span>
<span data-ttu-id="fd61c-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd61c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd61c-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd61c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd61c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="fd61c-122">INPUTS</span></span>

### <span data-ttu-id="fd61c-123">沒有</span><span class="sxs-lookup"><span data-stu-id="fd61c-123">None</span></span>

## <span data-ttu-id="fd61c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="fd61c-124">OUTPUTS</span></span>

### <span data-ttu-id="fd61c-125">Microsoft.Azure.Commands.Network.models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fd61c-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="fd61c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="fd61c-126">NOTES</span></span>

## <span data-ttu-id="fd61c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd61c-127">RELATED LINKS</span></span>
