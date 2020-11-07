---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965473"
---
# <span data-ttu-id="f0261-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f0261-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="f0261-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0261-102">SYNOPSIS</span></span>
<span data-ttu-id="f0261-103">移除負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="f0261-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="f0261-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0261-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0261-105">說明</span><span class="sxs-lookup"><span data-stu-id="f0261-105">DESCRIPTION</span></span>
<span data-ttu-id="f0261-106">**AzLoadBalancerRuleConfig** Cmdlet 會移除 Azure 負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="f0261-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f0261-107">示例</span><span class="sxs-lookup"><span data-stu-id="f0261-107">EXAMPLES</span></span>

### <span data-ttu-id="f0261-108">範例1：從負載平衡器移除規則配置</span><span class="sxs-lookup"><span data-stu-id="f0261-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f0261-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="f0261-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="f0261-110">第二個命令會從 $loadbalancer 中的負載平衡器移除名為 MyLBruleName 的規則配置。</span><span class="sxs-lookup"><span data-stu-id="f0261-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="f0261-111">參數</span><span class="sxs-lookup"><span data-stu-id="f0261-111">PARAMETERS</span></span>

### <span data-ttu-id="f0261-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0261-112">-DefaultProfile</span></span>
<span data-ttu-id="f0261-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0261-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0261-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0261-114">-LoadBalancer</span></span>
<span data-ttu-id="f0261-115">指定包含此 Cmdlet 移除之規則配置的 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="f0261-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f0261-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0261-116">-Name</span></span>
<span data-ttu-id="f0261-117">指定此 Cmdlet 移除的負載等化器規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="f0261-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f0261-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f0261-118">-Confirm</span></span>
<span data-ttu-id="f0261-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0261-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0261-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0261-120">-WhatIf</span></span>
<span data-ttu-id="f0261-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0261-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0261-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0261-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0261-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0261-123">CommonParameters</span></span>
<span data-ttu-id="f0261-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0261-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0261-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0261-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0261-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f0261-126">INPUTS</span></span>

### <span data-ttu-id="f0261-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f0261-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f0261-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f0261-128">OUTPUTS</span></span>

### <span data-ttu-id="f0261-129">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f0261-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f0261-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f0261-130">NOTES</span></span>

## <span data-ttu-id="f0261-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0261-131">RELATED LINKS</span></span>

[<span data-ttu-id="f0261-132">附加 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f0261-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f0261-133">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0261-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f0261-134">AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f0261-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f0261-135">新-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f0261-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f0261-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f0261-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


