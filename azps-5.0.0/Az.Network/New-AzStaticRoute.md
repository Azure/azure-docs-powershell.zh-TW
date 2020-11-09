---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286839"
---
# <span data-ttu-id="c8ad6-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="c8ad6-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="c8ad6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ad6-103">建立 StaticRoute 物件，然後將它新增到 RoutingConfiguration 物件。</span><span class="sxs-lookup"><span data-stu-id="c8ad6-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="c8ad6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8ad6-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8ad6-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="c8ad6-106">建立 StaticRoute 物件。</span><span class="sxs-lookup"><span data-stu-id="c8ad6-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="c8ad6-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8ad6-107">EXAMPLES</span></span>

### <span data-ttu-id="c8ad6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c8ad6-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="c8ad6-109">上述命令會建立 StaticRoute 物件，然後將它新增到 RoutingConfiguration 物件。</span><span class="sxs-lookup"><span data-stu-id="c8ad6-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="c8ad6-110">參數</span><span class="sxs-lookup"><span data-stu-id="c8ad6-110">PARAMETERS</span></span>

### <span data-ttu-id="c8ad6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ad6-111">-DefaultProfile</span></span>
<span data-ttu-id="c8ad6-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8ad6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8ad6-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c8ad6-113">-AddressPrefix</span></span>
<span data-ttu-id="c8ad6-114">位址首碼清單。</span><span class="sxs-lookup"><span data-stu-id="c8ad6-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="c8ad6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8ad6-115">-Name</span></span>
<span data-ttu-id="c8ad6-116">路由名稱。</span><span class="sxs-lookup"><span data-stu-id="c8ad6-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8ad6-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="c8ad6-117">-NextHopIpAddress</span></span>
<span data-ttu-id="c8ad6-118">下一個躍點 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="c8ad6-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="c8ad6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ad6-119">CommonParameters</span></span>
<span data-ttu-id="c8ad6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8ad6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ad6-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c8ad6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ad6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c8ad6-122">INPUTS</span></span>

### <span data-ttu-id="c8ad6-123">System.object</span><span class="sxs-lookup"><span data-stu-id="c8ad6-123">System.String</span></span>

## <span data-ttu-id="c8ad6-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c8ad6-124">OUTPUTS</span></span>

### <span data-ttu-id="c8ad6-125">PSStaticRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c8ad6-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="c8ad6-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c8ad6-126">NOTES</span></span>

## <span data-ttu-id="c8ad6-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8ad6-127">RELATED LINKS</span></span>

[<span data-ttu-id="c8ad6-128">新-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8ad6-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
