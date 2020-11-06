---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6bcf0957d389f45bb0e010446381303c6124146b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621765"
---
# <span data-ttu-id="de7d3-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de7d3-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="de7d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de7d3-102">SYNOPSIS</span></span>
<span data-ttu-id="de7d3-103">為負載平衡器建立探測配置。</span><span class="sxs-lookup"><span data-stu-id="de7d3-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="de7d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="de7d3-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de7d3-105">說明</span><span class="sxs-lookup"><span data-stu-id="de7d3-105">DESCRIPTION</span></span>
<span data-ttu-id="de7d3-106">**新的-AzLoadBalancerProbeConfig** Cmdlet 會為 Azure 負載平衡器建立探測配置。</span><span class="sxs-lookup"><span data-stu-id="de7d3-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="de7d3-107">示例</span><span class="sxs-lookup"><span data-stu-id="de7d3-107">EXAMPLES</span></span>

### <span data-ttu-id="de7d3-108">範例1：建立探測器設定</span><span class="sxs-lookup"><span data-stu-id="de7d3-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="de7d3-109">這個命令會使用 HTTP 通訊協定，建立名為 MyProbe 的探測配置。</span><span class="sxs-lookup"><span data-stu-id="de7d3-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="de7d3-110">新的探測會連接到埠80上的負載平衡服務。</span><span class="sxs-lookup"><span data-stu-id="de7d3-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="de7d3-111">參數</span><span class="sxs-lookup"><span data-stu-id="de7d3-111">PARAMETERS</span></span>

### <span data-ttu-id="de7d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de7d3-112">-DefaultProfile</span></span>
<span data-ttu-id="de7d3-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de7d3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de7d3-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="de7d3-114">-IntervalInSeconds</span></span>
<span data-ttu-id="de7d3-115">指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="de7d3-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="de7d3-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="de7d3-116">-Name</span></span>
<span data-ttu-id="de7d3-117">指定要建立的探針配置名稱。</span><span class="sxs-lookup"><span data-stu-id="de7d3-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="de7d3-118">-埠</span><span class="sxs-lookup"><span data-stu-id="de7d3-118">-Port</span></span>
<span data-ttu-id="de7d3-119">指定新的探測器應該連線到負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="de7d3-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="de7d3-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="de7d3-120">-ProbeCount</span></span>
<span data-ttu-id="de7d3-121">指定實例被視為不健康的每個實例連續失敗數。</span><span class="sxs-lookup"><span data-stu-id="de7d3-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="de7d3-122">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="de7d3-122">-Protocol</span></span>
<span data-ttu-id="de7d3-123">指定要用於探測設定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="de7d3-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="de7d3-124">此參數可接受的值為： Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="de7d3-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="de7d3-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="de7d3-125">-RequestPath</span></span>
<span data-ttu-id="de7d3-126">在負載平衡服務中指定要探測以判斷健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="de7d3-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="de7d3-127">-確認</span><span class="sxs-lookup"><span data-stu-id="de7d3-127">-Confirm</span></span>
<span data-ttu-id="de7d3-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="de7d3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de7d3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de7d3-129">-WhatIf</span></span>
<span data-ttu-id="de7d3-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de7d3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de7d3-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de7d3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de7d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de7d3-132">CommonParameters</span></span>
<span data-ttu-id="de7d3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de7d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de7d3-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de7d3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de7d3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="de7d3-135">INPUTS</span></span>

### <span data-ttu-id="de7d3-136">System.object</span><span class="sxs-lookup"><span data-stu-id="de7d3-136">System.String</span></span>

### <span data-ttu-id="de7d3-137">System.object</span><span class="sxs-lookup"><span data-stu-id="de7d3-137">System.Int32</span></span>

## <span data-ttu-id="de7d3-138">輸出</span><span class="sxs-lookup"><span data-stu-id="de7d3-138">OUTPUTS</span></span>

### <span data-ttu-id="de7d3-139">PSProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="de7d3-139">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="de7d3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="de7d3-140">NOTES</span></span>

## <span data-ttu-id="de7d3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="de7d3-141">RELATED LINKS</span></span>

[<span data-ttu-id="de7d3-142">附加 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de7d3-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="de7d3-143">AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de7d3-143">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="de7d3-144">移除-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de7d3-144">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="de7d3-145">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de7d3-145">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)

