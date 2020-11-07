---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 5d83678d26804c97a0e21da4dcbff3f5af75d409
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790041"
---
# <span data-ttu-id="27271-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27271-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="27271-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27271-102">SYNOPSIS</span></span>
<span data-ttu-id="27271-103">在路由篩選中取得路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="27271-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="27271-104">句法</span><span class="sxs-lookup"><span data-stu-id="27271-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27271-105">說明</span><span class="sxs-lookup"><span data-stu-id="27271-105">DESCRIPTION</span></span>
<span data-ttu-id="27271-106">**AzRouteFilterRuleConfig** Cmdlet 會在路由篩選中取得路由篩選規則或路由篩選規則清單。</span><span class="sxs-lookup"><span data-stu-id="27271-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="27271-107">示例</span><span class="sxs-lookup"><span data-stu-id="27271-107">EXAMPLES</span></span>

### <span data-ttu-id="27271-108">範例1</span><span class="sxs-lookup"><span data-stu-id="27271-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="27271-109">第一個命令會取得名為 MyRouteFilter 的路由篩選，然後將它儲存在 $rf 的變數中。</span><span class="sxs-lookup"><span data-stu-id="27271-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="27271-110">第二個命令會取得名為 Rule01 與該路由篩選器相關聯的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="27271-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="27271-111">第三個命令會取得與該路由篩選器相關聯的路由篩選規則清單。</span><span class="sxs-lookup"><span data-stu-id="27271-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="27271-112">參數</span><span class="sxs-lookup"><span data-stu-id="27271-112">PARAMETERS</span></span>

### <span data-ttu-id="27271-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27271-113">-DefaultProfile</span></span>
<span data-ttu-id="27271-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27271-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27271-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="27271-115">-Name</span></span>
<span data-ttu-id="27271-116">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="27271-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="27271-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="27271-117">-RouteFilter</span></span>
<span data-ttu-id="27271-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="27271-118">The RouteFilter</span></span>

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

### <span data-ttu-id="27271-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27271-119">CommonParameters</span></span>
<span data-ttu-id="27271-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27271-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27271-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="27271-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27271-122">輸入</span><span class="sxs-lookup"><span data-stu-id="27271-122">INPUTS</span></span>

### <span data-ttu-id="27271-123">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="27271-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="27271-124">輸出</span><span class="sxs-lookup"><span data-stu-id="27271-124">OUTPUTS</span></span>

### <span data-ttu-id="27271-125">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="27271-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="27271-126">筆記</span><span class="sxs-lookup"><span data-stu-id="27271-126">NOTES</span></span>

## <span data-ttu-id="27271-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="27271-127">RELATED LINKS</span></span>

[<span data-ttu-id="27271-128">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27271-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="27271-129">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27271-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="27271-130">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27271-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="27271-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27271-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="27271-132">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="27271-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="27271-133">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="27271-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="27271-134">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="27271-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="27271-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="27271-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
