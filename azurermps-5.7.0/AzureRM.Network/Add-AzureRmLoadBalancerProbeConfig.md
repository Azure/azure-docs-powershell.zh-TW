---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 81ff9c40045f78f961a90737d2142f5cd5189583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624480"
---
# <span data-ttu-id="a69bb-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a69bb-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a69bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a69bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a69bb-103">在負載平衡器中新增探測配置。</span><span class="sxs-lookup"><span data-stu-id="a69bb-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a69bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="a69bb-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a69bb-105">說明</span><span class="sxs-lookup"><span data-stu-id="a69bb-105">DESCRIPTION</span></span>
<span data-ttu-id="a69bb-106">**AzureRmLoadBalancerProbeConfig** Cmdlet 會將探測設定新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a69bb-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="a69bb-107">示例</span><span class="sxs-lookup"><span data-stu-id="a69bb-107">EXAMPLES</span></span>

### <span data-ttu-id="a69bb-108">範例1將探針設定新增到負載平衡器</span><span class="sxs-lookup"><span data-stu-id="a69bb-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="a69bb-109">這個命令會取得名為 myLb 的負載平衡器，將指定的探測器設定新增至它，然後使用 **Set AzureRmLoadBalancer** Cmdlet 來更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a69bb-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="a69bb-110">參數</span><span class="sxs-lookup"><span data-stu-id="a69bb-110">PARAMETERS</span></span>

### <span data-ttu-id="a69bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69bb-111">-DefaultProfile</span></span>
<span data-ttu-id="a69bb-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a69bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a69bb-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a69bb-113">-IntervalInSeconds</span></span>
<span data-ttu-id="a69bb-114">指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a69bb-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="a69bb-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a69bb-115">-LoadBalancer</span></span>
<span data-ttu-id="a69bb-116">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="a69bb-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="a69bb-117">這個 Cmdlet 會將探測設定新增到此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a69bb-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a69bb-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a69bb-118">-Name</span></span>
<span data-ttu-id="a69bb-119">指定要新增的探測配置名稱。</span><span class="sxs-lookup"><span data-stu-id="a69bb-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="a69bb-120">-埠</span><span class="sxs-lookup"><span data-stu-id="a69bb-120">-Port</span></span>
<span data-ttu-id="a69bb-121">指定探測器應連接到負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="a69bb-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="a69bb-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="a69bb-122">-ProbeCount</span></span>
<span data-ttu-id="a69bb-123">指定實例被視為不健康的每個實例連續失敗數。</span><span class="sxs-lookup"><span data-stu-id="a69bb-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="a69bb-124">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a69bb-124">-Protocol</span></span>
<span data-ttu-id="a69bb-125">指定要用於探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a69bb-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="a69bb-126">此參數可接受的值為： Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="a69bb-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="a69bb-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="a69bb-127">-RequestPath</span></span>
<span data-ttu-id="a69bb-128">指定負載平衡服務中要探測以判斷健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="a69bb-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="a69bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69bb-129">CommonParameters</span></span>
<span data-ttu-id="a69bb-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a69bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69bb-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a69bb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69bb-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a69bb-132">INPUTS</span></span>

### <span data-ttu-id="a69bb-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a69bb-133">PSLoadBalancer</span></span>
<span data-ttu-id="a69bb-134">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a69bb-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a69bb-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a69bb-135">OUTPUTS</span></span>

### <span data-ttu-id="a69bb-136">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a69bb-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a69bb-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a69bb-137">NOTES</span></span>

## <span data-ttu-id="a69bb-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a69bb-138">RELATED LINKS</span></span>

[<span data-ttu-id="a69bb-139">AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a69bb-139">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a69bb-140">新-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a69bb-140">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a69bb-141">移除-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a69bb-141">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a69bb-142">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a69bb-142">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="a69bb-143">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a69bb-143">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


