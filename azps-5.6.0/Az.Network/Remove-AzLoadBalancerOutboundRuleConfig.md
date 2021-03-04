---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 5652615cf8072e4a448f2fe6c6d4b3fd784cc330
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913417"
---
# <span data-ttu-id="17b6a-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17b6a-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="17b6a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="17b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="17b6a-103">從負載平衡器移除外發規則組式。</span><span class="sxs-lookup"><span data-stu-id="17b6a-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="17b6a-104">語法</span><span class="sxs-lookup"><span data-stu-id="17b6a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17b6a-105">描述</span><span class="sxs-lookup"><span data-stu-id="17b6a-105">DESCRIPTION</span></span>
<span data-ttu-id="17b6a-106">**Remove-AzLoadBalancerOutboundRuleConfig** Cmdlet 會從 Azure 負載平衡器移除輸出規則組式。</span><span class="sxs-lookup"><span data-stu-id="17b6a-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="17b6a-107">例子</span><span class="sxs-lookup"><span data-stu-id="17b6a-107">EXAMPLES</span></span>

### <span data-ttu-id="17b6a-108">範例 1：從 Azure 負載平衡器刪除外發規則</span><span class="sxs-lookup"><span data-stu-id="17b6a-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="17b6a-109">第一個命令會取得與您想要移除之外發規則組$slb平衡器。</span><span class="sxs-lookup"><span data-stu-id="17b6a-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="17b6a-110">第二個命令會從負載平衡器移除相關聯的外發規則組式。</span><span class="sxs-lookup"><span data-stu-id="17b6a-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="17b6a-111">第三個命令會更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="17b6a-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="17b6a-112">參數</span><span class="sxs-lookup"><span data-stu-id="17b6a-112">PARAMETERS</span></span>

### <span data-ttu-id="17b6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b6a-113">-DefaultProfile</span></span>
<span data-ttu-id="17b6a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="17b6a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b6a-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17b6a-115">-LoadBalancer</span></span>
<span data-ttu-id="17b6a-116">負載平衡器資源的參照。</span><span class="sxs-lookup"><span data-stu-id="17b6a-116">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b6a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="17b6a-117">-Name</span></span>
<span data-ttu-id="17b6a-118">外發規則的名稱</span><span class="sxs-lookup"><span data-stu-id="17b6a-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="17b6a-119">-確認</span><span class="sxs-lookup"><span data-stu-id="17b6a-119">-Confirm</span></span>
<span data-ttu-id="17b6a-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="17b6a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17b6a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17b6a-121">-WhatIf</span></span>
<span data-ttu-id="17b6a-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17b6a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17b6a-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17b6a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17b6a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b6a-124">CommonParameters</span></span>
<span data-ttu-id="17b6a-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="17b6a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b6a-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="17b6a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b6a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="17b6a-127">INPUTS</span></span>

### <span data-ttu-id="17b6a-128">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17b6a-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="17b6a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="17b6a-129">OUTPUTS</span></span>

### <span data-ttu-id="17b6a-130">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17b6a-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="17b6a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="17b6a-131">NOTES</span></span>

## <span data-ttu-id="17b6a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="17b6a-132">RELATED LINKS</span></span>

[<span data-ttu-id="17b6a-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17b6a-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="17b6a-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17b6a-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="17b6a-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17b6a-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="17b6a-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17b6a-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
