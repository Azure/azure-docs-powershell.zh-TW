---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 2309d49dcd91ddefbcbe0e40379a759d50d5ba2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802026"
---
# <span data-ttu-id="497f4-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="497f4-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="497f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="497f4-102">SYNOPSIS</span></span>
<span data-ttu-id="497f4-103">建立路由篩選器的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="497f4-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="497f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="497f4-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="497f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="497f4-105">DESCRIPTION</span></span>
<span data-ttu-id="497f4-106">New-AzureRmRouteFilterRuleConfig Cmdlet 會針對 Azure 路由篩選建立路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="497f4-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="497f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="497f4-107">EXAMPLES</span></span>

### <span data-ttu-id="497f4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="497f4-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="497f4-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="497f4-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="497f4-110">參數</span><span class="sxs-lookup"><span data-stu-id="497f4-110">PARAMETERS</span></span>

### <span data-ttu-id="497f4-111">-Access</span><span class="sxs-lookup"><span data-stu-id="497f4-111">-Access</span></span>
<span data-ttu-id="497f4-112">路由篩選規則的存取權。</span><span class="sxs-lookup"><span data-stu-id="497f4-112">Access for route filter rule.</span></span>
<span data-ttu-id="497f4-113">有效值為 [允許] 或 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="497f4-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="497f4-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="497f4-114">-CommunityList</span></span>
<span data-ttu-id="497f4-115">路由篩選將篩選的群組值清單</span><span class="sxs-lookup"><span data-stu-id="497f4-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="497f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497f4-116">-DefaultProfile</span></span>
<span data-ttu-id="497f4-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="497f4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="497f4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="497f4-118">-Force</span></span>
<span data-ttu-id="497f4-119">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="497f4-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="497f4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="497f4-120">-Name</span></span>
<span data-ttu-id="497f4-121">指定路由篩選規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="497f4-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="497f4-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="497f4-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="497f4-123">路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="497f4-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="497f4-124">有效值為： [群組]</span><span class="sxs-lookup"><span data-stu-id="497f4-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="497f4-125">-確認</span><span class="sxs-lookup"><span data-stu-id="497f4-125">-Confirm</span></span>
<span data-ttu-id="497f4-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="497f4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="497f4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="497f4-127">-WhatIf</span></span>
<span data-ttu-id="497f4-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="497f4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="497f4-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="497f4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="497f4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497f4-130">CommonParameters</span></span>
<span data-ttu-id="497f4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="497f4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497f4-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="497f4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497f4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="497f4-133">INPUTS</span></span>

## <span data-ttu-id="497f4-134">輸出</span><span class="sxs-lookup"><span data-stu-id="497f4-134">OUTPUTS</span></span>

### <span data-ttu-id="497f4-135">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="497f4-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="497f4-136">筆記</span><span class="sxs-lookup"><span data-stu-id="497f4-136">NOTES</span></span>
<span data-ttu-id="497f4-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="497f4-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="497f4-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="497f4-138">RELATED LINKS</span></span>

[<span data-ttu-id="497f4-139">附加 AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="497f4-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="497f4-140">AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="497f4-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="497f4-141">移除-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="497f4-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="497f4-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="497f4-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

