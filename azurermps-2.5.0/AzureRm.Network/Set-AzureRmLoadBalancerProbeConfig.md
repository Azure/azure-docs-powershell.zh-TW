---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: 902fa7e266583fe52c516ac3704bdc394215e2c7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801978"
---
# <span data-ttu-id="c9c3c-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c9c3c-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="c9c3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c3c-103">設定探測器配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9c3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9c3c-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9c3c-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="c9c3c-106">**AzureRmLoadBalancerProbeConfig** Cmdlet 會設定探針設定的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="c9c3c-107">示例</span><span class="sxs-lookup"><span data-stu-id="c9c3c-107">EXAMPLES</span></span>

### <span data-ttu-id="c9c3c-108">範例1：修改負載平衡器上的探測設定</span><span class="sxs-lookup"><span data-stu-id="c9c3c-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="c9c3c-109">第一個命令會取得名為 MyLoadBalancer 的 loadbalancer，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="c9c3c-110">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzureRmLoadBalancerProbeConfig，這會將新的探針設定新增到其中。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="c9c3c-111">第三個命令會將負載平衡器傳遞給 AzureRmLoadBalancerProbeConfig，以 **設定** 新的配置。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="c9c3c-112">請注意，您必須指定前面命令中指定的數個相同參數，因為目前的 Cmdlet 需要它們。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="c9c3c-113">參數</span><span class="sxs-lookup"><span data-stu-id="c9c3c-113">PARAMETERS</span></span>

### <span data-ttu-id="c9c3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c3c-114">-DefaultProfile</span></span>
<span data-ttu-id="c9c3c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9c3c-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c9c3c-116">-IntervalInSeconds</span></span>
<span data-ttu-id="c9c3c-117">指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c3c-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9c3c-118">-LoadBalancer</span></span>
<span data-ttu-id="c9c3c-119">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-119">Specifies a load balancer.</span></span>
<span data-ttu-id="c9c3c-120">這個 Cmdlet 會針對此參數指定的負載平衡器設定探測配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c3c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9c3c-121">-Name</span></span>
<span data-ttu-id="c9c3c-122">指定此 Cmdlet 所設定的探測配置名稱。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="c9c3c-123">-埠</span><span class="sxs-lookup"><span data-stu-id="c9c3c-123">-Port</span></span>
<span data-ttu-id="c9c3c-124">指定探測器應連接到負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c3c-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="c9c3c-125">-ProbeCount</span></span>
<span data-ttu-id="c9c3c-126">指定實例被視為不健康的每個實例連續失敗數。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c3c-127">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="c9c3c-127">-Protocol</span></span>
<span data-ttu-id="c9c3c-128">指定要用於探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="c9c3c-129">此參數可接受的值為： Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c3c-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="c9c3c-130">-RequestPath</span></span>
<span data-ttu-id="c9c3c-131">指定負載平衡服務中要探測以判斷健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c3c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c3c-132">CommonParameters</span></span>
<span data-ttu-id="c9c3c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c3c-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9c3c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c3c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c9c3c-135">INPUTS</span></span>

### <span data-ttu-id="c9c3c-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9c3c-136">PSLoadBalancer</span></span>
<span data-ttu-id="c9c3c-137">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c9c3c-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c9c3c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c9c3c-138">OUTPUTS</span></span>

### <span data-ttu-id="c9c3c-139">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c9c3c-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c9c3c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c9c3c-140">NOTES</span></span>

## <span data-ttu-id="c9c3c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9c3c-141">RELATED LINKS</span></span>

[<span data-ttu-id="c9c3c-142">附加 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c9c3c-142">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c9c3c-143">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9c3c-143">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c9c3c-144">AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c9c3c-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c9c3c-145">新-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c9c3c-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c9c3c-146">移除-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c9c3c-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


