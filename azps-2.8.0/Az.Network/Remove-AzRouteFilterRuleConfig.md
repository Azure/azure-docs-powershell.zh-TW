---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: a7414690e1d0e1f5a6d8242af7b1d27490dcde93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790601"
---
# <span data-ttu-id="f1165-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1165-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="f1165-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1165-102">SYNOPSIS</span></span>
<span data-ttu-id="f1165-103">從路由篩選器移除路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="f1165-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="f1165-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1165-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1165-105">說明</span><span class="sxs-lookup"><span data-stu-id="f1165-105">DESCRIPTION</span></span>
<span data-ttu-id="f1165-106">**AzRouteFilterRuleConfig** Cmdlet 會從路由篩選中移除路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="f1165-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="f1165-107">示例</span><span class="sxs-lookup"><span data-stu-id="f1165-107">EXAMPLES</span></span>

### <span data-ttu-id="f1165-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f1165-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="f1165-109">第一個命令會取得屬於名為 ResourceGroup01 之資源群組的名為 RouteFilter01 的路由篩選器，並將它儲存在 $rf 變數中。</span><span class="sxs-lookup"><span data-stu-id="f1165-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="f1165-110">第二個命令會從 $rf 中儲存的路由篩選，移除名為 Rule01 的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="f1165-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="f1165-111">參數</span><span class="sxs-lookup"><span data-stu-id="f1165-111">PARAMETERS</span></span>

### <span data-ttu-id="f1165-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1165-112">-DefaultProfile</span></span>
<span data-ttu-id="f1165-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1165-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1165-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f1165-114">-Force</span></span>
<span data-ttu-id="f1165-115">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="f1165-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f1165-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1165-116">-Name</span></span>
<span data-ttu-id="f1165-117">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="f1165-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="f1165-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f1165-118">-RouteFilter</span></span>
<span data-ttu-id="f1165-119">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f1165-119">The RouteFilter</span></span>

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

### <span data-ttu-id="f1165-120">-確認</span><span class="sxs-lookup"><span data-stu-id="f1165-120">-Confirm</span></span>
<span data-ttu-id="f1165-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1165-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1165-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1165-122">-WhatIf</span></span>
<span data-ttu-id="f1165-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1165-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1165-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1165-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1165-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1165-125">CommonParameters</span></span>
<span data-ttu-id="f1165-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1165-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1165-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1165-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1165-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f1165-128">INPUTS</span></span>

### <span data-ttu-id="f1165-129">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f1165-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f1165-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f1165-130">OUTPUTS</span></span>

### <span data-ttu-id="f1165-131">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f1165-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="f1165-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f1165-132">NOTES</span></span>

## <span data-ttu-id="f1165-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1165-133">RELATED LINKS</span></span>

[<span data-ttu-id="f1165-134">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1165-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f1165-135">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1165-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f1165-136">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1165-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f1165-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1165-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f1165-138">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f1165-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="f1165-139">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f1165-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="f1165-140">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f1165-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="f1165-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f1165-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
