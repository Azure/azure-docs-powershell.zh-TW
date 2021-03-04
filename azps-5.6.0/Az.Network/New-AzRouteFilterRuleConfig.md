---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: dbd1564ceb4a4315f62f11712c73c56b46dcff7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903473"
---
# <span data-ttu-id="60634-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60634-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="60634-102">簡介</span><span class="sxs-lookup"><span data-stu-id="60634-102">SYNOPSIS</span></span>
<span data-ttu-id="60634-103">建立路由篩選的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="60634-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="60634-104">語法</span><span class="sxs-lookup"><span data-stu-id="60634-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60634-105">描述</span><span class="sxs-lookup"><span data-stu-id="60634-105">DESCRIPTION</span></span>
<span data-ttu-id="60634-106">Cmdlet New-AzRouteFilterRuleConfig建立 Azure 路由篩選的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="60634-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="60634-107">例子</span><span class="sxs-lookup"><span data-stu-id="60634-107">EXAMPLES</span></span>

### <span data-ttu-id="60634-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="60634-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="60634-109">該命令會建立新的路由篩選規則，並儲存在變數 $rule 1。</span><span class="sxs-lookup"><span data-stu-id="60634-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="60634-110">參數</span><span class="sxs-lookup"><span data-stu-id="60634-110">PARAMETERS</span></span>

### <span data-ttu-id="60634-111">-Access</span><span class="sxs-lookup"><span data-stu-id="60634-111">-Access</span></span>
<span data-ttu-id="60634-112">存取路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="60634-112">Access for route filter rule.</span></span>
<span data-ttu-id="60634-113">有效的值為允許或拒絕。</span><span class="sxs-lookup"><span data-stu-id="60634-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="60634-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="60634-114">-CommunityList</span></span>
<span data-ttu-id="60634-115">路由篩選篩選所篩選的社群值清單</span><span class="sxs-lookup"><span data-stu-id="60634-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="60634-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60634-116">-DefaultProfile</span></span>
<span data-ttu-id="60634-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="60634-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60634-118">-強制</span><span class="sxs-lookup"><span data-stu-id="60634-118">-Force</span></span>
<span data-ttu-id="60634-119">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="60634-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="60634-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="60634-120">-Name</span></span>
<span data-ttu-id="60634-121">指定路由篩選規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="60634-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="60634-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="60634-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="60634-123">路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="60634-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="60634-124">有效的值為：社群</span><span class="sxs-lookup"><span data-stu-id="60634-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="60634-125">-確認</span><span class="sxs-lookup"><span data-stu-id="60634-125">-Confirm</span></span>
<span data-ttu-id="60634-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="60634-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60634-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60634-127">-WhatIf</span></span>
<span data-ttu-id="60634-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60634-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60634-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60634-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60634-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60634-130">CommonParameters</span></span>
<span data-ttu-id="60634-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="60634-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60634-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="60634-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60634-133">輸入</span><span class="sxs-lookup"><span data-stu-id="60634-133">INPUTS</span></span>

### <span data-ttu-id="60634-134">沒有</span><span class="sxs-lookup"><span data-stu-id="60634-134">None</span></span>

## <span data-ttu-id="60634-135">輸出</span><span class="sxs-lookup"><span data-stu-id="60634-135">OUTPUTS</span></span>

### <span data-ttu-id="60634-136">Microsoft.Azure.Commands.Network.models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="60634-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="60634-137">筆記</span><span class="sxs-lookup"><span data-stu-id="60634-137">NOTES</span></span>
<span data-ttu-id="60634-138">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="60634-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="60634-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="60634-139">RELATED LINKS</span></span>

[<span data-ttu-id="60634-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60634-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="60634-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60634-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="60634-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60634-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="60634-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60634-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="60634-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="60634-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="60634-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="60634-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="60634-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="60634-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="60634-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="60634-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
