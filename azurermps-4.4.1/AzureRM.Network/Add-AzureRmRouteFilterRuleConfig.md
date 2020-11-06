---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3cd01d2e9bb3673e2c0e42ea43418c9601796a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453407"
---
# <span data-ttu-id="34647-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34647-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="34647-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34647-102">SYNOPSIS</span></span>
<span data-ttu-id="34647-103">將路由篩選規則新增至路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="34647-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34647-104">句法</span><span class="sxs-lookup"><span data-stu-id="34647-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34647-105">說明</span><span class="sxs-lookup"><span data-stu-id="34647-105">DESCRIPTION</span></span>
<span data-ttu-id="34647-106">Add-AzureRmRouteFilterRuleConfig Cmdlet 會將路由篩選規則新增至 Azure 路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="34647-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="34647-107">示例</span><span class="sxs-lookup"><span data-stu-id="34647-107">EXAMPLES</span></span>

### <span data-ttu-id="34647-108">--------------------------範例1：將路由篩選規則新增至路由篩選器--------------------------</span><span class="sxs-lookup"><span data-stu-id="34647-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
<span data-ttu-id="34647-109">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="34647-109">@{paragraph=PS C:\\\>}</span></span>















```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="34647-110">第一個命令會使用 Get-AzureRmRouteFilter Cmdlet 來取得名為 routefilter01 的路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="34647-110">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="34647-111">該命令會將篩選儲存在 $RouteFilter 變數中。</span><span class="sxs-lookup"><span data-stu-id="34647-111">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="34647-112">參數</span><span class="sxs-lookup"><span data-stu-id="34647-112">PARAMETERS</span></span>

### <span data-ttu-id="34647-113">-Access</span><span class="sxs-lookup"><span data-stu-id="34647-113">-Access</span></span>
<span data-ttu-id="34647-114">指定路由篩選規則的存取權，有效值為 [拒絕] 或 [允許]。</span><span class="sxs-lookup"><span data-stu-id="34647-114">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="34647-115">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="34647-115">-CommunityList</span></span>
<span data-ttu-id="34647-116">路由篩選將篩選的群組值清單</span><span class="sxs-lookup"><span data-stu-id="34647-116">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="34647-117">-Force</span><span class="sxs-lookup"><span data-stu-id="34647-117">-Force</span></span>
<span data-ttu-id="34647-118">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="34647-118">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="34647-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="34647-119">-Name</span></span>
<span data-ttu-id="34647-120">指定要新增至路由篩選器之路由篩選規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="34647-120">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="34647-121">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="34647-121">-RouteFilter</span></span>
<span data-ttu-id="34647-122">指定此 Cmdlet 新增路由篩選規則的路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="34647-122">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="34647-123">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="34647-123">-RouteFilterRuleType</span></span>
<span data-ttu-id="34647-124">指定路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="34647-124">Specifies the route filter rule type.</span></span>
<span data-ttu-id="34647-125">有效值為： [群組]</span><span class="sxs-lookup"><span data-stu-id="34647-125">Valid values are: Community</span></span>

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

### <span data-ttu-id="34647-126">-確認</span><span class="sxs-lookup"><span data-stu-id="34647-126">-Confirm</span></span>
<span data-ttu-id="34647-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="34647-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34647-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34647-128">-WhatIf</span></span>
<span data-ttu-id="34647-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="34647-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34647-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34647-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34647-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34647-131">-DefaultProfile</span></span>
<span data-ttu-id="34647-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34647-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34647-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34647-133">CommonParameters</span></span>
<span data-ttu-id="34647-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34647-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34647-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="34647-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34647-136">輸入</span><span class="sxs-lookup"><span data-stu-id="34647-136">INPUTS</span></span>

### <span data-ttu-id="34647-137">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="34647-137">PSRouteFilter</span></span>
<span data-ttu-id="34647-138">形參 "RouteFilter" 接受管線中 "PSRouteFilter" 類型的值</span><span class="sxs-lookup"><span data-stu-id="34647-138">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="34647-139">輸出</span><span class="sxs-lookup"><span data-stu-id="34647-139">OUTPUTS</span></span>

### <span data-ttu-id="34647-140">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="34647-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="34647-141">筆記</span><span class="sxs-lookup"><span data-stu-id="34647-141">NOTES</span></span>
<span data-ttu-id="34647-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="34647-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="34647-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="34647-143">RELATED LINKS</span></span>

[<span data-ttu-id="34647-144">AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34647-144">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="34647-145">AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="34647-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="34647-146">新-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="34647-146">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="34647-147">移除-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="34647-147">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="34647-148">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="34647-148">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="34647-149">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="34647-149">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

