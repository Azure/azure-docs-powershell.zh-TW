---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: b608a8fe62f7316116409d4174ea01603b928ae2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904906"
---
# <span data-ttu-id="6559d-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6559d-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="6559d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6559d-102">SYNOPSIS</span></span>
<span data-ttu-id="6559d-103">更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="6559d-103">Updates a load balancer.</span></span>

## <span data-ttu-id="6559d-104">語法</span><span class="sxs-lookup"><span data-stu-id="6559d-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6559d-105">描述</span><span class="sxs-lookup"><span data-stu-id="6559d-105">DESCRIPTION</span></span>
<span data-ttu-id="6559d-106">**Set-AzLoadBalancer** Cmdlet 會更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="6559d-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="6559d-107">例子</span><span class="sxs-lookup"><span data-stu-id="6559d-107">EXAMPLES</span></span>

### <span data-ttu-id="6559d-108">範例 1：修改負載平衡器</span><span class="sxs-lookup"><span data-stu-id="6559d-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="6559d-109">第一個命令會取得名為 NRPLB 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="6559d-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="6559d-110">第二個命令使用管線運算子，將 $slb 中的負載平衡器傳遞到 Add-AzLoadBalancerInboundNatRuleConfig，這會增加名為 NewRule 的輸入 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="6559d-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="6559d-111">第三個命令會將負載平衡器傳遞至 **Set-AzLoadBalancer，** 它會更新負載平衡器設定並存盤。</span><span class="sxs-lookup"><span data-stu-id="6559d-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="6559d-112">參數</span><span class="sxs-lookup"><span data-stu-id="6559d-112">PARAMETERS</span></span>

### <span data-ttu-id="6559d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6559d-113">-AsJob</span></span>
<span data-ttu-id="6559d-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6559d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6559d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6559d-115">-DefaultProfile</span></span>
<span data-ttu-id="6559d-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6559d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6559d-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6559d-117">-LoadBalancer</span></span>
<span data-ttu-id="6559d-118">指定代表應設定負載平衡器之狀態負載平衡器的物件。</span><span class="sxs-lookup"><span data-stu-id="6559d-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="6559d-119">-確認</span><span class="sxs-lookup"><span data-stu-id="6559d-119">-Confirm</span></span>
<span data-ttu-id="6559d-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6559d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6559d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6559d-121">-WhatIf</span></span>
<span data-ttu-id="6559d-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6559d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6559d-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6559d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6559d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6559d-124">CommonParameters</span></span>
<span data-ttu-id="6559d-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6559d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6559d-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6559d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6559d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6559d-127">INPUTS</span></span>

### <span data-ttu-id="6559d-128">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6559d-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6559d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6559d-129">OUTPUTS</span></span>

### <span data-ttu-id="6559d-130">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6559d-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6559d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6559d-131">NOTES</span></span>

## <span data-ttu-id="6559d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="6559d-132">RELATED LINKS</span></span>

[<span data-ttu-id="6559d-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6559d-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6559d-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6559d-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="6559d-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6559d-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


