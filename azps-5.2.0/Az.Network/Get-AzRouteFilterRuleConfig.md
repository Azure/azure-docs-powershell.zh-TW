---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284276"
---
# <span data-ttu-id="75702-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75702-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="75702-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75702-102">SYNOPSIS</span></span>
<span data-ttu-id="75702-103">在路由篩選中取得路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="75702-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="75702-104">句法</span><span class="sxs-lookup"><span data-stu-id="75702-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75702-105">說明</span><span class="sxs-lookup"><span data-stu-id="75702-105">DESCRIPTION</span></span>
<span data-ttu-id="75702-106">**AzRouteFilterRuleConfig** Cmdlet 會在路由篩選中取得路由篩選規則或路由篩選規則清單。</span><span class="sxs-lookup"><span data-stu-id="75702-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="75702-107">示例</span><span class="sxs-lookup"><span data-stu-id="75702-107">EXAMPLES</span></span>

### <span data-ttu-id="75702-108">範例1</span><span class="sxs-lookup"><span data-stu-id="75702-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="75702-109">第一個命令會取得名為 MyRouteFilter 的路由篩選，然後將它儲存在 $rf 的變數中。</span><span class="sxs-lookup"><span data-stu-id="75702-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="75702-110">第二個命令會取得名為 Rule01 與該路由篩選器相關聯的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="75702-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="75702-111">第三個命令會取得與該路由篩選器相關聯的路由篩選規則清單。</span><span class="sxs-lookup"><span data-stu-id="75702-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="75702-112">參數</span><span class="sxs-lookup"><span data-stu-id="75702-112">PARAMETERS</span></span>

### <span data-ttu-id="75702-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75702-113">-DefaultProfile</span></span>
<span data-ttu-id="75702-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75702-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75702-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="75702-115">-Name</span></span>
<span data-ttu-id="75702-116">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="75702-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="75702-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="75702-117">-RouteFilter</span></span>
<span data-ttu-id="75702-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="75702-118">The RouteFilter</span></span>

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

### <span data-ttu-id="75702-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75702-119">CommonParameters</span></span>
<span data-ttu-id="75702-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75702-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75702-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="75702-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75702-122">輸入</span><span class="sxs-lookup"><span data-stu-id="75702-122">INPUTS</span></span>

### <span data-ttu-id="75702-123">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="75702-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="75702-124">輸出</span><span class="sxs-lookup"><span data-stu-id="75702-124">OUTPUTS</span></span>

### <span data-ttu-id="75702-125">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="75702-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="75702-126">筆記</span><span class="sxs-lookup"><span data-stu-id="75702-126">NOTES</span></span>

## <span data-ttu-id="75702-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="75702-127">RELATED LINKS</span></span>

[<span data-ttu-id="75702-128">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75702-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="75702-129">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75702-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="75702-130">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75702-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="75702-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75702-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="75702-132">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="75702-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="75702-133">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="75702-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="75702-134">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="75702-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="75702-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="75702-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
