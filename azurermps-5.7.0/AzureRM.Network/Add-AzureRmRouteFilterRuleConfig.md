---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 5daf0c5f764a095906e31167d6ddbc764ae68d19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451440"
---
# <span data-ttu-id="c5f0a-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5f0a-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="c5f0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f0a-103">將路由篩選規則新增至路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5f0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5f0a-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5f0a-105">說明</span><span class="sxs-lookup"><span data-stu-id="c5f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="c5f0a-106">Add-AzureRmRouteFilterRuleConfig Cmdlet 會將路由篩選規則新增至 Azure 路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="c5f0a-107">示例</span><span class="sxs-lookup"><span data-stu-id="c5f0a-107">EXAMPLES</span></span>

### <span data-ttu-id="c5f0a-108">--------------------------範例1：將路由篩選規則新增至路由篩選器--------------------------</span><span class="sxs-lookup"><span data-stu-id="c5f0a-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="c5f0a-109">第一個命令會使用 Get-AzureRmRouteFilter Cmdlet 來取得名為 routefilter01 的路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="c5f0a-110">該命令會將篩選儲存在 $RouteFilter 變數中。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="c5f0a-111">參數</span><span class="sxs-lookup"><span data-stu-id="c5f0a-111">PARAMETERS</span></span>

### <span data-ttu-id="c5f0a-112">-Access</span><span class="sxs-lookup"><span data-stu-id="c5f0a-112">-Access</span></span>
<span data-ttu-id="c5f0a-113">指定路由篩選規則的存取權，有效值為 [拒絕] 或 [允許]。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="c5f0a-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="c5f0a-114">-CommunityList</span></span>
<span data-ttu-id="c5f0a-115">路由篩選將篩選的群組值清單</span><span class="sxs-lookup"><span data-stu-id="c5f0a-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="c5f0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f0a-116">-DefaultProfile</span></span>
<span data-ttu-id="c5f0a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5f0a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c5f0a-118">-Force</span></span>
<span data-ttu-id="c5f0a-119">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="c5f0a-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="c5f0a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5f0a-120">-Name</span></span>
<span data-ttu-id="c5f0a-121">指定要新增至路由篩選器之路由篩選規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="c5f0a-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c5f0a-122">-RouteFilter</span></span>
<span data-ttu-id="c5f0a-123">指定此 Cmdlet 新增路由篩選規則的路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="c5f0a-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="c5f0a-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="c5f0a-125">指定路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="c5f0a-126">有效值為： [群組]</span><span class="sxs-lookup"><span data-stu-id="c5f0a-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="c5f0a-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c5f0a-127">-Confirm</span></span>
<span data-ttu-id="c5f0a-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5f0a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5f0a-129">-WhatIf</span></span>
<span data-ttu-id="c5f0a-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5f0a-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5f0a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f0a-132">CommonParameters</span></span>
<span data-ttu-id="c5f0a-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f0a-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5f0a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f0a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c5f0a-135">INPUTS</span></span>

### <span data-ttu-id="c5f0a-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c5f0a-136">PSRouteFilter</span></span>
<span data-ttu-id="c5f0a-137">形參 "RouteFilter" 接受管線中 "PSRouteFilter" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c5f0a-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="c5f0a-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c5f0a-138">OUTPUTS</span></span>

### <span data-ttu-id="c5f0a-139">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c5f0a-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c5f0a-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c5f0a-140">NOTES</span></span>
<span data-ttu-id="c5f0a-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="c5f0a-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c5f0a-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5f0a-142">RELATED LINKS</span></span>

[<span data-ttu-id="c5f0a-143">AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5f0a-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="c5f0a-144">AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c5f0a-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="c5f0a-145">新-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="c5f0a-145">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="c5f0a-146">移除-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="c5f0a-146">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="c5f0a-147">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="c5f0a-147">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="c5f0a-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c5f0a-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

