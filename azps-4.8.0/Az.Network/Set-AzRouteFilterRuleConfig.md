---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135508"
---
# <span data-ttu-id="b0f50-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b0f50-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b0f50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0f50-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f50-103">修改路由篩選的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="b0f50-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="b0f50-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0f50-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0f50-105">說明</span><span class="sxs-lookup"><span data-stu-id="b0f50-105">DESCRIPTION</span></span>
<span data-ttu-id="b0f50-106">**AzRouteFilterRuleConfig** Cmdlet 會修改路由篩選的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="b0f50-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="b0f50-107">示例</span><span class="sxs-lookup"><span data-stu-id="b0f50-107">EXAMPLES</span></span>

### <span data-ttu-id="b0f50-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b0f50-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="b0f50-109">第一個命令會取得名為 RouteFilter01 的路由篩選，並將它儲存在 $rf 變數中。</span><span class="sxs-lookup"><span data-stu-id="b0f50-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="b0f50-110">第二個命令會修改名為 Rule01 的路由篩選規則，並將更新的路由篩選器儲存在 $rf 變數中。</span><span class="sxs-lookup"><span data-stu-id="b0f50-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="b0f50-111">第三個命令會儲存更新的路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="b0f50-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="b0f50-112">參數</span><span class="sxs-lookup"><span data-stu-id="b0f50-112">PARAMETERS</span></span>

### <span data-ttu-id="b0f50-113">-Access</span><span class="sxs-lookup"><span data-stu-id="b0f50-113">-Access</span></span>
<span data-ttu-id="b0f50-114">規則的存取類型。</span><span class="sxs-lookup"><span data-stu-id="b0f50-114">The access type of the rule.</span></span>
<span data-ttu-id="b0f50-115">可能的值為： "Allow"，"Deny"</span><span class="sxs-lookup"><span data-stu-id="b0f50-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="b0f50-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="b0f50-116">-CommunityList</span></span>
<span data-ttu-id="b0f50-117">路由篩選將篩選的群組值清單</span><span class="sxs-lookup"><span data-stu-id="b0f50-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="b0f50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f50-118">-DefaultProfile</span></span>
<span data-ttu-id="b0f50-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0f50-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0f50-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b0f50-120">-Force</span></span>
<span data-ttu-id="b0f50-121">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="b0f50-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b0f50-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0f50-122">-Name</span></span>
<span data-ttu-id="b0f50-123">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="b0f50-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="b0f50-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b0f50-124">-RouteFilter</span></span>
<span data-ttu-id="b0f50-125">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b0f50-125">The RouteFilter</span></span>

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

### <span data-ttu-id="b0f50-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="b0f50-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="b0f50-127">規則的路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="b0f50-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="b0f50-128">可能的值為： "社團"</span><span class="sxs-lookup"><span data-stu-id="b0f50-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="b0f50-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b0f50-129">-Confirm</span></span>
<span data-ttu-id="b0f50-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b0f50-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0f50-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0f50-131">-WhatIf</span></span>
<span data-ttu-id="b0f50-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0f50-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0f50-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0f50-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0f50-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f50-134">CommonParameters</span></span>
<span data-ttu-id="b0f50-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0f50-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f50-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0f50-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f50-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b0f50-137">INPUTS</span></span>

### <span data-ttu-id="b0f50-138">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b0f50-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b0f50-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b0f50-139">OUTPUTS</span></span>

### <span data-ttu-id="b0f50-140">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b0f50-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b0f50-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b0f50-141">NOTES</span></span>

## <span data-ttu-id="b0f50-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0f50-142">RELATED LINKS</span></span>

[<span data-ttu-id="b0f50-143">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b0f50-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b0f50-144">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b0f50-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b0f50-145">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b0f50-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b0f50-146">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b0f50-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b0f50-147">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b0f50-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="b0f50-148">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b0f50-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="b0f50-149">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b0f50-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="b0f50-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b0f50-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)