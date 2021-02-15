---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131406"
---
# <span data-ttu-id="6eb3f-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="6eb3f-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="6eb3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6eb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb3f-103">建立 VirtualHubRoute 物件，該物件可以作為參數傳遞到 Add-AzVirtualHubRouteTable 命令。</span><span class="sxs-lookup"><span data-stu-id="6eb3f-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="6eb3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6eb3f-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eb3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="6eb3f-105">DESCRIPTION</span></span>
<span data-ttu-id="6eb3f-106">建立 VirtualHubRoute 物件。</span><span class="sxs-lookup"><span data-stu-id="6eb3f-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="6eb3f-107">示例</span><span class="sxs-lookup"><span data-stu-id="6eb3f-107">EXAMPLES</span></span>

### <span data-ttu-id="6eb3f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6eb3f-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="6eb3f-109">上述命令會建立 VirtualHubRoute 物件，然後將它新增到 VirtualHubRouteTable 資源，並將其設定為 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="6eb3f-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="6eb3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="6eb3f-110">PARAMETERS</span></span>

### <span data-ttu-id="6eb3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb3f-111">-DefaultProfile</span></span>
<span data-ttu-id="6eb3f-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6eb3f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eb3f-113">-目的地</span><span class="sxs-lookup"><span data-stu-id="6eb3f-113">-Destination</span></span>
<span data-ttu-id="6eb3f-114">目的地清單。</span><span class="sxs-lookup"><span data-stu-id="6eb3f-114">List of Destinations.</span></span>

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

### <span data-ttu-id="6eb3f-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="6eb3f-115">-DestinationType</span></span>
<span data-ttu-id="6eb3f-116">目的地類型。</span><span class="sxs-lookup"><span data-stu-id="6eb3f-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="6eb3f-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="6eb3f-117">-NextHop</span></span>
<span data-ttu-id="6eb3f-118">下一個躍點的清單。</span><span class="sxs-lookup"><span data-stu-id="6eb3f-118">List of Next hops.</span></span>

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

### <span data-ttu-id="6eb3f-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="6eb3f-119">-NextHopType</span></span>
<span data-ttu-id="6eb3f-120">下一個躍點類型。</span><span class="sxs-lookup"><span data-stu-id="6eb3f-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="6eb3f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb3f-121">CommonParameters</span></span>
<span data-ttu-id="6eb3f-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6eb3f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb3f-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6eb3f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb3f-124">輸入</span><span class="sxs-lookup"><span data-stu-id="6eb3f-124">INPUTS</span></span>

### <span data-ttu-id="6eb3f-125">所有</span><span class="sxs-lookup"><span data-stu-id="6eb3f-125">None</span></span>

## <span data-ttu-id="6eb3f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="6eb3f-126">OUTPUTS</span></span>

### <span data-ttu-id="6eb3f-127">PSVirtualHubRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6eb3f-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="6eb3f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6eb3f-128">NOTES</span></span>

## <span data-ttu-id="6eb3f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6eb3f-129">RELATED LINKS</span></span>
