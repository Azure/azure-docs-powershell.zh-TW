---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 0ed7233cda87c376707e0a5b5682a61a179550d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902442"
---
# <span data-ttu-id="2492c-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2492c-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="2492c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2492c-102">SYNOPSIS</span></span>
<span data-ttu-id="2492c-103">在路由篩選中獲得路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="2492c-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="2492c-104">語法</span><span class="sxs-lookup"><span data-stu-id="2492c-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2492c-105">描述</span><span class="sxs-lookup"><span data-stu-id="2492c-105">DESCRIPTION</span></span>
<span data-ttu-id="2492c-106">**Get-AzRouteFilterRuleConfig** Cmdlet 會取得路由篩選規則或路由篩選篩選規則的清單。</span><span class="sxs-lookup"><span data-stu-id="2492c-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="2492c-107">例子</span><span class="sxs-lookup"><span data-stu-id="2492c-107">EXAMPLES</span></span>

### <span data-ttu-id="2492c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2492c-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="2492c-109">第一個命令會獲得名為 MyRouteFilter 的路由篩選，然後將它儲存在變數 $rf。</span><span class="sxs-lookup"><span data-stu-id="2492c-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="2492c-110">第二個命令會獲得名為 Rule01 的路由篩選規則，該規則與該路由篩選相關聯。</span><span class="sxs-lookup"><span data-stu-id="2492c-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="2492c-111">第三個命令會獲得與該路由篩選相關聯的路由篩選規則清單。</span><span class="sxs-lookup"><span data-stu-id="2492c-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="2492c-112">參數</span><span class="sxs-lookup"><span data-stu-id="2492c-112">PARAMETERS</span></span>

### <span data-ttu-id="2492c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2492c-113">-DefaultProfile</span></span>
<span data-ttu-id="2492c-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2492c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2492c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2492c-115">-Name</span></span>
<span data-ttu-id="2492c-116">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="2492c-116">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2492c-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2492c-117">-RouteFilter</span></span>
<span data-ttu-id="2492c-118">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2492c-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2492c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2492c-119">CommonParameters</span></span>
<span data-ttu-id="2492c-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2492c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2492c-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2492c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2492c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2492c-122">INPUTS</span></span>

### <span data-ttu-id="2492c-123">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2492c-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2492c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2492c-124">OUTPUTS</span></span>

### <span data-ttu-id="2492c-125">Microsoft.Azure.Commands.Network.models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="2492c-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="2492c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2492c-126">NOTES</span></span>

## <span data-ttu-id="2492c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2492c-127">RELATED LINKS</span></span>

[<span data-ttu-id="2492c-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2492c-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2492c-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2492c-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2492c-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2492c-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2492c-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2492c-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2492c-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2492c-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="2492c-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2492c-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="2492c-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2492c-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="2492c-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2492c-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
