---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 053f86f0b29346c98f60a3160a8e1f2a51ab0e14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913413"
---
# <span data-ttu-id="d91cf-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d91cf-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="d91cf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d91cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d91cf-103">移除負載平衡器的規則組。</span><span class="sxs-lookup"><span data-stu-id="d91cf-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="d91cf-104">語法</span><span class="sxs-lookup"><span data-stu-id="d91cf-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d91cf-105">描述</span><span class="sxs-lookup"><span data-stu-id="d91cf-105">DESCRIPTION</span></span>
<span data-ttu-id="d91cf-106">**Remove-AzLoadBalancerRuleConfig** Cmdlet 會移除 Azure 負載平衡器的規則組。</span><span class="sxs-lookup"><span data-stu-id="d91cf-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d91cf-107">例子</span><span class="sxs-lookup"><span data-stu-id="d91cf-107">EXAMPLES</span></span>

### <span data-ttu-id="d91cf-108">範例 1：從負載平衡器移除規則組</span><span class="sxs-lookup"><span data-stu-id="d91cf-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="d91cf-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在$loadbalancer變數中。</span><span class="sxs-lookup"><span data-stu-id="d91cf-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="d91cf-110">第二個命令會從 $loadbalancer 中的負載平衡器移除名為 MyLBruleName 的規則$loadbalancer。</span><span class="sxs-lookup"><span data-stu-id="d91cf-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="d91cf-111">參數</span><span class="sxs-lookup"><span data-stu-id="d91cf-111">PARAMETERS</span></span>

### <span data-ttu-id="d91cf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d91cf-112">-DefaultProfile</span></span>
<span data-ttu-id="d91cf-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d91cf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d91cf-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d91cf-114">-LoadBalancer</span></span>
<span data-ttu-id="d91cf-115">指定 **包含此 Cmdlet** 移除之規則配置的 LoadBalancer 物件。</span><span class="sxs-lookup"><span data-stu-id="d91cf-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d91cf-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="d91cf-116">-Name</span></span>
<span data-ttu-id="d91cf-117">指定此 Cmdlet 移除的負載平衡器規則組名。</span><span class="sxs-lookup"><span data-stu-id="d91cf-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91cf-118">-確認</span><span class="sxs-lookup"><span data-stu-id="d91cf-118">-Confirm</span></span>
<span data-ttu-id="d91cf-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d91cf-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d91cf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d91cf-120">-WhatIf</span></span>
<span data-ttu-id="d91cf-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d91cf-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d91cf-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d91cf-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d91cf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91cf-123">CommonParameters</span></span>
<span data-ttu-id="d91cf-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d91cf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91cf-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d91cf-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91cf-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d91cf-126">INPUTS</span></span>

### <span data-ttu-id="d91cf-127">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d91cf-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d91cf-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d91cf-128">OUTPUTS</span></span>

### <span data-ttu-id="d91cf-129">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d91cf-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d91cf-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d91cf-130">NOTES</span></span>

## <span data-ttu-id="d91cf-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d91cf-131">RELATED LINKS</span></span>

[<span data-ttu-id="d91cf-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d91cf-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d91cf-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d91cf-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d91cf-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d91cf-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d91cf-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d91cf-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d91cf-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d91cf-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


