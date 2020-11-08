---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 76cf9e2624c812d99702823b303e4e6427845670
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126421"
---
# <span data-ttu-id="46a43-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46a43-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="46a43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46a43-102">SYNOPSIS</span></span>
<span data-ttu-id="46a43-103">從負載平衡器移除入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="46a43-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="46a43-104">句法</span><span class="sxs-lookup"><span data-stu-id="46a43-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a43-105">說明</span><span class="sxs-lookup"><span data-stu-id="46a43-105">DESCRIPTION</span></span>
<span data-ttu-id="46a43-106">**AzLoadBalancerInboundNatRuleConfig** Cmdlet 會從 Azure 負載平衡器移除入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="46a43-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="46a43-107">示例</span><span class="sxs-lookup"><span data-stu-id="46a43-107">EXAMPLES</span></span>

### <span data-ttu-id="46a43-108">1：從 Azure 負載平衡器刪除入站 NAT 規則</span><span class="sxs-lookup"><span data-stu-id="46a43-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="46a43-109">第一個命令會載入一個名為 "mylb" 的現有負載等化器，並將它儲存在 $load 平衡器的變數中。</span><span class="sxs-lookup"><span data-stu-id="46a43-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="46a43-110">第二個命令會移除與此負載平衡器相關聯的輸入 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="46a43-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="46a43-111">參數</span><span class="sxs-lookup"><span data-stu-id="46a43-111">PARAMETERS</span></span>

### <span data-ttu-id="46a43-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a43-112">-DefaultProfile</span></span>
<span data-ttu-id="46a43-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46a43-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46a43-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46a43-114">-LoadBalancer</span></span>
<span data-ttu-id="46a43-115">指定包含此 Cmdlet 移除之入站 NAT 規則配置的 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="46a43-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="46a43-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="46a43-116">-Name</span></span>
<span data-ttu-id="46a43-117">指定此 Cmdlet 移除的輸入 NAT 規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="46a43-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="46a43-118">-確認</span><span class="sxs-lookup"><span data-stu-id="46a43-118">-Confirm</span></span>
<span data-ttu-id="46a43-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46a43-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a43-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a43-120">-WhatIf</span></span>
<span data-ttu-id="46a43-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46a43-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46a43-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46a43-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a43-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a43-123">CommonParameters</span></span>
<span data-ttu-id="46a43-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46a43-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a43-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46a43-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a43-126">輸入</span><span class="sxs-lookup"><span data-stu-id="46a43-126">INPUTS</span></span>

### <span data-ttu-id="46a43-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="46a43-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="46a43-128">輸出</span><span class="sxs-lookup"><span data-stu-id="46a43-128">OUTPUTS</span></span>

### <span data-ttu-id="46a43-129">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="46a43-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="46a43-130">筆記</span><span class="sxs-lookup"><span data-stu-id="46a43-130">NOTES</span></span>

## <span data-ttu-id="46a43-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="46a43-131">RELATED LINKS</span></span>

[<span data-ttu-id="46a43-132">附加 AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46a43-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="46a43-133">AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46a43-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="46a43-134">新-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46a43-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="46a43-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46a43-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)

