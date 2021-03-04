---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 622501a69632be9c9c70cfccaf4e806df94e7276
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916074"
---
# <span data-ttu-id="96296-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="96296-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="96296-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96296-102">SYNOPSIS</span></span>
<span data-ttu-id="96296-103">在負載平衡器中加入加量組。</span><span class="sxs-lookup"><span data-stu-id="96296-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="96296-104">語法</span><span class="sxs-lookup"><span data-stu-id="96296-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96296-105">描述</span><span class="sxs-lookup"><span data-stu-id="96296-105">DESCRIPTION</span></span>
<span data-ttu-id="96296-106">**Add-AzLoadBalancerProbeConfig** Cmdlet 會為 Azure 負載平衡器新增一個加值組。</span><span class="sxs-lookup"><span data-stu-id="96296-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="96296-107">例子</span><span class="sxs-lookup"><span data-stu-id="96296-107">EXAMPLES</span></span>

### <span data-ttu-id="96296-108">範例 1：在負載平衡器中新增安裝組式</span><span class="sxs-lookup"><span data-stu-id="96296-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="96296-109">此命令會取得名為 myLb 的負載平衡器，新增指定的安裝設定，然後使用 **Set-AzLoadBalancer Cmdlet** 來更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="96296-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="96296-110">參數</span><span class="sxs-lookup"><span data-stu-id="96296-110">PARAMETERS</span></span>

### <span data-ttu-id="96296-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96296-111">-DefaultProfile</span></span>
<span data-ttu-id="96296-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="96296-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96296-113">-IntervalIn以秒為單位</span><span class="sxs-lookup"><span data-stu-id="96296-113">-IntervalInSeconds</span></span>
<span data-ttu-id="96296-114">指定每個負載平衡服務實例之間的間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="96296-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="96296-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="96296-115">-LoadBalancer</span></span>
<span data-ttu-id="96296-116">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="96296-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="96296-117">此 Cmdlet 會為此參數指定的負載平衡器新增設定。</span><span class="sxs-lookup"><span data-stu-id="96296-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="96296-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="96296-118">-Name</span></span>
<span data-ttu-id="96296-119">指定要新增的群組原則組名。</span><span class="sxs-lookup"><span data-stu-id="96296-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="96296-120">-埠</span><span class="sxs-lookup"><span data-stu-id="96296-120">-Port</span></span>
<span data-ttu-id="96296-121">指定應該連接負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="96296-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="96296-122">-Count</span><span class="sxs-lookup"><span data-stu-id="96296-122">-ProbeCount</span></span>
<span data-ttu-id="96296-123">指定將實例視為不健康之每例連續失敗次數。</span><span class="sxs-lookup"><span data-stu-id="96296-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="96296-124">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="96296-124">-Protocol</span></span>
<span data-ttu-id="96296-125">指定要用於探索的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="96296-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="96296-126">此參數可接受的值為：Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="96296-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="96296-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="96296-127">-RequestPath</span></span>
<span data-ttu-id="96296-128">指定負載平衡服務中的路徑，以進位決定健康狀態。</span><span class="sxs-lookup"><span data-stu-id="96296-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="96296-129">-確認</span><span class="sxs-lookup"><span data-stu-id="96296-129">-Confirm</span></span>
<span data-ttu-id="96296-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="96296-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96296-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96296-131">-WhatIf</span></span>
<span data-ttu-id="96296-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96296-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96296-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96296-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96296-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96296-134">CommonParameters</span></span>
<span data-ttu-id="96296-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96296-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96296-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="96296-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96296-137">輸入</span><span class="sxs-lookup"><span data-stu-id="96296-137">INPUTS</span></span>

### <span data-ttu-id="96296-138">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="96296-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="96296-139">System.String</span><span class="sxs-lookup"><span data-stu-id="96296-139">System.String</span></span>

### <span data-ttu-id="96296-140">System.Int32</span><span class="sxs-lookup"><span data-stu-id="96296-140">System.Int32</span></span>

## <span data-ttu-id="96296-141">輸出</span><span class="sxs-lookup"><span data-stu-id="96296-141">OUTPUTS</span></span>

### <span data-ttu-id="96296-142">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="96296-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="96296-143">筆記</span><span class="sxs-lookup"><span data-stu-id="96296-143">NOTES</span></span>

## <span data-ttu-id="96296-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="96296-144">RELATED LINKS</span></span>

[<span data-ttu-id="96296-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="96296-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="96296-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="96296-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="96296-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="96296-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="96296-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="96296-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="96296-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="96296-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


