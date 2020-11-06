---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 62ed11a2819a2b0c31756c90ce4ab623a1feae91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453687"
---
# <span data-ttu-id="0d81d-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d81d-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="0d81d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d81d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d81d-103">在負載平衡器中新增探測配置。</span><span class="sxs-lookup"><span data-stu-id="0d81d-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d81d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d81d-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d81d-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d81d-105">DESCRIPTION</span></span>
<span data-ttu-id="0d81d-106">**AzureRmLoadBalancerProbeConfig** Cmdlet 會將探測設定新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="0d81d-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="0d81d-107">示例</span><span class="sxs-lookup"><span data-stu-id="0d81d-107">EXAMPLES</span></span>

### <span data-ttu-id="0d81d-108">範例1將探針設定新增到負載平衡器</span><span class="sxs-lookup"><span data-stu-id="0d81d-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="0d81d-109">這個命令會取得名為 myLb 的負載平衡器，將指定的探測器設定新增至它，然後使用 **Set AzureRmLoadBalancer** Cmdlet 來更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="0d81d-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="0d81d-110">參數</span><span class="sxs-lookup"><span data-stu-id="0d81d-110">PARAMETERS</span></span>

### <span data-ttu-id="0d81d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d81d-111">-DefaultProfile</span></span>
<span data-ttu-id="0d81d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d81d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d81d-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0d81d-113">-IntervalInSeconds</span></span>
<span data-ttu-id="0d81d-114">指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0d81d-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="0d81d-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d81d-115">-LoadBalancer</span></span>
<span data-ttu-id="0d81d-116">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="0d81d-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="0d81d-117">這個 Cmdlet 會將探測設定新增到此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="0d81d-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0d81d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d81d-118">-Name</span></span>
<span data-ttu-id="0d81d-119">指定要新增的探測配置名稱。</span><span class="sxs-lookup"><span data-stu-id="0d81d-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="0d81d-120">-埠</span><span class="sxs-lookup"><span data-stu-id="0d81d-120">-Port</span></span>
<span data-ttu-id="0d81d-121">指定探測器應連接到負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="0d81d-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="0d81d-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="0d81d-122">-ProbeCount</span></span>
<span data-ttu-id="0d81d-123">指定實例被視為不健康的每個實例連續失敗數。</span><span class="sxs-lookup"><span data-stu-id="0d81d-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="0d81d-124">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="0d81d-124">-Protocol</span></span>
<span data-ttu-id="0d81d-125">指定要用於探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0d81d-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="0d81d-126">此參數可接受的值為： Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="0d81d-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="0d81d-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="0d81d-127">-RequestPath</span></span>
<span data-ttu-id="0d81d-128">指定負載平衡服務中要探測以判斷健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="0d81d-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="0d81d-129">-確認</span><span class="sxs-lookup"><span data-stu-id="0d81d-129">-Confirm</span></span>
<span data-ttu-id="0d81d-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d81d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d81d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d81d-131">-WhatIf</span></span>
<span data-ttu-id="0d81d-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d81d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d81d-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d81d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d81d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d81d-134">CommonParameters</span></span>
<span data-ttu-id="0d81d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d81d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d81d-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d81d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d81d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="0d81d-137">INPUTS</span></span>

### <span data-ttu-id="0d81d-138">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0d81d-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="0d81d-139">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="0d81d-139">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="0d81d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="0d81d-140">OUTPUTS</span></span>

### <span data-ttu-id="0d81d-141">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0d81d-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0d81d-142">筆記</span><span class="sxs-lookup"><span data-stu-id="0d81d-142">NOTES</span></span>

## <span data-ttu-id="0d81d-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d81d-143">RELATED LINKS</span></span>

[<span data-ttu-id="0d81d-144">AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d81d-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0d81d-145">新-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d81d-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0d81d-146">移除-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d81d-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0d81d-147">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d81d-147">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="0d81d-148">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d81d-148">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


