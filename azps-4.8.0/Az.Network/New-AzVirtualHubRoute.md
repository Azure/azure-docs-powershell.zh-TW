---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: baf349f56d3ebbf55c21d99dbfefd64ad7b295a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135818"
---
# <span data-ttu-id="f91dc-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f91dc-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="f91dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f91dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f91dc-103">建立 Azure 虛擬中樞路由物件。</span><span class="sxs-lookup"><span data-stu-id="f91dc-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="f91dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="f91dc-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f91dc-105">說明</span><span class="sxs-lookup"><span data-stu-id="f91dc-105">DESCRIPTION</span></span>
<span data-ttu-id="f91dc-106">建立 Azure 虛擬中樞路由物件。</span><span class="sxs-lookup"><span data-stu-id="f91dc-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="f91dc-107">示例</span><span class="sxs-lookup"><span data-stu-id="f91dc-107">EXAMPLES</span></span>

### <span data-ttu-id="f91dc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f91dc-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="f91dc-109">上述將會建立可包含在虛擬中樞路由表中的虛擬中樞路由物件。</span><span class="sxs-lookup"><span data-stu-id="f91dc-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="f91dc-110">虛擬中樞路由是一個記憶體中的物件，可用於建立 VirtualHubRouteTable 物件。</span><span class="sxs-lookup"><span data-stu-id="f91dc-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="f91dc-111">參數</span><span class="sxs-lookup"><span data-stu-id="f91dc-111">PARAMETERS</span></span>

### <span data-ttu-id="f91dc-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f91dc-112">-AddressPrefix</span></span>
<span data-ttu-id="f91dc-113">位址首碼清單。</span><span class="sxs-lookup"><span data-stu-id="f91dc-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="f91dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91dc-114">-DefaultProfile</span></span>
<span data-ttu-id="f91dc-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f91dc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f91dc-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="f91dc-116">-NextHopIpAddress</span></span>
<span data-ttu-id="f91dc-117">下一個躍點 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="f91dc-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="f91dc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91dc-118">CommonParameters</span></span>
<span data-ttu-id="f91dc-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f91dc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91dc-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f91dc-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91dc-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f91dc-121">INPUTS</span></span>

### <span data-ttu-id="f91dc-122">所有</span><span class="sxs-lookup"><span data-stu-id="f91dc-122">None</span></span>

## <span data-ttu-id="f91dc-123">輸出</span><span class="sxs-lookup"><span data-stu-id="f91dc-123">OUTPUTS</span></span>

### <span data-ttu-id="f91dc-124">PSVirtualHubRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f91dc-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="f91dc-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f91dc-125">NOTES</span></span>

## <span data-ttu-id="f91dc-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f91dc-126">RELATED LINKS</span></span>

[<span data-ttu-id="f91dc-127">新-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f91dc-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
