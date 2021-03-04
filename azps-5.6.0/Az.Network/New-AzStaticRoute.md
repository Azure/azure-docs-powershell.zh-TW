---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: 2cf661ab2bcc531c0a88ae86934a53b212bb91d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902366"
---
# <span data-ttu-id="9e521-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="9e521-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="9e521-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9e521-102">SYNOPSIS</span></span>
<span data-ttu-id="9e521-103">建立一個 StaticRoute 物件，然後可以新加入到 RoutingConfiguration 物件。</span><span class="sxs-lookup"><span data-stu-id="9e521-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="9e521-104">語法</span><span class="sxs-lookup"><span data-stu-id="9e521-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e521-105">描述</span><span class="sxs-lookup"><span data-stu-id="9e521-105">DESCRIPTION</span></span>
<span data-ttu-id="9e521-106">建立 StaticRoute 物件。</span><span class="sxs-lookup"><span data-stu-id="9e521-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="9e521-107">例子</span><span class="sxs-lookup"><span data-stu-id="9e521-107">EXAMPLES</span></span>

### <span data-ttu-id="9e521-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9e521-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="9e521-109">上述命令會建立一個 StaticRoute 物件，然後可以新加到 RoutingConfiguration 物件中。</span><span class="sxs-lookup"><span data-stu-id="9e521-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="9e521-110">參數</span><span class="sxs-lookup"><span data-stu-id="9e521-110">PARAMETERS</span></span>

### <span data-ttu-id="9e521-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e521-111">-DefaultProfile</span></span>
<span data-ttu-id="9e521-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e521-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e521-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9e521-113">-AddressPrefix</span></span>
<span data-ttu-id="9e521-114">位址首碼清單。</span><span class="sxs-lookup"><span data-stu-id="9e521-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="9e521-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e521-115">-Name</span></span>
<span data-ttu-id="9e521-116">路由名稱。</span><span class="sxs-lookup"><span data-stu-id="9e521-116">The route name.</span></span>

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

### <span data-ttu-id="9e521-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e521-117">-NextHopIpAddress</span></span>
<span data-ttu-id="9e521-118">下一個躍點 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="9e521-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="9e521-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e521-119">CommonParameters</span></span>
<span data-ttu-id="9e521-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9e521-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e521-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e521-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e521-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9e521-122">INPUTS</span></span>

### <span data-ttu-id="9e521-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9e521-123">System.String</span></span>

## <span data-ttu-id="9e521-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9e521-124">OUTPUTS</span></span>

### <span data-ttu-id="9e521-125">Microsoft.Azure.Commands.Network.models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="9e521-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="9e521-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9e521-126">NOTES</span></span>

## <span data-ttu-id="9e521-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e521-127">RELATED LINKS</span></span>

[<span data-ttu-id="9e521-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e521-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
