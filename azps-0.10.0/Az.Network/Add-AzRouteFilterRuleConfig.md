---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 910b432382eb24f6c5eaf77d3e0c7fe3dc547413
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794500"
---
# <span data-ttu-id="f4ec6-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4ec6-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="f4ec6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ec6-103">將路由篩選規則新增至路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="f4ec6-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4ec6-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ec6-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4ec6-105">DESCRIPTION</span></span>
<span data-ttu-id="f4ec6-106">Add-AzRouteFilterRuleConfig Cmdlet 會將路由篩選規則新增至 Azure 路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="f4ec6-107">示例</span><span class="sxs-lookup"><span data-stu-id="f4ec6-107">EXAMPLES</span></span>

### <span data-ttu-id="f4ec6-108">--------------------------範例1：將路由篩選規則新增至路由篩選器--------------------------</span><span class="sxs-lookup"><span data-stu-id="f4ec6-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="f4ec6-109">第一個命令會使用 Get-AzRouteFilter Cmdlet 來取得名為 routefilter01 的路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="f4ec6-110">該命令會將篩選儲存在 $RouteFilter 變數中。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="f4ec6-111">參數</span><span class="sxs-lookup"><span data-stu-id="f4ec6-111">PARAMETERS</span></span>

### <span data-ttu-id="f4ec6-112">-Access</span><span class="sxs-lookup"><span data-stu-id="f4ec6-112">-Access</span></span>
<span data-ttu-id="f4ec6-113">指定路由篩選規則的存取權，有效值為 [拒絕] 或 [允許]。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="f4ec6-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="f4ec6-114">-CommunityList</span></span>
<span data-ttu-id="f4ec6-115">路由篩選將篩選的群組值清單</span><span class="sxs-lookup"><span data-stu-id="f4ec6-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="f4ec6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ec6-116">-DefaultProfile</span></span>
<span data-ttu-id="f4ec6-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4ec6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f4ec6-118">-Force</span></span>
<span data-ttu-id="f4ec6-119">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="f4ec6-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="f4ec6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4ec6-120">-Name</span></span>
<span data-ttu-id="f4ec6-121">指定要新增至路由篩選器之路由篩選規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="f4ec6-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f4ec6-122">-RouteFilter</span></span>
<span data-ttu-id="f4ec6-123">指定此 Cmdlet 新增路由篩選規則的路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="f4ec6-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="f4ec6-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="f4ec6-125">指定路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="f4ec6-126">有效值為： [群組]</span><span class="sxs-lookup"><span data-stu-id="f4ec6-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="f4ec6-127">-確認</span><span class="sxs-lookup"><span data-stu-id="f4ec6-127">-Confirm</span></span>
<span data-ttu-id="f4ec6-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ec6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ec6-129">-WhatIf</span></span>
<span data-ttu-id="f4ec6-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4ec6-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ec6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ec6-132">CommonParameters</span></span>
<span data-ttu-id="f4ec6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ec6-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4ec6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ec6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f4ec6-135">INPUTS</span></span>

### <span data-ttu-id="f4ec6-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f4ec6-136">PSRouteFilter</span></span>
<span data-ttu-id="f4ec6-137">形參 "RouteFilter" 接受管線中 "PSRouteFilter" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f4ec6-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="f4ec6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f4ec6-138">OUTPUTS</span></span>

### <span data-ttu-id="f4ec6-139">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f4ec6-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f4ec6-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f4ec6-140">NOTES</span></span>
<span data-ttu-id="f4ec6-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="f4ec6-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f4ec6-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4ec6-142">RELATED LINKS</span></span>

[<span data-ttu-id="f4ec6-143">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4ec6-143">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f4ec6-144">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f4ec6-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="f4ec6-145">新-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="f4ec6-145">New-AzRouteFilterRuleConfigConfig</span></span>](./New-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="f4ec6-146">移除-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="f4ec6-146">Remove-AzRouteFilterRuleConfigConfig</span></span>](./Remove-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="f4ec6-147">Set-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="f4ec6-147">Set-AzRouteFilterRuleConfigConfig</span></span>](./Set-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="f4ec6-148">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f4ec6-148">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

