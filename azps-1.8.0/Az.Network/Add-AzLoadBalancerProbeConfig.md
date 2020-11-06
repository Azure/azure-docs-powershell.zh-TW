---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 071a6db22f6788f76a6c4323c26247c070f164b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622150"
---
# <span data-ttu-id="a28d8-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a28d8-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a28d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a28d8-102">SYNOPSIS</span></span>
<span data-ttu-id="a28d8-103">在負載平衡器中新增探測配置。</span><span class="sxs-lookup"><span data-stu-id="a28d8-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="a28d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="a28d8-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a28d8-105">說明</span><span class="sxs-lookup"><span data-stu-id="a28d8-105">DESCRIPTION</span></span>
<span data-ttu-id="a28d8-106">**AzLoadBalancerProbeConfig** Cmdlet 會將探測設定新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a28d8-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="a28d8-107">示例</span><span class="sxs-lookup"><span data-stu-id="a28d8-107">EXAMPLES</span></span>

### <span data-ttu-id="a28d8-108">範例1將探針設定新增到負載平衡器</span><span class="sxs-lookup"><span data-stu-id="a28d8-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="a28d8-109">這個命令會取得名為 myLb 的負載平衡器，將指定的探測器設定新增至它，然後使用 **Set AzLoadBalancer** Cmdlet 來更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a28d8-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="a28d8-110">參數</span><span class="sxs-lookup"><span data-stu-id="a28d8-110">PARAMETERS</span></span>

### <span data-ttu-id="a28d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28d8-111">-DefaultProfile</span></span>
<span data-ttu-id="a28d8-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a28d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a28d8-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a28d8-113">-IntervalInSeconds</span></span>
<span data-ttu-id="a28d8-114">指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a28d8-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="a28d8-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a28d8-115">-LoadBalancer</span></span>
<span data-ttu-id="a28d8-116">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="a28d8-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="a28d8-117">這個 Cmdlet 會將探測設定新增到此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a28d8-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a28d8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a28d8-118">-Name</span></span>
<span data-ttu-id="a28d8-119">指定要新增的探測配置名稱。</span><span class="sxs-lookup"><span data-stu-id="a28d8-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="a28d8-120">-埠</span><span class="sxs-lookup"><span data-stu-id="a28d8-120">-Port</span></span>
<span data-ttu-id="a28d8-121">指定探測器應連接到負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="a28d8-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="a28d8-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="a28d8-122">-ProbeCount</span></span>
<span data-ttu-id="a28d8-123">指定實例被視為不健康的每個實例連續失敗數。</span><span class="sxs-lookup"><span data-stu-id="a28d8-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="a28d8-124">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a28d8-124">-Protocol</span></span>
<span data-ttu-id="a28d8-125">指定要用於探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a28d8-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="a28d8-126">此參數可接受的值為： Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="a28d8-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="a28d8-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="a28d8-127">-RequestPath</span></span>
<span data-ttu-id="a28d8-128">指定負載平衡服務中要探測以判斷健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="a28d8-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="a28d8-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a28d8-129">-Confirm</span></span>
<span data-ttu-id="a28d8-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a28d8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a28d8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a28d8-131">-WhatIf</span></span>
<span data-ttu-id="a28d8-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a28d8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a28d8-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a28d8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a28d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28d8-134">CommonParameters</span></span>
<span data-ttu-id="a28d8-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a28d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28d8-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a28d8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28d8-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a28d8-137">INPUTS</span></span>

### <span data-ttu-id="a28d8-138">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a28d8-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a28d8-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a28d8-139">System.String</span></span>

### <span data-ttu-id="a28d8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="a28d8-140">System.Int32</span></span>

## <span data-ttu-id="a28d8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a28d8-141">OUTPUTS</span></span>

### <span data-ttu-id="a28d8-142">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a28d8-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a28d8-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a28d8-143">NOTES</span></span>

## <span data-ttu-id="a28d8-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a28d8-144">RELATED LINKS</span></span>

[<span data-ttu-id="a28d8-145">AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a28d8-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a28d8-146">新-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a28d8-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a28d8-147">移除-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a28d8-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a28d8-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a28d8-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="a28d8-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a28d8-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)

