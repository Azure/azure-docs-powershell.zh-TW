---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274255"
---
# <span data-ttu-id="80392-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80392-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="80392-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80392-102">SYNOPSIS</span></span>
<span data-ttu-id="80392-103">更新負載平衡器的探測配置。</span><span class="sxs-lookup"><span data-stu-id="80392-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="80392-104">句法</span><span class="sxs-lookup"><span data-stu-id="80392-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80392-105">說明</span><span class="sxs-lookup"><span data-stu-id="80392-105">DESCRIPTION</span></span>
<span data-ttu-id="80392-106">**AzLoadBalancerProbeConfig** Cmdlet 會更新負載平衡器的探測配置。</span><span class="sxs-lookup"><span data-stu-id="80392-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="80392-107">示例</span><span class="sxs-lookup"><span data-stu-id="80392-107">EXAMPLES</span></span>

### <span data-ttu-id="80392-108">範例1：修改負載平衡器上的探測設定</span><span class="sxs-lookup"><span data-stu-id="80392-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="80392-109">第一個命令會取得名為 MyLoadBalancer 的 loadbalancer，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="80392-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="80392-110">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzLoadBalancerProbeConfig，這會將新的探針設定新增到其中。</span><span class="sxs-lookup"><span data-stu-id="80392-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="80392-111">第三個命令會將負載平衡器傳遞給 AzLoadBalancerProbeConfig，以 **設定** 新的配置。</span><span class="sxs-lookup"><span data-stu-id="80392-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="80392-112">請注意，您必須指定前面命令中指定的數個相同參數，因為目前的 Cmdlet 需要它們。</span><span class="sxs-lookup"><span data-stu-id="80392-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="80392-113">參數</span><span class="sxs-lookup"><span data-stu-id="80392-113">PARAMETERS</span></span>

### <span data-ttu-id="80392-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80392-114">-DefaultProfile</span></span>
<span data-ttu-id="80392-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80392-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80392-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="80392-116">-IntervalInSeconds</span></span>
<span data-ttu-id="80392-117">指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="80392-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="80392-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80392-118">-LoadBalancer</span></span>
<span data-ttu-id="80392-119">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="80392-119">Specifies a load balancer.</span></span>
<span data-ttu-id="80392-120">這個 Cmdlet 會針對此參數指定的負載平衡器更新探測設定。</span><span class="sxs-lookup"><span data-stu-id="80392-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="80392-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="80392-121">-Name</span></span>
<span data-ttu-id="80392-122">指定此 Cmdlet 所設定的探測配置名稱。</span><span class="sxs-lookup"><span data-stu-id="80392-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="80392-123">-埠</span><span class="sxs-lookup"><span data-stu-id="80392-123">-Port</span></span>
<span data-ttu-id="80392-124">指定探測器應連接到負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="80392-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="80392-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="80392-125">-ProbeCount</span></span>
<span data-ttu-id="80392-126">指定實例被視為不健康的每個實例連續失敗數。</span><span class="sxs-lookup"><span data-stu-id="80392-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="80392-127">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="80392-127">-Protocol</span></span>
<span data-ttu-id="80392-128">指定要用於探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="80392-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="80392-129">此參數可接受的值為： Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="80392-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="80392-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="80392-130">-RequestPath</span></span>
<span data-ttu-id="80392-131">指定負載平衡服務中要探測以判斷健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="80392-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="80392-132">-確認</span><span class="sxs-lookup"><span data-stu-id="80392-132">-Confirm</span></span>
<span data-ttu-id="80392-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80392-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80392-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80392-134">-WhatIf</span></span>
<span data-ttu-id="80392-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80392-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80392-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80392-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80392-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80392-137">CommonParameters</span></span>
<span data-ttu-id="80392-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80392-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80392-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80392-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80392-140">輸入</span><span class="sxs-lookup"><span data-stu-id="80392-140">INPUTS</span></span>

### <span data-ttu-id="80392-141">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="80392-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="80392-142">System.object</span><span class="sxs-lookup"><span data-stu-id="80392-142">System.String</span></span>

### <span data-ttu-id="80392-143">System.object</span><span class="sxs-lookup"><span data-stu-id="80392-143">System.Int32</span></span>

## <span data-ttu-id="80392-144">輸出</span><span class="sxs-lookup"><span data-stu-id="80392-144">OUTPUTS</span></span>

### <span data-ttu-id="80392-145">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="80392-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="80392-146">筆記</span><span class="sxs-lookup"><span data-stu-id="80392-146">NOTES</span></span>

## <span data-ttu-id="80392-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="80392-147">RELATED LINKS</span></span>

[<span data-ttu-id="80392-148">附加 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80392-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="80392-149">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80392-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="80392-150">AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80392-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="80392-151">新-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80392-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="80392-152">移除-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80392-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


