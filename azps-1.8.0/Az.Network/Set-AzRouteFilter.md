---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 5222f6428bd7e57b71268465d60790869b12ef64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621419"
---
# <span data-ttu-id="56c3c-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="56c3c-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="56c3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="56c3c-103">更新路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="56c3c-103">Updates a route filter.</span></span>

## <span data-ttu-id="56c3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="56c3c-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56c3c-105">說明</span><span class="sxs-lookup"><span data-stu-id="56c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="56c3c-106">**AzApplicationGateway** Cmdlet 會更新路由篩選器</span><span class="sxs-lookup"><span data-stu-id="56c3c-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="56c3c-107">示例</span><span class="sxs-lookup"><span data-stu-id="56c3c-107">EXAMPLES</span></span>

### <span data-ttu-id="56c3c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="56c3c-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="56c3c-109">這個命令會使用 $rf 變數中的設定來更新路由篩選。</span><span class="sxs-lookup"><span data-stu-id="56c3c-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="56c3c-110">參數</span><span class="sxs-lookup"><span data-stu-id="56c3c-110">PARAMETERS</span></span>

### <span data-ttu-id="56c3c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56c3c-111">-AsJob</span></span>
<span data-ttu-id="56c3c-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="56c3c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56c3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c3c-113">-DefaultProfile</span></span>
<span data-ttu-id="56c3c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56c3c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56c3c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="56c3c-115">-Force</span></span>
<span data-ttu-id="56c3c-116">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="56c3c-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="56c3c-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="56c3c-117">-RouteFilter</span></span>
<span data-ttu-id="56c3c-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="56c3c-118">The RouteFilter</span></span>

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

### <span data-ttu-id="56c3c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="56c3c-119">-Confirm</span></span>
<span data-ttu-id="56c3c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="56c3c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56c3c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56c3c-121">-WhatIf</span></span>
<span data-ttu-id="56c3c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56c3c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56c3c-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56c3c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56c3c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c3c-124">CommonParameters</span></span>
<span data-ttu-id="56c3c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56c3c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c3c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="56c3c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c3c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="56c3c-127">INPUTS</span></span>

### <span data-ttu-id="56c3c-128">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="56c3c-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="56c3c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="56c3c-129">OUTPUTS</span></span>

### <span data-ttu-id="56c3c-130">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="56c3c-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="56c3c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="56c3c-131">NOTES</span></span>

## <span data-ttu-id="56c3c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="56c3c-132">RELATED LINKS</span></span>

[<span data-ttu-id="56c3c-133">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="56c3c-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="56c3c-134">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="56c3c-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="56c3c-135">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="56c3c-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="56c3c-136">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56c3c-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="56c3c-137">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56c3c-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="56c3c-138">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56c3c-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="56c3c-139">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56c3c-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="56c3c-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56c3c-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
