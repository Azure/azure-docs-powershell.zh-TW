---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 0c6fa8b973af2f2ab4a9c8547dddffda18eb15c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911881"
---
# <span data-ttu-id="32e2f-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32e2f-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="32e2f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="32e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="32e2f-103">更新路由篩選。</span><span class="sxs-lookup"><span data-stu-id="32e2f-103">Updates a route filter.</span></span>

## <span data-ttu-id="32e2f-104">語法</span><span class="sxs-lookup"><span data-stu-id="32e2f-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32e2f-105">描述</span><span class="sxs-lookup"><span data-stu-id="32e2f-105">DESCRIPTION</span></span>
<span data-ttu-id="32e2f-106">**Set-AzApplicationGateway** Cmdlet 會更新路由篩選</span><span class="sxs-lookup"><span data-stu-id="32e2f-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="32e2f-107">例子</span><span class="sxs-lookup"><span data-stu-id="32e2f-107">EXAMPLES</span></span>

### <span data-ttu-id="32e2f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="32e2f-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="32e2f-109">此命令會更新路由篩選，並包含 $rf 變數中的設定。</span><span class="sxs-lookup"><span data-stu-id="32e2f-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="32e2f-110">參數</span><span class="sxs-lookup"><span data-stu-id="32e2f-110">PARAMETERS</span></span>

### <span data-ttu-id="32e2f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32e2f-111">-AsJob</span></span>
<span data-ttu-id="32e2f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="32e2f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32e2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e2f-113">-DefaultProfile</span></span>
<span data-ttu-id="32e2f-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="32e2f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32e2f-115">-強制</span><span class="sxs-lookup"><span data-stu-id="32e2f-115">-Force</span></span>
<span data-ttu-id="32e2f-116">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="32e2f-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="32e2f-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="32e2f-117">-RouteFilter</span></span>
<span data-ttu-id="32e2f-118">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="32e2f-118">The RouteFilter</span></span>

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

### <span data-ttu-id="32e2f-119">-確認</span><span class="sxs-lookup"><span data-stu-id="32e2f-119">-Confirm</span></span>
<span data-ttu-id="32e2f-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="32e2f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32e2f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e2f-121">-WhatIf</span></span>
<span data-ttu-id="32e2f-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32e2f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32e2f-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32e2f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32e2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e2f-124">CommonParameters</span></span>
<span data-ttu-id="32e2f-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="32e2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e2f-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="32e2f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e2f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="32e2f-127">INPUTS</span></span>

### <span data-ttu-id="32e2f-128">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32e2f-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="32e2f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="32e2f-129">OUTPUTS</span></span>

### <span data-ttu-id="32e2f-130">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32e2f-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="32e2f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="32e2f-131">NOTES</span></span>

## <span data-ttu-id="32e2f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="32e2f-132">RELATED LINKS</span></span>

[<span data-ttu-id="32e2f-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32e2f-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="32e2f-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32e2f-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="32e2f-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32e2f-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="32e2f-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32e2f-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32e2f-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32e2f-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32e2f-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32e2f-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32e2f-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32e2f-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32e2f-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32e2f-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
