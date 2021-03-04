---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 42553004f8d084496a1f4809bca408e0b4c62cef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911630"
---
# <span data-ttu-id="56771-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="56771-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="56771-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56771-102">SYNOPSIS</span></span>
<span data-ttu-id="56771-103">建立 Azure 虛擬中樞路由物件。</span><span class="sxs-lookup"><span data-stu-id="56771-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="56771-104">語法</span><span class="sxs-lookup"><span data-stu-id="56771-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56771-105">描述</span><span class="sxs-lookup"><span data-stu-id="56771-105">DESCRIPTION</span></span>
<span data-ttu-id="56771-106">建立 Azure 虛擬中樞路由物件。</span><span class="sxs-lookup"><span data-stu-id="56771-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="56771-107">例子</span><span class="sxs-lookup"><span data-stu-id="56771-107">EXAMPLES</span></span>

### <span data-ttu-id="56771-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="56771-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="56771-109">上述將會建立虛擬中樞路由物件，該物件可包含在虛擬中樞路由資料表中。</span><span class="sxs-lookup"><span data-stu-id="56771-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="56771-110">虛擬中樞路由是記憶體內的物件，可用來建立 VirtualHubRouteTable 物件。</span><span class="sxs-lookup"><span data-stu-id="56771-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="56771-111">參數</span><span class="sxs-lookup"><span data-stu-id="56771-111">PARAMETERS</span></span>

### <span data-ttu-id="56771-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="56771-112">-AddressPrefix</span></span>
<span data-ttu-id="56771-113">位址首碼清單。</span><span class="sxs-lookup"><span data-stu-id="56771-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56771-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56771-114">-DefaultProfile</span></span>
<span data-ttu-id="56771-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56771-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56771-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="56771-116">-NextHopIpAddress</span></span>
<span data-ttu-id="56771-117">下一個躍點 IpAddress。</span><span class="sxs-lookup"><span data-stu-id="56771-117">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56771-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56771-118">CommonParameters</span></span>
<span data-ttu-id="56771-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56771-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56771-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="56771-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56771-121">輸入</span><span class="sxs-lookup"><span data-stu-id="56771-121">INPUTS</span></span>

### <span data-ttu-id="56771-122">沒有</span><span class="sxs-lookup"><span data-stu-id="56771-122">None</span></span>

## <span data-ttu-id="56771-123">輸出</span><span class="sxs-lookup"><span data-stu-id="56771-123">OUTPUTS</span></span>

### <span data-ttu-id="56771-124">Microsoft.Azure.Commands.Network.models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="56771-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="56771-125">筆記</span><span class="sxs-lookup"><span data-stu-id="56771-125">NOTES</span></span>

## <span data-ttu-id="56771-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="56771-126">RELATED LINKS</span></span>

[<span data-ttu-id="56771-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="56771-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
