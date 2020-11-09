---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287860"
---
# <span data-ttu-id="32f8f-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32f8f-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="32f8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="32f8f-103">更新路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="32f8f-103">Updates a route filter.</span></span>

## <span data-ttu-id="32f8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="32f8f-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32f8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="32f8f-105">DESCRIPTION</span></span>
<span data-ttu-id="32f8f-106">**AzApplicationGateway** Cmdlet 會更新路由篩選器</span><span class="sxs-lookup"><span data-stu-id="32f8f-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="32f8f-107">示例</span><span class="sxs-lookup"><span data-stu-id="32f8f-107">EXAMPLES</span></span>

### <span data-ttu-id="32f8f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="32f8f-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="32f8f-109">這個命令會使用 $rf 變數中的設定來更新路由篩選。</span><span class="sxs-lookup"><span data-stu-id="32f8f-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="32f8f-110">參數</span><span class="sxs-lookup"><span data-stu-id="32f8f-110">PARAMETERS</span></span>

### <span data-ttu-id="32f8f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32f8f-111">-AsJob</span></span>
<span data-ttu-id="32f8f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="32f8f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32f8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f8f-113">-DefaultProfile</span></span>
<span data-ttu-id="32f8f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32f8f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32f8f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="32f8f-115">-Force</span></span>
<span data-ttu-id="32f8f-116">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="32f8f-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="32f8f-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="32f8f-117">-RouteFilter</span></span>
<span data-ttu-id="32f8f-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="32f8f-118">The RouteFilter</span></span>

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

### <span data-ttu-id="32f8f-119">-確認</span><span class="sxs-lookup"><span data-stu-id="32f8f-119">-Confirm</span></span>
<span data-ttu-id="32f8f-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="32f8f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32f8f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32f8f-121">-WhatIf</span></span>
<span data-ttu-id="32f8f-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32f8f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32f8f-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32f8f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32f8f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f8f-124">CommonParameters</span></span>
<span data-ttu-id="32f8f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32f8f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f8f-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32f8f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f8f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="32f8f-127">INPUTS</span></span>

### <span data-ttu-id="32f8f-128">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="32f8f-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="32f8f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="32f8f-129">OUTPUTS</span></span>

### <span data-ttu-id="32f8f-130">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="32f8f-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="32f8f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="32f8f-131">NOTES</span></span>

## <span data-ttu-id="32f8f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="32f8f-132">RELATED LINKS</span></span>

[<span data-ttu-id="32f8f-133">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32f8f-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="32f8f-134">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32f8f-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="32f8f-135">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32f8f-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="32f8f-136">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32f8f-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32f8f-137">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32f8f-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32f8f-138">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32f8f-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32f8f-139">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32f8f-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32f8f-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32f8f-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
