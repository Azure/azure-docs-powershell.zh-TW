---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 2dd00c21a0badaca90419615df179299dc2d4240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915310"
---
# <span data-ttu-id="9fd7a-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9fd7a-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="9fd7a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9fd7a-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd7a-103">更新負載平衡器的更新設置。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="9fd7a-104">語法</span><span class="sxs-lookup"><span data-stu-id="9fd7a-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fd7a-105">描述</span><span class="sxs-lookup"><span data-stu-id="9fd7a-105">DESCRIPTION</span></span>
<span data-ttu-id="9fd7a-106">**Set-AzLoadBalancerProbeConfig** Cmdlet 會更新負載平衡器的最新設定。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="9fd7a-107">例子</span><span class="sxs-lookup"><span data-stu-id="9fd7a-107">EXAMPLES</span></span>

### <span data-ttu-id="9fd7a-108">範例 1：修改負載平衡器上的安裝配置</span><span class="sxs-lookup"><span data-stu-id="9fd7a-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="9fd7a-109">第一個命令會獲得名為 MyLoadBalancer 的載入平衡器，然後將它儲存在$slb變數中。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="9fd7a-110">第二個命令使用管線運算子，將 $slb 中的負載平衡器傳遞到 Add-AzLoadBalancerProbeConfig，為它新增了新的加總組式組。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="9fd7a-111">第三個命令會將負載平衡器傳遞至 **Set-AzLoadBalancerProbeConfig，** 以設定新的設定。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="9fd7a-112">請注意，必須指定數個在上一個命令中指定的相同參數，因為目前的 Cmdlet 需要這些參數。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="9fd7a-113">參數</span><span class="sxs-lookup"><span data-stu-id="9fd7a-113">PARAMETERS</span></span>

### <span data-ttu-id="9fd7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd7a-114">-DefaultProfile</span></span>
<span data-ttu-id="9fd7a-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fd7a-116">-IntervalIn以秒為單位</span><span class="sxs-lookup"><span data-stu-id="9fd7a-116">-IntervalInSeconds</span></span>
<span data-ttu-id="9fd7a-117">指定每個負載平衡服務實例之間的間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd7a-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fd7a-118">-LoadBalancer</span></span>
<span data-ttu-id="9fd7a-119">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-119">Specifies a load balancer.</span></span>
<span data-ttu-id="9fd7a-120">此 Cmdlet 會更新此參數指定的負載平衡器設定。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="9fd7a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9fd7a-121">-Name</span></span>
<span data-ttu-id="9fd7a-122">指定此 Cmdlet 所設定之設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="9fd7a-123">-埠</span><span class="sxs-lookup"><span data-stu-id="9fd7a-123">-Port</span></span>
<span data-ttu-id="9fd7a-124">指定應該連接負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd7a-125">-Count</span><span class="sxs-lookup"><span data-stu-id="9fd7a-125">-ProbeCount</span></span>
<span data-ttu-id="9fd7a-126">指定將實例視為不健康之每例連續失敗次數。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd7a-127">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="9fd7a-127">-Protocol</span></span>
<span data-ttu-id="9fd7a-128">指定用於進行探索的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="9fd7a-129">此參數可接受的值為：Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd7a-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="9fd7a-130">-RequestPath</span></span>
<span data-ttu-id="9fd7a-131">指定負載平衡服務中的路徑，以進位決定健康狀態。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd7a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="9fd7a-132">-Confirm</span></span>
<span data-ttu-id="9fd7a-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fd7a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fd7a-134">-WhatIf</span></span>
<span data-ttu-id="9fd7a-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fd7a-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fd7a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd7a-137">CommonParameters</span></span>
<span data-ttu-id="9fd7a-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd7a-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9fd7a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd7a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="9fd7a-140">INPUTS</span></span>

### <span data-ttu-id="9fd7a-141">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fd7a-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="9fd7a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9fd7a-142">System.String</span></span>

### <span data-ttu-id="9fd7a-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9fd7a-143">System.Int32</span></span>

## <span data-ttu-id="9fd7a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="9fd7a-144">OUTPUTS</span></span>

### <span data-ttu-id="9fd7a-145">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fd7a-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9fd7a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="9fd7a-146">NOTES</span></span>

## <span data-ttu-id="9fd7a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fd7a-147">RELATED LINKS</span></span>

[<span data-ttu-id="9fd7a-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9fd7a-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9fd7a-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fd7a-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9fd7a-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9fd7a-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9fd7a-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9fd7a-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9fd7a-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9fd7a-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


