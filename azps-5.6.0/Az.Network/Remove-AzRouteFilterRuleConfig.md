---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 2212ffb43f646e49a4552713b6408091dd985aae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913369"
---
# <span data-ttu-id="33711-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33711-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="33711-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33711-102">SYNOPSIS</span></span>
<span data-ttu-id="33711-103">從路由篩選移除路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="33711-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="33711-104">語法</span><span class="sxs-lookup"><span data-stu-id="33711-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33711-105">描述</span><span class="sxs-lookup"><span data-stu-id="33711-105">DESCRIPTION</span></span>
<span data-ttu-id="33711-106">**Remove-AzRouteFilterRuleConfig** Cmdlet 會從路由篩選移除路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="33711-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="33711-107">例子</span><span class="sxs-lookup"><span data-stu-id="33711-107">EXAMPLES</span></span>

### <span data-ttu-id="33711-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="33711-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="33711-109">第一個命令會獲得名為 RouteFilter01 的路由篩選，該路由篩選屬於名為 ResourceGroup01 的資源群組，並儲存在 $rf 變數中。</span><span class="sxs-lookup"><span data-stu-id="33711-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="33711-110">第二個命令會從儲存在該位置的路由篩選移除名為 Rule01 的路由篩選$rf。</span><span class="sxs-lookup"><span data-stu-id="33711-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="33711-111">參數</span><span class="sxs-lookup"><span data-stu-id="33711-111">PARAMETERS</span></span>

### <span data-ttu-id="33711-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33711-112">-DefaultProfile</span></span>
<span data-ttu-id="33711-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="33711-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33711-114">-強制</span><span class="sxs-lookup"><span data-stu-id="33711-114">-Force</span></span>
<span data-ttu-id="33711-115">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="33711-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33711-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="33711-116">-Name</span></span>
<span data-ttu-id="33711-117">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="33711-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="33711-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="33711-118">-RouteFilter</span></span>
<span data-ttu-id="33711-119">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="33711-119">The RouteFilter</span></span>

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

### <span data-ttu-id="33711-120">-確認</span><span class="sxs-lookup"><span data-stu-id="33711-120">-Confirm</span></span>
<span data-ttu-id="33711-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="33711-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33711-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33711-122">-WhatIf</span></span>
<span data-ttu-id="33711-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33711-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33711-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33711-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33711-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33711-125">CommonParameters</span></span>
<span data-ttu-id="33711-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33711-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33711-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="33711-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33711-128">輸入</span><span class="sxs-lookup"><span data-stu-id="33711-128">INPUTS</span></span>

### <span data-ttu-id="33711-129">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="33711-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="33711-130">輸出</span><span class="sxs-lookup"><span data-stu-id="33711-130">OUTPUTS</span></span>

### <span data-ttu-id="33711-131">Microsoft.Azure.Commands.Network.models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="33711-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="33711-132">筆記</span><span class="sxs-lookup"><span data-stu-id="33711-132">NOTES</span></span>

## <span data-ttu-id="33711-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="33711-133">RELATED LINKS</span></span>

[<span data-ttu-id="33711-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33711-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="33711-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33711-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="33711-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33711-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="33711-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33711-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="33711-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="33711-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="33711-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="33711-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="33711-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="33711-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="33711-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="33711-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
