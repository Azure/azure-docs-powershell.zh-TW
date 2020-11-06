---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 6e0ff70671ceff4094d7f1a48bbebcc81398d5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446192"
---
# <span data-ttu-id="f9a84-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9a84-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="f9a84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9a84-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a84-103">建立路由篩選器的路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="f9a84-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a84-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9a84-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9a84-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9a84-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a84-106">New-AzureRmRouteFilterRuleConfig Cmdlet 會針對 Azure 路由篩選建立路由篩選規則。</span><span class="sxs-lookup"><span data-stu-id="f9a84-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="f9a84-107">示例</span><span class="sxs-lookup"><span data-stu-id="f9a84-107">EXAMPLES</span></span>

### <span data-ttu-id="f9a84-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f9a84-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f9a84-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="f9a84-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f9a84-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9a84-110">PARAMETERS</span></span>

### <span data-ttu-id="f9a84-111">-Access</span><span class="sxs-lookup"><span data-stu-id="f9a84-111">-Access</span></span>
<span data-ttu-id="f9a84-112">路由篩選規則的存取權。</span><span class="sxs-lookup"><span data-stu-id="f9a84-112">Access for route filter rule.</span></span>
<span data-ttu-id="f9a84-113">有效值為 [允許] 或 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="f9a84-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="f9a84-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="f9a84-114">-CommunityList</span></span>
<span data-ttu-id="f9a84-115">路由篩選將篩選的群組值清單</span><span class="sxs-lookup"><span data-stu-id="f9a84-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="f9a84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a84-116">-DefaultProfile</span></span>
<span data-ttu-id="f9a84-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9a84-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9a84-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f9a84-118">-Force</span></span>
<span data-ttu-id="f9a84-119">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="f9a84-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="f9a84-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9a84-120">-Name</span></span>
<span data-ttu-id="f9a84-121">指定路由篩選規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9a84-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="f9a84-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="f9a84-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="f9a84-123">路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="f9a84-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="f9a84-124">有效值為： [群組]</span><span class="sxs-lookup"><span data-stu-id="f9a84-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="f9a84-125">-確認</span><span class="sxs-lookup"><span data-stu-id="f9a84-125">-Confirm</span></span>
<span data-ttu-id="f9a84-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9a84-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9a84-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9a84-127">-WhatIf</span></span>
<span data-ttu-id="f9a84-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9a84-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9a84-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9a84-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9a84-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a84-130">CommonParameters</span></span>
<span data-ttu-id="f9a84-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9a84-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a84-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9a84-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a84-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f9a84-133">INPUTS</span></span>

### <span data-ttu-id="f9a84-134">所有</span><span class="sxs-lookup"><span data-stu-id="f9a84-134">None</span></span>
<span data-ttu-id="f9a84-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f9a84-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9a84-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f9a84-136">OUTPUTS</span></span>

### <span data-ttu-id="f9a84-137">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f9a84-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="f9a84-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f9a84-138">NOTES</span></span>
<span data-ttu-id="f9a84-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="f9a84-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f9a84-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9a84-140">RELATED LINKS</span></span>

[<span data-ttu-id="f9a84-141">附加 AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9a84-141">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="f9a84-142">AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9a84-142">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="f9a84-143">移除-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9a84-143">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="f9a84-144">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9a84-144">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

