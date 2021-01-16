---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281729"
---
# <span data-ttu-id="be469-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="be469-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="be469-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be469-102">SYNOPSIS</span></span>
<span data-ttu-id="be469-103">建立作為 VirtualHub 子級的虛擬中樞路由資料表資源。</span><span class="sxs-lookup"><span data-stu-id="be469-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="be469-104">句法</span><span class="sxs-lookup"><span data-stu-id="be469-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be469-105">說明</span><span class="sxs-lookup"><span data-stu-id="be469-105">DESCRIPTION</span></span>
<span data-ttu-id="be469-106">虛擬中心路由資料表資源包含路由清單以及它可以附加到的連線清單，並用於路由虛擬中樞中的流量。</span><span class="sxs-lookup"><span data-stu-id="be469-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="be469-107">示例</span><span class="sxs-lookup"><span data-stu-id="be469-107">EXAMPLES</span></span>

### <span data-ttu-id="be469-108">範例1</span><span class="sxs-lookup"><span data-stu-id="be469-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="be469-109">上述命令會從傳遞給它的路由建立虛擬中樞路由資料表資源，而且這個物件可用於在虛擬中樞中路由流量。</span><span class="sxs-lookup"><span data-stu-id="be469-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="be469-110">參數</span><span class="sxs-lookup"><span data-stu-id="be469-110">PARAMETERS</span></span>

### <span data-ttu-id="be469-111">-連接</span><span class="sxs-lookup"><span data-stu-id="be469-111">-Connection</span></span>
<span data-ttu-id="be469-112">此路由表附加到的連線清單。</span><span class="sxs-lookup"><span data-stu-id="be469-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="be469-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be469-113">-DefaultProfile</span></span>
<span data-ttu-id="be469-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be469-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be469-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="be469-115">-Name</span></span>
<span data-ttu-id="be469-116">路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="be469-116">Name of the route table.</span></span>

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

### <span data-ttu-id="be469-117">-Route</span><span class="sxs-lookup"><span data-stu-id="be469-117">-Route</span></span>
<span data-ttu-id="be469-118">虛擬中樞路由的清單。</span><span class="sxs-lookup"><span data-stu-id="be469-118">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="be469-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be469-119">CommonParameters</span></span>
<span data-ttu-id="be469-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be469-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be469-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="be469-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be469-122">輸入</span><span class="sxs-lookup"><span data-stu-id="be469-122">INPUTS</span></span>

### <span data-ttu-id="be469-123">所有</span><span class="sxs-lookup"><span data-stu-id="be469-123">None</span></span>

## <span data-ttu-id="be469-124">輸出</span><span class="sxs-lookup"><span data-stu-id="be469-124">OUTPUTS</span></span>

### <span data-ttu-id="be469-125">PSVirtualHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="be469-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="be469-126">筆記</span><span class="sxs-lookup"><span data-stu-id="be469-126">NOTES</span></span>

## <span data-ttu-id="be469-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="be469-127">RELATED LINKS</span></span>
