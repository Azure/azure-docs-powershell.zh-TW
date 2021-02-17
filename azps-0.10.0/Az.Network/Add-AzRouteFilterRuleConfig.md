---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: ded23a30c078cd1d474310d73d94717d050f6824
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399272"
---
# <span data-ttu-id="44ef4-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44ef4-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="44ef4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="44ef4-103">新增路由篩選規則至路由篩選。</span><span class="sxs-lookup"><span data-stu-id="44ef4-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="44ef4-104">語法</span><span class="sxs-lookup"><span data-stu-id="44ef4-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44ef4-105">描述</span><span class="sxs-lookup"><span data-stu-id="44ef4-105">DESCRIPTION</span></span>
<span data-ttu-id="44ef4-106">Cmdlet Add-AzRouteFilterRuleConfig新增路由篩選規則至 Azure 路由篩選。</span><span class="sxs-lookup"><span data-stu-id="44ef4-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="44ef4-107">例子</span><span class="sxs-lookup"><span data-stu-id="44ef4-107">EXAMPLES</span></span>

### <span data-ttu-id="44ef4-108">--------------------------範例 1：新增路由篩選規則至路由篩選--------------------------</span><span class="sxs-lookup"><span data-stu-id="44ef4-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="44ef4-109">第一個命令會使用 Get-AzRouteFilter Cmdlet，獲得名為 routefilter01 的路由篩選。</span><span class="sxs-lookup"><span data-stu-id="44ef4-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="44ef4-110">命令會儲存篩選$RouteFilter變數。</span><span class="sxs-lookup"><span data-stu-id="44ef4-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="44ef4-111">參數</span><span class="sxs-lookup"><span data-stu-id="44ef4-111">PARAMETERS</span></span>

### <span data-ttu-id="44ef4-112">-Access</span><span class="sxs-lookup"><span data-stu-id="44ef4-112">-Access</span></span>
<span data-ttu-id="44ef4-113">指定路由篩選規則的存取權，有效值為拒絕或允許。</span><span class="sxs-lookup"><span data-stu-id="44ef4-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef4-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="44ef4-114">-CommunityList</span></span>
<span data-ttu-id="44ef4-115">路由篩選篩選所篩選的社群值清單</span><span class="sxs-lookup"><span data-stu-id="44ef4-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ef4-116">-DefaultProfile</span></span>
<span data-ttu-id="44ef4-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44ef4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef4-118">-強制</span><span class="sxs-lookup"><span data-stu-id="44ef4-118">-Force</span></span>
<span data-ttu-id="44ef4-119">如果您想要過度使用資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="44ef4-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="44ef4-120">-Name</span></span>
<span data-ttu-id="44ef4-121">指定要新加入路由篩選的路由篩選規則名稱。</span><span class="sxs-lookup"><span data-stu-id="44ef4-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="44ef4-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="44ef4-122">-RouteFilter</span></span>
<span data-ttu-id="44ef4-123">指定此 Cmdlet 新增路由篩選規則的路由篩選。</span><span class="sxs-lookup"><span data-stu-id="44ef4-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44ef4-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="44ef4-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="44ef4-125">指定路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="44ef4-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="44ef4-126">有效的值為：社群</span><span class="sxs-lookup"><span data-stu-id="44ef4-126">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef4-127">-確認</span><span class="sxs-lookup"><span data-stu-id="44ef4-127">-Confirm</span></span>
<span data-ttu-id="44ef4-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="44ef4-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44ef4-129">-WhatIf</span></span>
<span data-ttu-id="44ef4-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="44ef4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44ef4-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="44ef4-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ef4-132">CommonParameters</span></span>
<span data-ttu-id="44ef4-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44ef4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ef4-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="44ef4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ef4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="44ef4-135">INPUTS</span></span>

### <span data-ttu-id="44ef4-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="44ef4-136">PSRouteFilter</span></span>
<span data-ttu-id="44ef4-137">參數 'RouteFilter' 接受來自管線之類型 'PSRouteFilter' 的值</span><span class="sxs-lookup"><span data-stu-id="44ef4-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="44ef4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="44ef4-138">OUTPUTS</span></span>

### <span data-ttu-id="44ef4-139">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="44ef4-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="44ef4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="44ef4-140">NOTES</span></span>
<span data-ttu-id="44ef4-141">關鍵字：azure、azurerm、arm、resource、management、manager、network、network、network</span><span class="sxs-lookup"><span data-stu-id="44ef4-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="44ef4-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="44ef4-142">RELATED LINKS</span></span>

[<span data-ttu-id="44ef4-143">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44ef4-143">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="44ef4-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="44ef4-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)




[<span data-ttu-id="44ef4-145">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="44ef4-145">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

