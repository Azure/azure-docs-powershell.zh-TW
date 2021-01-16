---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: e596ea3092cd5fda045c20f80c9208015b57a42d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288663"
---
# <span data-ttu-id="c4bcf-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4bcf-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="c4bcf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bcf-103">從路由篩選器移除路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="c4bcf-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="c4bcf-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4bcf-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4bcf-105">說明</span><span class="sxs-lookup"><span data-stu-id="c4bcf-105">DESCRIPTION</span></span>
<span data-ttu-id="c4bcf-106">**AzRouteFilterRuleConfig** Cmdlet 會從路由篩選中移除路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="c4bcf-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="c4bcf-107">示例</span><span class="sxs-lookup"><span data-stu-id="c4bcf-107">EXAMPLES</span></span>

### <span data-ttu-id="c4bcf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c4bcf-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="c4bcf-109">第一個命令會取得屬於名為 ResourceGroup01 之資源群組的名為 RouteFilter01 的路由篩選器，並將它儲存在 $rf 變數中。</span><span class="sxs-lookup"><span data-stu-id="c4bcf-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="c4bcf-110">第二個命令會從 $rf 中儲存的路由篩選，移除名為 Rule01 的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="c4bcf-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="c4bcf-111">參數</span><span class="sxs-lookup"><span data-stu-id="c4bcf-111">PARAMETERS</span></span>

### <span data-ttu-id="c4bcf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bcf-112">-DefaultProfile</span></span>
<span data-ttu-id="c4bcf-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4bcf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4bcf-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c4bcf-114">-Force</span></span>
<span data-ttu-id="c4bcf-115">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="c4bcf-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c4bcf-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4bcf-116">-Name</span></span>
<span data-ttu-id="c4bcf-117">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="c4bcf-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="c4bcf-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c4bcf-118">-RouteFilter</span></span>
<span data-ttu-id="c4bcf-119">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c4bcf-119">The RouteFilter</span></span>

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

### <span data-ttu-id="c4bcf-120">-確認</span><span class="sxs-lookup"><span data-stu-id="c4bcf-120">-Confirm</span></span>
<span data-ttu-id="c4bcf-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4bcf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4bcf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4bcf-122">-WhatIf</span></span>
<span data-ttu-id="c4bcf-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4bcf-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4bcf-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4bcf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4bcf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bcf-125">CommonParameters</span></span>
<span data-ttu-id="c4bcf-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4bcf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bcf-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4bcf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bcf-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c4bcf-128">INPUTS</span></span>

### <span data-ttu-id="c4bcf-129">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c4bcf-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c4bcf-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c4bcf-130">OUTPUTS</span></span>

### <span data-ttu-id="c4bcf-131">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c4bcf-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="c4bcf-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c4bcf-132">NOTES</span></span>

## <span data-ttu-id="c4bcf-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4bcf-133">RELATED LINKS</span></span>

[<span data-ttu-id="c4bcf-134">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4bcf-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c4bcf-135">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4bcf-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c4bcf-136">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4bcf-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c4bcf-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4bcf-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c4bcf-138">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c4bcf-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="c4bcf-139">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c4bcf-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="c4bcf-140">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c4bcf-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="c4bcf-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c4bcf-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
