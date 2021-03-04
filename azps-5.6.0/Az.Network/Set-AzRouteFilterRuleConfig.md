---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: a58a6216d49539d4fc40f9c9131a335f7a31b87f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911878"
---
# <span data-ttu-id="4eb7a-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4eb7a-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="4eb7a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4eb7a-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb7a-103">修改路由篩選的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="4eb7a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4eb7a-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb7a-105">描述</span><span class="sxs-lookup"><span data-stu-id="4eb7a-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb7a-106">**Set-AzRouteFilterRuleConfig** Cmdlet 會修改路由篩選的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="4eb7a-107">例子</span><span class="sxs-lookup"><span data-stu-id="4eb7a-107">EXAMPLES</span></span>

### <span data-ttu-id="4eb7a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4eb7a-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="4eb7a-109">第一個命令會獲得名為 RouteFilter01 的路由篩選，並儲存在 $rf 變數中。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="4eb7a-110">第二個命令會修改名為 Rule01 的路由篩選規則，並儲存更新的路由篩選$rf變數。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="4eb7a-111">第三個命令會保存更新的路由篩選。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="4eb7a-112">參數</span><span class="sxs-lookup"><span data-stu-id="4eb7a-112">PARAMETERS</span></span>

### <span data-ttu-id="4eb7a-113">-Access</span><span class="sxs-lookup"><span data-stu-id="4eb7a-113">-Access</span></span>
<span data-ttu-id="4eb7a-114">規則的存取類型。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-114">The access type of the rule.</span></span>
<span data-ttu-id="4eb7a-115">可能的值為：'允許'、'拒絕'</span><span class="sxs-lookup"><span data-stu-id="4eb7a-115">Possible values are: 'Allow', 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb7a-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="4eb7a-116">-CommunityList</span></span>
<span data-ttu-id="4eb7a-117">路由篩選篩選所篩選的社群值清單</span><span class="sxs-lookup"><span data-stu-id="4eb7a-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="4eb7a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb7a-118">-DefaultProfile</span></span>
<span data-ttu-id="4eb7a-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eb7a-120">-強制</span><span class="sxs-lookup"><span data-stu-id="4eb7a-120">-Force</span></span>
<span data-ttu-id="4eb7a-121">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="4eb7a-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4eb7a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4eb7a-122">-Name</span></span>
<span data-ttu-id="4eb7a-123">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="4eb7a-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="4eb7a-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4eb7a-124">-RouteFilter</span></span>
<span data-ttu-id="4eb7a-125">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4eb7a-125">The RouteFilter</span></span>

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

### <span data-ttu-id="4eb7a-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="4eb7a-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="4eb7a-127">規則的路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="4eb7a-128">可能的值為：'社群'</span><span class="sxs-lookup"><span data-stu-id="4eb7a-128">Possible values are: 'Community'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb7a-129">-確認</span><span class="sxs-lookup"><span data-stu-id="4eb7a-129">-Confirm</span></span>
<span data-ttu-id="4eb7a-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb7a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb7a-131">-WhatIf</span></span>
<span data-ttu-id="4eb7a-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4eb7a-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb7a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb7a-134">CommonParameters</span></span>
<span data-ttu-id="4eb7a-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb7a-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4eb7a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb7a-137">輸入</span><span class="sxs-lookup"><span data-stu-id="4eb7a-137">INPUTS</span></span>

### <span data-ttu-id="4eb7a-138">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4eb7a-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4eb7a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="4eb7a-139">OUTPUTS</span></span>

### <span data-ttu-id="4eb7a-140">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4eb7a-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4eb7a-141">筆記</span><span class="sxs-lookup"><span data-stu-id="4eb7a-141">NOTES</span></span>

## <span data-ttu-id="4eb7a-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="4eb7a-142">RELATED LINKS</span></span>

[<span data-ttu-id="4eb7a-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4eb7a-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4eb7a-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4eb7a-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4eb7a-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4eb7a-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4eb7a-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4eb7a-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4eb7a-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4eb7a-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="4eb7a-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4eb7a-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="4eb7a-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4eb7a-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="4eb7a-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4eb7a-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
