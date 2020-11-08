---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127480"
---
# <span data-ttu-id="6bc82-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6bc82-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="6bc82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6bc82-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc82-103">移除路由篩選。</span><span class="sxs-lookup"><span data-stu-id="6bc82-103">Removes a route filter.</span></span>

## <span data-ttu-id="6bc82-104">句法</span><span class="sxs-lookup"><span data-stu-id="6bc82-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bc82-105">說明</span><span class="sxs-lookup"><span data-stu-id="6bc82-105">DESCRIPTION</span></span>
<span data-ttu-id="6bc82-106">**AzRouteFilter** Cmdlet 會移除路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="6bc82-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="6bc82-107">示例</span><span class="sxs-lookup"><span data-stu-id="6bc82-107">EXAMPLES</span></span>

### <span data-ttu-id="6bc82-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6bc82-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6bc82-109">此命令會在名為 ResourceGroup01 的資源群組中移除名為 RouteFilter01 的路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="6bc82-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="6bc82-110">參數</span><span class="sxs-lookup"><span data-stu-id="6bc82-110">PARAMETERS</span></span>

### <span data-ttu-id="6bc82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc82-111">-DefaultProfile</span></span>
<span data-ttu-id="6bc82-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bc82-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bc82-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6bc82-113">-Force</span></span>
<span data-ttu-id="6bc82-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="6bc82-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6bc82-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6bc82-115">-Name</span></span>
<span data-ttu-id="6bc82-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6bc82-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc82-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bc82-117">-PassThru</span></span>
<span data-ttu-id="6bc82-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6bc82-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="6bc82-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bc82-119">-ResourceGroupName</span></span>
<span data-ttu-id="6bc82-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bc82-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc82-121">-確認</span><span class="sxs-lookup"><span data-stu-id="6bc82-121">-Confirm</span></span>
<span data-ttu-id="6bc82-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6bc82-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bc82-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bc82-123">-WhatIf</span></span>
<span data-ttu-id="6bc82-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6bc82-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bc82-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6bc82-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bc82-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc82-126">CommonParameters</span></span>
<span data-ttu-id="6bc82-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6bc82-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc82-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6bc82-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc82-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6bc82-129">INPUTS</span></span>

### <span data-ttu-id="6bc82-130">System.object</span><span class="sxs-lookup"><span data-stu-id="6bc82-130">System.String</span></span>

## <span data-ttu-id="6bc82-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6bc82-131">OUTPUTS</span></span>

### <span data-ttu-id="6bc82-132">System.object</span><span class="sxs-lookup"><span data-stu-id="6bc82-132">System.Boolean</span></span>

## <span data-ttu-id="6bc82-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6bc82-133">NOTES</span></span>

## <span data-ttu-id="6bc82-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bc82-134">RELATED LINKS</span></span>

[<span data-ttu-id="6bc82-135">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6bc82-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="6bc82-136">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6bc82-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="6bc82-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6bc82-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="6bc82-138">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bc82-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6bc82-139">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bc82-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6bc82-140">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bc82-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6bc82-141">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bc82-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6bc82-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bc82-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
