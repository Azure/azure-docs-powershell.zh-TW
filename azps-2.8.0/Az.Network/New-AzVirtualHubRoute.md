---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 8a9184eddaf5b614b4338a95e1d895d645e0832e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789261"
---
# <span data-ttu-id="ee87c-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="ee87c-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="ee87c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee87c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee87c-103">建立 Azure 虛擬中樞路由物件。</span><span class="sxs-lookup"><span data-stu-id="ee87c-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="ee87c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee87c-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee87c-105">說明</span><span class="sxs-lookup"><span data-stu-id="ee87c-105">DESCRIPTION</span></span>
<span data-ttu-id="ee87c-106">建立 Azure 虛擬中樞路由物件。</span><span class="sxs-lookup"><span data-stu-id="ee87c-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="ee87c-107">示例</span><span class="sxs-lookup"><span data-stu-id="ee87c-107">EXAMPLES</span></span>

### <span data-ttu-id="ee87c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ee87c-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="ee87c-109">上述將會建立可包含在虛擬中樞路由表中的虛擬中樞路由物件。</span><span class="sxs-lookup"><span data-stu-id="ee87c-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="ee87c-110">虛擬中樞路由是一個記憶體中的物件，可用於建立 VirtualHubRouteTable 物件。</span><span class="sxs-lookup"><span data-stu-id="ee87c-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="ee87c-111">參數</span><span class="sxs-lookup"><span data-stu-id="ee87c-111">PARAMETERS</span></span>

### <span data-ttu-id="ee87c-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ee87c-112">-AddressPrefix</span></span>
<span data-ttu-id="ee87c-113">位址首碼清單。</span><span class="sxs-lookup"><span data-stu-id="ee87c-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="ee87c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee87c-114">-DefaultProfile</span></span>
<span data-ttu-id="ee87c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee87c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee87c-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="ee87c-116">-NextHopIpAddress</span></span>
<span data-ttu-id="ee87c-117">下一個躍點 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="ee87c-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="ee87c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee87c-118">CommonParameters</span></span>
<span data-ttu-id="ee87c-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee87c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee87c-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee87c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee87c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ee87c-121">INPUTS</span></span>

### <span data-ttu-id="ee87c-122">所有</span><span class="sxs-lookup"><span data-stu-id="ee87c-122">None</span></span>

## <span data-ttu-id="ee87c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ee87c-123">OUTPUTS</span></span>

### <span data-ttu-id="ee87c-124">PSVirtualHubRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ee87c-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="ee87c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ee87c-125">NOTES</span></span>

## <span data-ttu-id="ee87c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee87c-126">RELATED LINKS</span></span>

[<span data-ttu-id="ee87c-127">新-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ee87c-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
