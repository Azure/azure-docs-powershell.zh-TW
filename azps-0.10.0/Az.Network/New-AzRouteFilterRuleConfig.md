---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 6f8943fb4e75c96a97ad2b7f128d671a8be7c906
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794242"
---
# <span data-ttu-id="c6407-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6407-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="c6407-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6407-102">SYNOPSIS</span></span>
<span data-ttu-id="c6407-103">建立路由篩選器的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="c6407-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="c6407-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6407-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6407-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6407-105">DESCRIPTION</span></span>
<span data-ttu-id="c6407-106">New-AzRouteFilterRuleConfig Cmdlet 會針對 Azure 路由篩選建立路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="c6407-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="c6407-107">示例</span><span class="sxs-lookup"><span data-stu-id="c6407-107">EXAMPLES</span></span>

### <span data-ttu-id="c6407-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c6407-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c6407-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="c6407-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c6407-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6407-110">PARAMETERS</span></span>

### <span data-ttu-id="c6407-111">-Access</span><span class="sxs-lookup"><span data-stu-id="c6407-111">-Access</span></span>
<span data-ttu-id="c6407-112">路由篩選規則的存取權。</span><span class="sxs-lookup"><span data-stu-id="c6407-112">Access for route filter rule.</span></span>
<span data-ttu-id="c6407-113">有效值為 [允許] 或 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="c6407-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6407-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="c6407-114">-CommunityList</span></span>
<span data-ttu-id="c6407-115">路由篩選將篩選的群組值清單</span><span class="sxs-lookup"><span data-stu-id="c6407-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="c6407-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6407-116">-DefaultProfile</span></span>
<span data-ttu-id="c6407-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6407-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6407-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c6407-118">-Force</span></span>
<span data-ttu-id="c6407-119">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="c6407-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6407-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6407-120">-Name</span></span>
<span data-ttu-id="c6407-121">指定路由篩選規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6407-121">Specifies a name for the route filter rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6407-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="c6407-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="c6407-123">路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="c6407-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="c6407-124">有效值為： [群組]</span><span class="sxs-lookup"><span data-stu-id="c6407-124">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6407-125">-確認</span><span class="sxs-lookup"><span data-stu-id="c6407-125">-Confirm</span></span>
<span data-ttu-id="c6407-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6407-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6407-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6407-127">-WhatIf</span></span>
<span data-ttu-id="c6407-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6407-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6407-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6407-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6407-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6407-130">CommonParameters</span></span>
<span data-ttu-id="c6407-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6407-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6407-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6407-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6407-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c6407-133">INPUTS</span></span>

## <span data-ttu-id="c6407-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c6407-134">OUTPUTS</span></span>

### <span data-ttu-id="c6407-135">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c6407-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="c6407-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c6407-136">NOTES</span></span>
<span data-ttu-id="c6407-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="c6407-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c6407-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6407-138">RELATED LINKS</span></span>

[<span data-ttu-id="c6407-139">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6407-139">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6407-140">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6407-140">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6407-141">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6407-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6407-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6407-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

