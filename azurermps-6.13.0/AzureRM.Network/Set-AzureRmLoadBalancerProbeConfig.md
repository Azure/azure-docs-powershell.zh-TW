---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 3fe5345e6d3cbad90d99f5a94e72873beaca7c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624240"
---
# <span data-ttu-id="45c30-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="45c30-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="45c30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45c30-102">SYNOPSIS</span></span>
<span data-ttu-id="45c30-103">設定探測器配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="45c30-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45c30-104">句法</span><span class="sxs-lookup"><span data-stu-id="45c30-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45c30-105">說明</span><span class="sxs-lookup"><span data-stu-id="45c30-105">DESCRIPTION</span></span>
<span data-ttu-id="45c30-106">**AzureRmLoadBalancerProbeConfig** Cmdlet 會設定探針設定的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="45c30-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="45c30-107">示例</span><span class="sxs-lookup"><span data-stu-id="45c30-107">EXAMPLES</span></span>

### <span data-ttu-id="45c30-108">範例1：修改負載平衡器上的探測設定</span><span class="sxs-lookup"><span data-stu-id="45c30-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="45c30-109">第一個命令會取得名為 MyLoadBalancer 的 loadbalancer，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="45c30-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="45c30-110">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzureRmLoadBalancerProbeConfig，這會將新的探針設定新增到其中。</span><span class="sxs-lookup"><span data-stu-id="45c30-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="45c30-111">第三個命令會將負載平衡器傳遞給 AzureRmLoadBalancerProbeConfig，以 **設定** 新的配置。</span><span class="sxs-lookup"><span data-stu-id="45c30-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="45c30-112">請注意，您必須指定前面命令中指定的數個相同參數，因為目前的 Cmdlet 需要它們。</span><span class="sxs-lookup"><span data-stu-id="45c30-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="45c30-113">參數</span><span class="sxs-lookup"><span data-stu-id="45c30-113">PARAMETERS</span></span>

### <span data-ttu-id="45c30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c30-114">-DefaultProfile</span></span>
<span data-ttu-id="45c30-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45c30-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c30-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="45c30-116">-IntervalInSeconds</span></span>
<span data-ttu-id="45c30-117">指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="45c30-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="45c30-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45c30-118">-LoadBalancer</span></span>
<span data-ttu-id="45c30-119">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="45c30-119">Specifies a load balancer.</span></span>
<span data-ttu-id="45c30-120">這個 Cmdlet 會針對此參數指定的負載平衡器設定探測配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="45c30-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="45c30-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="45c30-121">-Name</span></span>
<span data-ttu-id="45c30-122">指定此 Cmdlet 所設定的探測配置名稱。</span><span class="sxs-lookup"><span data-stu-id="45c30-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="45c30-123">-埠</span><span class="sxs-lookup"><span data-stu-id="45c30-123">-Port</span></span>
<span data-ttu-id="45c30-124">指定探測器應連接到負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="45c30-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="45c30-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="45c30-125">-ProbeCount</span></span>
<span data-ttu-id="45c30-126">指定實例被視為不健康的每個實例連續失敗數。</span><span class="sxs-lookup"><span data-stu-id="45c30-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="45c30-127">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="45c30-127">-Protocol</span></span>
<span data-ttu-id="45c30-128">指定要用於探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="45c30-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="45c30-129">此參數可接受的值為： Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="45c30-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="45c30-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="45c30-130">-RequestPath</span></span>
<span data-ttu-id="45c30-131">指定負載平衡服務中要探測以判斷健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="45c30-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="45c30-132">-確認</span><span class="sxs-lookup"><span data-stu-id="45c30-132">-Confirm</span></span>
<span data-ttu-id="45c30-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45c30-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c30-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c30-134">-WhatIf</span></span>
<span data-ttu-id="45c30-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45c30-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45c30-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45c30-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c30-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c30-137">CommonParameters</span></span>
<span data-ttu-id="45c30-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45c30-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c30-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45c30-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c30-140">輸入</span><span class="sxs-lookup"><span data-stu-id="45c30-140">INPUTS</span></span>

### <span data-ttu-id="45c30-141">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="45c30-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="45c30-142">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="45c30-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="45c30-143">輸出</span><span class="sxs-lookup"><span data-stu-id="45c30-143">OUTPUTS</span></span>

### <span data-ttu-id="45c30-144">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="45c30-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="45c30-145">筆記</span><span class="sxs-lookup"><span data-stu-id="45c30-145">NOTES</span></span>

## <span data-ttu-id="45c30-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="45c30-146">RELATED LINKS</span></span>

[<span data-ttu-id="45c30-147">附加 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="45c30-147">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="45c30-148">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45c30-148">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="45c30-149">AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="45c30-149">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="45c30-150">新-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="45c30-150">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="45c30-151">移除-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="45c30-151">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


