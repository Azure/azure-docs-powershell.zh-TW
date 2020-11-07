---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959190"
---
# <span data-ttu-id="e3fc9-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3fc9-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="e3fc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fc9-103">建立路由篩選器的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="e3fc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3fc9-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3fc9-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="e3fc9-106">New-AzRouteFilterRuleConfig Cmdlet 會針對 Azure 路由篩選建立路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="e3fc9-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3fc9-107">EXAMPLES</span></span>

### <span data-ttu-id="e3fc9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e3fc9-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="e3fc9-109">此命令會建立新的路由篩選規則，並將它儲存在變數 $rule 1 中。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="e3fc9-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3fc9-110">PARAMETERS</span></span>

### <span data-ttu-id="e3fc9-111">-Access</span><span class="sxs-lookup"><span data-stu-id="e3fc9-111">-Access</span></span>
<span data-ttu-id="e3fc9-112">路由篩選規則的存取權。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-112">Access for route filter rule.</span></span>
<span data-ttu-id="e3fc9-113">有效值為 [允許] 或 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="e3fc9-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="e3fc9-114">-CommunityList</span></span>
<span data-ttu-id="e3fc9-115">路由篩選將篩選的群組值清單</span><span class="sxs-lookup"><span data-stu-id="e3fc9-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="e3fc9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fc9-116">-DefaultProfile</span></span>
<span data-ttu-id="e3fc9-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3fc9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e3fc9-118">-Force</span></span>
<span data-ttu-id="e3fc9-119">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="e3fc9-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e3fc9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3fc9-120">-Name</span></span>
<span data-ttu-id="e3fc9-121">指定路由篩選規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="e3fc9-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="e3fc9-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="e3fc9-123">路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="e3fc9-124">有效值為： [群組]</span><span class="sxs-lookup"><span data-stu-id="e3fc9-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="e3fc9-125">-確認</span><span class="sxs-lookup"><span data-stu-id="e3fc9-125">-Confirm</span></span>
<span data-ttu-id="e3fc9-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3fc9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3fc9-127">-WhatIf</span></span>
<span data-ttu-id="e3fc9-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3fc9-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3fc9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fc9-130">CommonParameters</span></span>
<span data-ttu-id="e3fc9-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fc9-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3fc9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fc9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e3fc9-133">INPUTS</span></span>

### <span data-ttu-id="e3fc9-134">所有</span><span class="sxs-lookup"><span data-stu-id="e3fc9-134">None</span></span>

## <span data-ttu-id="e3fc9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e3fc9-135">OUTPUTS</span></span>

### <span data-ttu-id="e3fc9-136">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3fc9-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="e3fc9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e3fc9-137">NOTES</span></span>
<span data-ttu-id="e3fc9-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="e3fc9-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e3fc9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3fc9-139">RELATED LINKS</span></span>

[<span data-ttu-id="e3fc9-140">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3fc9-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e3fc9-141">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3fc9-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e3fc9-142">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3fc9-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e3fc9-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3fc9-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e3fc9-144">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e3fc9-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="e3fc9-145">新-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e3fc9-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="e3fc9-146">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e3fc9-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="e3fc9-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e3fc9-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
