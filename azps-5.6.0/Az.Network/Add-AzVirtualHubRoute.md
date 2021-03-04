---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: d90d25776f895bee47549dfb08a4588f0e446883
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908861"
---
# <span data-ttu-id="f31cf-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f31cf-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="f31cf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f31cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f31cf-103">建立 VirtualHubRoute 物件，該物件可以傳遞為參數至命令Add-AzVirtualHubRouteTable命令。</span><span class="sxs-lookup"><span data-stu-id="f31cf-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="f31cf-104">語法</span><span class="sxs-lookup"><span data-stu-id="f31cf-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f31cf-105">描述</span><span class="sxs-lookup"><span data-stu-id="f31cf-105">DESCRIPTION</span></span>
<span data-ttu-id="f31cf-106">建立 VirtualHubRoute 物件。</span><span class="sxs-lookup"><span data-stu-id="f31cf-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="f31cf-107">例子</span><span class="sxs-lookup"><span data-stu-id="f31cf-107">EXAMPLES</span></span>

### <span data-ttu-id="f31cf-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f31cf-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="f31cf-109">上述命令會建立 VirtualHubRoute 物件，然後可以新加入 VirtualHubRouteTable 資源，並設定為 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="f31cf-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="f31cf-110">參數</span><span class="sxs-lookup"><span data-stu-id="f31cf-110">PARAMETERS</span></span>

### <span data-ttu-id="f31cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31cf-111">-DefaultProfile</span></span>
<span data-ttu-id="f31cf-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f31cf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f31cf-113">-目的地</span><span class="sxs-lookup"><span data-stu-id="f31cf-113">-Destination</span></span>
<span data-ttu-id="f31cf-114">目的地清單。</span><span class="sxs-lookup"><span data-stu-id="f31cf-114">List of Destinations.</span></span>

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

### <span data-ttu-id="f31cf-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="f31cf-115">-DestinationType</span></span>
<span data-ttu-id="f31cf-116">目的地類型。</span><span class="sxs-lookup"><span data-stu-id="f31cf-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="f31cf-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="f31cf-117">-NextHop</span></span>
<span data-ttu-id="f31cf-118">下一個躍點清單。</span><span class="sxs-lookup"><span data-stu-id="f31cf-118">List of Next hops.</span></span>

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

### <span data-ttu-id="f31cf-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="f31cf-119">-NextHopType</span></span>
<span data-ttu-id="f31cf-120">下一個躍點類型。</span><span class="sxs-lookup"><span data-stu-id="f31cf-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="f31cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31cf-121">CommonParameters</span></span>
<span data-ttu-id="f31cf-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f31cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31cf-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f31cf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31cf-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f31cf-124">INPUTS</span></span>

### <span data-ttu-id="f31cf-125">沒有</span><span class="sxs-lookup"><span data-stu-id="f31cf-125">None</span></span>

## <span data-ttu-id="f31cf-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f31cf-126">OUTPUTS</span></span>

### <span data-ttu-id="f31cf-127">Microsoft.Azure.Commands.Network.models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f31cf-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="f31cf-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f31cf-128">NOTES</span></span>

## <span data-ttu-id="f31cf-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f31cf-129">RELATED LINKS</span></span>
