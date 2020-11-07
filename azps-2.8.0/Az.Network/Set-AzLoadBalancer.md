---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: d16e0579224907885a2239aa0669ae865ed19dd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790493"
---
# <span data-ttu-id="8e778-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8e778-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="8e778-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e778-102">SYNOPSIS</span></span>
<span data-ttu-id="8e778-103">更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8e778-103">Updates a load balancer.</span></span>

## <span data-ttu-id="8e778-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e778-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e778-105">說明</span><span class="sxs-lookup"><span data-stu-id="8e778-105">DESCRIPTION</span></span>
<span data-ttu-id="8e778-106">**AzLoadBalancer** Cmdlet 會更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8e778-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="8e778-107">示例</span><span class="sxs-lookup"><span data-stu-id="8e778-107">EXAMPLES</span></span>

### <span data-ttu-id="8e778-108">範例1：修改負載平衡器</span><span class="sxs-lookup"><span data-stu-id="8e778-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="8e778-109">第一個命令會取得名為 NRPLB 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="8e778-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="8e778-110">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzLoadBalancerInboundNatRuleConfig，這會新增一個名為 NewRule 的輸入 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="8e778-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="8e778-111">第三個命令會將負載平衡器傳到 AzLoadBalancer，這會更新負載平衡器 **設定** 並儲存。</span><span class="sxs-lookup"><span data-stu-id="8e778-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="8e778-112">參數</span><span class="sxs-lookup"><span data-stu-id="8e778-112">PARAMETERS</span></span>

### <span data-ttu-id="8e778-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e778-113">-AsJob</span></span>
<span data-ttu-id="8e778-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e778-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e778-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e778-115">-DefaultProfile</span></span>
<span data-ttu-id="8e778-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e778-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e778-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8e778-117">-LoadBalancer</span></span>
<span data-ttu-id="8e778-118">指定代表應設定負載平衡器之狀態的負載平衡器物件。</span><span class="sxs-lookup"><span data-stu-id="8e778-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e778-119">-確認</span><span class="sxs-lookup"><span data-stu-id="8e778-119">-Confirm</span></span>
<span data-ttu-id="8e778-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e778-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e778-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e778-121">-WhatIf</span></span>
<span data-ttu-id="8e778-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e778-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e778-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e778-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e778-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e778-124">CommonParameters</span></span>
<span data-ttu-id="8e778-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e778-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e778-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e778-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e778-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8e778-127">INPUTS</span></span>

### <span data-ttu-id="8e778-128">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e778-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8e778-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8e778-129">OUTPUTS</span></span>

### <span data-ttu-id="8e778-130">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e778-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8e778-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8e778-131">NOTES</span></span>

## <span data-ttu-id="8e778-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e778-132">RELATED LINKS</span></span>

[<span data-ttu-id="8e778-133">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8e778-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8e778-134">新-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8e778-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="8e778-135">移除-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8e778-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


